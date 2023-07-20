# esswap

ethscriptions trading market

contract address [0xCc54425fb13880C4833f51E615646163EaC2f975](https://etherscan.io/address/0xcc54425fb13880c4833f51e615646163eac2f975)

## createOrder

``` js
//tx info
{
    from:'Account with ownership of ES',
    to: '0xCc54425fb13880C4833f51E615646163EaC2f975',
    data: 'ethscriptionId',
    value: 'Not less than minTradeFee (0.00005 ETH), used as a trade fee, set the order ETH price according to the tradling fee ratio (2%)',
    ...
}
```

## updateOrder

function updateOrder(bytes32 ethscriptionId, address token, uint256 amount);

token: erc-20 address;
amount: order price;

``` js
encodeFunctionSignature('updateOrder(bytes32,address,uint256)'); // 0x4b300b40

// tx info
{
    from: 'createOrder from address',
    to: '0xCc54425fb13880C4833f51E615646163EaC2f975',
    data: '0x4b300b40...',
    ...
}
```

## cancelOrder

function cancelOrder(bytes32 ethscriptionId);

```js
encodeFunctionSignature('cancelOrder(bytes32)'); // 0x7489ec23

// tx info
{
    from: 'createOrder from address',
    to: '0xCc54425fb13880C4833f51E615646163EaC2f975',
    data: '0x7489ec23...',
    ...
}
```

## fillOrder

function fillOrder(bytes32 ethscriptionId);

```js
encodeFunctionSignature('fillOrder(bytes32)'); // 0xece21fb7

// tx info
{
    from: '',
    to: '0xCc54425fb13880C4833f51E615646163EaC2f975',
    data: '0xece21fb7...',
    value: 'If the order payment currency is ETH, ETH needs to be paid', // and other erc-20 tokens need to be approved in advance, value set 0x0
    ...
}
```

## buyOwner

Purchase ownership and continue listing.

function buyOwner(bytes32 ethscriptionId, address token, uint256 amount);

token: erc-20 address;
amount: order price;

```js
encodeFunctionSignature('buyOwner(bytes32,address,uint256)'); // 0xff80e384

// tx info
{
    from: '',
    to: '0xCc54425fb13880C4833f51E615646163EaC2f975',
    data: '0xff80e384...',
    value: 'If the order payment currency is ETH, ETH needs to be paid', // and other erc-20 tokens need to be approved in advance, value set 0x0
    ...
}
```