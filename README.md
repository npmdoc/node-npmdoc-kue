# npmdoc-kue

#### basic api documentation for  [kue (v0.11.5)](http://automattic.github.io/kue/)  [![npm package](https://img.shields.io/npm/v/npmdoc-kue.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-kue) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-kue.svg)](https://travis-ci.org/npmdoc/node-npmdoc-kue)

#### Feature rich priority job queue backed by redis

[![NPM](https://nodei.co/npm/kue.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/kue)

- [https://npmdoc.github.io/node-npmdoc-kue/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-kue/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-kue/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-kue/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-kue/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-kue/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk"
    },
    "bin": {
        "kue-dashboard": "bin/kue-dashboard"
    },
    "bugs": {
        "url": "https://github.com/Automattic/kue/issues"
    },
    "contributors": [
        {
            "name": "Behrad Zari"
        }
    ],
    "dependencies": {
        "body-parser": "^1.12.2",
        "express": "^4.12.2",
        "lodash": "^4.0.0",
        "nib": "~1.1.2",
        "node-redis-warlock": "~0.2.0",
        "pug": "^2.0.0-beta3",
        "redis": "~2.6.0-2",
        "reds": "^0.2.5",
        "stylus": "~0.54.5",
        "yargs": "^4.0.0"
    },
    "description": "Feature rich priority job queue backed by redis",
    "devDependencies": {
        "async": "^1.4.2",
        "chai": "^3.3.0",
        "coffee-script": "~1.10.0",
        "mocha": "^2.3.3",
        "should": "^3.1.0",
        "sinon": "^1.17.2",
        "supertest": "^1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "ac2fa8c8087e4d4c48e5c9c2d4b17687eed0e1df",
        "tarball": "https://registry.npmjs.org/kue/-/kue-0.11.5.tgz"
    },
    "gitHead": "d5f0b655c6d697f526e0c8105faa06a153703cdf",
    "homepage": "http://automattic.github.io/kue/",
    "keywords": [
        "job",
        "queue",
        "worker",
        "redis"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "tjholowaychuk"
        },
        {
            "name": "drudge"
        },
        {
            "name": "behrad"
        }
    ],
    "name": "kue",
    "optionalDependencies": {
        "reds": "^0.2.5"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/Automattic/kue.git"
    },
    "scripts": {
        "test": "make test-all"
    },
    "version": "0.11.5"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
