---
layout: post
title:  "Using matplotlib in Python"
description: Using matplotlib in Python
date:   2019-10-01 15:00:36 +0530
categories: Python matplotlib
---
The lib matplotlib is widely used in Python and Machine Learning. The good news is that using this lib is very easy.
First of all, we will be installing the dependencies needed:

```sh
python3.7 -m pip install -U matplotlib
```

```sh
sudo apt install python-tk
```

Now, we will plot a simple graphic:
```python
import matplotlib.pyplot as plt

plt.plot([1,2,3,4], [1,5,9,7])
plt.show()
```

In the first line, the packages needed were imported.
Then, we created mock data and plotted it.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.

Sources: [Sources](https://github.com/fagnercandido/tests-matplotlib)
