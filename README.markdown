CouchDBServer
=============

This is an extended version of the `couch.js` JavaScript library included with CouchDB It is intended for use in JavaScript environments where cross-domain requests are not a problem and the CouchDB server is hosted remotely.

It can be used without modification and behave exactly as the original `couch.js`, but it adds a new "class" (CouchDBServer) to allow access to a remote server. It has been tried and appears to work (though has not been througoughly tested) on Jaxer and ASP.

# Usage

Most all of the original "static" methods of the `CouchDB `class are also members of the `CouchDBServer` class. So:

    var server = new CouchDBServer("http://example.com");
    server.allDbs();
    var myDb = server.openDb('existing');
    myDb.save({ a : 1, b : 2}); // And so on...
    var newDb = server.createDb('new');

See the source for more.

# Compatibility

The [master branch](http://github.com/smith/couch.js/tree/master) is updated frequently to track changes in CouchDB trunk. Use this if you are using the latest development version.

The [0.8.1 tag](http://github.com/smith/couch.js/tree/0.8.1) is compatible with CouchDB 0.8.1 and is not in active development.
