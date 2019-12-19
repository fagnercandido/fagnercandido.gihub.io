---
layout: post
title:  "Python and Flask to build Rest API"
description: Python and Flask to build Rest API
date:   2019-11-12 15:00:36 +0530
categories: python flask rest api
---
Do you know Rest API? Certainly, yes. How about in Python? Follow this example to build two endpoints with Python and Flask.

First, we are going to install Flask:

```python
pip3 install Flask
```
Now, create a file, for example, main.py:
```python
from flask import Flask

app = Flask(__name__)
```
In the example above, we're importing Flask and getting a reference to it.
Now, add to the code:

```python
@app.route('/info', methods = ['GET'])
def info():
    return 'This a simple endpoint to test and provides information about things.'

@app.route('/insert', methods = ['POST'])
def insert():
    return 'This a simple endpoint to test insert data.'
```

In the code above, ``@app`` is a decorator to create routes. The first argument is an URI. The second argument informs the HTTP Method.
Finally, to execute:
```python
if __name__ == '__main__':
    app.run(debug=True)
```

Running the code is:
```python
python3 Main.py
```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.

Sources: [Sources](https://github.com/fagnercandido/pythonandflaskendpoint)
