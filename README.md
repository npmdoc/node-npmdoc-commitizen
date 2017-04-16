# api documentation for  [commitizen (v2.9.6)](https://github.com/commitizen/cz-cli)  [![npm package](https://img.shields.io/npm/v/npmdoc-commitizen.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-commitizen) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-commitizen.svg)](https://travis-ci.org/npmdoc/node-npmdoc-commitizen)
#### Git commit, but play nice with conventions.

[![NPM](https://nodei.co/npm/commitizen.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/commitizen)

[![apidoc](https://npmdoc.github.io/node-npmdoc-commitizen/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-commitizen/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-commitizen/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-commitizen/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jim Cummins",
        "url": "https://github.com/jimthedev"
    },
    "babel": {
        "presets": [
            "es2015",
            "stage-2"
        ]
    },
    "bin": {
        "git-cz": "./bin/git-cz",
        "commitizen": "./bin/commitizen"
    },
    "bugs": {
        "url": "https://github.com/commitizen/cz-cli/issues"
    },
    "config": {
        "commitizen": {
            "path": "./node_modules/cz-conventional-changelog"
        },
        "ghooks": {
            "pre-commit": "npm run lint && npm run test && npm run check-coverage"
        }
    },
    "dependencies": {
        "cachedir": "^1.1.0",
        "chalk": "1.1.3",
        "cz-conventional-changelog": "1.2.0",
        "dedent": "0.6.0",
        "detect-indent": "4.0.0",
        "find-node-modules": "1.0.4",
        "find-root": "1.0.0",
        "fs-extra": "^1.0.0",
        "glob": "7.1.1",
        "inquirer": "1.2.3",
        "lodash": "4.17.2",
        "minimist": "1.2.0",
        "path-exists": "2.1.0",
        "shelljs": "0.7.6",
        "strip-json-comments": "2.0.1"
    },
    "description": "Git commit, but play nice with conventions.",
    "devDependencies": {
        "axios": "0.15.2",
        "babel-cli": "6.18.0",
        "babel-core": "6.18.2",
        "babel-preset-es2015": "6.18.0",
        "babel-preset-stage-2": "6.18.0",
        "chai": "3.5.0",
        "codecov.io": "0.1.6",
        "cz-conventional-changelog-default-export": "0.0.0-semantically-released.1",
        "eslint": "3.12.2",
        "eslint-config-standard": "6.2.1",
        "eslint-plugin-promise": "3.4.0",
        "eslint-plugin-standard": "2.0.1",
        "ghooks": "1.3.2",
        "in-publish": "^2.0.0",
        "mocha": "3.1.2",
        "node-uuid": "1.4.7",
        "nodemon": "1.11.0",
        "nyc": "10.0.0",
        "proxyquire": "1.7.10",
        "semantic-release": "6.3.5",
        "semver": "5.3.0",
        "sinon": "1.17.6"
    },
    "directories": {},
    "dist": {
        "shasum": "c0d00535ef264da7f63737edfda4228983fa2291",
        "tarball": "https://registry.npmjs.org/commitizen/-/commitizen-2.9.6.tgz"
    },
    "engineStrict": true,
    "engines": {
        "node": ">= 0.12"
    },
    "gitHead": "2a101b8615ea1d992d2c009c7b49bc4d134c24a8",
    "homepage": "https://github.com/commitizen/cz-cli",
    "keywords": [
        "commit",
        "pretty",
        "format",
        "conventional changelog",
        "commitizen"
    ],
    "license": "MIT",
    "main": "dist/index.js",
    "maintainers": [
        {
            "name": "commitizen-bot"
        },
        {
            "name": "jimthedev"
        },
        {
            "name": "kentcdodds"
        },
        {
            "name": "linusu"
        }
    ],
    "name": "commitizen",
    "nyc": {
        "exclude": [
            "src/cli",
            "test"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/commitizen/cz-cli.git"
    },
    "scripts": {
        "build": "babel src --out-dir dist",
        "build:watch": "babel --watch src --out-dir dist",
        "check-coverage": "nyc check-coverage --statements 80 --branches 80 --functions 80 --lines 80 ",
        "commit": "node bin/git-cz",
        "lint": "eslint --ignore-path .gitignore .",
        "prepublish": "not-in-install && npm run build || true",
        "report-coverage": "nyc report --reporter=lcov | codecov",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "start": "npm run test:watch",
        "test": "nyc --require babel-core/register _mocha -- test/tests/index.js",
        "test:watch": "nodemon -q --ignore test/.tmp/ --ignore test/artifacts/ --ignore coverage/ --exec \"npm run test\" --",
        "test:windows": "node ./test/tools/trigger-appveyor-tests.js",
        "write-coverage": "nyc report --reporter=lcov"
    },
    "version": "2.9.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module commitizen](#apidoc.module.commitizen)
1.  [function <span class="apidocSignatureSpan">commitizen.</span>commit (sh, inquirer, repoPath, prompter, options, done)](#apidoc.element.commitizen.commit)
1.  [function <span class="apidocSignatureSpan">commitizen.</span>init (sh, repoPath, adapterNpmName)](#apidoc.element.commitizen.init)
1.  object <span class="apidocSignatureSpan">commitizen.</span>adapter
1.  object <span class="apidocSignatureSpan">commitizen.</span>cache
1.  object <span class="apidocSignatureSpan">commitizen.</span>configLoader
1.  object <span class="apidocSignatureSpan">commitizen.</span>staging

#### [module commitizen.adapter](#apidoc.module.commitizen.adapter)
1.  [function <span class="apidocSignatureSpan">commitizen.adapter.</span>addPathToAdapterConfig (sh, cliPath, repoPath, adapterNpmName)](#apidoc.element.commitizen.adapter.addPathToAdapterConfig)
1.  [function <span class="apidocSignatureSpan">commitizen.adapter.</span>generateNpmInstallAdapterCommand (stringMappings, adapterNpmName)](#apidoc.element.commitizen.adapter.generateNpmInstallAdapterCommand)
1.  [function <span class="apidocSignatureSpan">commitizen.adapter.</span>getNearestNodeModulesDirectory (options)](#apidoc.element.commitizen.adapter.getNearestNodeModulesDirectory)
1.  [function <span class="apidocSignatureSpan">commitizen.adapter.</span>getNearestProjectRootDirectory (options)](#apidoc.element.commitizen.adapter.getNearestProjectRootDirectory)
1.  [function <span class="apidocSignatureSpan">commitizen.adapter.</span>getNpmInstallStringMappings (save, saveDev, saveExact, force)](#apidoc.element.commitizen.adapter.getNpmInstallStringMappings)
1.  [function <span class="apidocSignatureSpan">commitizen.adapter.</span>getPrompter (adapterPath)](#apidoc.element.commitizen.adapter.getPrompter)
1.  [function <span class="apidocSignatureSpan">commitizen.adapter.</span>resolveAdapterPath (inboundAdapterPath)](#apidoc.element.commitizen.adapter.resolveAdapterPath)

#### [module commitizen.cache](#apidoc.module.commitizen.cache)
1.  [function <span class="apidocSignatureSpan">commitizen.cache.</span>getCacheValueSync (cachePath, repoPath)](#apidoc.element.commitizen.cache.getCacheValueSync)
1.  [function <span class="apidocSignatureSpan">commitizen.cache.</span>readCacheSync (cachePath)](#apidoc.element.commitizen.cache.readCacheSync)
1.  [function <span class="apidocSignatureSpan">commitizen.cache.</span>setCacheValueSync (cachePath, key, value)](#apidoc.element.commitizen.cache.setCacheValueSync)

#### [module commitizen.configLoader](#apidoc.module.commitizen.configLoader)
1.  [function <span class="apidocSignatureSpan">commitizen.configLoader.</span>load (config, cwd)](#apidoc.element.commitizen.configLoader.load)

#### [module commitizen.staging](#apidoc.module.commitizen.staging)
1.  [function <span class="apidocSignatureSpan">commitizen.staging.</span>isClean (repoPath, done)](#apidoc.element.commitizen.staging.isClean)



# <a name="apidoc.module.commitizen"></a>[module commitizen](#apidoc.module.commitizen)

#### <a name="apidoc.element.commitizen.commit"></a>[function <span class="apidocSignatureSpan">commitizen.</span>commit (sh, inquirer, repoPath, prompter, options, done)](#apidoc.element.commitizen.commit)
- description and source-code
```javascript
function commit(sh, inquirer, repoPath, prompter, options, done) {
  var cacheDirectory = (0, _cachedir2.default)('commitizen');
  var cachePath = _path2.default.join(cacheDirectory, 'commitizen.json');

  (0, _fsExtra.ensureDir)(cacheDirectory, function (error) {
    if (error) {
      console.error("Couldn't create commitizen cache directory: ", error);
      // TODO: properly handle error?
    } else {
      if (options.retryLastCommit) {

        console.log('Retrying last commit attempt.');

        // We want to use the last commit instead of the current commit,
        // so lets override some options using the values from cache.

        var _cache$getCacheValueS = cache.getCacheValueSync(cachePath, repoPath),
            retryOptions = _cache$getCacheValueS.options,
            retryOverrideOptions = _cache$getCacheValueS.overrideOptions,
            retryTemplate = _cache$getCacheValueS.template;

        dispatchGitCommit(sh, repoPath, retryTemplate, retryOptions, retryOverrideOptions, done);
      } else {
        // Get user input -- side effect that is hard to test
        prompter(inquirer, function (error, template, overrideOptions) {
          // Allow adapters to error out
          // (error: Error?, template: String, overrideOptions: Object)
          if (!(error instanceof Error)) {
            overrideOptions = template;
            template = error;
            error = null;
          }

          if (error) {
            return done(error);
          }

          // We don't want to add retries to the cache, only actual commands
          cache.setCacheValueSync(cachePath, repoPath, { template: template, options: options, overrideOptions: overrideOptions });
          dispatchGitCommit(sh, repoPath, template, options, overrideOptions, done);
        });
      }
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.init"></a>[function <span class="apidocSignatureSpan">commitizen.</span>init (sh, repoPath, adapterNpmName)](#apidoc.element.commitizen.init)
- description and source-code
```javascript
function init(sh, repoPath, adapterNpmName) {
  var _ref = arguments.length > 3 && arguments[3] !== undefined ? arguments[3] : defaultInitOptions,
      _ref$save = _ref.save,
      save = _ref$save === undefined ? false : _ref$save,
      _ref$saveDev = _ref.saveDev,
      saveDev = _ref$saveDev === undefined ? true : _ref$saveDev,
      _ref$saveExact = _ref.saveExact,
      saveExact = _ref$saveExact === undefined ? false : _ref$saveExact,
      _ref$force = _ref.force,
      force = _ref$force === undefined ? false : _ref$force;

  // Don't let things move forward if required args are missing
  checkRequiredArguments(sh, repoPath, adapterNpmName);

  // Move to the correct directory so we can run commands
  sh.cd(repoPath);

  // Load the current adapter config
  var adapterConfig = loadAdapterConfig();

  // Get the npm string mappings based on the arguments provided
  var stringMappings = getNpmInstallStringMappings(save, saveDev, saveExact, force);

  // Generate a string that represents the npm install command
  var installAdapterCommand = generateNpmInstallAdapterCommand(stringMappings, adapterNpmName);

  // Check for previously installed adapters
  if (adapterConfig && adapterConfig.path && adapterConfig.path.length > 0) {

    // console.log('
    //   Previous adapter detected!
    // ');

    if (!force) {

      // console.log('
      //   Previous adapter detected!
      // ');

      throw 'A previous adapter is already configured. Use --force to override';
    } else {
      // Override it
      try {
        (0, _util.executeShellCommand)(sh, repoPath, installAdapterCommand);
        addPathToAdapterConfig(sh, CLI_PATH, repoPath, adapterNpmName);
      } catch (e) {
        console.error(e);
      }
    }
  } else {

    // console.log('
    //   No previous adapter was detected
    // ');

    try {

      (0, _util.executeShellCommand)(sh, repoPath, installAdapterCommand);
      addPathToAdapterConfig(sh, CLI_PATH, repoPath, adapterNpmName);
    } catch (e) {
      console.error(e);
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.commitizen.adapter"></a>[module commitizen.adapter](#apidoc.module.commitizen.adapter)

#### <a name="apidoc.element.commitizen.adapter.addPathToAdapterConfig"></a>[function <span class="apidocSignatureSpan">commitizen.adapter.</span>addPathToAdapterConfig (sh, cliPath, repoPath, adapterNpmName)](#apidoc.element.commitizen.adapter.addPathToAdapterConfig)
- description and source-code
```javascript
function addPathToAdapterConfig(sh, cliPath, repoPath, adapterNpmName) {

  var commitizenAdapterConfig = {
    config: {
      commitizen: {
        path: './node_modules/' + adapterNpmName
      }
    }
  };

  var packageJsonPath = _path2.default.join(getNearestProjectRootDirectory(), 'package.json');
  var packageJsonString = _fs2.default.readFileSync(packageJsonPath, 'utf-8');
  // tries to detect the indentation and falls back to a default if it can't
  var indent = (0, _detectIndent2.default)(packageJsonString).indent || '  ';
  var packageJsonContent = JSON.parse(packageJsonString);
  var newPackageJsonContent = '';
  if (_lodash2.default.get(packageJsonContent, 'config.commitizen.path') !== adapterNpmName) {
    newPackageJsonContent = _lodash2.default.merge(packageJsonContent, commitizenAdapterConfig);
  }
  _fs2.default.writeFileSync(packageJsonPath, JSON.stringify(newPackageJsonContent, null, indent) + '\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.adapter.generateNpmInstallAdapterCommand"></a>[function <span class="apidocSignatureSpan">commitizen.adapter.</span>generateNpmInstallAdapterCommand (stringMappings, adapterNpmName)](#apidoc.element.commitizen.adapter.generateNpmInstallAdapterCommand)
- description and source-code
```javascript
function generateNpmInstallAdapterCommand(stringMappings, adapterNpmName) {

  // Start with an initial npm install command
  var installAdapterCommand = 'npm install ' + adapterNpmName;

  // Append the neccesary arguments to it based on user preferences
  var _iteratorNormalCompletion = true;
  var _didIteratorError = false;
  var _iteratorError = undefined;

  try {
    for (var _iterator = stringMappings.entries()[Symbol.iterator](), _step; !(_iteratorNormalCompletion = (_step = _iterator.next
()).done); _iteratorNormalCompletion = true) {
      var _step$value = _slicedToArray(_step.value, 2),
          key = _step$value[0],
          value = _step$value[1];

      if (value) {
        installAdapterCommand = installAdapterCommand + ' ' + value;
      }
    }
  } catch (err) {
    _didIteratorError = true;
    _iteratorError = err;
  } finally {
    try {
      if (!_iteratorNormalCompletion && _iterator.return) {
        _iterator.return();
      }
    } finally {
      if (_didIteratorError) {
        throw _iteratorError;
      }
    }
  }

  return installAdapterCommand;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.adapter.getNearestNodeModulesDirectory"></a>[function <span class="apidocSignatureSpan">commitizen.adapter.</span>getNearestNodeModulesDirectory (options)](#apidoc.element.commitizen.adapter.getNearestNodeModulesDirectory)
- description and source-code
```javascript
function getNearestNodeModulesDirectory(options) {

  // Get the nearest node_modules directories to the current working directory
  var nodeModulesDirectories = (0, _findNodeModules2.default)(options);

  // Make sure we find a node_modules folder

<span class="apidocCodeCommentSpan">  /* istanbul ignore else */
</span>  if (nodeModulesDirectories && nodeModulesDirectories.length > 0) {
    return nodeModulesDirectories[0];
  } else {
    console.error('Error: Could not locate node_modules in your project\'s root directory. Did you forget to npm init or npm install
?');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.adapter.getNearestProjectRootDirectory"></a>[function <span class="apidocSignatureSpan">commitizen.adapter.</span>getNearestProjectRootDirectory (options)](#apidoc.element.commitizen.adapter.getNearestProjectRootDirectory)
- description and source-code
```javascript
function getNearestProjectRootDirectory(options) {
  return _path2.default.join(process.cwd(), getNearestNodeModulesDirectory(options), '/../');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.adapter.getNpmInstallStringMappings"></a>[function <span class="apidocSignatureSpan">commitizen.adapter.</span>getNpmInstallStringMappings (save, saveDev, saveExact, force)](#apidoc.element.commitizen.adapter.getNpmInstallStringMappings)
- description and source-code
```javascript
function getNpmInstallStringMappings(save, saveDev, saveExact, force) {
  return new Map().set('save', save && !saveDev ? '--save' : undefined).set('saveDev', saveDev ? '--save-dev' : undefined).set('
saveExact', saveExact ? '--save-exact' : undefined).set('force', force ? '--force' : undefined);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.adapter.getPrompter"></a>[function <span class="apidocSignatureSpan">commitizen.adapter.</span>getPrompter (adapterPath)](#apidoc.element.commitizen.adapter.getPrompter)
- description and source-code
```javascript
function getPrompter(adapterPath) {
  // Resolve the adapter path
  var resolvedAdapterPath = resolveAdapterPath(adapterPath);

  // Load the adapter
  var adapter = require(resolvedAdapterPath);

<span class="apidocCodeCommentSpan">  /* istanbul ignore next */
</span>  if (adapter && adapter.prompter && (0, _util.isFunction)(adapter.prompter)) {
    return adapter.prompter;
  } else if (adapter && adapter.default && adapter.default.prompter && (0, _util.isFunction)(adapter.default.prompter)) {
    return adapter.default.prompter;
  } else {
    throw "Could not find prompter method in the provided adapter module: " + adapterPath;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.adapter.resolveAdapterPath"></a>[function <span class="apidocSignatureSpan">commitizen.adapter.</span>resolveAdapterPath (inboundAdapterPath)](#apidoc.element.commitizen.adapter.resolveAdapterPath)
- description and source-code
```javascript
function resolveAdapterPath(inboundAdapterPath) {
  // Check if inboundAdapterPath is a path or node module name
  var parsed = _path2.default.parse(inboundAdapterPath);
  var isPath = parsed.dir.length > 0 && parsed.dir.charAt(0) !== "@";

  // Resolve from the root of the git repo if inboundAdapterPath is a path
  var absoluteAdapterPath = isPath ? _path2.default.resolve(getGitRootPath(), inboundAdapterPath) : inboundAdapterPath;

  try {
    // try to resolve the given path
    return require.resolve(absoluteAdapterPath);
  } catch (error) {
    error.message = "Could not resolve " + absoluteAdapterPath + ". " + error.message;
    throw error;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.commitizen.cache"></a>[module commitizen.cache](#apidoc.module.commitizen.cache)

#### <a name="apidoc.element.commitizen.cache.getCacheValueSync"></a>[function <span class="apidocSignatureSpan">commitizen.cache.</span>getCacheValueSync (cachePath, repoPath)](#apidoc.element.commitizen.cache.getCacheValueSync)
- description and source-code
```javascript
function getCacheValueSync(cachePath, repoPath) {
  try {
    var cache = readCacheSync(cachePath);
    return cache[repoPath];
  } catch (e) {
    return;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.cache.readCacheSync"></a>[function <span class="apidocSignatureSpan">commitizen.cache.</span>readCacheSync (cachePath)](#apidoc.element.commitizen.cache.readCacheSync)
- description and source-code
```javascript
function readCacheSync(cachePath) {
  return JSON.parse(_fs2.default.readFileSync(cachePath, 'utf8'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.commitizen.cache.setCacheValueSync"></a>[function <span class="apidocSignatureSpan">commitizen.cache.</span>setCacheValueSync (cachePath, key, value)](#apidoc.element.commitizen.cache.setCacheValueSync)
- description and source-code
```javascript
function setCacheValueSync(cachePath, key, value) {
  var originalCache;
  try {
    originalCache = readCacheSync(cachePath);
  } catch (e) {
    originalCache = {};
  }
  var newCache = _lodash2.default.assign(originalCache, _defineProperty({}, key, value));
  _fs2.default.writeFileSync(cachePath, JSON.stringify(newCache, null, '  '));
  return newCache;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.commitizen.configLoader"></a>[module commitizen.configLoader](#apidoc.module.commitizen.configLoader)

#### <a name="apidoc.element.commitizen.configLoader.load"></a>[function <span class="apidocSignatureSpan">commitizen.configLoader.</span>load (config, cwd)](#apidoc.element.commitizen.configLoader.load)
- description and source-code
```javascript
function load(config, cwd) {
  return (0, _configLoader.loader)(configs, config, cwd);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.commitizen.staging"></a>[module commitizen.staging](#apidoc.module.commitizen.staging)

#### <a name="apidoc.element.commitizen.staging.isClean"></a>[function <span class="apidocSignatureSpan">commitizen.staging.</span>isClean (repoPath, done)](#apidoc.element.commitizen.staging.isClean)
- description and source-code
```javascript
function isClean(repoPath, done) {
  (0, _child_process.exec)('git diff --cached --name-only', {
    maxBuffer: Infinity,
    cwd: repoPath || process.cwd()
  }, function (error, stdout) {
    if (error) {
      return done(error);
    }
    var output = stdout || '';
    done(null, output.trim().length === 0);
  });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
