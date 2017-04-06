# api documentation for  [emberfire (v2.0.6)](https://github.com/firebase/emberfire/)  [![npm package](https://img.shields.io/npm/v/npmdoc-emberfire.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-emberfire) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-emberfire.svg)](https://travis-ci.org/npmdoc/node-npmdoc-emberfire)
#### The officially supported Ember binding for Firebase

[![NPM](https://nodei.co/npm/emberfire.png?downloads=true)](https://www.npmjs.com/package/emberfire)

[![apidoc](https://npmdoc.github.io/node-npmdoc-emberfire/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-emberfire_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-emberfire/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-emberfire/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-emberfire/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Firebase",
        "url": "https://firebase.google.com/"
    },
    "browserify": {
        "transform": [
            "babelify",
            "browserify-shim"
        ]
    },
    "browserify-shim": {
        "ember": "global:Ember",
        "ember-data": "global:DS",
        "firebase": "global:firebase"
    },
    "bugs": {
        "url": "https://github.com/firebase/emberfire/issues"
    },
    "dependencies": {
        "broccoli-merge-trees": "^1.2.1",
        "broccoli-webpack": "^1.0.0",
        "chalk": "1.1.3",
        "ember-cli-babel": "5.1.6",
        "ember-lodash": "0.0.7",
        "firebase": "^3.4.1"
    },
    "description": "The officially supported Ember binding for Firebase",
    "devDependencies": {
        "babelify": "6.4.0",
        "broccoli-asset-rev": "^2.4.2",
        "browserify": "10.2.6",
        "browserify-shim": "3.8.12",
        "codeclimate-test-reporter": "^0.3.3",
        "del": "1.2.0",
        "ember-ajax": "0.7.1",
        "ember-cli": "2.5.1",
        "ember-cli-app-version": "^1.0.0",
        "ember-cli-code-coverage": "^0.3.2",
        "ember-cli-dependency-checker": "^1.2.0",
        "ember-cli-htmlbars": "^1.0.3",
        "ember-cli-htmlbars-inline-precompile": "^0.3.1",
        "ember-cli-inject-live-reload": "^1.4.0",
        "ember-cli-jshint": "^1.0.0",
        "ember-cli-mocha": "^0.12.0",
        "ember-cli-release": "0.2.8",
        "ember-cli-sri": "^2.1.0",
        "ember-cli-uglify": "^1.2.0",
        "ember-data": "^2.5.0",
        "ember-disable-prototype-extensions": "^1.1.0",
        "ember-export-application-global": "^1.0.5",
        "ember-load-initializers": "^0.5.1",
        "ember-resolver": "^2.0.3",
        "ember-sinon": "0.5.1",
        "ember-try": "^0.2.2",
        "glob": "5.0.13",
        "gulp": "3.9.1",
        "gulp-concat": "2.6.0",
        "gulp-header": "1.8.2",
        "gulp-jshint": "1.11.2",
        "gulp-load-plugins": "0.10.0",
        "gulp-rename": "1.2.2",
        "gulp-sourcemaps": "1.6.0",
        "gulp-uglify": "1.5.3",
        "gulp-util": "3.0.7",
        "loader.js": "^4.0.1",
        "lodash": "3.10.1",
        "sinon": "^1.17.3",
        "torii": "0.8.0",
        "vinyl-buffer": "1.0.0",
        "vinyl-source-stream": "1.1.0"
    },
    "directories": {
        "doc": "doc",
        "test": "tests"
    },
    "dist": {
        "shasum": "53ccd86eeb7e2d3102d64fbcf86c74b2a9d3a62c",
        "tarball": "https://registry.npmjs.org/emberfire/-/emberfire-2.0.6.tgz"
    },
    "ember-addon": {
        "configPath": "tests/dummy/config",
        "fastbootDependencies": [
            "firebase"
        ]
    },
    "gitHead": "8937d7e530a2b9e8b85a38c8f4a37ac225ef2f57",
    "homepage": "https://github.com/firebase/emberfire/",
    "keywords": [
        "ember",
        "firebase",
        "realtime",
        "ember-addon"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "firebase",
            "email": "operations@firebase.com"
        }
    ],
    "name": "emberfire",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/firebase/emberfire.git"
    },
    "scripts": {
        "build": "ember build",
        "legacy": "gulp legacy",
        "start": "ember server",
        "test": "ember try:testall"
    },
    "version": "2.0.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module emberfire](#apidoc.module.emberfire)
1.  [function <span class="apidocSignatureSpan">emberfire.</span>included (app)](#apidoc.element.emberfire.included)
1.  [function <span class="apidocSignatureSpan">emberfire.</span>treeForVendor (tree)](#apidoc.element.emberfire.treeForVendor)
1.  string <span class="apidocSignatureSpan">emberfire.</span>name



# <a name="apidoc.module.emberfire"></a>[module emberfire](#apidoc.module.emberfire)

#### <a name="apidoc.element.emberfire.included"></a>[function <span class="apidocSignatureSpan">emberfire.</span>included (app)](#apidoc.element.emberfire.included)
- description and source-code
```javascript
function included(app) {
  this._super.included(app);

  // make sure app is correctly assigned when being used as a nested addon
  if (app.app) {
    app = app.app;
  }
  this.app = app;

  this.app.import('vendor/firebase.amd.js');
}
```
- example usage
```shell
...
var Webpack = require('broccoli-webpack');
var mergeTrees = require('broccoli-merge-trees');

module.exports = {
  name: 'emberfire',

  included: function included(app) {
this._super.included(app);

// make sure app is correctly assigned when being used as a nested addon
if (app.app) {
  app = app.app;
}
this.app = app;
...
```

#### <a name="apidoc.element.emberfire.treeForVendor"></a>[function <span class="apidocSignatureSpan">emberfire.</span>treeForVendor (tree)](#apidoc.element.emberfire.treeForVendor)
- description and source-code
```javascript
treeForVendor = function (tree) {
  var trees = [];

  var firebase;

  try {
    var resolve = require('resolve');
    firebase = resolve.sync('firebase/package.json', {
      basedir: this.project.root
    });
  } catch (e) {
    firebase = require.resolve('firebase/package.json');
  }

  trees.push(new Webpack([
    path.dirname(firebase)
  ], {
    entry: './firebase-browser.js',
    output: {
      library: 'firebase',
      libraryTarget: 'amd',
      filename: 'firebase.amd.js'
    }
  }));

  if (tree) {
    trees.push(tree);
  }

  return mergeTrees(trees, { overwrite: true });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
