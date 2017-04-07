# api documentation for  [power-assert (v1.4.2)](https://github.com/power-assert-js/power-assert)  [![npm package](https://img.shields.io/npm/v/npmdoc-power-assert.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-power-assert) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-power-assert.svg)](https://travis-ci.org/npmdoc/node-npmdoc-power-assert)
#### Power Assert in JavaScript

[![NPM](https://nodei.co/npm/power-assert.png?downloads=true)](https://www.npmjs.com/package/power-assert)

[![apidoc](https://npmdoc.github.io/node-npmdoc-power-assert/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-power-assert_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-power-assert/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-power-assert/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-power-assert/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Takuto Wada",
        "email": "takuto.wada@gmail.com",
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
            "name": "twada",
            "email": "takuto.wada@gmail.com"
        }
    ],
    "name": "power-assert",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "1.4.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module power-assert](#apidoc.module.power-assert)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>AssertionError (options)](#apidoc.element.power-assert.AssertionError)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>AssertionError.super_ ()](#apidoc.element.power-assert.AssertionError.super_)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>customize (customOptions)](#apidoc.element.power-assert.customize)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>deepEqual ()](#apidoc.element.power-assert.deepEqual)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>deepStrictEqual ()](#apidoc.element.power-assert.deepStrictEqual)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>default ()](#apidoc.element.power-assert.default)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>doesNotThrow (block, error, message)](#apidoc.element.power-assert.doesNotThrow)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>equal ()](#apidoc.element.power-assert.equal)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>fail (actual, expected, message, operator, stackStartFunction)](#apidoc.element.power-assert.fail)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>ifError (err)](#apidoc.element.power-assert.ifError)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>notDeepEqual ()](#apidoc.element.power-assert.notDeepEqual)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>notDeepStrictEqual ()](#apidoc.element.power-assert.notDeepStrictEqual)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>notEqual ()](#apidoc.element.power-assert.notEqual)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>notStrictEqual ()](#apidoc.element.power-assert.notStrictEqual)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>ok ()](#apidoc.element.power-assert.ok)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>strictEqual ()](#apidoc.element.power-assert.strictEqual)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>throws (block, error, message)](#apidoc.element.power-assert.throws)

#### [module power-assert.AssertionError](#apidoc.module.power-assert.AssertionError)
1.  [function <span class="apidocSignatureSpan">power-assert.</span>AssertionError (options)](#apidoc.element.power-assert.AssertionError.AssertionError)
1.  [function <span class="apidocSignatureSpan">power-assert.AssertionError.</span>super_ ()](#apidoc.element.power-assert.AssertionError.super_)

#### [module power-assert.AssertionError.super_](#apidoc.module.power-assert.AssertionError.super_)
1.  [function <span class="apidocSignatureSpan">power-assert.AssertionError.</span>super_ ()](#apidoc.element.power-assert.AssertionError.super_.super_)
1.  [function <span class="apidocSignatureSpan">power-assert.AssertionError.super_.</span>captureStackTrace ()](#apidoc.element.power-assert.AssertionError.super_.captureStackTrace)
1.  number <span class="apidocSignatureSpan">power-assert.AssertionError.super_.</span>stackTraceLimit



# <a name="apidoc.module.power-assert"></a>[module power-assert](#apidoc.module.power-assert)

#### <a name="apidoc.element.power-assert.AssertionError"></a>[function <span class="apidocSignatureSpan">power-assert.</span>AssertionError (options)](#apidoc.element.power-assert.AssertionError)
- description and source-code
```javascript
function AssertionError(options) {
  this.name = 'AssertionError';
  this.actual = options.actual;
  this.expected = options.expected;
  this.operator = options.operator;
  if (options.message) {
    this.message = options.message;
    this.generatedMessage = false;
  } else {
    this.message = getMessage(this);
    this.generatedMessage = true;
  }
  var stackStartFunction = options.stackStartFunction || fail;
  Error.captureStackTrace(this, stackStartFunction);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.power-assert.AssertionError.super_"></a>[function <span class="apidocSignatureSpan">power-assert.</span>AssertionError.super_ ()](#apidoc.element.power-assert.AssertionError.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.power-assert.customize"></a>[function <span class="apidocSignatureSpan">power-assert.</span>customize (customOptions)](#apidoc.element.power-assert.customize)
- description and source-code
```javascript
function customize(customOptions) {
    var options = customOptions || {};
    var poweredAssert = empower(
        baseAssert,
        formatter(options.output),
        extend(empowerOptions, options.assertion)
    );
    poweredAssert.customize = customize;
    return poweredAssert;
}
```
- example usage
```shell
...
* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
* 'assert.doesNotThrow(block, [message])'
* 'assert.ifError(value)'

power-assert provides an [API for customization](https://github.com/power-assert-js/power-assert#customization-api).

* 'assert.customize(options)'


### No API is the best API

Though power-assert is fully compatible with standard [assert](https://nodejs.org/api/assert.html) interface, all you need to remember
 is just an 'assert(any_expression)' function in most cases.

The core value of power-assert is absolute simplicity and stability. Especially, power-assert sticks to the simplest form of testing
, 'assert(any_expression)'.
...
```

#### <a name="apidoc.element.power-assert.deepEqual"></a>[function <span class="apidocSignatureSpan">power-assert.</span>deepEqual ()](#apidoc.element.power-assert.deepEqual)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...

* 'assert(value, [message])'
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
...
```

#### <a name="apidoc.element.power-assert.deepStrictEqual"></a>[function <span class="apidocSignatureSpan">power-assert.</span>deepStrictEqual ()](#apidoc.element.power-assert.deepStrictEqual)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
* 'assert.doesNotThrow(block, [message])'
...
```

#### <a name="apidoc.element.power-assert.default"></a>[function <span class="apidocSignatureSpan">power-assert.</span>default ()](#apidoc.element.power-assert.default)
- description and source-code
```javascript
function powerAssert() {
    return enhancement.apply(null, slice.apply(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.power-assert.doesNotThrow"></a>[function <span class="apidocSignatureSpan">power-assert.</span>doesNotThrow (block, error, message)](#apidoc.element.power-assert.doesNotThrow)
- description and source-code
```javascript
doesNotThrow = function (block, error, message) {
  _throws(false, block, error, message);
}
```
- example usage
```shell
...
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
* 'assert.doesNotThrow(block, [message])'
* 'assert.ifError(value)'

power-assert provides an [API for customization](https://github.com/power-assert-js/power-assert#customization-api).

* 'assert.customize(options)'
...
```

#### <a name="apidoc.element.power-assert.equal"></a>[function <span class="apidocSignatureSpan">power-assert.</span>equal ()](#apidoc.element.power-assert.equal)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...
API
---------------------------------------

power-assert enhances these assert functions by [espower](https://github.com/power-assert-js/espower). Produces descriptive message
 when assertion is failed.

* 'assert(value, [message])'
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'
...
```

#### <a name="apidoc.element.power-assert.fail"></a>[function <span class="apidocSignatureSpan">power-assert.</span>fail (actual, expected, message, operator, stackStartFunction)](#apidoc.element.power-assert.fail)
- description and source-code
```javascript
function fail(actual, expected, message, operator, stackStartFunction) {
  throw new assert.AssertionError({
    message: message,
    actual: actual,
    expected: expected,
    operator: operator,
    stackStartFunction: stackStartFunction
  });
}
```
- example usage
```shell
...
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
* 'assert.doesNotThrow(block, [message])'
* 'assert.ifError(value)'

power-assert provides an [API for customization](https://github.com/power-assert-js/power-assert#customization-api).

* 'assert.customize(options)'
...
```

#### <a name="apidoc.element.power-assert.ifError"></a>[function <span class="apidocSignatureSpan">power-assert.</span>ifError (err)](#apidoc.element.power-assert.ifError)
- description and source-code
```javascript
ifError = function (err) { if (err) throw err; }
```
- example usage
```shell
...
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
* 'assert.doesNotThrow(block, [message])'
* 'assert.ifError(value)'

power-assert provides an [API for customization](https://github.com/power-assert-js/power-assert#customization-api).

* 'assert.customize(options)'


### No API is the best API
...
```

#### <a name="apidoc.element.power-assert.notDeepEqual"></a>[function <span class="apidocSignatureSpan">power-assert.</span>notDeepEqual ()](#apidoc.element.power-assert.notDeepEqual)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...
* 'assert(value, [message])'
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
...
```

#### <a name="apidoc.element.power-assert.notDeepStrictEqual"></a>[function <span class="apidocSignatureSpan">power-assert.</span>notDeepStrictEqual ()](#apidoc.element.power-assert.notDeepStrictEqual)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
* 'assert.doesNotThrow(block, [message])'
* 'assert.ifError(value)'
...
```

#### <a name="apidoc.element.power-assert.notEqual"></a>[function <span class="apidocSignatureSpan">power-assert.</span>notEqual ()](#apidoc.element.power-assert.notEqual)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...
---------------------------------------

power-assert enhances these assert functions by [espower](https://github.com/power-assert-js/espower). Produces descriptive message
 when assertion is failed.

* 'assert(value, [message])'
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'
...
```

#### <a name="apidoc.element.power-assert.notStrictEqual"></a>[function <span class="apidocSignatureSpan">power-assert.</span>notStrictEqual ()](#apidoc.element.power-assert.notStrictEqual)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...
power-assert enhances these assert functions by [espower](https://github.com/power-assert-js/espower). Produces descriptive message
 when assertion is failed.

* 'assert(value, [message])'
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).
...
```

#### <a name="apidoc.element.power-assert.ok"></a>[function <span class="apidocSignatureSpan">power-assert.</span>ok ()](#apidoc.element.power-assert.ok)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...

API
---------------------------------------

power-assert enhances these assert functions by [espower](https://github.com/power-assert-js/espower). Produces descriptive message
 when assertion is failed.

* 'assert(value, [message])'
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
...
```

#### <a name="apidoc.element.power-assert.strictEqual"></a>[function <span class="apidocSignatureSpan">power-assert.</span>strictEqual ()](#apidoc.element.power-assert.strictEqual)
- description and source-code
```javascript
function decoratedAssert() {
    var context, message, hasMessage = false;

    // see: https://github.com/twada/empower-core/pull/8#issue-127859465
    // see: https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#32-leaking-arguments
    var args = new Array(arguments.length);
    for(var i = 0; i < args.length; ++i) {
        args[i] = arguments[i];
    }

    if (numArgsToCapture === (args.length - 1)) {
        message = args.pop();
        hasMessage = true;
    }

    var invocation = {
        thisObj: this,
        values: args,
        message: message,
        hasMessage: hasMessage
    };

    if (some(args, isCaptured)) {
        invocation.values = map(args.slice(0, numArgsToCapture), function (arg) {
            if (isNotCaptured(arg)) {
                return arg;
            }
            if (!context) {
                context = {
                    source: arg.source,
                    args: []
                };
            }
            context.args.push({
                value: arg.powerAssertContext.value,
                events: arg.powerAssertContext.events
            });
            return arg.powerAssertContext.value;
        });

        return decorator.concreteAssert(callSpec, invocation, context);
    } else {
        return decorator.concreteAssert(callSpec, invocation);
    }
}
```
- example usage
```shell
...

power-assert enhances these assert functions by [espower](https://github.com/power-assert-js/espower). Produces descriptive message
 when assertion is failed.

* 'assert(value, [message])'
* 'assert.ok(value, [message])'
* 'assert.equal(actual, expected, [message])'
* 'assert.notEqual(actual, expected, [message])'
* 'assert.strictEqual(actual, expected, [message])'
* 'assert.notStrictEqual(actual, expected, [message])'
* 'assert.deepEqual(actual, expected, [message])'
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).
...
```

#### <a name="apidoc.element.power-assert.throws"></a>[function <span class="apidocSignatureSpan">power-assert.</span>throws (block, error, message)](#apidoc.element.power-assert.throws)
- description and source-code
```javascript
throws = function (block, error, message) {
  _throws(true, block, error, message);
}
```
- example usage
```shell
...
* 'assert.notDeepEqual(actual, expected, [message])'
* 'assert.deepStrictEqual(actual, expected, [message])'
* 'assert.notDeepStrictEqual(actual, expected, [message])'

power-assert is fully compatible with [assert](https://nodejs.org/api/assert.html). So functions below are also available though
 they are not enhanced (does not produce descriptive message).

* 'assert.fail(actual, expected, message, operator)'
* 'assert.throws(block, [error], [message])'
* 'assert.doesNotThrow(block, [message])'
* 'assert.ifError(value)'

power-assert provides an [API for customization](https://github.com/power-assert-js/power-assert#customization-api).

* 'assert.customize(options)'
...
```



# <a name="apidoc.module.power-assert.AssertionError"></a>[module power-assert.AssertionError](#apidoc.module.power-assert.AssertionError)

#### <a name="apidoc.element.power-assert.AssertionError.AssertionError"></a>[function <span class="apidocSignatureSpan">power-assert.</span>AssertionError (options)](#apidoc.element.power-assert.AssertionError.AssertionError)
- description and source-code
```javascript
function AssertionError(options) {
  this.name = 'AssertionError';
  this.actual = options.actual;
  this.expected = options.expected;
  this.operator = options.operator;
  if (options.message) {
    this.message = options.message;
    this.generatedMessage = false;
  } else {
    this.message = getMessage(this);
    this.generatedMessage = true;
  }
  var stackStartFunction = options.stackStartFunction || fail;
  Error.captureStackTrace(this, stackStartFunction);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.power-assert.AssertionError.super_"></a>[function <span class="apidocSignatureSpan">power-assert.AssertionError.</span>super_ ()](#apidoc.element.power-assert.AssertionError.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.power-assert.AssertionError.super_"></a>[module power-assert.AssertionError.super_](#apidoc.module.power-assert.AssertionError.super_)

#### <a name="apidoc.element.power-assert.AssertionError.super_.super_"></a>[function <span class="apidocSignatureSpan">power-assert.AssertionError.</span>super_ ()](#apidoc.element.power-assert.AssertionError.super_.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.power-assert.AssertionError.super_.captureStackTrace"></a>[function <span class="apidocSignatureSpan">power-assert.AssertionError.super_.</span>captureStackTrace ()](#apidoc.element.power-assert.AssertionError.super_.captureStackTrace)
- description and source-code
```javascript
function captureStackTrace() { [native code] }
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
