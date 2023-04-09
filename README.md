# React Truffle Box

This box comes with everything you need to start using Truffle to write, compile, test, and deploy smart contracts, and interact with them from a React app.

## Running

```sh
# first terminal
$ npm install -g truffle ganache
$ cd truffle
...
$ ganache

This version of µWS is not compatible with your Node.js build:

Error: Cannot find module './uws_linux_x64_108.node'
Falling back to a NodeJS implementation; performance may be degraded.


ganache v7.0.0 (@ganache/cli: 0.1.1, @ganache/core: 0.1.1)
Starting RPC server

Available Accounts
==================
(0) 0x8295d487800481A98b1E761D88E3d050Ef7574ff (1000 ETH)
(1) 0x71Cc150503ACd46358bfE056a43A4b364D2D1eFe (1000 ETH)
(2) 0x077c70C5D7fB2923654E3D4f570f0d524E8451b5 (1000 ETH)
(3) 0xe38AE961C27dCC0Fa9B99e75258c3AA74258f77e (1000 ETH)
....
```

```sh
# second terminal (from DApp root)
$ cd truffle
$ truffle migrate --network development
# This will deploy to development network
...
$ cd ../client
$ npm start
```

### Metamask. 

Login to Metamask, `accounts` > `Import Account`. 
Paste any of the private keys (this will make sure that metamask uses a ganache available account). Also set that account as active account.

```sh
# see in the terminal running ganache
Private Keys
==================
(0) 0xbdc780b688293a6705a42496153dc5a0cd9880931e752ca87eeae2e0dff628e9
(1) 0xf6e8231ba8eaa24f14fbfa4d5780ec6dd1d401cb201cc600dabdd029dcc6a762
(2) 0x0a0ff6735e1db8d9f22978877decb7f756f1b8bfb582866e46445111e0beea67
(3) 0x3d38ffbbe7479be6bf7b846410c98a3abbcaa12c693c0a27fe30683fb0cc5be8

```

## Installation

First ensure you are in an empty directory.

Run the `unbox` command using 1 of 2 ways.

```sh
# Install Truffle globally and run `truffle unbox`
$ npm install -g truffle
$ truffle unbox react
```

```sh
# Alternatively, run `truffle unbox` via npx
$ npx truffle unbox react
```

Start the react dev server.

```sh
$ cd client
$ npm start
```

From there, follow the instructions on the hosted React app. It will walk you through using Truffle and Ganache to deploy the `SimpleStorage` contract, making calls to it, and sending transactions to change the contract's state.

## FAQ

- __How do I use this with Ganache (or any other network)?__

  The Truffle project is set to deploy to Ganache by default. If you'd like to change this, it's as easy as modifying the Truffle config file! Check out [our documentation on adding network configurations](https://trufflesuite.com/docs/truffle/reference/configuration/#networks). From there, you can run `truffle migrate` pointed to another network, restart the React dev server, and see the change take place.

- __Where can I find more resources?__

  This Box is a sweet combo of [Truffle](https://trufflesuite.com) and [Webpack](https://webpack.js.org). Either one would be a great place to start!
