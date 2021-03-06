# Instagram NodeJS API

This repo contains a NodeJS API for an Unofficial Instagram API which allows you to retrieve information that the offical API doens't allow

This was my simple one-day project. I will keep it updated.

## Dependencies

[install babel-preset-react](https://babeljs.io/docs/en/babel-preset-react.html)

### Libraries
```
var ReactDOMServer = require('react-dom/server')
var express = require('express')
var bodyParser = require('body-parser');
var browserify = require('browserify')
var path = require('path')
var request = require('request')
var session = require('express-session')
var uuidv1 = require('uuid/v1');
var crypto = require('crypto')
var utf8 = require('utf8')
```

## Details

```
1. instagramauth.js contains the NodeJS Instagram API in this repo
2. start.js and webapp.js are examples file on how to execute the code

```

## Sample code

```
var InstagramLoginAPI = require('./app/index.js')

var AuthSession = new InstagramAPI("your_user_name", "your_pass_word") 



/* Some basic info is parsed after login*/
AuthSession.login((data) => { 
	//typeof(data) == object
	//console.log(data) => {success: True or False, data: Response data in string}
		if(data.success)
		{
			console.log(AuthSession.fullname) // ----> User instagram account's full name

			console.log(Authsession.profile_pic) // ----> Profile pic

			var responseDataJSON = JSON.parse(data.data) --> response data from instagram API

			AuthSession.getFollowings( (data) =>
				if(data)
				{
					followings = JSON.parse(data)
				}
			)
		}
})
```

### To start the WebApp demo
`node start.js`



### Quick demo
[![InstaNodeJS](http://img.youtube.com/vi/h5GW_4cWvCc/0.jpg)](http://www.youtube.com/watch?v=h5GW_4cWvCc)

