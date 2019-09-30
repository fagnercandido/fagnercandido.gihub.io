---
layout: post
title:  "Using Redis with NodeJS"
description: Using Redis, Docker in NodeJS
date:   2019-09-30 14:00:36 +0530
categories: Node JS JavaScript Redis Docker
---
To use Redis with NodeJS is more simple. In this example, we will use Docker to obtain an instance of Redis. Follow the example:

First of all, pull docker image redis:
```sh
docker pull redis
```

After this, start image given a name:
```sh
docker start redis7
```

Now, we will create a new node project:
```sh
npm init -y
```

The next step, add the redis dependencies:
```sh
npm install redis
```
Now, time's to code. Create a new file, import redis and create a client redis object:
```javascript
const redis = require('redis')

const clientRedis = redis.createClient(process.env.REDIS_URL)

clientRedis.on('connect', () => {
    console.log(`Server connect with redis`)
});

clientRedis.on('error', err => {
    console.log(`Server redis with error: ${err}`)
});
```
In the above code, we create a redis client and start the server. One thing important, is the url of redis. In my case, i'm using the environment variable. In enviroment linux, for instance:
```sh
 export REDIS_URL="redis://127.0.0.1:6379"
``` 
The port 6379 is default, and in this case, the redis be in instance docker.

Finally, just get and set content in redis:
```javascript
clientRedis.get(args, function(err, data) {
    if (data) {
        return response.send(data)
    }
})

clientRedis.setex(url, 3600, JSON.stringify(someData))//3600 is when data will expires
```
and that's all folks!

To any doubt, problem or suggestion, just say.
