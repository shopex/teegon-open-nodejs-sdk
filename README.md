teegon.Client NodeJS SDK
======================

Usage
-----

In the shell:

```
npm install teegon-js
```

In your app:

```
teegon = require("../lib/teegon")

client = teegon.Client("http://127.0.0.1:8080/api", "umjj5xj6", "xa4k7gzyemzjkscapdjb");

client.rpc("platform/notify/write", {
    async: false,
    type: "POST",
    params: {"a":"b"},
    success: function(result){
        console.info("test-success:");
        console.info(result)
    },
    error: function(err){
        console.info("test-error:");
        console.info(err)
    },
    timeout: 3
    });

```
