---
layout: post
title:  "Using Redis with NodeJS"
description: Using Redis, Docker in NodeJS
date:   2019-09-30 14:00:36 +0530
categories: Node JS JavaScript Redis Docker
---
To use Redis with NodeJS is more simple. In this example, we will use Docker to obtain an instance of Redis. Follow the example:

First of all, pull the docker image for redis:
```sh
docker pull redis
```

After that, start image given a name:
```sh
docker start redis7
```

Now, we will create a new node project:
```sh
npm init -y
```

The next step is to add the redis dependencies:
```sh
npm install redis
```
Now, it is time to code. Create a new file, import redis and create a client redis object:
```javascript
const redis = require('redis')

const clientRedis = redis.createClient(process.env.REDIS_URL)

clientRedis.on('connect', () => {
    console.log(`Server connected with redis`)
});

clientRedis.on('error', err => {
    console.log(`Server redis with error: ${err}`)
});
```
In the code above we created a redis client and started the server. One important thing is the url of redis. In my case, I'm using an environment variable. To setup the variable in linux, for instance, we can run the following:
```sh
 export REDIS_URL="redis://127.0.0.1:6379"
``` 
The default port is 6379, and in this case, the redis is in a docker instance.

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

If you have any doubts, problems or suggestions, just leave a message.
