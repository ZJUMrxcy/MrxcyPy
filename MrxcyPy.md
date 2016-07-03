# 第一章 程序之道
## 1.1 Python
###Python 是一种**解释性语言**，含有_交互模式_、*脚本模式*
     
	"""程序的执行过程
     1.高级语言(high-level language)[源代码(source code)]
     2a.解释语言(interpret)            2b.编译语言(compile)
          ①交互模式                    3b.目标代码(object code)
          ②脚本模式                    4b.可执行(executable)     
                      3a(5b).输出(output)"""

###调试与出错
调试(debugging)	

可能出现3种类型的错误：*语法错误*、*运行时错误（异常）*、*语义错误（可运行，结果错误）*

## 1.2 术语表
**提示符(prompt)、算法(alogorithm)、调试(debugging)、语法(syntax)、异常(exception)、语义(semantics)、记号(token)、语法分析(parse)、语句(statement)**

## 1.3 练习
	
# 第二章 变量、表达式和语句
## 2.1 值和类型
### 值(value)
    """值有不同的类型
    整数(int)、浮点数(float)、字符串(str)…
    思考："""
    >>> 1,000,000   
    (1,0,0)
## 2.2 变量
### **变量***是指向一个值的名称*
	>>>n = 17 #n → 17
	>>>type(n)
	<type'int'>
## 2.3 变量名称和关键字
### **变量名称**
#### 可以使用数字（不可作开头）、字母、'_'，最好使用*小写字母*开头
### **关键字**
	and    as   assert   break      class  continue   def       del 
	elif  else  except  exec(Py2)  finally   for     lambda   nonlocal(Py3)
	not    or   pass     print      raise   return    try      while   
    with  yield      
## 2.4 操作符和对象
### +、-、*、/、**、^
	对于除法
	Py2 /：两个对象都是整数(int)时表示舍去式除法(floor division)
    Py3 /：正常除法 //：舍去式除法
## 2.5 表达式和语句
## 2.6 交互模式与脚本模式
## 2.7 操作顺序
### P.E.M.D.A.S
	Parenthness/Exponentination/Multiplication/Division/Addition/Substraction
## 2.8 字符串操作
### 不适用数学操作
#### 可使用'+'：拼接
#### 可'*'整数(int)：成倍拼接
## 2.9 注释(comments)
	#.....行尾忽略
	#尽量解释为什么这么做，而不是单纯的翻译代码
## 2.10 调试
### 最常见错误：SyntaxError
### bad run：缺失操作符
### use before def：未定义就使用
## 2.11 术语表
# 第三章 函数
## 3.1 函数调用
	>>>type(32)
	<type'int'> #int是返回值(return value)
## 3.2 类型转换函数
	>>>int('32')
	32
	>>>int(3.9999)
	3
	>>>int('Hello')
	ValueError:invaid literal for int():Hello
	>>>floar(32)
	32.0
	>>>float('3.14159')
	3.14159
	>>>str(32)
	'32'
	>>>str(3.14159)
	'3.14159'
## 3.3 数学函数
### 使用模块导入(import)运行环境
	>>>import math #建立模块对象(module object)
	>>>print math
	<module 'math' (built-in)>
### 句点表示法(dot notation)
	>>>ratio = signal_power/noise_power
	>>>descibels = 10*math.log10(ratio)
	>>>radians = 0.7
	>>>height = math.sin(redians) #sin函数中接受的参数是弧度
## 3.4 组合
### 构建块(building block)
	x = math.sin(degrees/360.0*2*math.pi)
### 赋值表达左边必须是变量名称
## 3.5 添加新函数
### 3.5.1 定义函数
#### ①第一个字不能是数字
#### ②关键字不能作函数名
#### ③尽量避免函数和变量同名
### 3.5.2 函数定义
#### 函数头(header)以冒号结束
#### 函数体(body)整体缩进一级(4个空格)
#### 单引号与双引号作用相同
#### 定义之后会创建一个*同名变量*
#### 定义之后可以在其它函数中调用它，包括它*本身*
### 3.5.3 交互模式
#### 交互模式下需要一个空行来表示函数结束(脚本模式不需要)
## 3.6 定义和使用
### 函数定义
#### ①会产生(创建)函数对象
#### ②不会产生输出，不会执行
#### ③调用时才会执行
## 3.7 执行流程
	"""第一行 #从上到下执行
       函数A  #跳至函数A第一行，执行，再返回
       函数B  #跳至函数B第一行，执行，再返回
	   第N行  #阅读代码要用 *执行顺序*"""
## 3.8 形参(parameter)和实参(argument)
### 函数定义中的是形参
### 函数调用时传入的是实参
## 3.9 变量和形参是局部的(local)
	def cat_twice(part1,part2):
	    cat = part1 + part2 #cat是局部的
	    print_twice(cat)
    >>>line1 = 'B'          #<module>: line1 → 'B', line2 → 'A'
    >>>line2 = 'A'
    >>>cat_twice(line1, line2) #函数执行后，cat被销毁
    BA               #cat_twice: part1 → 'B', part2 → 'A', cat → 'BA'
	BA               #print_twice: bruce → 'BA'
	>>>print cat
	NameError:name 'cat' is not defined
## 3.10 栈图(stack diagram)
### 跟踪变量
### 回溯(traceback)
## 3.11 有返回值函数(fruitful function)和无返回值函数(void function)
## 3.12 为什么要有函数
## 3.13 使用from导入模块
	from math import pi
    from math import *
## 3.14 调试
### 开头写一句print 'hello'，再运行一次，确认是否运行的是面前的程序
## 3.15 术语表
## 3.a 增加知识
	print 'a', # Py2中不换行
	print ('a', end = ''), # Py3中不换行
# 第4章 案例研究：接口设计
## 4.1 乌龟世界
	print bob # bob是变量
	<TurtlrWorld.Turtle instance at 0xb7bfbf4c> # instant(实例)
## 4.2 简单重复
	for i in range() # for语句有时称为循环(loop)
## 4.3 练习
## 4.4 封装(encapsulation)
## 4.5 泛化(generalization)
## 4.6 接口设计
## 4.7 重构(refactoring)
## 4.8 一个开发计划(development plan)
### 1. 写个小程序，不需要函数定义
### 2. 一旦运行成功，*封装*到一个函数中，命名
### 3. *泛化*函数，添加合适的形参
### 4. *重复*1-3，得到一组可行的函数
### 5. 寻找*重构*的机会，改善程序，发现相似之处可以做*通用函数*
## 4.9 文档字符串(docstring)
### """.....
###    .....
###    .....""" #解释接口的字符串
### 一个设计良好的接口应该很简单就能解释清楚
## 4.10 调试
### polyline() #含有4个参数
### t → Turtle
### n → int
### length → 正数
### angle → 数字
### 上述函数开始时满足的条件：前置条件
### 函数结束时满足的条件：后置条件(*1.函数预期效果；2.副作用*)
## 4.11 术语表
## 4.12 练习
## 4.a 本章练习代码
### 用bob画正方形、多边、多边形、圆弧、圆
	from swampy.TurtleWorld import *
	import math

	world=TurtleWorld()
	bob=Turtle()
	print bob

	def square(t,length):
    	for i in range(4):
        	fd(t,length)
        	lt(t)

	"""Draws n line segments with the given length
	and angle(in degrees) between them.t is a turtle"""

	def polyline(t,n,length,angle):    #generalization
    	for i in range(n):
        	fd(t,length)
        	lt(t,angle)
    	print t
    	print n
    	print length
    	print angle
    
	def polygon(t,n,length):      #generalization
	    angle=360.0/n
	    polyline(t,n,length,angle)

	"""Draws a arc with the given radius and angle(in degrees)
	between them.t is a turtle"""
	
	def arc(t,r,angle):           #generalization
	    arc_circumference=2*math.pi*r*angle/360.0
	    n=int(arc_circumference/0.1)+1
	    step_angle=float(angle)/n
	    step_length=arc_circumference/n
	    bob.delay=0.0001
	
	    # making a slight left turn before starting reduces
	    # the error caused by the linear approximation of the arc
	    lt(t,step_angle/2)
	    polyline(t,n,step_length,step_angle)
	    rt(t,step_angle/2)
	
	    print arc_circumference
	    print n
	    print t
	    print r
	    print angle
	    print step_length
	    print step_angle

	"""Draws a circle with the given radius.t is a turtle"""

	def circle(t,r):
	    arc(t,r,360)              #encapsulation
	    print t
	    print r


	arc(bob,r=100,angle=120)
	
	wait_for_user()

### 用bob画花朵图案
	from swampy.TurtleWorld import *
	import math

	world=TurtleWorld()
	bob=Turtle()
	print bob

	def square(t,length):
    	for i in range(4):
    	    fd(t,length)
    	    lt(t)

	"""Draws n line segments with the given length
	and angle(in degrees) between them.t is a turtle"""

	def polyline(t,n,length,angle):    #generalization
	    for i in range(n):
	        fd(t,length)
	        lt(t,angle)
	    
	def polygon(t,n,length):      #generalization
	    angle=360.0/n
	    polyline(t,n,length,angle)
	
	"""Draws a arc with the given radius and angle(in degrees)
	between them.t is a turtle"""
	
	def arc(t,r,angle):           #generalization
	    arc_circumference=2*math.pi*r*angle/360.0
	    n=int(arc_circumference/1)+1
	    step_angle=float(angle)/n
	    step_length=arc_circumference/n
	    bob.delay=0.00001
	
	    # making a slight left turn before starting reduces
	    # the error caused by the linear approximation of the arc
	    lt(t,step_angle/2)
	    polyline(t,n,step_length,step_angle)
	    rt(t,step_angle/2)

	def flower(t,r,num):
	    flower_angle=360.0/num
	    turn_angle=180-flower_angle/2
	    for i in range(num):
	        arc(t,r,flower_angle)
	        lt(t,turn_angle)
	
	flower(bob,100,9)

### 4-3 画pie
	from swampy.TurtleWorld import *
	import math

	world=TurtleWorld()

	bob=Turtle()
	bob.delay=1
	
	print bob
	
	
	def pie(t,n,l):
	    r=(l/2.0)/math.sin(math.pi/n)
	    step_angle=180-(180.0-360.0/n)/2.0
	    lt(t,180.0/n)
	    
	    for i in range(n):
	        fd(t,r)
	        lt(t,step_angle)
	        fd(t,l)
	        pu(t)
	        lt(t,step_angle)
	        fd(t,r)
	        lt(t,180)
	        pd(t)
	
	    for j in range(n,n+1):
	        rt(t,180.0/n)
	        pu(t)
	        way=4*r
	        fd(t,way)
	        pd(t)
	    
	pie(bob,5,40)
	pie(bob,6,60)
	pie(bob,7,40)
	pie(bob,8,80)
	
	wait_for_user()
### 4-4 画字母，乌龟打字机
	from swampy.TurtleWorld import *
	import math
	
	world=TurtleWorld()
	
	bob=Turtle()
	bob.delay=0.0001
	
	print bob
	"""Draws n line segments with the given length
	and angle(in degrees) between them.t is a turtle"""

	
	
	
	def polyline(t,n,length,angle):    #generalization
	    for i in range(n):
	        fd(t,length)
	        lt(t,angle)
	    
	def polygon(t,n,length):      #generalization
	    angle=360.0/n
	    polyline(t,n,length,angle)
	
	"""Draws a arc with the given radius and angle(in degrees)
	between them.t is a turtle"""
	
	def arc(t,r,angle):           #generalization
	    arc_circumference=2*math.pi*r*angle/360.0
	    n=int(arc_circumference/1)+1
	    step_angle=float(angle)/n
	    step_length=arc_circumference/n
	
	    # making a slight left turn before starting reduces
	    # the error caused by the linear approximation of the arc
	    lt(t,step_angle/2)
	    polyline(t,n,step_length,step_angle)
	    rt(t,step_angle/2)

	    
	def draw_a():
	    t=bob
	    lt(t,90)
	    pu(t)
	    fd(t,10)
	    pd(t)
    	fd(t,90)
    	pu(t)
    	bk(t,10)
    	lt(t,45)
    	pd(t)
    	arc(t,80.0/1.41,270)
    	rt(t,135)
    	arc(t,15,120)
    

	def draw_b():
    	t=bob
    	rt(t,90)
    	fd(t,200)
    	lt(t,90)
    	arc(t,50,180)
	
	def draw_c():
	    t=bob
	    lt(t,135)
	    arc(t,50,270)
	
	def draw_d():
	    t=bob
	    rt(t,90)
	    fd(t,200)
	    pu(t)
	    bk(t,100)
	    pd(t)
	    rt(t,90)
	    arc(t,50,180)
	
	draw_d()
### 4-5 阿基米德螺旋线
