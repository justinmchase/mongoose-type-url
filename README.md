# mongoose-type-url

A url field-type for Mongoose schemas

[![npm](https://nodei.co/npm/mongoose-type-url.png)](https://www.npmjs.com/package/mongoose-type-url)
[![Build Status](https://travis-ci.org/konsumer/mongoose-type-url.svg?branch=master)](https://travis-ci.org/konsumer/mongoose-type-url)
[![Code Climate](https://codeclimate.com/github/konsumer/mongoose-type-url/badges/gpa.svg)](https://codeclimate.com/github/konsumer/mongoose-type-url)

## usage

This will validate a url, correctly:

```
var mongoose = require('mongoose');
require('mongoose-type-url');

var UserSchema = new mongoose.Schema({
    url: {
        work: mongoose.SchemaTypes.Url,
        profile: mongoose.SchemaTypes.Url
    }
});
```

You can also use the stuff in `String` type:

```javascript
var UserSchema = new mongoose.Schema({
    url: {
        work: {type: mongoose.SchemaTypes.Url, required: true},
        profile: {type: mongoose.SchemaTypes.Url, required: true},
    }
});
```

You can also use it as an array:


```javascript
var UserSchema = new mongoose.Schema({
    urls: [{type: mongoose.SchemaTypes.Url}]
});
```