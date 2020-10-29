# 实验三

## 1.安装pyqt5和pyqt5-tools

用以下命令安装

```
$ pip install -i https://mirrors.aliyun.com/pypi/simple/ pyqt5
$ pip install -i https://mirrors.aliyun.com/pypi/simple/ pyqt5-tools`
```



## 2.使用QT designer绘制窗口

在。。。。。打开designer
绘制如下窗口
![p.01]()
在右边的属性编辑器中修改窗口，按钮，如图
![p.02]()
保存为ui文件，在文件目录下进行py文件编译

```
$pyuic5 -o [FileName].py [FileName].ui
```

新建项目，将写好的离散信号源代码与窗体源代码放在同一目录
在main中，定义编译函数绑定至按钮点击事件

```
import sys
import os
.
.
.
self.pushButton.clicked.connect(self.button1) 
.
.
.
def button1(self):
		str1=('python button1.py')
		os.system(str1)`
加入pyqt主函数运行窗口
`if __name__ == "__main__":
	app = QApplication(sys.argv)
	test_demo = Function()
	test_demo.show()
	sys.exit(app.exec_())`
```

源代码

```
# -*- coding: utf-8 -*-
import numpy as np
import matplotlib.pyplot as plt
plt.rcParams['font.sans-serif']=['SimHei'] 
plt.rcParams['axes.unicode_minus']=False 
plt.subplot(111)
y=[1,0,0,0,0,0,0,0,0]
plt.stem(y)
plt.grid(True)
plt.title('单位脉冲序列')
plt.show()
```

------



```
# -*- coding: utf-8 -*-
import numpy as np
import matplotlib.pyplot as plt
plt.rcParams['font.sans-serif']=['SimHei'] 
plt.rcParams['axes.unicode_minus']=False 
x=np.linspace(0,5,20)
plt.subplot(111)
y2=2*np.sin(0.5*np.pi*x+2)
plt.title('正弦信号')
plt.grid(True)
plt.stem(x,y2)
plt.show()
```

***

```
-*- coding: utf-8 -*-
import numpy as np
import matplotlib.pyplot as plt
plt.rcParams['font.sans-serif']=['SimHei'] 
plt.rcParams['axes.unicode_minus']=False 
x=np.linspace(0,8,10)
plt.subplot(111)
A=2
a=0.6
y=A*a**x
plt.grid(True)
plt.title('实指数信号')
plt.stem(x,y)
plt.show()
```



------



```
# -*- coding: utf-8 -*-
import sys
import os
from PyQt5.QtWidgets import QApplication,QMainWindow
from PyQt5 import QtCore, QtGui, QtWidgets
class Ui_Form(object):
    def setupUi(self, Form):
        Form.setObjectName("Form")
        Form.resize(400, 300)
        self.pushButton = QtWidgets.QPushButton(Form)
        self.pushButton.setGeometry(QtCore.QRect(100, 30, 201, 41))
        self.pushButton.setObjectName("pushButton")
        self.pushButton.clicked.connect(self.button1)
        self.pushButton_2 = QtWidgets.QPushButton(Form)
        self.pushButton_2.setGeometry(QtCore.QRect(100, 130, 201, 41))
        self.pushButton_2.setObjectName("pushButton_2")
        self.pushButton_2.clicked.connect(self.button2)
        self.pushButton_3 = QtWidgets.QPushButton(Form)
        self.pushButton_3.setGeometry(QtCore.QRect(100, 230, 201, 41))
        self.pushButton_3.setObjectName("pushButton_3")
        self.pushButton_3.clicked.connect(self.button3)
        self.retranslateUi(Form)
        QtCore.QMetaObject.connectSlotsByName(Form)
    def retranslateUi(self, Form):
        _translate = QtCore.QCoreApplication.translate
        Form.setWindowTitle(_translate("Form", "离散信号"))
        self.pushButton.setText(_translate("Form", "单位脉冲序列"))
        self.pushButton_2.setText(_translate("Form", "正弦信号"))
        self.pushButton_3.setText(_translate("Form", "实指数信号"))
class Function(QMainWindow,Ui_Form):
	def __init__(self,parent=None):
		super(Function,self).__init__(parent)
		self.setupUi(self)
	def button1(self):
		str1=('python button1.py')
		os.system(str1)
	def button2(self):
		str2=('python button2.py')
		os.system(str2)
	def button3(self):
		str3=('python button3.py')
		os.system(str3)
if __name__ == "__main__":
	app = QApplication(sys.argv)
	test_demo = Function()
	test_demo.show()
	sys.exit(app.exec_())
```

