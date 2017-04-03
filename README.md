# api documentation for  [knox (v0.9.2)](https://github.com/LearnBoost/knox)  [![npm package](https://img.shields.io/npm/v/npmdoc-knox.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-knox) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-knox.svg)](https://travis-ci.org/npmdoc/node-npmdoc-knox)
#### Amazon S3 client

[![NPM](https://nodei.co/npm/knox.png?downloads=true)](https://www.npmjs.com/package/knox)

[![apidoc](https://npmdoc.github.io/node-npmdoc-knox/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-knox_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-knox/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-knox/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-knox/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk",
        "email": "tj@learnboost.com"
    },
    "bugs": {
        "url": "https://github.com/LearnBoost/knox/issues"
    },
    "contributors": [
        {
            "name": "TJ Holowaychuk",
            "email": "tj@learnboost.com"
        },
        {
            "name": "Domenic Denicola",
            "email": "domenic@domenicdenicola.com"
        },
        {
            "name": "Oleg Slobodksoi",
            "email": "oleg008@gmail.com"
        }
    ],
    "dependencies": {
        "debug": "^1.0.2",
        "mime": "*",
        "once": "^1.3.0",
        "stream-counter": "^1.0.0",
        "xml2js": "^0.4.4"
    },
    "description": "Amazon S3 client",
    "devDependencies": {
        "mocha": "*"
    },
    "directories": {
        "lib": "./lib"
    },
    "dist": {
        "shasum": "3736593669e24f024fdaf723b6a1dc4afd839a71",
        "tarball": "https://registry.npmjs.org/knox/-/knox-0.9.2.tgz"
    },
    "engines": {
        "node": ">= 0.8"
    },
    "gitHead": "5e006ab67d492d1304c30a934466700a7eb79925",
    "homepage": "https://github.com/LearnBoost/knox",
    "keywords": [
        "aws",
        "amazon",
        "s3"
    ],
    "license": "MIT",
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "tjholowaychuk",
            "email": "tj@vision-media.ca"
        },
        {
            "name": "domenic",
            "email": "domenic@domenicdenicola.com"
        }
    ],
    "name": "knox",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/LearnBoost/knox.git"
    },
    "scripts": {
        "test": "mocha"
    },
    "version": "0.9.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module knox](#apidoc.module.knox)
1.  [function <span class="apidocSignatureSpan">knox.</span>createClient (options)](#apidoc.element.knox.createClient)
1.  object <span class="apidocSignatureSpan">knox.</span>auth
1.  object <span class="apidocSignatureSpan">knox.</span>utils
1.  object <span class="apidocSignatureSpan">knox.</span>utils.base64

#### [module knox.auth](#apidoc.module.knox.auth)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>authorization (options)](#apidoc.element.knox.auth.authorization)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>canonicalizeHeaders (headers)](#apidoc.element.knox.auth.canonicalizeHeaders)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>canonicalizeResource (resource)](#apidoc.element.knox.auth.canonicalizeResource)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>hmacSha1 (options)](#apidoc.element.knox.auth.hmacSha1)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>queryStringToSign (options)](#apidoc.element.knox.auth.queryStringToSign)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>sign (options)](#apidoc.element.knox.auth.sign)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>signQuery (options)](#apidoc.element.knox.auth.signQuery)
1.  [function <span class="apidocSignatureSpan">knox.auth.</span>stringToSign (options)](#apidoc.element.knox.auth.stringToSign)

#### [module knox.utils](#apidoc.module.knox.utils)
1.  [function <span class="apidocSignatureSpan">knox.utils.</span>merge (a, b)](#apidoc.element.knox.utils.merge)
1.  object <span class="apidocSignatureSpan">knox.utils.</span>base64

#### [module knox.utils.base64](#apidoc.module.knox.utils.base64)
1.  [function <span class="apidocSignatureSpan">knox.utils.base64.</span>decode (str)](#apidoc.element.knox.utils.base64.decode)
1.  [function <span class="apidocSignatureSpan">knox.utils.base64.</span>encode (str)](#apidoc.element.knox.utils.base64.encode)



# <a name="apidoc.module.knox"></a>[module knox](#apidoc.module.knox)

#### <a name="apidoc.element.knox.createClient"></a>[function <span class="apidocSignatureSpan">knox.</span>createClient (options)](#apidoc.element.knox.createClient)
- description and source-code
```javascript
createClient = function (options){
  return new Client(options);
}
```
- example usage
```shell
...

## Examples

The following examples demonstrate some capabilities of knox and the S3 REST
API. First things first, create an S3 client:

'''js
var client = knox.createClient({
    key: '<api-key-here>'
  , secret: '<secret-here>'
  , bucket: 'learnboost'
});
'''

More options are documented below for features like other endpoints or regions.
...
```



# <a name="apidoc.module.knox.auth"></a>[module knox.auth](#apidoc.module.knox.auth)

#### <a name="apidoc.element.knox.auth.authorization"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>authorization (options)](#apidoc.element.knox.auth.authorization)
- description and source-code
```javascript
authorization = function (options){
  return 'AWS ' + options.key + ':' + exports.sign(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.auth.canonicalizeHeaders"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>canonicalizeHeaders (headers)](#apidoc.element.knox.auth.canonicalizeHeaders)
- description and source-code
```javascript
canonicalizeHeaders = function (headers){
  var buf = []
    , fields = Object.keys(headers);
  for (var i = 0, len = fields.length; i < len; ++i) {
    var field = fields[i]
      , val = headers[field];

    field = field.toLowerCase();

    if (field.indexOf('x-amz') !== 0 || field === 'x-amz-date') {
      continue;
    }

    buf.push(field + ':' + val);
  }

  var headerSort = function(a, b) {
    // Headers are sorted lexigraphically based on the header name only.
    a = a.split(":")[0]
    b = b.split(":")[0]

    return a > b ? 1 : -1;
  }
  return buf.sort(headerSort).join('\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.auth.canonicalizeResource"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>canonicalizeResource (resource)](#apidoc.element.knox.auth.canonicalizeResource)
- description and source-code
```javascript
canonicalizeResource = function (resource){
  var url = parse(resource, true)
    , path = url.pathname
    , buf = [];

  // apply the query string whitelist
  Object.keys(url.query).forEach(function (key) {
      if (whitelist.indexOf(key) != -1) {
          buf.push(key + (url.query[key] ? "=" + url.query[key] : ''));
      }
  });

  return path + (buf.length
    ? '?' + buf.sort().join('&')
    : '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.auth.hmacSha1"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>hmacSha1 (options)](#apidoc.element.knox.auth.hmacSha1)
- description and source-code
```javascript
hmacSha1 = function (options){
  return crypto.createHmac('sha1', options.secret).update(new Buffer(options.message, 'utf-8')).digest('base64');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.auth.queryStringToSign"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>queryStringToSign (options)](#apidoc.element.knox.auth.queryStringToSign)
- description and source-code
```javascript
queryStringToSign = function (options){
  return (options.verb || 'GET') + '\n\n' +
    (typeof options.contentType !== 'undefined' ?
      options.contentType : '') + '\n' +
    options.date + '\n' +
    (typeof options.extraHeaders !== 'undefined' ?
      exports.canonicalizeHeaders(options.extraHeaders) + '\n' : '') +
    (typeof options.token !== 'undefined' ?
      'x-amz-security-token:' + options.token + '\n' : '') +
    options.resource;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.auth.sign"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>sign (options)](#apidoc.element.knox.auth.sign)
- description and source-code
```javascript
sign = function (options){
  options.message = exports.stringToSign(options);
  return exports.hmacSha1(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.auth.signQuery"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>signQuery (options)](#apidoc.element.knox.auth.signQuery)
- description and source-code
```javascript
signQuery = function (options){
  options.message = exports.queryStringToSign(options);
  return exports.hmacSha1(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.auth.stringToSign"></a>[function <span class="apidocSignatureSpan">knox.auth.</span>stringToSign (options)](#apidoc.element.knox.auth.stringToSign)
- description and source-code
```javascript
stringToSign = function (options){
  var headers = options.amazonHeaders || '';
  if (headers) headers += '\n';
  return [
      options.verb
    , options.md5
    , options.contentType
    , options.date instanceof Date ? options.date.toUTCString() : options.date
    , headers + options.resource
  ].join('\n');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.knox.utils"></a>[module knox.utils](#apidoc.module.knox.utils)

#### <a name="apidoc.element.knox.utils.merge"></a>[function <span class="apidocSignatureSpan">knox.utils.</span>merge (a, b)](#apidoc.element.knox.utils.merge)
- description and source-code
```javascript
merge = function (a, b){
  var keys = Object.keys(b);
  for (var i = 0, len = keys.length; i < len; ++i) {
    var key = keys[i];
    a[key] = b[key]
  }
  return a;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.knox.utils.base64"></a>[module knox.utils.base64](#apidoc.module.knox.utils.base64)

#### <a name="apidoc.element.knox.utils.base64.decode"></a>[function <span class="apidocSignatureSpan">knox.utils.base64.</span>decode (str)](#apidoc.element.knox.utils.base64.decode)
- description and source-code
```javascript
decode = function (str){
  return new Buffer(str, 'base64').toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.knox.utils.base64.encode"></a>[function <span class="apidocSignatureSpan">knox.utils.base64.</span>encode (str)](#apidoc.element.knox.utils.base64.encode)
- description and source-code
```javascript
encode = function (str){
  return new Buffer(str).toString('base64');
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
