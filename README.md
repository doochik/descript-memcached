[![Build Status](https://travis-ci.org/doochik/descript2-memcached.svg?branch=master)](https://travis-ci.org/doochik/descript2-memcached)
[![NPM version](https://badge.fury.io/js/descript2-memcached.svg)](https://www.npmjs.com/package/descript2-memcached)


# descript2-memcached

## Usage

```
const de = require('descript2');
const deMemcached = require('descript2-memcached');

const context = new de.Context(req, res, {
    cache: new deMemcached(myCacheConfig)  
});
```

## Config

```
{
    servers: 'my-memcached-server:9000'// memcached servers @see https://github.com/3rd-Eden/memcached#options
    defaultKeyTTL: 60 * 60 * 24, // key ttl in seconds
    generation: 1, // increment generation to invalidate all key across breaking changes releases
    readTimeout: 100, // read timeout in milliseconds,
    memcachedOptions: {}, // @see https://github.com/3rd-Eden/memcached#options
}
```
