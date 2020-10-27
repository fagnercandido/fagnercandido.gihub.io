---
layout: post
title:  "Async and Await in Python"
description: Using Async and Await in Python
date:   2020-10-27 20:00:00 +0530
categories: python concurrency async await
---

Did you know that it is possible to run Python code with Async/Await? Since Python 3x it's possible.
Follow the code, it's very simple:

```
    import asyncio
    import random
    import time

    async def coroutine_task_a():
        tasks = []
        for iteraction in range(100):
            tasks.append(asyncio.create_task(coroutine_task(iteraction)))
        await asyncio.gather(*tasks)


    async def coroutine_task(iteraction):    
        process_time = random.randint(1,5)
        await asyncio.sleep(process_time)
        print(f'Iteration {iteraction}')

    def main():
        asyncio.run(coroutine_task_a())

    if __name__ == '__main__':
        main()

```

In first lines, we do the imports. And we use the keywords async and await to use in coroutines.
The statement 'asyncio.gather(*tasks)' do the magic happened.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
