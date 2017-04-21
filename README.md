# npmtest-liquid-node

#### basic test coverage for  [liquid-node (v2.6.1)](https://github.com/sirlantis/liquid-node)  [![npm package](https://img.shields.io/npm/v/npmtest-liquid-node.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-liquid-node) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-liquid-node.svg)](https://travis-ci.org/npmtest/node-npmtest-liquid-node)

#### Node.js port of Tobias Lütke's Liquid template engine.

[![NPM](https://nodei.co/npm/liquid-node.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/liquid-node)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-liquid-node/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-liquid-node/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-liquid-node/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-liquid-node/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-liquid-node/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-liquid-node/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-liquid-node/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-liquid-node/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-liquid-node/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-liquid-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-liquid-node/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-liquid-node/build/test-report.html](https://npmtest.github.io/node-npmtest-liquid-node/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-liquid-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-liquid-node/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-liquid-node/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-liquid-node/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-liquid-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-liquid-node/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-liquid-node/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-liquid-node/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marcel Jackwerth"
    },
    "bugs": {
        "url": "https://github.com/sirlantis/liquid-node/issues"
    },
    "contributors": [
        {
            "name": "Tony Heupel"
        },
        {
            "name": "Henry Bergius"
        },
        {
            "name": "Chen Yicai"
        }
    ],
    "dependencies": {
        "native-or-bluebird": "~1.2.0",
        "strftime": "~0.9.2"
    },
    "description": "Node.js port of Tobias Lütke's Liquid template engine.",
    "devDependencies": {
        "chai": "~3.2.0",
        "chai-as-promised": "~5.1.0",
        "coffee-script": "~1.10.0",
        "coffeelint": "^1.11.1",
        "coveralls": "^2.11.4",
        "jscoverage": "^0.6.0",
        "mocha": "~2.3.2",
        "mocha-lcov-reporter": "0.0.2",
        "sinon": "^1.16.1",
        "sinon-chai": "^2.8.0"
    },
    "directories": {
        "lib": "./lib"
    },
    "dist": {
        "shasum": "bd388b1459fef4fc12c993c80699a1e1e41d7570",
        "tarball": "https://registry.npmjs.org/liquid-node/-/liquid-node-2.6.1.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "gitHead": "9ea9038a02490b76e5a9394ad4a753e2f2f4889d",
    "homepage": "https://github.com/sirlantis/liquid-node",
    "keywords": [
        "liquid",
        "template",
        "jinja"
    ],
    "license": "MIT",
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "sirlantis"
        }
    ],
    "name": "liquid-node",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/sirlantis/liquid-node.git"
    },
    "scripts": {
        "compile": "rm -rf lib && coffee --output lib --map --compile src",
        "coverage": "npm run compile && LIQUID_NODE_COVERAGE=1 mocha --compilers coffee:coffee-script/register -r jscoverage --reporter mocha-lcov-reporter test | coveralls",
        "coverage-report": "npm run compile && LIQUID_NODE_COVERAGE=1 mocha --compilers coffee:coffee-script/register -r jscoverage --covout html test",
        "lint": "coffeelint src/** test/**",
        "precommit": "npm test && npm run lint",
        "prepublish": "npm run precommit && npm run compile",
        "test": "mocha --compilers coffee:coffee-script/register -R spec test"
    },
    "version": "2.6.1",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
