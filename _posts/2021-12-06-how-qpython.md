---
title: How to use qpython
author: Tao Sun
date: 2021-12-06
category: qpython
layout: post
---

## QPython 使用

### 文档地址:

https://qpython.readthedocs.io/en/latest/index.html

### 使用样例:
q端：

```sh
q [filepath] -p [port]
```

python端：

```python
from qpython import qconnection

q = qconnection.QConnection(host = [host], port = [port])
try:
    q.open()
    temp = q('{[x;y] select wind_code,date,ret from stock_daily where date within (x;y)}', 
             x,y, 
             pandas=True)
finally:
    q.close()
```

or  recommended:

```python
with qconnection.QConnection(host = [host], port = [port]) as q:
    temp = q('{[x;y] select wind_code,date,ret from stock_daily where date within (x;y)}', 
             x,y, 
             pandas=True)
```

