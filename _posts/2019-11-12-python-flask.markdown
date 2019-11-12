---
layout: post
title:  "Python and Flask to build Rest API"
description: Python and Flask to build Rest API
date:   2019-11-12 15:00:36 +0530
categories: python flask rest api
---
Do you know Rest API? Certanly, yes. But, in Python? Follow the example to build two endpoints with Python and Flask.

First, we are install Flask:

```python
pip3 install Flask
```
Now, create a file, for example, main.py:
```python
from flask import Flask

app = Flask(__name__)
```
In example above, we're importing Flask and getting reference the Flask.
Now, we're create the code:

```python
@app.route('/info', methods = ['GET'])
def info():
    return 'This a simple endpoint to test and provides information about things.'

@app.route('/insert', methods = ['POST'])
def insert():
    return 'This a simple endpoint to test insert data.'
```

In the code above, @app is a decorator to create routes. The first argument is a URI. The second argument informes the HTTP Method.
Finally, to execute:
```python
if __name__ == '__main__':
    app.run(debug=True)
```

Executing code is:
```python
python3 Main.py
```

and that's all folks!

To any doubt, problem or suggestion, just say.

Sources: [Sources](https://github.com/fagnercandido/pythonandflaskendpoint)
