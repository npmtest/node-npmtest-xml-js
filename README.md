# npmtest-xml-js

#### basic test coverage for  [xml-js (v1.0.2)](https://github.com/nashwaan/xml-js#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-xml-js.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-xml-js) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-xml-js.svg)](https://travis-ci.org/npmtest/node-npmtest-xml-js)

#### A convertor between XML text and Javascript object / JSON text.

[![NPM](https://nodei.co/npm/xml-js.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/xml-js)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-xml-js/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-xml-js/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-xml-js/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-xml-js/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-xml-js/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-xml-js/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-xml-js/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-xml-js/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-xml-js/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-xml-js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-xml-js/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-xml-js/build/test-report.html](https://npmtest.github.io/node-npmtest-xml-js/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-xml-js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-xml-js/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-xml-js/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-xml-js/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-xml-js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-xml-js/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-xml-js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-xml-js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "xml-js",
    "version": "1.0.2",
    "description": "A convertor between XML text and Javascript object / JSON text.",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/nashwaan/xml-js.git"
    },
    "author": "Yousuf Almarzooqi",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/nashwaan/xml-js/issues"
    },
    "homepage": "https://github.com/nashwaan/xml-js#readme",
    "keywords": [
        "XML",
        "xml",
        "js",
        "JSON",
        "json",
        "cdata",
        "CDATA",
        "Javascript",
        "js2xml",
        "json2xml",
        "xml2js",
        "xml2json",
        "transform",
        "transformer",
        "transforming",
        "transformation",
        "convert",
        "convertor",
        "converting",
        "conversion",
        "parse",
        "parser",
        "parsing"
    ],
    "main": "lib/index.js",
    "bin": "./bin/cli.js",
    "dependencies": {
        "sax": "^1.2.1"
    },
    "devDependencies": {
        "biased-opener": "^0.2.8",
        "browser-sync": "^2.18.6",
        "cash-cat": "^0.2.0",
        "codacy-coverage": "^2.0.0",
        "codeclimate-test-reporter": "^0.4.0",
        "coveralls": "^2.11.15",
        "cross-env": "^3.1.4",
        "globify": "^2.0.0",
        "istanbul": "^0.4.5",
        "jasmine": "^2.5.3",
        "node-inspector": "^0.12.8",
        "nodemon": "^1.11.0",
        "npm-run-all": "^4.0.1",
        "typescript": "^2.1.5",
        "watch": "^1.0.1"
    },
    "scripts": {
        "debug": "nodemon --inspect --watch lib/ --watch test/ --debug-brk test/index.js",
        "pre-node6.3.1-debug": "npm-run-all --parallel debug:*",
        "debug:listener": "node-inspect",
        "debug:jasmine": "nodemon --watch lib/ --watch test/ --debug-brk test/index.js",
        "xdebug:cli": "nodemon --watch lib/ --debug-brk index.js -- --help",
        "debug:live": "browser-sync start --port 8080 --server --startPath ?port=5858 --files lib/ test/ --no-open --no-ui --no-online",
        "debug:open": "biased-opener --browser chrome http://localhost:8080/?port=5858",
        "jasmine": "jasmine JASMINE_CONFIG_PATH=./test/jasmine.json",
        "watch:jasmine": "watch \"npm run jasmine\" lib/ test/",
        "bundle:jasmine": "globify test/*_test.js --watch --verbose --list --outfile test/browse-jasmine/bundle.js",
        "live:jasmine": "browser-sync start --port 9991 --server test/browse-jasmine/ --files test/browse-jasmine/ --no-open --no-ui --no-online",
        "open:jasmine": "biased-opener --browser chrome http://localhost:9991",
        "istanbul": "istanbul cover --dir test/browse-coverage -x test/browse-** test/index.js",
        "watch:istanbul": "watch \"npm run istanbul\" lib/ test/ --ignoreDirectoryPattern=/browse-.+/",
        "live:istanbul": "browser-sync start --port 9992 --server test/browse-coverage/lcov-report/ --files test/browse-coverage/lcov-report/ --no-open --no-ui --no-online",
        "open:istanbul": "biased-opener --browser chrome http://localhost:9992",
        "live": "npm-run-all --parallel live:* open:*",
        "start": "npm-run-all --parallel bundle:jasmine watch:istanbul live:* open:*",
        "git:commit": "git add . && git commit -a -m \"Committed by npm script.\" && git push origin master",
        "git:push": "git push origin master",
        "deploy": "npm-run-all --serial coverage git:commit",
        "coverage": "npm-run-all coverage:*",
        "coverage:a-step": "npm run istanbul",
        "coverage:coveralls": "cat ./test/browse-coverage/lcov.info | coveralls",
        "coverage:codacy": "cross-env CODACY_PROJECT_TOKEN=0207815122ea49a68241d1aa435f21f1 cat ./test/browse-coverage/lcov.info | codacy-coverage",
        "coverage:codeclimate": "cross-env CODECLIMATE_REPO_TOKEN=60848a077f9070acf358b0c7145f0a2698a460ddeca7d8250815e75aa4333f7d codeclimate-test-reporter < test\\browse-coverage\\lcov.info",
        "prepublish": "npm run test",
        "test": "npm run jasmine && npm run test:types",
        "test:types": "tsc -p ./types"
    },
    "types": "./types/index.d.ts"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
