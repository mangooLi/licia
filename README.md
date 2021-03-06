[中文](README_CN.md)

# Licia

[![NPM version][npm-image]][npm-url]
[![Build status][travis-image]][travis-url]
[![License][license-image]][npm-url]

[npm-image]: https://img.shields.io/npm/v/licia.svg
[npm-url]: https://npmjs.org/package/licia
[travis-image]: https://img.shields.io/travis/liriliri/licia.svg
[travis-url]: https://travis-ci.org/liriliri/licia
[license-image]: https://img.shields.io/npm/l/licia.svg

Useful utility collection with zero dependencies.

To check all current available functions, click
[here](http://eustia.liriliri.io/module.html).

## Another Lodash?

No. The goal of Licia is to provide a huge number of useful and small JavaScript codes, not just functions, but also modules and classes. Think of it as a mini version of npm suitable for tiny packages.

## Usage

It is recommended to use the official bundler [eustia](http://eustia.liriliri.io/) to easily build a customized utility library for your project. But if you don't like it, just install **licia** and use it like any other npm utility modules such as lodash.

```bash
npm i licia --save
```

```javascript
var uuid = require('licia/uuid');

console.log(uuid()); // -> 0e3b84af-f911-4a55-b78a-cedf6f0bd815
```

There is also an online tool to build a customized utility library, check [here](http://eustia.liriliri.io/builder.html).

## Submitting New Modules

Unable to find one suitable? Fork it on GitHub, add the module and submit a pull
request.

Please check [Eustia Documentation](http://eustia.liriliri.io/docs.html#create-module)
about how to write an eustia module.

### Rules

* Must have full documentation about usage.
* Must have test.
* Must named with **a-zA-Z0-9$** characters only.
* Must not be repeated. (e.g. leftPad is not allowed because there is already a
  module called lpad)
* Must within a file, less than 500 lines. (with comments and blank lines counted)  

### How to Add

* Fork and clone the repository.
* `npm i && npm link` to register **licia** command in your system.
* Create a js file named with the module name and its corresponding test file.
* Write the source code along with the documentaion and test. (documentation is the first block comment written in markdown)
* `licia test <module-name>` run the test. (use `-b` if test should run in a browser)
* `npm run cov` for checking the test coverage. (istanbul is required)
* Update **index.json** and **doc.md** by running `npm run update`.

Now it's time to submit a pull request:)
