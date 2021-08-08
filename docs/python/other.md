# Python绘图问题：Matplotlib中%matplotlib inline是什么、如何使用？

 [Python绘图问题：Matplotlib中%matplotlib inline是什么、如何使用？_liangzuojiayi的博客-CSDN博客_%matplotlib inline](https://blog.csdn.net/liangzuojiayi/article/details/78183783) 



%matplotlib inline

是一个魔法函数（Magic Functions）。官方给出的定义是：IPython有一组预先定义好的所谓的魔法函数（Magic Functions），你可以通过命令行的语法形式来访问它们。可见“%matplotlib inline”就是模仿命令行来访问magic函数的在IPython中独有的形式。

magic函数分两种：一种是面向行的，另一种是面向单元型的。

行magic函数是用前缀“%”标注的，很像我们在系统中使用命令行时的形式，例如在Mac中就是你的用户名后面跟着“$”。“%”后面就是magic函数的参数了，但是它的参数是没有被写在括号或者引号中来传值的。

单元型magic函数是由两个“%%”做前缀的，它的参数不仅是当前“%%”行后面的内容，也包括了在当前行以下的行。

注意：既然是IPython的内置magic函数，那么在Pycharm中是不会支持的。

#内嵌画图
%matplotlib inline
import matplotlib # 注意这个也要import一次
import matplotlib.pyplot as plt
myfont = matplotlib.font_manager.FontProperties(fname=r'C:/Windows/Fonts/msyh.ttf') # 这一行
plt.plot((1,2,3),(4,3,-1))
plt.xlabel(u'横坐标',  fontproperties=myfont) # 这一段
plt.ylabel(u'纵坐标',  fontproperties=myfont) # 这一段
#plt.show() # 有了%matplotlib inline 就可以省掉plt.show()了
————————————————
版权声明：本文为CSDN博主「LthID」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/liangzuojiayi/article/details/78183783

