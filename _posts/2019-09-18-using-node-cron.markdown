---
layout: post
title:  "Using Scheduling with NodeJS"
description: A brief introduction to use cron scheduling in node
date:   2019-09-29 20:00:36 +0530
categories: Node JS JavaScript Cron Schedule
---
To use a scheduling solution in node js, an possible solution is package node-cron. It's very simple to use.

To install the package node-cron:
```sh
npm install node-cron
```

To import the package, follow:
```sh
const cron = require('node-cron')
```

To use this package is very simple:
```sh
cron.schedule('*/2 * * * *', () => {
    console.log('run every 2 minutes');
});
```

Now, just follow the pattern of cron.

To any doubt, problem or suggestion, just say.

Source: [Sources](https://github.com/fagnercandido/node-scheduling)
