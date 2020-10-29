# 实验二
## 1.安装python
 我参考了[这个网页](https://blog.csdn.net/nmjuzi/article/details/79075736)
## 2.绘制典型连续信号
因为清理电脑的缘故所以没有图片了所以直接放源代码
# 源代码
```
# -*- coding: utf-8 -*-
import numpy as np
import math
import matplotlib.pyplot as plt             #图表绘图
fig = plt.figure(figsize=(6, 4))            #新建图表
ax1 = fig.add_subplot(111)      

x=np.arange(-4,4,0.01)          
y=np.exp(x)

plt.rcParams['font.sans-serif']=['SimHei'] 
plt.rcParams['axes.unicode_minus']=False 

ax1.spines['right'].set_color('none')
ax1.spines['top'].set_color('none')
ax1.xaxis.set_ticks_position('bottom')
ax1.spines['bottom'].set_position(('data', 0))
ax1.yaxis.set_ticks_position('left')
ax1.spines['left'].set_position(('data',0))

plt.title(r'$f(x)=e^x$') 
plt.plot(x,y)
plt.show()`
```



***
```
`# -*- coding: utf-8 -*-
import numpy as np
import matplotlib.pyplot as plt             #图表绘图
fig = plt.figure(figsize=(6, 4))            #新建图表
ax1 = fig.add_subplot(111)                  #新建坐标轴

x=np.arange(-2*np.pi,2*np.pi,0.01)          #-2pi到2pi为区间 每0.01描点
y=np.sin(x)                                 #绘制函数sin(x)

plt.rcParams['font.sans-serif']=['SimHei'] 
plt.rcParams['axes.unicode_minus']=False 

ax1.spines['right'].set_color('none')
ax1.spines['top'].set_color('none')
ax1.xaxis.set_ticks_position('bottom')
ax1.spines['bottom'].set_position(('data', 0))
ax1.yaxis.set_ticks_position('left')
ax1.spines['left'].set_position(('data',0))

plt.title(r'$f(x)=sin x$') 
plt.plot(x,y)
plt.show()`

***

`# -*- coding: utf-8 -*-
import numpy as np
import matplotlib.pyplot as plt             #图表绘图
fig = plt.figure(figsize=(6, 4))            #新建图表
ax1 = fig.add_subplot(111)                  #新建坐标轴

x=np.arange(-2*np.pi,2*np.pi,0.01)          #-2pi到2pi为区间 每0.01描点
y=np.sin(x)                                 #绘制函数sin(x)

plt.rcParams['font.sans-serif']=['SimHei'] 
plt.rcParams['axes.unicode_minus']=False 

ax1.spines['right'].set_color('none')
ax1.spines['top'].set_color('none')
ax1.xaxis.set_ticks_position('bottom')
ax1.spines['bottom'].set_position(('data', 0))
ax1.yaxis.set_ticks_position('left')
ax1.spines['left'].set_position(('data',0))

plt.title(r'$f(x)=sin x$') 
plt.plot(x,y)
plt.show()`
```

