<!--
title: 'Serverless Websocket Example With Authorizers'
description: 'The example shows you how to deploy simple websocket authorizers'
framework: v1
platform: AWS
language: nodeJS
authorLink: 'https://github.com/yehonadav'
authorName: 'yehonadav bar elan'
-->

# Simple Websockets Authorizers Example

* Deploy the example service: ```sls deploy```  
* connect to the outputted wss url using `wscat`: ```npm install -g wscat```

```
wscat -c wss://xxxxxxx.execute-api.us-east-1.amazonaws.com/dev
```

* Connection should fail.  
* Try again, this time specify an `Auth` header:

 ```
 wscat -c <wss-url> -H Auth:secret
 ```

* Connection succeeds.
* Enjoy chatting with yourself :)