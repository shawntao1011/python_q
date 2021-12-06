---
title: Why qpython
author: Tao Sun
date: 2021-12-06
category: qpython
layout: post
---

# 为什么使用 qpython
1.更快 

&nbsp;&nbsp;&nbsp;&nbsp;相比于使用 pyodbc来实现python对[tdb][1]数据的访问，使用qpython更加迅速。

2.支持嵌入q语句    

&nbsp;&nbsp;&nbsp;&nbsp;在实际运行中，需要在python端实现调用q脚本等操作，qpython支持q语言嵌入。

3.版本支持完善

&nbsp;&nbsp;&nbsp;&nbsp;q的免费版本为32bit，而实际使用过程中，多使用64位的python，相较于其他python和q交互需要额外配置，qpython直接通过:

```cmd
pip install qpython
```
4.多支持

&nbsp;&nbsp;&nbsp;&nbsp;实际使用中，会有
- [q端下载数据后, 在python端计算的场景][2]
- python端下载python api数据，在python端计算的场景
- [python端处理所有数据，在q端计算的场景][3] 

为了满足以上需求，qpython提供了 Qconnection方法，以便两端传递数据.



[1]:http://www.timestored.com/kdb-guides/kdb-tick-data-store
[2]:https://qpython.readthedocs.io/en/latest/usage-examples.html
[3]:https://stackoverflow.com/questions/59956842/how-can-i-commit-a-dataframe-to-kdb-as-a-new-table





