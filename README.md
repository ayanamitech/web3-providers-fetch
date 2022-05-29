# web3-providers-fetch

[![NPM Package][npm-image]][npm-url]

This is a fork of web3-providers-http with WHATWG Fetch API support for [web3.js][repo].

Please read the [documentation][docs] for more.

## Installation

### Node.js

```bash
npm install web3-providers-fetch
```

## Usage

```js
const http = require('http');
const Web3HttpProvider = require('web3-providers-fetch');

const options = {
    keepAlive: true,
    timeout: 20000, // milliseconds,
    headers: [{name: 'Access-Control-Allow-Origin', value: '*'},{...}],
    withCredentials: false,
    agent: {http: http.Agent(...), baseUrl: ''}
};

const provider = new Web3HttpProvider('http://localhost:8545', options);
```

## Types

All the TypeScript typings are placed in the `types` folder.

[docs]: http://web3js.readthedocs.io/en/1.0/
[repo]: https://github.com/ayanamitech/web3-providers-fetch
[npm-image]: https://img.shields.io/npm/dm/web3-providers-fetch.svg
[npm-url]: https://npmjs.org/package/web3-providers-fetch
