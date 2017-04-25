# npmdoc-power-assert

#### basic api documentation for  [power-assert (v1.4.2)](https://github.com/power-assert-js/power-assert)  [![npm package](https://img.shields.io/npm/v/npmdoc-power-assert.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-power-assert) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-power-assert.svg)](https://travis-ci.org/npmdoc/node-npmdoc-power-assert)

#### Power Assert in JavaScript

[![NPM](https://nodei.co/npm/power-assert.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/power-assert)

- [https://npmdoc.github.io/node-npmdoc-power-assert/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-power-assert/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-power-assert/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-power-assert/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-power-assert/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-power-assert/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Takuto Wada",
        "url": "https://github.com/twada"
    },
    "bugs": {
        "url": "https://github.com/power-assert-js/power-assert/issues"
    },
    "contributors": [
        {
            "name": "azu",
            "url": "https://github.com/azu"
        },
        {
            "name": "vvakame",
            "url": "https://github.com/vvakame"
        },
        {
            "name": "yosuke-furukawa",
            "url": "https://github.com/yosuke-furukawa"
        },
        {
            "name": "teppeis",
            "url": "https://github.com/teppeis"
        },
        {
            "name": "zoncoen",
            "url": "https://github.com/zoncoen"
        },
        {
            "name": "falsandtru",
            "url": "https://github.com/falsandtru"
        },
        {
            "name": "James Talmage",
            "url": "https://github.com/jamestalmage"
        },
        {
            "name": "Lesha Koss"
        }
    ],
    "dependencies": {
        "define-properties": "^1.1.2",
        "empower": "^1.1.0",
        "power-assert-formatter": "^1.3.1",
        "universal-deep-strict-equal": "^1.2.1",
        "xtend": "^4.0.0"
    },
    "description": "Power Assert in JavaScript",
    "devDependencies": {
        "babel-cli": "^6.0.0",
        "babel-plugin-espower": "^2.2.0",
        "babel-preset-es2015": "^6.0.0",
        "babel-register": "^6.0.0",
        "browserify": "^13.0.1",
        "derequire": "^2.0.3",
        "dereserve": "^1.0.0",
        "expect.js": "^0.3.1",
        "karma": "^1.3.0",
        "karma-chrome-launcher": "^2.0.0",
        "karma-expect": "^1.1.2",
        "karma-firefox-launcher": "^1.0.0",
        "karma-mocha": "^1.0.0",
        "karma-phantomjs-launcher": "^1.0.0",
        "licensify": "^3.0.0",
        "mocha": "^3.0.0",
        "package-json-filterify": "^1.0.4",
        "phantomjs-prebuilt": "^2.1.7",
        "qunit-tap": "^1.5.0",
        "qunitjs": "1.14.0",
        "requirejs": "^2.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "43319cd0fecd3221f276f1cc49ffa2eaeb9a1815",
        "tarball": "https://registry.npmjs.org/power-assert/-/power-assert-1.4.2.tgz"
    },
    "files": [
        "CHANGELOG.md",
        "MIT-LICENSE.txt",
        "README.md",
        "index.js",
        "build/power-assert.js",
        "package.json"
    ],
    "gitHead": "d59d15cf846679dbabcf06bce3ecf4a9376cead0",
    "homepage": "https://github.com/power-assert-js/power-assert",
    "keywords": [
        "power-assert",
        "assert",
        "assertion",
        "test",
        "testing",
        "ecmascript",
        "ast"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "twada"
        }
    ],
    "name": "power-assert",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/power-assert-js/power-assert.git"
    },
    "scripts": {
        "build": "mkdir -p ./build && npm prune && npm dedupe && browserify -p licensify --global-transform package-json-filterify --standalone assert ./index.js | dereserve | derequire > build/power-assert.js",
        "clean": "rm -rf ./espowered_tests && rm -rf ./build",
        "preversion": "npm test",
        "setup": "npm run clean && npm run setup-dir && npm run setup-espower && npm run build",
        "setup-dir": "mkdir -p ./build && mkdir -p ./espowered_tests/tobe_instrumented && cp -r test/not_tobe_instrumented/ ./espowered_tests/not_tobe_instrumented/",
        "setup-espower": "for i in $(find ./test/tobe_instrumented -name '*.js'); do babel $i > ./espowered_tests/tobe_instrumented/$(basename $i); done",
        "test": "npm run setup && npm run test-all",
        "test-all": "npm run test-unit && npm run test-generated && npm run test-browser",
        "test-browser": "karma start",
        "test-generated": "mocha --reporter dot ./espowered_tests/**/*.js",
        "test-unit": "mocha --reporter dot --require ./enable_power_assert.js ./test/**/*.js",
        "version": "npm run build && git add -A build"
    },
    "version": "1.4.2",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
