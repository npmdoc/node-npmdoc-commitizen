# npmdoc-commitizen

#### api documentation for  [commitizen (v2.9.6)](https://github.com/commitizen/cz-cli)  [![npm package](https://img.shields.io/npm/v/npmdoc-commitizen.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-commitizen) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-commitizen.svg)](https://travis-ci.org/npmdoc/node-npmdoc-commitizen)

#### Git commit, but play nice with conventions.

[![NPM](https://nodei.co/npm/commitizen.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/commitizen)

- [https://npmdoc.github.io/node-npmdoc-commitizen/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-commitizen/build/apidoc.html)

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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
