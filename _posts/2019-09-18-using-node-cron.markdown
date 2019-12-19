---
layout: post
title:  "Using Scheduling with NodeJS"
description: A brief introduction to use cron scheduling in node
date:   2019-09-29 20:00:36 +0530
categories: Node JS JavaScript Cron Schedule
---
node-cron is a possible solution for scheduling in NodeJS. It's very simple to use.

First, run the following command to install the package node-cron:
```sh
npm install node-cron
```

Then add the following line to import the package:
```sh
const cron = require('node-cron')
```

After that the usage is as easy as writing:
```sh
cron.schedule('*/2 * * * *', () => {
    console.log('run every 2 minutes');
});
```

Now, just follow the pattern of cron.

If you have any doubts, problems or suggestions, just leave a message.

Source: [Sources](https://github.com/fagnercandido/node-scheduling)
