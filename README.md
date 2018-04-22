# Innova Message Verification and Signing for Bitcore-Innova


[![NPM Package](https://img.shields.io/npm/v/bitcore-message-innova.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-message-innova)
[![Build Status](https://img.shields.io/travis/innovacoin/bitcore-message-innova.svg?branch=master&style=flat-square)](https://travis-ci.org/innovacoin/bitcore-message-innova)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-message-innova.svg?style=flat-square)](https://coveralls.io/r/innovacoin/bitcore-message-innova?branch=master)

bitcore-message-innova adds support for verifying and signing innova messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-innova repo](https://github.com/innovacoin/bitcore-innova) for more information.

## Getting Started

```sh
npm install bitcore-message-innova
```

```sh
bower install bitcore-message-innova
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-innova');
var Message = require('bitcore-message-innova');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/innovacoin/bitcore-innova/blob/master/CONTRIBUTING.md) on the main bitcore-innova repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

