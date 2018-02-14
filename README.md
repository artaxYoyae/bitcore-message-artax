# Artax Message Verification and Signing for Bitcore-Artax


[![NPM Package](https://img.shields.io/npm/v/bitcore-message-artax.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-message-artax)
[![Build Status](https://img.shields.io/travis/yoyaeArtax/bitcore-message-artax.svg?branch=master&style=flat-square)](https://travis-ci.org/yoyaeArtax/bitcore-message-artax)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-message-artax.svg?style=flat-square)](https://coveralls.io/r/yoyaeArtax/bitcore-message-artax?branch=master)

bitcore-message-artax adds support for verifying and signing artax messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-artax repo](https://github.com/yoyaeArtax/bitcore-artax) for more information.

## Getting Started

```sh
npm install bitcore-message-artax
```

```sh
bower install bitcore-message-artax
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-artax');
var Message = require('bitcore-message-artax');

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

See [CONTRIBUTING.md](https://github.com/yoyaeArtax/bitcore-artax/blob/master/CONTRIBUTING.md) on the main bitcore-artax repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

