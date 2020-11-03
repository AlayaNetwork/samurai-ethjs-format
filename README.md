## ethjs-format

<div>
  <!-- Dependency Status -->
  <a href="https://david-dm.org/ethjs/ethjs-format">
    <img src="https://david-dm.org/ethjs/ethjs-format.svg"
    alt="Dependency Status" />
  </a>

  <!-- devDependency Status -->
  <a href="https://david-dm.org/ethjs/ethjs-format#info=devDependencies">
    <img src="https://david-dm.org/ethjs/ethjs-format/dev-status.svg" alt="devDependency Status" />
  </a>

  <!-- Build Status -->
  <a href="https://travis-ci.org/ethjs/ethjs-format">
    <img src="https://travis-ci.org/ethjs/ethjs-format.svg"
    alt="Build Status" />
  </a>

  <!-- NPM Version -->
  <a href="https://www.npmjs.org/package/ethjs-format">
    <img src="http://img.shields.io/npm/v/ethjs-format.svg"
    alt="NPM version" />
  </a>

  <!-- Test Coverage -->
  <a href="https://coveralls.io/r/ethjs/ethjs-format">
    <img src="https://coveralls.io/repos/github/ethjs/ethjs-format/badge.svg" alt="Test Coverage" />
  </a>

  <!-- Javascript Style -->
  <a href="http://airbnb.io/javascript/">
    <img src="https://img.shields.io/badge/code%20style-airbnb-brightgreen.svg" alt="js-airbnb-style" />
  </a>
</div>

<br />

A payload formatter for the Ethereum RPC layer.

## Install

```
npm install --save ethjs-format
```

## Usage

```js
const format = require('@alayanetwork/ethjs-format');

const inputPayload = format.formatInputs('platon_getBalance', ["0x407d73d8a49eeb85d32cf465507dd71d507100c1", 405938494]);

// result ['0x407d73d8a49eeb85d32cf465507dd71d507100c1', '0x1832213E']

const outputPayload = format.formatOutputs('platon_getBalance', "0x0234c8a3397aab58");

// result <BigNumber ...>
// result outputPayload.toString(10) 158972490234375000
```

## About

A straight forward and complete RPC formatting layer for the Ethereum RPC spec.

## Supported RPC Methods

```
web3_clientVersion
web3_sha3
net_version
net_peerCount
net_listening
platon_protocolVersion
platon_syncing
platon_coinbase
platon_mining
platon_hashrate
platon_gasPrice
platon_accounts
platon_blockNumber
platon_getBalance
platon_getStorageAt
platon_getTransactionCount
platon_getBlockTransactionCountByHash
platon_getBlockTransactionCountByNumber
platon_getUncleCountByBlockHash
platon_getUncleCountByBlockNumber
platon_getCode
platon_sign
platon_sendTransaction
platon_sendRawTransaction
platon_call
platon_estimateGas
platon_getBlockByHash
platon_getBlockByNumber
platon_getTransactionByHash
platon_getTransactionByBlockHashAndIndex
platon_getTransactionByBlockNumberAndIndex
platon_getTransactionReceipt
platon_getUncleByBlockHashAndIndex
platon_getUncleByBlockNumberAndIndex
platon_getCompilers
platon_compileLLL
platon_compileSolidity
platon_compileSerpent
platon_newFilter
platon_newBlockFilter
platon_newPendingTransactionFilter
platon_uninstallFilter
platon_getFilterChanges
platon_getFilterLogs
platon_getLogs
platon_getWork
platon_submitWork
platon_submitHashrate
db_putString
db_getString
db_putHex
db_getHex
shh_post
shh_version
shh_newIdentity
shh_hasIdentity
shh_newGroup
shh_addToGroup
shh_newFilter
shh_uninstallFilter
shh_getFilterChanges
shh_getMessages
```

## Contributing

Please help better the ecosystem by submitting issues and pull requests to `ethjs-format`. We need all the help we can get to build the absolute best linting standards and utilities. We follow the AirBNB linting standard and the unix philosophy.

## Guides

You'll find more detailed information on using `ethjs-format` and tailoring it to your needs in our guides:

- [User guide](docs/user-guide.md) - Usage, configuration, FAQ and complementary tools.
- [Developer guide](docs/developer-guide.md) - Contributing to `ethjs-format` and writing your own code and coverage.

## Help out

There is always a lot of work to do, and will have many rules to maintain. So please help out in any way that you can:

- Create, enhance, and debug ethjs rules (see our guide to ["Working on rules"](./github/CONTRIBUTING.md)).
- Improve documentation.
- Chime in on any open issue or pull request.
- Open new issues about your ideas for making `ethjs-format` better, and pull requests to show us how your idea works.
- Add new tests to *absolutely anything*.
- Create or contribute to ecosystem tools, like modules for encoding or contracts.
- Spread the word.

Please consult our [Code of Conduct](CODE_OF_CONDUCT.md) docs before helping out.

We communicate via [issues](https://github.com/AlayaNetwork/samurai-ethjs-format/issues) and [pull requests](https://github.com/AlayaNetwork/samurai-ethjs-format/pulls).

## Important documents

- [Changelog](CHANGELOG.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [License](https://raw.githubusercontent.com/ethjs/ethjs-format/master/LICENSE)

## Licence

This project is licensed under the MIT license, Copyright (c) 2016 Nick Dodson. For more information see LICENSE.md.

```
The MIT License

Copyright (c) 2016 Nick Dodson. nickdodson.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
