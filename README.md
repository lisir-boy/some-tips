# some-tips
关于arduino
1、打开或关闭串口监视器时相当于对aduino板进行重置 reset 即系统从头开始运行 系统变量变为初始值  millis()也变为初始的值（应该是0）
2、关于python中类中的__init__，其下的变量在调时后面不用加（），而之外用def定义的函数需要加（），里面有的还需要加参数，
3、python中双下划线的函数，代表私有的，不可以之间被外部调用，但是可以在同一类下调用
4.python定义类中的函数时 如果在之前加@property 在调用时不用加（）相关例子代码：
class Student(object):
    def __init__(self, name, score):
        self.name = name
        self._score = score
#    @property
    def score(self):
        return self._score
#    @score.setter

#    def score(self, score):
#        if score < 0 or score > 100:
#            raise ValueError('invalid score')
 #       self._score = score
s=Student('bob',23)
#s.score=340

#s.score(33)
print(s.score())

