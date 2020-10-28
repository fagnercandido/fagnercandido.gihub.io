---
layout: post
title:  "Download videos of Youtube with Retry in Python"
description: Using Python to download videos of Youtube
date:   2020-10-28 15:00:00 +0530
categories: python retry videos
---

Do you want download videos of Youtube in sequence? In Python this task is very simple.
I add one retry, because the videos are downloaded in high resolution, so, sometimes, the Youtube can fail.
To treat this, i add one retry.

First, we need install two libraries with pip:

```
pip3 install retrying
pip3 install pytube3
```

Now the script:


```
from pytube import YouTube
from retrying import retry

url = ['myListVideos']


def main():
    for item in url:
        download(item)

@retry(stop_max_attempt_number=5)
def download(item):
    YouTube(item).streams.get_highest_resolution().download()

if __name__ == '__main__':
    main()

```

In the initials lines, the imports.
So, we defined URL that we want download. And the script iterate about the URLs.
And using the API do pytube3, we download with high resolution of videos.
Observe that '@retry', here, we define max retrys we want.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
