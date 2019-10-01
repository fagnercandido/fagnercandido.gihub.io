---
layout: post
title:  "Using matplotlib in Python"
description: Using matplotlib in Python
date:   2019-09-30 14:00:36 +0530
categories: Python matplotlib
---
The lib matplotlib is widely used in Python and Machine Learning. Ont the better parts is that use this lib is very easy.
First of all, we will installing the dependencies needed:

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

In the first line, was imported the packages needed.
Then, we will create data and plot the data.

and that's all folks!

To any doubt, problem or suggestion, just say.

Sources: [Sources](https://github.com/fagnercandido/tests-matplotlib)
