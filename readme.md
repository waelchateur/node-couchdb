Simple node CouchDB client
==========================

- Best use of [www.partialjs.com](http://partialjs.com)
- Easy use with [Iris Couch](http://www.iriscouch.com)

***

## NPM partial-couchdb

- create on your desktop empty directory with name: website
- open terminal and find this directory: cd /Desktop/website/
- write and run on terminal:

```text
$ npm install partial-couchdb
```

## Methods

```js
/*
    Constructor
    @connectionString {String} :: url address (http://petersirka:123456@127.0.0.1:5984/yourdatabase/)
*/
CouchDB(connectionString);
 
/*
    Usage / Constructor
    @connectionString {String} :: url address
    return {CouchDB};
*/
require('partial-couchdb').init(connectionString);
 
/*
    CouchDB command
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.compactDatabase(cb);
couchdb.compactViews(cb);
couchdb.cleanupViews(cb);
 
/*
    CouchDB command
    @namespace {String}
    @name {String}
    @params {Object}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.view(namespace, name, params, cb);
couchdb.list(namespace, name, params, cb);
couchdb.show(namespace, name, params, cb);
 
/*
    CouchDB command
    @id {String}
    @revs {String} :: optional
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
CouchDB.find(id, revs, cb);
 
/*
    CouchDB command
    @params {Object}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.all(params, cb);
couchdb.changes(params, cb);
 
/*
    CouchDB command
    @funcMap {Function or String} :: string with function declaration
    @funcReduce {Function or String} :: string with function declaration
    @params {Object}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.query(funcMap, funcReduce, params, cb);
 
/*
    CouchDB command
    @doc {Object}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.insert(doc, cb);
 
/*
    CouchDB command
    @doc {Object}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.update(doc, cb);
 
/*
    CouchDB command
    @namespace {String}
    @view {Object} :: view = { map: { name: 'function... ', reduce: 'function...'}}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.insertView(namespace, view, cb);
 
/*
    CouchDB command
    @rev {String} :: old revision
    @namespace {String}
    @view {Object} :: view = { map: { name: 'function... ', reduce: 'function...'}}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.updateView(rev, namespace, view, cb);
 
/*
    CouchDB command
    @path {String}
    @method {String}
    @obj {Object}
    @params {Object}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.request(path, method, obj, params, cb);
 
/*
    CouchDB command
    @doc {Object or String}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.delete(doc, cb);
 
/*
    CouchDB command
    @doc {Object}
    @fileName {String}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.deleteAttachment(doc, fileName, cb);
 
/*
    CouchDB command
    @arr {Object array}
    @cb {Function} :: function(error, object)
    return {CouchDB}
*/
couchdb.bulk(arr, cb);
 
/*
    CouchDB command
    @docOrId {String or Object}
    @fileName {String}
    @response {Function or ServerResponse} :: function(data)
    return {CouchDB}
*/
couchdb.attachment(docOrId, fileName, response);
 
/*
    CouchDB command
    @docOrId {String or Object}
    @fileName {String}
    @fileSave {String}
    @cb {Function} :: optional function(error, object)
    return {CouchDB}
*/
couchdb.upload(docOrId, fileName, fileSave, cb);
 
/*
    CouchDB command
    @max {Number}
    @cb {Function} :: optional function(error, object)
    return {CouchDB}
*/
couchdb.uuids(max, cb);
```

***

## The MIT License

Copyright (c) 2012-2013 Peter Širka <petersirka@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Contact

[www.petersirka.sk](http://www.petersirka.sk)
