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
	""".....
	   .....
	   .....""" #解释接口的字符串
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
# 第5章 条件和递归
## 5.1 求模操作符(%)(modulus operator)
### 只作用于整数
#### ①测试整除 x%y == 0
#### ②获取一个数后一位或几位 # x%10 x%100 ...
	>>>quotient = 7 / 3
	>>>print quotient
	2
	
	>>>reminder = 7 % 3
	>>>print reminder
	1
## 5.2 布尔表达式(值为真或假)
### 关系操作符(relational operator)
	x == y
	x != y
	x > y
	x < y
	x >= y
	x <= y
## 5.3 逻辑操作符(logical operator)
### and or not 
### python中，任何非0的数都被解释为“true”
	>>>17 and True
	True
## 5.4 条件执行
### 条件语句(conditional statement)
	if x > 0: # 条件(condition)
		print 'x is position' # 最少需要一行
	
	if x < 0:
		pass # 通常标记为一个没来得及写代码的位置(如需要处理负值的情况)
## 5.5 选择执行
	if x % 2 == 0:
		print 'x is even' # 分支(branch)
	else:
		print 'x is odd' # 分支(branch)
## 5.6 条件链(chained conditional)
	if x < y:
		print 'x is less than y'
	elif x > y:
		print 'x is greater than y'
	else:
		print 'x and y are equal' # else语句必须放最后，或者没有
### false → false → true → 执行 → 结束 --- true --- true
### 执行第一个true！
## 5.7 嵌套条件(nested condition)
	if x == y:
		print 'x and y are equal'
	else:
		if x < y:
			print 'x is less than y'
		else:
			print 'x is greater than y' # 嵌套越多，可读性越差，尽量避免
### 逻辑操作符通常可以简化嵌套
## 5.8 递归(recursion)
### 函数调用另一个函数，或者调用自己都是合法的
	def print_n (s, n):
		if n <= 0:
			return # return直接退出函数
		print s
		print_n (s, n-1)
## 5.9 递归函数的栈图
### 函数每一次被调用 → Python → 新建一个函数帧(function frame)(包括局部变量、参数)
	"""<module> 函数 n = 3: # → __main__ 函数帧
	   countdown n → 3
	   countdown n → 2
	   countdown n → 1
       countdown n → 0 # 基准情形(base case):后面没有其他函数帧"""
	
	"""print_n 函数 s = 'Hello', n = 2
	   <module> # → __main__ 函数帧  
	   print_n s → 'Hello', n → 2
	   print_n s → 'Hello', n → 1
	   print_n s → 'Hello', n → 0"""
## 5.10 无限递归(infinite recursion)
### Python会在递归深度到达上限时报告一个错误信息：Runtime Error
## 5.11 键盘输入
### Python2: raw_input('提示信息')
### Python3: input('提示信息')
### 如果希望输入整数 
	>>>speed = raw_input(prompt)
	>>>int(speed)
	
	>>>speed = int(raw_input(prompt))
## 5.12 调试
### 回溯 → 最有用：①错误类型；②错误发生的地方
## 5.13 练习
### 5-2
	"""do_n(f, n)：进行n次f()操作"""
	def do_n(f, n):
   
	    if n <= 0:
    	    return
    	else:
    	    f
    	    do_n(f, n-1) 
    
	def f():
	    print ('xcy is talent')

	
	do_n(f,8) # 这是个错的，因为执行f时就回打印后停止执行
	
	    
	def do_n(g, n):
	   
	    if n <= 0:
	        return
	    else: 
	        print(g)
	        do_n(g, n-1)
	    
	def f():
	    return 'xcy is talent'
	
	
	do_n(f(), 8) # 可是为什么这个执行了print(g)，不会停止执行呢？，可能因为上面那个是无返回值函数，下面这个是有返回值的函数？
### 5-3
	"""输入三个整数与一个整数指数来检验费马大定理"""
	def check_fermat(a,b,c,n):
	   	int(a)
    	int(b)
    	int(c)
    	int(n)
    
    	if n>2 and a**n+b**n==c**n:
    	    print('天哪，费马弄错了')
    	else:
    	    print('不，那样不行')

	def input_check_fermat(): 
	    x=int(input('请输入整数a\n'))
	    y=int(input('请输入整数b\n'))
	    z=int(input('请输入整数c\n'))
	    m=int(input('请输入整数n,其中n>2\n'))
	    check_fermat(x,y,z,m)
	
	input_check_fermat()
### 5-4
	"""检验输入的边长是否可以组成三角形，如果可以打印Yes，不行打印No"""
	def is_triangle():
    	a=int(input('请输入边长a\n'))
    	b=int(input('请输入边长b\n'))
    	c=int(input('请输入边长c\n'))
    	
    	if a+b<=c or a+c<=b or b+c<=a:
    	    print('No')
    	else:
    	    print('Yes')

	is_triangle()
### 5-5
	"""用bob绘制一个分叉"""
	from swampy.TurtleWorld import *
	world=TurtleWorld()
	bob=Turtle()
	bob.delay=0.1

	def draw(t,length,n):
    	if n==0:
    	    return
    	angle=50
	    fd(t,length*n)
	    lt(t,angle)
	    draw(t,length,n-1)
	    rt(t,2*angle)
	    draw(t,length,n-1)
	    lt(t,angle)
	    bk(t,length*n)
	
	draw(bob,10,2)
### 5-6 
	"""从雪花泛化为科勒曲线"""
	from swampy.TurtleWorld import *
	world=TurtleWorld()
	bob=Turtle()
	bob.delay=0.01
	bob.x = -150
	bob.y = -250
	
	import math
	
	"""设置对象t，直线距离总长度l，每次变化角度angle作为科勒曲线的初始化值"""
	def koch(t,l,angle):
	    if l<3.0:
	        fd(t,l)
	        return
	    else:
	        float(angle)
	        m=l/(2+math.cos(angle/180*math.pi))
	        koch(t,m,angle)
	        lt(t,angle)
	        koch(t,m,angle)
	        rt(t,2*angle)
	        koch(t,m,angle)
	        lt(t,angle)
	        koch(t,m,angle)

	"""设置对象s_t，雪花边直线距离总长s_l，雪花每条边的每次变化角度为s_angle"""
	def snowflake(s_t,s_l,s_angle):
	    for i in range(3):
	        koch(s_t,s_l,s_angle)
	        rt(s_t,2*s_angle)
	
	"""设置科勒曲线输入函数，给定对象为bob"""
	def input_koch():
	    k=float(raw_input('input length\n'))
	    k_angle=float(raw_input('input angle\n'))
	    koch(bob,k,k_angle)
	
	"""设置雪花曲线输入函数，给定对象为bob"""
	def input_snowflake():
    	k=float(raw_input('input length\n'))
	    k_angle=float(raw_input('input angle\n'))
	    koch(bob,k,k_angle)
	
	input_koch()
	
	bob.redraw()
# 第6章 有返回值函数
## 6.1 返回值
	def area(redius):
		return math.pi * redius ** 2
	
	def area(redius):
		temp = math.pi * redius ** 2
		return temp
### return语句后的语句不再被执行 → 无效代码(dead code)
### 有返回值函数上应保证每个可能执行路径上都会遇到 *return*
	def absolute_value(x):
		if x < 0:
			return -x
		if x > 0:
			return x
		if x = 0:
			return x
	# abs()绝对值函数
## 6.2 增量开发(incremental development)
### 每次只测试一小部分代码
### 考虑函数： 输入(形参)？  输出(返回值)？
### → 确认简单正确的语法结构
### → 确认形参的输入并打印出来确认正确 *这个代码叫 脚手架代码(scaffolding)*
### → 返回结果
## 6.3 组合
### 在一个函数中可以调用其他函数
	def circle_area(xc, yc, xp, yp):
		redius = distance(xc, yc, xp, yp)
		result = area(redius)
		return result

	"""简化"""
	def circle_area(xc, yc, xp, yp)：
		return area(distance(xc, yc, xp, yp))
## 6.4 布尔函数
	def is_divisible(x, y):
		if x % y == 0:
			return True
		else:
			return False

	"""简化"""
	def is_divisible(x, y):
		return x % y == 0
	
	if is_divisble(x ,y): # is_divisible(x, y) == True 不必要
		print 'x is divisble by y'
## 6.5 再谈递归
### 画栈图，从递归最里层开始向外推
## 6.6 坚持信念
### 假设调用的函数是正确的
## 6.7 另一个示例
	def fibonacci(n):
		if n == 0:
			return 0
		elif n == 1:
			return 1
		else:
			retuen fibonacci(n-1) + fibonacci(n-2)
## 6.8 检查类型
### 检查实参类型	
	if not isinstance(x, int): # isinstance函数，检查实参类型
		print '... is only defined for integers'
	elif n < 0:
		print '.... is not for negative integers'
	elif n == 0:
		return 1
	else:
		return n * factorial(n-1)
### 上述被称作守卫代码(guardian code)，用作防止输入错误(前置条件)
## 6.9 调试
### 函数不能正常工作：
#### ① 函数获得的实参有问题，每个前置条件没达到；
#### ② 函数本身有问题，某个后置条件没达到；
#### ③ 函数返回值有问题，或者使用的方式不正确
### 脚手架代码：
#### 对①：加print，显示实参值于类型，若没错，下一项
#### 对③：在每个return前加print，显示返回值(手动检查返回值)，若没错，下一项
#### 对③：检查*调用它的代码*，确保返回值正确使用，若没错，下一项
#### 在函数开端和结尾加print语句,如下：
	def factorial(n):
		space = ' ' * (4 * n)
		print space, 'factorial', n # 查看运行之前 n 的值
		if n == 0:
			print space, 'returning 1'
			return 1
		else:
			recurse = factorial(n-1)
			result = n * recurse
			print space, 'returning', result # 查看运行后 result 的值
			return result
## 6.10 术语表
## 6.11 练习
### 6-1
	"""比较x,y大小，返回1,0,-1"""
	def compare(x,y):
	    if x>y:
    	    return 1
    	elif x==y:
    	    return 0
    	elif x<y:
    	    return -1

	print(compare(2,1))
### 6-2
	"""求直角三角形斜边"""
	import math

	def hypotenuse(a,b):
	    squared=a**2+b**2
	    result=math.sqrt(squared)
	    return result
	    
	print(hypotenuse(3,4))
### 6-3
	"""比较x,y,z大小，x<=y<=z为真"""
	def is_between(x,y,z):
	    return x<=y<=z

	print(is_between(1,2,3))
### 6-5
	"""设计Ackermann函数"""

	def ack(m,n):
    	if m==0:
    	    return n+1
	    elif m>0 and n==0:
	        return ack(m-1,1)
	    elif m>0 and n>0:
	        return ack(m-1,ack(m,n-1))
	
	def input_ack():
	    input_m=float(input('please input m\n'))
	    input_n=float(input('please input n\n'))
	    result=ack(input_m,input_n)
	    print('ack(',input_m,input_n,'):',result)

	input_ack()
### 6-6
	"""用递归检查字符串是否是回文"""
	def first(word):
	    return word[0]

	def last(word):
    	return word[-1]
	
	def middle(word):
	    return word[1:-1]
	
	def input_palindrome():
	    input_word=str(input('please input word:\n'))    
	    print (middle(input_word))
	
	def is_palindrome(word):
	    """Returns True if word is a palindrome."""
	    if len(word) <= 1:
        return True
	    if first(word) != last(word):
	        return False
	    return is_palindrome(middle(word))
	           
	
	def input_is_palindrome():
	    input_word=str(input('please input word:\n'))    
	    print (is_palindrome(input_word))
        
	input_is_palindrome()
### 6-7
	"""判断a是否是b的乘方"""
	def is_power(a,b):
	    if a==1 and b!=0:
    	    return True       
    	elif b==1 or b==0 or a%b!=0:
    	    return False
    	elif a%b==0:        
    	    return is_power(a/b,b)

	print(is_power(-64,-4))
### 6-8
	"""求a和b的最大公约数"""
	def gcd(a,b):
	    if b==0:
	        return a
	    elif b!=0:
	        r=a%b
	        return gcd(b,r)
	
	def input_gcd():
	    input_a=float(input('input a:\n'))
	    input_b=float(input('input b:\n'))
	    print('GCD: ',gcd(input_a,input_b))

	input_gcd()
# 第7章 迭代(iteration)
## 7.1 多重赋值(multiple assignment)
### 谨慎使用，降低可读性
	>>>a = 5
	>>>b = a
	>>>a = 3
## 7.2 更新变量(update)
	>>>x = 0 #初始化(initialization)
	>>>x = x + 1 
## 7.3 while语句
### while condition(计算，True:执行loop，False:执行后续语句)
## 7.4 break语句
### if ...
### break : 跳出循环
## 7.5 平方根
### 练习 7-2
	import math

	def square_root(a,s): 
	    x=s
	    while True:
	        y=(x+a/x)/2
	        if abs(y-x)<0.0000001:
	            break
	        x=y        
	    return x
    
	def input_square_root():
	    while True:
	        input_a=float(input('input nubmer:'))
	        input_s=float(input('input estimated value:'))        
	        input_line=str(input('OK?(Y/N)\n'))
	        if input_line=='Y':
	            break
	        elif input_line=='N':
	            input_square_root()
	    print(square_root(input_a,input_s))
                  

	def test_square_root():
	    while True:
	        s_test=3.0
	        a_test=float(input('>'))
	        if a_test<0:
	            break  
	        result_test=square_root(a_test,s_test)
	        compared_test=math.sqrt(a_test)
	        dif=abs(result_test-compared_test)
	        print(a_test,result_test,compared_test,dif)
## 7.6 算法
### ***算法***是程序设计的核心
### 牛顿方法是算法的一个例子
## 7.7 调试
### ***二分调试***(debugging by bisection)
### 利用程序的中点调试
## 7.8 术语表
# 第8章 字符串
## 8.1 字符串是一个字符的序列(sequence)
	>>>fruit = 'banana'
	>>>letter = fruit[1] #下标(index)，离字符串开头的偏移量，必须是整数
## 8.2 len
	>>>fruit[-1] 返回最后一个字母
	>>>length = len(fruit)
	>>>fruit[length - 1]
## 8.3 使用for循环进行遍历(traversal)
## 8.4 字符串切片(slice)
## 8.5 字符串是不可变的(immutable)
## 8.6 搜索
### 遍历一个序列，当找到目标时返回
## 8.7 循环和计数
	word = 'banana'
	count = 0
	for letter in word:
		if letter == 'a':
			count += 1
	print count
## 8.8 字符串方法
### ① find (搜索)
	>>>'with a meo-moo here'.find('moo')
	2
	>>>title = 'with a meo-moo here' 
	>>>title.find('Monty')
	0 #若没有:返回‘-1’
### ② join (合并)
	>>>seq = ['1', '2', '3', '4', '5']
	>>>sep = '+'
	>>>sep.join(seq)
	'1+2+3+4+5'
	>>>dirs = '', 'user', 'bin', 'env'
	>>>print ('C:'+ '\\'.join(dirs))
	C:\user\bin\env
### ③ lower(返回字符串的小写字母版)
	>>>name = 'Gumby'
	>>>names = ['gumby', 'smith', 'jones']
	>>>if name.lower() in names: print 'Found it!'
### ④ replace(多个字符查找替换)
	>>>'This is a test'.replace('is', 'eez')
	Theez eez a test
### ⑤ split(拆分)
	>>> '1+2+3+4+5'.split('+')
	['1', '2', '3', '4', '5']
### ⑥ strip(去除两侧空格或指定字符)
	>>>'dictory.txt'.readline().strip()
	
	>>>line.strip('*j')
### ⑦ translate(查找替换单个字符)
	>>>from string import maketrans
	>>>table = maketrans('cs', 'kz')
	>>>translate(table)
	'thiz iz an inkredible tezt'
	>>>translate(table, 'l') #用table中的单个字符去替换，可选删除'l'
## 8.9 操作符in(布尔操作符)
## 8.10 字符串比较
### 大写字母在小写字母之前(大写<小写)，其余按照字母排序
## 8.11 调试
## 8.12 术语表
## 8.13 练习
### 练习 8-1 
	def cba():
    	line=str(input('input word:'))
	    x=0    
	    for i in range(1,len(line)+1):
	        x=x+1
	        y=int(len(line)-x)
	        print(line[y])

	cba()
### 练习 8-2
	def abc():
	    prefixes='JKLMNOPQ'
	    suffix='ack'
    
	    for letter in prefixes:
	        if letter=='O' or letter=='Q':
	            print(letter+'u'+suffix)
	        print(letter+suffix)


	abc()
### 练习 8-3
	def fruit():
    	fruit='banana'
    	print(fruit[:])

	fruit()
### 练习 8-4
	def find(word,letter,index):
    	while index<len(word):
        	if word[index]==letter:
        		return index
    	    index=index+1
    	return -1
### 练习 8-5
	def count():
	    word=str(input('input word:\n'))
    	count_letter=str(input('input letter\n'))
	    count=0
	    for letter in word:
	        if letter==count_letter:
	            count=count+1
	    print(count)

	count()
### 练习 8-6
	def count():	
	    word=str(input('input word:'))
    	count_letter=str(input('input letter:'))
	    index=int(input('start index:'))
	    count1=0
	    while index<len(word):
	        if word[index]==count_letter:
	            count1=count1+1
	        index=index+1
	    print(count1)

	count()
### 练习 8-7
	def count():
	    line=str(input('input word:'))
    	letter=str(input('input letter:'))
    	number=line.count(letter)
    	print(number)

	count()
### 练习 8-10
	def is_palindrome():
	    line=str(input('input word:'))
    	print(line[::-1])

	is_palindrome()
### 练习 8-11
	def any_lowercasel(s):
    	for c in s:
        	if not c.islower():
        	    return False
    	return True

	print(any_lowercasel('AADDDASS'))

	print(any_lowercasel('aaaaaA'))
### 练习 8-12
	def rotate_word(letter,numcode):
	    if letter.islower():
    	    start_order=ord('a')
	    elif letter.isupper():
	        start_order=ord('A')     
	    else:
	        return letter
	    mid_order=ord(letter)-start_order
	    order=(mid_order+numcode)%26+start_order
	    order_letter=chr(order)
	    return order_letter

	def print_rotate_word():
	    word=str(input('input word:'))
	    input_numcode=int(input('input numcode:'))
	    res=''
	    for letter in word:
	        res+=rotate_word(letter,input_numcode)
	    print (res)

	if __name__=='__main__':
	    print_rotate_word()
# 第9章 案例分析：文字游戏
## 9.1 读取单词列表
	>>>fin = open('words.txt')
	>>>print (fin)
	<open file 'words.txt', mode 'r' at 0xb7f4b380> #'w':写入
	>>>fin.readline() #从文件里读入字符，直到获得换行符为止
	'aa\r\n' #\r:回车符号;\n:换行符
	>>>fin.readline() #再次调用readline(),文件会继续向下读入
	'aah\r\n'
	>>>line = fin.readline()
	>>>word = line.strip() #可以使用strip()去掉\r\n
	>>>print (word)
	aah
	# 循环
	fin = open('words.txt')
	for line in fin:
		word = line.strip()
		print (words)
### 练习 9-1
	fin=open('words.txt')
	for line in fin:
    	word=line.strip()
	    if len(word)>20:
	        print(word)
## 9.2 练习
### 练习 9-2
	def has_no_e(word):
	    for letter in word:
    	    if letter=='e':
    	        return False
	    return True
        
	def print_words():
	    fin=open('words.txt')
	    n=0
	    for line in fin:
	        word=line.strip()
	        if has_no_e(word)==True:
	            n=n+1
	            print(word)
	    print(n)

	print_words()
## 9.3 搜索
### 问题识别(problem recognition),像计算机科学家一样思考
### 想想以前有没有造过能用的轮子
## 9.4 使用下标循环
### 'for';'while';递归
## 9.5 调试
### 注意空字符串也有可能引起bug
## 9.6 术语表
## 9.7 练习
### 练习 9-3
	def avoids(word,a):
	    for a_letter in a:
	        if a_letter in word:
		        return False
	    return True 
    
	def has_no_e(word):
	    for letter in word:
	        if letter=='e':
    	        return False
	    return True
        
	def print_words():
	    fin=open('words.txt')
	    a=str(input('avoid letter:'))
	    n=0
	    for line in fin:
	        word=line.strip()
	        if avoids(word,a)==True:
	            n=n+1
	            print(word)
	    print(n)

	print_words()
### 练习 9-4
	def use_only(word,b):
	    x=0
	    for word_letter in word:
	        if word_letter in b:
	            x=x+1
	    if x==len(word):
	        return True
	    return False

	def avoids(word,a):
	    for a_letter in a:
	        if a_letter in word:
	            return False
	    return True 
    
	def has_no_e(word):
	    for letter in word:
	        if letter=='e':
	            return False
	    return True
        
	def print_words():
	    fin=open('words.txt')
	    a=str(input('use only letters:'))
	    n=0
	    for line in fin:
	        word=line.strip()
	        if use_only(word,a)==True:
	            n=n+1
	            print(word)
	    print(n)

	print_words()
### 练习 9-5
	def uses_all(word,c):
	    x=0
	    for c_letter in c:
	        if c_letter in word:
	            x=x+1
	        if x==len(c):
	            return True
	    return False
            
	def uses_only(word,b):
	    x=0
	    for word_letter in word:
	        if word_letter in b:
	            x=x+1
	    if x==len(word):
	        return True
	    return False

	def avoids(word,a):
	    for a_letter in a:
	        if a_letter in word:
	            return False
	    return True 
    
	def has_no_e(word):
	    for letter in word:
	        if letter=='e':
	            return False
	    return True
        
	def print_words():
	    fin=open('words.txt')
	    a=str(input('uses all letters:'))
	    n=0
	    for line in fin:
	        word=line.strip()
	        if uses_all(word,a)==True:
	            n=n+1
	            print(word)
	    print(n)

	print_words()
### 练习 9-6
	def is_abecedarian(word):
	    order=ord('a')
	    for word_letter in word:
	        if ord(word_letter)>=order:
	            order=ord(word_letter)
	        else:
	            return False
	    return True    
    
	def uses_all(word,c):
	    x=0
	    for c_letter in c:
	        if c_letter in word:
	            x=x+1
	        if x==len(c):
	            return True
	    return False
            
	def uses_only(word,b):
	    x=0
	    for word_letter in word:
	        if word_letter in b:
	            x=x+1
	    if x==len(word):
	        return True
	    return False

	def avoids(word,a):
	    for a_letter in word:
	        if a_letter in a:
	            return False
	    return True 
    
	def has_no_e(word):
	    for letter in word:
	        if letter=='e':
	            return False
	    return True
        
	def print_words():
	    fin=open('words.txt')
	    n=0
	    for line in fin:
	        word=line.strip()
	        if is_abecedarian(word)==True:
	            n=n+1
	            print(word)
	    print(n)
    
	print_words()
### 练习 9-7
	def found_thr(word):
	    if len(word)>=6:
	        for i in range(0,len(word)-5):
	            if word[i]==word[i+1] and word[i+2]==word[i+3] and word[i+4]==word[i+5]:
	                return True
	    return False
            

	def is_abecedarian(word):
	    order=ord('a')
	    for word_letter in word:
	        if ord(word_letter)>=order:
	            order=ord(word_letter)
	        else:
	            return False
	    return True    
    
	def uses_all(word,c):
	    x=0
	    for c_letter in c:
	        if c_letter in word:
	            x=x+1
	        if x==len(c):
	            return True
	    return False
            
	def uses_only(word,b):
	    x=0
	    for word_letter in word:
	        if word_letter in b:
	            x=x+1
	    if x==len(word):
	        return True
	    return False

	def avoids(word,a):
	    for a_letter in word:
	        if a_letter in a:
	            return False
	    return True 
    
	def has_no_e(word):
	    for letter in word:
	        if letter=='e':
	            return False
	    return True
        
	def print_words():
	    fin=open('words.txt')
	    n=0
	    for line in fin:
	        word=line.strip()
	        if found_thr(word)==True:
	            n=n+1
	            print(word)
	    print(n)
    
	print_words()
### 练习 9-8
	def first(word):
	    return word[0]

	def last(word):
	    return word[-1]

	def middle(word):
	    return word[1:-1]

	def is_palindrome(word):
	    """Returns True if word is a palindrome."""
	    if len(word) <= 1:
	        return True
	    if first(word) != last(word):
	        return False
	    return is_palindrome(middle(word))

	def judge(num,y,z):
	    s=str(num)[y:z]
	    return is_palindrome(s)

	def huiwen():
	    num=100000
	    while num<=999996:
	        if (judge(num,2,6) 
	           and judge(num+1,1,6) 
	           and judge(num+2,1,5)
	           and judge(num+3,0,6))==True:
	            print(num)
	        num=num+1

	def judge2(num,y,z):
	    num_str='0'*(6-len(str(num)))+str(num)
	    s2=num_str[y:z]
	    return is_palindrome(s2)

	def huiwen2():
	    num=000000
	    while num<=999999:
	        if (judge2(num,2,6) 
	           and judge2(num+1,1,6) 
	           and judge2(num+2,1,5)
	           and judge2(num+3,0,6))==True:
	            print(str(num))
	        num=num+1


	huiwen()
	huiwen2()
### 练习 9-9
	def abba(num1,num2):
	    s1=str(num1).zfill(2)
	    s2=str(num2).zfill(2)
	    if s1[:]==s2[::-1]:
	        return True

	def count_years_old(add,m):
	    num1=0       
	    num2=add
	    n=0 
	    while num1<84 and num2<100:
	        if abba(num1,num2)==True:
	            n=n+1
	            if n==m:
	                print('num1:',num1,'num2:',num2)
	        num1=num1+1
	        num2=num1+add

	def check_years_old(add):
	    num1=0       
	    num2=add
	    n=0 
	    while num1<84 and num2<100:
	        if abba(num1,num2)==True:
	            n=n+1
	            if n==8:
	                return True
	        num1=num1+1
	        num2=num1+add

	def print_years_old(m):
	    add=15
	    for i in range(40):
	        if check_years_old(add)==True:
	            count_years_old(add,m)
	        add=add+1

	print_years_old(6)            
# 第10章 列表
## 10.1 列表是一个序列
## 10.2 列表是可变的
### ① 任何整型的表达式都可以用作下标
### ② 如果尝试读写一个并不存在的元素会 IndexError
### ③ 如果下标是负数，则从结尾处反过来数下标访问
## 10.3 遍历一个列表
### 注：嵌套列表仍被看做一个单独的元素，长度算1
## 10.4 列表操作
	>>>a = [1, 2, 3]
	>>>b = [4, 5, 6]
	>>>c = a + b
	>>>c
	[1, 2, 3, 4, 5, 6]
	>>>a * 2
	[1, 2, 3, 1, 2, 3]
## 10.5 列表切片
	>>>t[:] #列表副本，因为列表可变，创建副本十分有用
	>>>t[1:3] = ['x', 'y'] #更新多个元素
## 10.6 列表方法
### 列表的方法除了pop()，全都没有返回值！
### ① t.append() # 创造，不改变 相比之下'+'是新建列表
### ② t.extend() # 改变，不创造
### ③ t.sort(key, reverse) # 默认从低到高排列，或按照特性key(e.g. len)
### ④ t.count() # 无返回值！
### ⑤ t.index() # 下标
### ⑥ t.insert(3, 'four') # 在下标3后插入'four'
### ⑦ t.pop() # 移除下标后元素，默认最后一个，并返回该值
### ⑧ t.remove() # 移除某值的第一个匹配项, 还有del后接切片下标
### ⑨ t.reverse() # 反向存放
## 10.7 映射(map)、过滤(filter)和化简(reduce)
## 10.8 删除元素
## 10.9 列表和字符串
### 列表:值的序列；字符串:字符的序列
### ① 避免使用list作变量名
### ② 避免使用l，因为看起来像1
### 1. list:把字符串拆成单个字母的列表
### 2. split:把句子拆成单词
### 3. join:把列表合并为字符串
## 10.10 对象和值
	>>>a = 'banana'
	>>>b = 'banana'
	>>>a is b
	True
	>>>a = [1, 2, 3]
	>>>b = [1, 2, 3]
	>>>a is b
	False
## 10.11 别名
	>>>a = [1, 2, 3]
	>>>b = a #b是a的别名(aliase)
	>>>b is a
	True
	>>>b[0] = 17
	>>>a
	[17, 2, 3]
### 避免使用别名！
## 10.12 列表参数
	>>>t1 = [1, 2]
	>>>t2 = t1.append(3)
	>>>t1
	[1, 2, 3]
	>>>t2
	None
	>>>t3 = t1 + [4]
	>>>t3
	[1, 2, 3, 4]
## 10.13 调试
### 1.大部分列表方法:①修改参数；②返回None
### 2.有很多种方法达到目的，选择一种风格并坚持不变
### 3.通过赋值来避免别名
	>>>orig = t[:]
	t.sort()
## 10.14 术语表
## 10.15 练习
### 10-1
	def nested_sum(a):
	    s=0
	    for item in a:
	        s=s+sum(item)
	    print(s)

	nested_sum([[1,2],[3,4],[5,-6,-6]])
### 10-2
	def capitalize_all(t):
	    res=[]
	    for s in t:
	        res.append(s.capitalize())
	    return res

	def capitalize_nested(m):
	    M=[]
	    for item in m:
	        M.append(capitalize_all(item))
	    print(M)

	capitalize_nested([['a','b'],['c','d'],['e','f']])
### 10-3
	def accum(a):
	    s=0
	    add=[]
	    for i in range(len(a)):
	        s=sum(a[:i+1])
	        add.append(s)
	    print(add)

	accum([1,2,3,4,5,6,7])
### 10-4
	def middle(a):
	    del a[0]
	    del a[-1]
	    b=a
	    return b

	print(middle([1,2,3,4]))
### 10-5
	def chop(a):
	    del a[0]
	    del a[-1]

	print(chop([1,2,3,4]))
### 10-6
	def is_sorted(a):
	    for i in range(len(a)-1):
	        if a[i]>a[i+1]:
	            return False
	    return True

	print(is_sorted(['a','b','b']))
### 10-7
	def is_anagram(a,b):
		a_t=list(a)
	    b_t=list(b)
	    a_t.sort()
	    b_t.sort()
	    a_t_str=''.join(a_t)
	    b_t_str=''.join(b_t)
	    if a_t_str==b_t_str:
	        return True
	    return False

	print(is_anagram('and','dan'))
### 10-8
	import random

	def has_duplicates(a):
	    for i in a:
	        num=a.count(i)
	        if num>1:
	            return True
	    return False
	def p(b):
	    b_t=[]
	    for i in range(b):
	        b_num=random.randint(1,365)
	        b_t.append(b_num)
	    return has_duplicates(b_t)

	def p_f(c):
	    b=int(input('input people num:'))
	    sum_p=0
	    for i in range(c):
	        if p(b)==True:
	            sum_p+=1
	    print(sum_p)
	    print(sum_p/c*100)

	p_f(100000)
### 10-9
	def remove_dupicates(a):
	    t=a[:]    
	    t.sort()
	    for i in t:
	        num=t.count(i)
	        if num>1:
	            t.remove(i) 
	    return t
    
	print(remove_dupicates([1,2,3,4,0,0,1]))
### 10-10
	import time

	def read_word1():
	    t1=[]
	    time1=time.time()
	    fin=open('words.txt')
	    for line in fin:
	        word=line.strip()
	        t1.append(word)
	    time2=time.time()
	    div1=time2-time1
	    print(len(t1))
	    print(t1[:10])
	    print('div1:',div1)

	def read_word2():
	    t2=[]
	    time3=time.time()
	    fin=open('words.txt')
	    for line in fin:
	        word=line.strip()
	        t2+=[word]
	    time4=time.time()
	    div2=time4-time3
	    print(len(t2))
	    print(t2[:10])
	    print('div2:',div2)
    


	read_word1()
	read_word2()
### 10-11
	import time

	def bisect(a,t):
	    t_half1=t[:len(t)//2]
	    t_half2=t[len(t)//2:]    
	    if a in t_half1:
	        return True    
	    elif len(t)//2>0:
	        bisect(a,t_half2)
    


	def sect(a,t):
	    for i in range(len(t)):
	       if a==t[i]:
	           return i

	def words_list():
	    fin=open('words.txt')
	    t=[]
	    for line in fin:
	        word=line.strip()
	        t.append(word)
	    return t

	time_s=time.time()
	result=bisect('zoo',words_list())
	time_e=time.time()-time_s
	print(result)
	print(time_e)

	time_s=time.time()
	result=sect('zoo',words_list())
	time_e=time.time()-time_s
	print(result)
	print(time_e)
### 10-12
	def word_list():
	    fin=open('words.txt')
	    word_list=[]
	    for line in fin:
	        word=line.strip()
	        word_list.append(word)
	    return word_list

	def find_reverse(t):
	    a=t[:]
	    n=0
	    for line in a:
	        l_list=list(line)
	        l_list.reverse()
	        n_line=''.join(l_list)
	        if line!=n_line and n_line in a:
	            print(line,n_line)
	            a.remove(n_line)
	            n+=1
	    print(n)

	find_reverse(word_list())
### 10-13
## 10-* 二分法
### 前提：假设已经排好序
	import bisect
	bisect.bisect_left(a, x) #在a中查找x，x存在时返回x左下标；不存在返回应插入位置左下标
	bisect.bisect_right(a, x) #在a中查找x，x存在时返回x右下标；不存在返回应插入位置右下标
	bisect.insort_left(a, x) #将x插入列表a，x存在时插入x左侧位置；
	bisect.insort_right(a, x) #将x插入列表a，x存在时插入x右侧位置；
# 第11章 字典
### 字典的下标：键 → 值 构成键值对
	>>>vals = eng2sp.values() #vals是由字典eng2p里值构成的列表
### 打印字典的顺序无法预料
### 字典是散列表(hashtable)
### 不论多少项，in操作符的花费时间都差不多
## 11.1 使用字典作为计数器集合
	"""直方图"""
	def histogram(s):
		d = dict()
		for c in s:
			if c not in d:
				d[c] = 1
			if c in d:
				d[c] += 1
		return d
## 11.2 循环和字典
### for循环遍历字典的键：键的出现没有特定顺序
## 11.3 反向查找
	def reverse_lookup(d, v):
		for k in d:
			if d[k] == v:
				return k
		raise ValueError
## 11.4 字典和列表
### 字典的键必须是可散列的(hashable)
### 列表只能作为值
## 11.5 备忘
### 记录已经计算过的值，保存在一个字典中 → 备忘(memo)
## 11.6 全局变量
### (global.varible)
### __main__ 特殊帧 中的变量：全局变量 常用作标志(flags)，一种布尔变量
### 如果需要重新赋值：
	def examples():
		global been_called
		been_called = True
## 11.7 长整数
### 123456789123123***L*** py2<type：long> py3<type:int>
## 11.8 调试
### ① 缩小输入：出现错误，缩小样本
### ② 检查概要信息和类型：print 一些概要信息
### ③ 编写自检逻辑，例如：求平均数（比较与最大最小值大小，看看是否有悖逻辑）
### ④ 美化输出(pprint)
### 脚手架代码！！！！
## 11.9 术语表
## 11.10 练习
### 11-1
	import time

	def bisect(a,t):
	    t_half1=t[:len(t)//2]
	    t_half2=t[len(t)//2:]    
	    if a in t_half1:
	        return True    
	    elif len(t)//2>0:
	        bisect(a,t_half2)
    
	def sect(a,t):
	    for i in range(len(t)):
	       if a==t[i]:
	           return i

	def words_list():
	    fin=open('words.txt')
	    t=[]
	    for line in fin:
	        word=line.strip()
	        t.append(word)
	    return t
    
	def words_read(a):
	    t1={}
	    n=0
	    fin=open('words.txt')
	    for line in fin:
	        n+=1
	        word=line.strip()
	        t1[word]=n
	    return a in t1

    
	time_s=time.time()
	result=bisect('and',words_list())
	time_e=time.time()-time_s
	print(result)
	print(time_e)

	time_s=time.time()
	result=sect('and',words_list())
	time_e=time.time()-time_s
	print(result)
	print(time_e)

	time1=time.time()
	result=words_read('and')
	time2=time.time()
	div=time2-time1
	print(result)
	print(div)
### 11-2
	def histogram(s):
	    d=dict()
	    for c in s:
	        d[c]=d.get(c,0)+1
	    return d

	print(histogram('brontosaurus'))
### 11-3
	def histogram(s):
	    d=dict()
	    for c in s:
	        d[c]=d.get(c,0)+1
	    return d

	def print_hist(h):
	    h_sort=sorted(h.keys())
	    print(h_sort)
	    for c in h_sort:
	        print (c,h[c])

	h=histogram('brontosaurus')
	print_hist(h)
### 11-4
	def histogram(s):
	    d=dict()
	    for c in s:
	        d[c]=d.get(c,0)+1
	    return d

	def print_hist(h):
	    h_sort=sorted(h.keys())
	    print(h_sort)
	    for c in h_sort:
	        print (c,h[c])


	def reverse_lookup(d,v):
	    fin=[]
	    for k in d:
	        if d[k]==v:
	            fin.append(k)
	    return fin


	h=histogram('brontosauruss')
	print(reverse_lookup(h,3))
### 11-5
	def histogram(s):
	    d=dict()
	    for c in s:
	        d[c]=d.get(c,0)+1
	    return d

	def print_hist(h):
	    h_sort=sorted(h.keys())
	    print(h_sort)
	    for c in h_sort:
	        print (c,h[c])


	def reverse_lookup(d,v):
	    fin=[]
	    for k in d:
	        if d[k]==v:
	            fin.append(k)
	    return fin


	def invert_dict(d):
	    inverse=dict()
	    for key in d:
	        inverse.setdefault(d[key],[]).append(key)
	    return inverse
        
	h=histogram('parrot')
	print(invert_dict(h))
### 11-6
	import time

	def fibonacci(n):
	    if n==0:
	        return 0
	    elif n==1:
	        return 1
	    else:
	        return fibonacci(n-1)+fibonacci(n-2)

	known={0:0,1:1}

	def fibonacci2(n):
	    if n in known:
	        return known[n]
	    res=fibonacci2(n-1)+fibonacci2(n-2)
	    known[n]=res
	    return res

	time1=time.time()
	fibonacci(50)
	print(time.time()-time1)
	print(fibonacci(50))

	time2=time.time()
	fibonacci2(50)
	print(time.time()-time2)
	print(fibonacci2(50))
### 11-7
	import time

	def factorial(n):
	    if n==0:
	        return 1
	    else:
	        recurse=factorial(n-1)
	        result=n*recurse
	        return result

	known={0:1}

	def factorial2(n):
	    if n in known:
	        return known[n]
	    res=n*factorial2(n-1)
	    known[n]=res
	    return res

	time1=time.time()
	factorial(100)
	print(time.time()-time1)
	print(factorial(100))    

	time2=time.time()
	factorial2(100)
	print(time.time()-time2)
	print(factorial2(100)) 
### 11-8
	import random
	import math

	"""制作一个质数表"""
	def zhishu(m,n):                                            
	    list_num = [n]    
	    for i in range(m, n):        
	        for num in range(2, int(math.sqrt(n))+1):            
	            if i % num == 0 and i != num:                
	                break            
	            elif i % num != 0 and num == int(math.sqrt(n)):                
	                list_num.append(i)    
	    return list_num
                
	"""最大公约数，欧几里德算法"""
	def gcd(a,b):
	    if b==0:
	        return a
	    return gcd(b,a%b)

	"""最大公约数、x、y，欧几里得扩展算法，求乘法逆元"""
	def egcd(a,b):
	    if b==0:
	        return (1,0,a)
	    (x,y,r)=egcd(b,a%b)
	    tmp=x
	    x=y
	    y=tmp-(a//b)*y
	    return (x,y,r)

	"""取e"""
	def ef(x):
	    e_list=[]
	    for e in range(x):
	        if gcd(e,x)==1:
	            e_list.append(e)
	    return e_list
    
	"""随机取质数取p、q，得到N，根据egcd求出乘法逆元d"""
	def miyao():
	    p=random.choice(zhishu(100,999))
	    q=random.choice(zhishu(100,999))
	    N=p*q
	    F_N=(p-1)*(q-1)
	    e=random.choice(ef(F_N))
	    d=egcd(e,F_N)[0]
	    if d<0:
	        d=(d%F_N+F_N)%F_N   
	    return (d,e,N)    

	"""加密明文a，得到密文b"""
	def jiami(): 
	    tulpe_miyao=miyao()
	    d=tulpe_miyao[0]
	    e=tulpe_miyao[1]   
	    N=tulpe_miyao[2]    
	    print('公开加密秘钥：',e)
	    print('公开模数：',N)
	    print('请记住你的秘钥：',d)
	    a=int(input('请输入需要加密的信息(小于100000)：'))
	    b=(a**e)%N
	    print('加密信息：',b)

	"""解密密文b，得到明文a"""
	def jiemi():
	    N=int(input('请输入公开模数：'))
	    b=int(input('请输入需要解密的信息：'))
	    d=int(input('请输入你的秘钥：'))
	    a=(b**d)%N
	    print('这段密文的意思是：',a)

	jiemi()
### 11-9
	def histogram(s):
	    d=dict()
	    for c in s:
	        d[c]=d.get(c,0)+1
	    return d

	def xhas_duplicateds(list_t):
	    t_d=histogram(list_t)
	    for t in t_d:
	        if t_d[t]>1:
	            return True
	    return False
        
    
	print(xhas_duplicateds(['a','b','c','e','d']))  
### 11-10
	from bisect import bisect_left

	def word_dict():
	    d={}
	    fin=open('words.txt')
	    for line in fin:
	        word=line.strip()
	        d[word]=word
	    return d

	def word_list():
	    d_list=[]
	    fin=open('words.txt')
	    for line in fin:
	        word=line.strip()
	        d_list.append(word)
	    return d_list

	def in_bisect(d_list, word):
	    """Checks whether a word is in a list using bisection search.
	
	    Precondition: the words in the list are sorted
	
	    d_list: list of strings
	    word: string
	    """
	    i = bisect_left(d_list, word)
	    if i != len(d_list) and d_list[i] == word:
	        return True
	    else:
	        return False
        
	def rotate_word(letter,numcode):
	    if letter.islower():
	        start_order=ord('a')
	    elif letter.isupper():
	        start_order=ord('A')     
	    else:
	        return letter
	    mid_order=ord(letter)-start_order
	    order=(mid_order+numcode)%26+start_order
	    order_letter=chr(order)
	    return order_letter

	def list_rotate_word(word,numcode):
	    res=''
	    for letter in word:
	        res+=rotate_word(letter,numcode)
	    return res

	def rotate_pairs():
	    d=word_dict()
	    d_list=word_list()
	    for word in d:
	        for i in range(1,14):
	            rotated=list_rotate_word(word,i)
	            if in_bisect(d_list,rotated):       
	                print(word,i,rotated)

	rotate_pairs()
### 11-11
	from pronounce import read_dictionary

	from bisect import bisect_left

	def word_list():
	    d_list=[]
	    fin=open('words.txt')
	    for line in fin:
	        word=line.strip().lower()
	        d_list.append(word)
	    return d_list

	def in_bisect(d_list, word):
	    """Checks whether a word is in a list using bisection search.

	    Precondition: the words in the list are sorted

	    d_list: list of strings
	    word: string
	    """
	    i = bisect_left(d_list, word)
	    if i != len(d_list) and d_list[i] == word:
	        return True
	    else:
	        return False

	def homophones(a, b, phonetic):
	    """Checks if words two can be pronounced the same way.
	
	    If either word is not in the pronouncing dictionary, return False
	
	    a, b: strings
	    phonetic: map from words to pronunciation codes
	    """
	    if a not in phonetic or b not in phonetic:
	        return False

	    return phonetic[a] == phonetic[b]

	def p_words(word,d_list,phonetic):
 
	    word1=word[1:]
	    if in_bisect(d_list,word1)==False:
	        return False
	    if not homophones(word, word1, phonetic):
	        return False
        
	    word2=word[0]+word[2:]
	    if in_bisect(d_list,word2)==False:
	        return False
	    if not homophones(word, word2, phonetic):
	        return False
        
	    return True

	if __name__=='__main__':
	    d_list=word_list()
	    phonetic = read_dictionary()  
    
	    for word in d_list:                
	        if p_words(word,d_list,phonetic):
	            print (word,word[1:],word[0]+word[2:])    
# 第14章 文件
## 14.1 持久化
## 14.2 读和写
	>>>fout = open('output.txt','w') 
	# 若存在，则清除旧数据重新开始写入，谨慎！！！
	# 若不存在，则新建一个
	>>>print fout
	<open file 'output.txt', mode 'w' at 0xb7eb2410>
	
	>>>line1 = "This here's the wattle,\n"
	>>>four.write(line1) 
	# write方法把数据写入文件中，如果再次调用write，会在结尾处添加新数据
    >>>fout.close()
    #写入完毕时需要关闭文件
## 14.3 格式操作符
### write参数必须是字符串(str)，若要输入其他类型值，先转换为字符串
	>>>x = 52
	>>>f.write(str(x))
### 另一个方法是使用*格式操作符*%
	"""%：用于整数是求余操作符；用于字符串是格式操作符"""

	>>>camels = 42
	>>>'%d' % camels 
	# 第一个操作对象(前者)是 格式字符串，包括一个或多个 格式序列
    # 第二个操作对象被第一个指定如何格式化，其结果是一个字符串
	'42'
    
	>>>camels = 42
	>>>'I have spotted %d camels.' % camels
	# 格式序列可以出现在字符串的任意地方
	'I have spotted 42 camels'

	>>>'In %d years I have spotted %g %s.' % (3, 0.1, 'camels')
	# 如果字符串中有多于一个格式序列， 第二个操作对象必须是元组，按顺序对应每个元素
	# '%d':格式化整数;'%g':格式化浮点数;'%s':格式化字符串
	'In 3 years I have spotted 0.1 camels.'

	>>>'%d %d %d' % (1, 2)
	TypeError:not enough arguments for format string
	>>>'%d' % 'dollar'
	TypeError:illegal argument type for built-in operation
## 14.4 文件名和路径
### 当你打开一个文件用于读取时，默认在当前目录查找
### os模块(operating system)提供用于操作文件和目录的函数
	>>>import os
	>>>cwd = os.getcwd()
	# os.getcwd返回当前目录名称,cwd:current working directory
	>>>print cwd
	/home/dinsdale # 这里是名为dinsdale的用户的主目录
### 类似于cwd这样的定位文件的字符串被称为一个*路径*(path)
### *相对路径*从当前目录开始，至今为止我们看到的路径都是简单的文件名，所以它们都是相对于当前目录的。
### *绝对路径*从文件系统的顶层目录开始
	>>>os.path.abspath('memo.txt')
	# os.path.abspath 可用于寻找文件的绝对路径
	'/home/dinsdale/memo.txt'
    
    >>>os.path.exists('memo.txt')
    # os.path.exists 检查一个文件或目录是否存在
    True

	>>>os.path.isdir('memo.txt')
	# os.path.isdir 检查它是否为目录，如果它存在的话
    False
	>>>os.path.isdir('music')
	True
    
    >>>os.path.isfile('memo.txt')
    # os.path.isfile 检查它是否为文件
	True

	>>>os.listdir(cwd)
	# os.listdir 返回指定目录中文件（以及其他目录）的列表
	['music', 'photos', 'memo.txt']

    def walk(dirname):
		for name in os.listdir(dirname):
			path = os.path.join(dirname, name)
			# os.path.join 接受一个目录和一个文件名称，并拼接为一个完整的路径

			if os.path.isfile(path)
				print path
			else:
				walk(path)
### 练习14-1
	"""练习使用os.walk"""
	import os

	def print_path (path):
	    for root, dirs, files in os.walk(path):
	# os.walk (top, topdown=True, onerror=None, followlinks=False)
	# os.walk 必须接受一个根目录(top)，从根目录开始遍历目录

	        for filename in files:
	            print (root, dirs, files)
				# os.walk 返回一个元组:
			    # root(str):目录的路径
				# dirs(list):目录中的非文件项列表
				# files(list):目录中的文件项列表

	            print (os.path.join(root,filename))
				# root与filename组合起来就是全路径
	            
	print_path ('C:\\Users\\Mrxcy\\Documents\\Python Scripts')
	print_path ('.') # '.'表示当前目录

## 14.5 捕获异常
	>>>fin = open('bad_file')
	IOError: [Errno 2] No such file or directory: 'bad file'
	# 尝试打开一个不存在的文件

	>>>fourt = open('/etc/passwd, 'w')
	IOError: [Errno 13] Permission denied: '/etc/passwd'
	# 访问一个没有访问权限的文件

	>>>fin = open('/home')
	IOError: [Errno 21] Is a directory
	# 尝试打开一个目录用作文件读取

### 要避免这些错误可以使用os.path.exists和os.path.isfile等函数
### 检查可能需要花费大量时间和代码，最好去尝试，在发生的时候解决
### try语句：
	try:
		fin = open('bad_file')
		for line in fin:
			print line
		fin.close()
	except:
		print 'Something went wrong'
	# Py先从try语句开始，如果正确跳过except，发生异常则跳出try，执行except
### 使用try处理异常称为*捕获*一个异常
### 练习 14-2
	"""取出文件filename1中的字符串写入filename2中，
	并且在遇到s_str时用r_str替换，在遇到异常时捕获异常"""
	def sed(s_str, r_str, filename1, filename2):
    	try:
    	    fin1 = open(filename1, 'r')
    	    fin2 = open(filename2, 'w')
    	    for line in fin1:
    	        word = line.strip()
    	        if word == s_str:
    	            fin2.write(r_str + '\n')
    	        fin2.write(word + '\n')
        
		fin1.close()
        fin2.close()
   		#注意别忘了关闭文件！
    	except:
    	    print ('There are errors')

	sed('and', 'or', 'words.txt', 'no_and_words.txt')
	for word2 in open('no_and_words.txt'):
    	print(word2)

## 14.6 数据库
### *数据库*是一个有组织的用于存储数据的文件
### 跟字典不同的地方是数据库是保存在磁盘上的，程序结束时持续存在
	>>>import anydbm
	# 模块anydbm 提供了接口用于创建和更新数据库文件
	>>>db = anydbm.open('caption.db', 'c')
	# 模式'c'意味着如果不存在，数据库会被创建
	>>>db['cleese.png'] = 'Photo of John Cleese.'
	# 调用的结果是一个数据库对象，可以当做字典来用
	>>>print db['cleese.png']
	Photo of John Cleese.
	# 访问数据库中的一项时，anydbm会读取文件
	>>>db['cleese.png'] = 'Photo of John Cleese doing a silly walk.'
	>>>print db['cleese.png']
	Photo of John Cleese doing a silly walk.
	# 对一个已经存在的值赋值，anydbm会替换旧值
	for key in db:
		print key
	# 很多字典方法，比如keys和items对数据库适用，包括for循环
	>>>db.close()
	# 操作结束时需要关闭数据库

## 14.7 封存
### anydbm的限制之一是键和值必须是字符串
### 可以使用*pickle*模块，其可以将几乎所有类型的对象转换成适合保存到数据库的字符串模式，并可以将字符串还原为对象。
	>>>import pickle
	>>>t = [1, 2, 3]
	>>>pickle.dumps(t)
	'(lp0\nI1\naI2\naI3\na.'
	# pickle.dumps 接受一个对象作为参数，并返回它的字符串表达式
	
	>>>t1 = [1, 2, 3]
	>>>s = pickle.dumps(t1)
	>>>t2 = pickle.loads(s)
	>>>print t2
	[1, 2, 3]
	# pickle.loads 接受字符串，重新构造对象
	
	>>>t1 == t2
	True
	>>>t1 is t2
	False
	# 封存再解封后，新旧对象的值相同，但是不是同一个对象，相当于复制了对象
### 因为太常用，Py已经将这两个封装成了一个模块*shelve*
### 练习 14-3
	from anagram_sets import *

	import shelve
	import sys

	def store_anagrams(filename, ad):
	    """input filename of word txt, return a db for anagrams"""
	    shelf = shelve.open(filename, 'c')
    
	    for word, word_list in ad.items():
	        shelf[word] = word_list
	    
	    shelf.close()
	
	def read_anagrams(filename, word):
	    shelf = shelve.open(filename)
	    sig = signature(word)
	 
	    try:
	        return shelf[sig]
	    except KeyError:
	        return []
	
	def main(name, command ='store'):
	    if command == 'store': 
	        ad = all_anagrams('words.txt')
	        store_anagrams(name, ad)
	    else:
	        print (read_anagrams(name, command))
	    
	if __name__ == '__main__':
	    main('anagram1.db', 'and')

## 14.8 管道(pipe)
### 大部分操作系统提供了命令行接口，也称为*字符界面(shell)*
### 任何在字符界面能启动的程序都可以在Python中通过一个管道(pipe)来启动。管道代表一个正在运行的程序的对象。
	>>>cmd = 'ls -l' # Unix命令'ls -l'，展示当前目录的内容
	>>>fp = os.popen(cmd) 
	#返回值是一个和打开的文件差不多的对象,可以使用readline来逐行阅读，
	>>>res = fp.read()
	#也可以使用read一次读取所有的输出
	>>>stat = fp.close()
	>>>print stat
	None # None代表它正常结束了（没有错误）

	>>>filename = 'book.tex'
	>>>cmd = 'md5sum' + filename
	# md5sum 是Unix系统提供的读取文件内容并计算一个“校验和”(checksum)
	# 这个命令提供了一个高效的方法，用来对比两个文件是否包含相同的内容
	# 不同内容生成相同校验和的几率极低
	>>>fp = os.popen(cmd)
	>>>res = fp.read()
	>>>stat = fp.close()
	>>>print res
	................. book.tex
	>>>print stat
	None 
### 练习 14-4
	>>>没做，一定要做！
## 14.9 编写模块
	if __name__ == '__main__':
		# __name__是一个内置变量，程序启动时会被设置。
		#如果程序作为脚本执行，__name__的值是__main__；此时，测试代码会被执行。
		#否则，如果程序作为模块被导入，则测试代码就被跳过了
		print linecount('wc.py')
### 当一个模块被导入的时候，Python什么都不会做，即使模块被修改，它也不会重新读取文件。
### 可以使用内置函数reload()，但是它也可能会出别的问题，最好的办法是关掉解释器，重启。
### 练习 14-5
	def linecount(filename):
    	count = 0
    	for line in open(filename):
        	count += 1
    	return count

	if __name__ == '__main__':    
		# 也就是说，若是还需要将这个代码当模块使用的话，要写上面这一句
		# 不然模块里面的代码在最后执行的时候也会被执行  
		# 当其被当做模块执行时，__name__的值是它自己的名字，比如这里wc
	    print (linecount('wc.py'))
## 14.10 调试
### 当读取和写入文件的时候很可能遇到一些看不见的空白字符
### 可以使用内置函数repr()
	>>>s = '1 2\t 3\n 4'
	>>>print s
	1 2  3 
     4
	>>>print repr(s)
	'1 2\t 3\n 4'
### 另外有的系统使用一个换行符\n，另外的系统使用一个回车符\r。也有两种一起使用的系统。如果在不同系统之间移动文件可能导致问题。
### 大多数系统都有程序可以将一种格式转换成另一种，当然，也可以用repr()等自己写一个。
## 14.11 术语表
## 14.12 练习
### 练习 14-6
	"""建立名为zipcoder的主模块用来存储及查询网上抓取的信息"""
	import shelve

	from zipcode_scrip import *
	from num_str import *

	def store(s_code, f_code, zipcoder):
    """将得到的列表中的信息存入一个数据库zipcoder中
	    zip_list: list
	    zipcoder: db"""
    
	    shelf = shelve.open(zipcoder, 'c')
    	for i in range(s_code, f_code+1):
        	zip_list = scrip(i)
        	zipcode = num_str(i, 5) 
        	if  zip_list == []:
        	    shelf[zipcode] = ()
        	else:
        	    name = zip_list[0] 
        	    population = zip_list[1]  
        	    shelf[zipcode] = (name, population)
        	print (zipcode, shelf[zipcode])
	    
	    shelf.close()
        
	def search(zipcode, zipcoder):
	    """利用数据库zipcoder，检索zipcode的地方信息
	    zipcode: string
	    zipcoder: db"""  
	    
	    shelf = shelve.open(zipcoder, 'r')    

	    return shelf[zipcode]
	
	if __name__ == '__main__':
	    
	    store(2915, 3000, 'zipcoder.db')
	    
	    print(search('02492', 'zipcoder.db'))
	
	"""建立名为zipcode_scrip子模块，用来从网站上抓取需要的信息"""
	import urllib.request
	from num_str import * #运用了num_str子模块
	
	def scrip(code):
    	"""从网站上抽取code的zipcode，及与之对应的地方name，population，
	    存入列表zipcode_group中
	    s_code:int
	    f_code:int
	    zipcode_group: list"""
	    zipcode_group = [] # 初始化zipname为空字典，用于存储zipcode与population
	    try:     
	        UID = num_str(code, 5)
	        website = 'http://www.uszip.com/zip/' + UID
	        conn = urllib.request.urlopen(website)
	        n = 0
           
	        for line in conn:
	                
	            if b'<title>' in line:
	                name = line.strip().decode()
	                # 得到关于name的字符串
	                    
	                name = name.strip('zip cod </title>')
	                # 去掉开头结尾的不需要的字符
                        
	            elif b'Total population' in line:
                    
	                n = 1
                    
	                p_raw = line.strip().decode() 
	                # 得到关于population的长字符串
	                    
	                p_list = p_raw.split('Total population</dt><dd>')
	                # 以'Total population</dt><dd>'为界，所需要的人口数字就在其后                
                    
	                p_list2 = p_list[1].split('<')
	                # 取出所需人口数字所在的字符串，以'<span'为界断开其与尾部
                    
	                population = p_list2[0]
	                # 得到最终人口数字就在列表第一个元素
	                    
	            if n == 0:
                	zipcode_group = []
            	else:
                	zipcode_group = [name, population]
       
	        return zipcode_group
	       
	    except:
	        print ('There are errors')
             
	
	if __name__ == '__main__':
	    print (scrip(0))

	"""num_str子模块可以将数字在需要的高位上加0，然后返回其字符串"""
	def num_str (num, x):
    """补齐数字num高位上的零，以满足位数x要求, 并返回满足位数要求的字符串
    	num: int
    	x: int
    	num_str: str"""

    	num_str='0'*(x-len(str(num)))+str(num)
    
    	return num_str
# 第15章 类和对象
## 15.1 用户定义类型
### 用户定义的类型称为*类(class)*
	class Point(object): # 表示新的类是一个Point，它是object的一种，object是一个内置类型。
		"""Represents a point in 2-D space.""" # 解释这个类的用途
	>>>print Point
	<class '__main__.Point'> # 因为Point是在程序顶层定义的，它的全名是__main__.Point
### 类对对象像一个创建对象的工厂
	>>>blamk = Point()
	>>>print blank #返回值是到一个Point对象的引用，我们将它赋值给变量blank
	<__main__.Point instance at 0xb7e9d3ac>
### 新建一个对象的过程称为*实例化(instantiation)*，而对象是这个类的一个*实例*
## 15.2 属性
### 可以用句点表示法来给实例赋值：
	>>>blank.x = 3.0
	>>>blank.y = 4.0
### 在这个情况下，我们将值赋给了一个对象的有命名的元素。这些元素称为*属性(attribute)*
### *对象图(object diagram)*
			Point
	blank → |x → 3.0|
			|y → 4.0|
### 变量blank引用向一个Point对象，它包含两个属性。每个属性引用一个浮点数。
	>>>x = blank.x # 我们将其赋值给一个变量x，变量x与属性x并不冲突！
	>>>print x
	3.0
### blank.x表示找到blank引用的对象，并取得它的x属性的值
	>>>print '(%g, %g)' % (blank.x, blank.y)
	(3.0, 4.0)
	>>>distance = math.sqrt(blank.x**2 + blank.y**2)
	>>>print distance
	5.0

	def print_point(p)
		print '(%g, %g)' % (p.x, p.y)
	>>>print_point(blank)
	(3.0, 4.0)
### 练习15-1
	import math

	class Point(object):
	    """Represent a 2-D point"""

	def distance_between_points(a, b):
	    
	    distance = math.sqrt((a.x - b.x)**2 + (a.y - b.y)**2)
	
	    return distance
	
	a = Point()
	b = Point()
	
	a.x = 0
	a.y = 0
	b.x = 1
	b.y = 1

	print(distance_between_points(a, b))
## 15.3 矩形
### ① 可以指定一个矩形的一个角落（或者中心点）、宽度以及高度；
### ② 可以指定两个相对的角落
	class Rectangle(object):
		"""Represent a rectangle.
		attributes: width, height, coner.
		"""
	
	box = Rectangle()
	box.width = 100.0
	box.height = 200.0
	box.corner = Point() # 作为另一个对象的属性，存在的对象是内嵌的
	box.corner.x = 0.0
	box.corner.y = 0.0
## 15.4 作为返回值的实例
### 返回Rectangle的中心点坐标：
	def find_center(rect):
		p = Point()
		p.x =rect.corner.x + rect.width/2.0
		p.y =rect.corner.y + rect.width/2.0
		return p
	
	>>>center = find_center(box)
	>>>print_point(center)
	(50.0, 100.0)
## 15.5 对象是可变的
	box.width = box.width + 50
	box.height = box.width + 100

	def grow_rectangle(rect, dwidth, dheight):
		rect.width += dwidth
		rect.height += dheight
	>>>print box.width
	100.0
	>>>print box.height
	200.0
	>>>grow_rectangle(box, 50, 100)
	>>>print box.width
	150.0
	>>>print box.height
	300.0
### 在函数中，rect是box的别名，所以如果函数修改了rect，则box也改变。
### 练习15-2
	import math

	class Point(object):
    	"""Represent a 2-D point"""

	def distance_between_points(a, b):
    	
	    distance = math.sqrt((a.x - b.x)**2 + (a.y - b.y)**2)
	
	    return distance
		
	a = Point()
	b = Point()

	a.x = 0
	a.y = 0
	b.x = 1
	b.y = 1
	
	class Rectangle(object):
			"""Represent a rectangle.
			attributes: width, height, coner.
				"""
	box = Rectangle()
	box.width = 100.0
	box.height = 200.0
	box.corner = Point() # 作为另一个对象的属性，存在的对象是内嵌的
	box.corner.x = 0.0
	box.corner.y = 0.0
	
	def move_rectangle(rect, dx, dy):
	    rect.corner.x = dx
	    rect.corner.y = dy
	    return rect.corner
	
	def print_point(p):
	    print ('(%g, %g)' % (p.x, p.y))
	
	print_point(move_rectangle(box, 10.0, 10.0))
## 15.6 复制
### 别名的使用有时候会让程序更难阅读，一个修改其他地方也都要变。
#### 使用别名的常用替代方案是复制对象。
	>>>p1 = Point()
	>>>p1.x = 3.0
	>>>p1.y = 4.0
	>>>import copy
	>>>p2 = copy.copy(p1)
### p1和p2包含有相同的数据，但是它们不是同一个Point对象。
	>>>print_point(p1)
	(3.0, 4.0)
	>>>print_point(p2)
	(3.0, 4.0)
	>>>p1 is p2
	False
	>>>p1 == p2
	False
#### 在实例中==与is是相同的，检查对象的同一性，这种行为可以改变
### 如果使用copy.copy复制一个Rectangle，只复制Rectangle对象，但并不复制内嵌的Point对象
	>>>box2 = copy.copy(box)
	>>>box2 is box
	False
	>>>box2.corner is box.corner
	True
### 这种行为被称为*浅复制(shallow copy)*，复制对象和其包含的任何引用，但不复制内嵌对象
	box → | width → 100.0|                      |100.0  ← width | ← box2
		  |height → 200.0|	    |x → 0.0|       |200.0  ← height|
		  |corner           →   |y → 0.0|   ←             corner|
#### 对象图(object diagram)
### *深复制(deep copy)*
	>>>box3 = copy.deepcopy(box)
	>>>box3 is box
	False
	>>>box3.corner is box.corner
	False
#### box3与box是两个完全分开的对象
### 练习 15-3
 	import math
	import copy

	class Point(object):
    	"""Represent a 2-D point"""

	def distance_between_points(a, b):
    
	    distance = math.sqrt((a.x - b.x)**2 + (a.y - b.y)**2)
	
	    return distance
	
	a = Point()
	b = Point()
	
	a.x = 0
	a.y = 0
	b.x = 1
	b.y = 1
	
	class Rectangle(object):
			"""Represent a rectangle.
			attributes: width, height, coner.
			"""
	box = Rectangle()
	box.width = 100.0
	box.height = 200.0
	box.corner = Point() # 作为另一个对象的属性，存在的对象是内嵌的
	box.corner.x = 0.0
	box.corner.y = 0.0
	
	def move_rectangle(rect, dx, dy):
	    rect2 = copy.deepcopy(rect)
	    rect2.corner.x = dx
	    rect2.corner.y = dy
	    return rect2
	
	def print_point(p):
	    print ('(%g, %g)' % (p.x, p.y))
	
	box2 = move_rectangle(box, 10.0, 12.0)
	print_point(box2.corner)
	print(box.corner == box2.corner)
## 15.7 调试
### 试图访问一个并不存在的属性，会得到*AttributeError*:
### 如果不清楚一个对象是什么类型：
	>>>type(p)
	<type '__mian_.Point'>
### 如果你不确定一个对象是否拥有某个特点的属性，可以用内置函数hasattr:
	>>>hasattr(p, 'x')
	True
	>>>hasattr(p, 'z')
	False
#### 第一个形参可以是任何对象；第二个形参是一个*字符串*，包含属性的名称。
## 15.8 术语表
## 15.9 练习
### 练习 15-4
	 
# 第16章 类和函数
## 16.1 时间
	class Time(object):
		"""Represents the time of day.
		attributes: hour, minute, second
		"""
	time = Time()
	time.hour = 11
	time.minute = 59
	time.second = 30
### 练习 16-1
	class Time(object):
		"""Represents the time of day.
		attributes: hour, minute, second
		"""
	time = Time()
	time.hour = 11
	time.minute = 59
	time.second = 0
	
	def print_time(t):
	    print('%.2d: %.2d: %.2d' % (t.hour, t.minute, t.second))
	
	print_time(time)
### 练习 16-2
	class Time(object):
		"""Represents the time of day.
		attributes: hour, minute, second
		"""
	time = Time()
	time.hour = 11
	time.minute = 59
	time.second = 0

	def print_time(t):
	    print('%.2d: %.2d: %.2d' % (t.hour, t.minute, t.second))
	
	def is_after(t1, t2):
	    """接收两个时间变量t1、t2，
	    如果t1在t2时间之后返回True，
	    否则返回False
	    """
		    sum_t1 = 3600 * t1.hour + 60 * t1.minute + t1.second 
	    sum_t2 = 3600 * t2.hour + 60 * t2.minute + t2.second 
	    return (sum_t1 > sum_t2)
		
	time1 = Time()
	time1.hour = 13
	time1.minute = 45
	time1.second = 12
	
	time2 = Time()
	time2.hour = 13
	time2.minute = 53
	time2.second = 33

	print(is_after(time1, time2))
## 16.2 纯函数
### 纯函数和修改器，根据这个得到开发计划，原型和补丁(prototype and patch)
	def add_time(t1, t2):
		sum = Time()
		sum.hour = t1.hour + t2.hour
		sum.minute = t1.minute + t2.minute
		sum.second = t2.second + t2.second
		return sum
### 纯函数：除了返回一个值之外，并不修改作为实参传入的任何对象，也没有任何如显示值或用户输入之类的副作用
	def add_time(t1, t2):
		sum = Time()
		sum.hour = t1.hour + t2.hour
		sum.minute = t1.minute + t2.minute
		sum.second = t2.second + t2.second

		if sum.second >= 60:
			sum.second -= 60
			sum.minute += 1

		if sum.minute >= 60:
			sum.minute -= 60
			sum.hour += 1

		return sum
### 虽然有了进位功能，但是函数已经变得臃肿起来了
## 16.3 修改器
### 有时候函数修改*传入的参数对象*很有用，这种情况下，修改对调用者是可见的，这样工作的函数称为*修改器(modifier)*
	def increment(time, seconds):
		time.second += seconds
		
		if time.second >= 60:
			time.second -= 60
			time.minute += 1

		if time.minute >= 60:
			time.minute -= 60
			time.hour += 1
### 如果seconds比60大很多上述函数无法正常工作
### 练习 16-3
	def increment(time, seconds):   
    	num1 = seconds // 60
    	time.second += seconds % 60
    	time.minute += num1
    	# print (num1, time.hour, time.minute, time.second)
     
	    if time.second >= 60:
    	    time.second -= 60
    	    time.minute += 1
    	     
    	num2 = time.minute // 60     
	    time.minute = time.minute % 60
	    time.hour += num2
	    # print (num2, time.hour, time.minute, time.second)
    
	    if time.minute >= 60:
	        time.minute -= 60
	        time.hour +=1
     
	    time.hour = time.hour % 24
    
	    if time.hour < 24 and time.minute < 60 and time.second < 60:    
	        return time
	    else:
	        print (time.hour, time.minute, time.second, '\nThere something wrong!')
     
	print_time(increment(time, 360000))

### 只要合理的时候，尽量编写纯函数，*函数式编程风格*
### 练习 16-4
	def increment(time, seconds):   
	    i_time = Time()
    
    	num1 = seconds // 60
	    i_time.second = time.second + seconds % 60
	    i_time.minute = time.minute + num1
    	# print (num1, time.hour, time.minute, time.second)
     
	    if i_time.second >= 60:
	        i_time.second -= 60
	        i_time.minute += 1
	         
	    num2 = i_time.minute // 60     
	    i_time.minute = i_time.minute % 60
	    i_time.hour = time.hour + num2
	    # print (num2, time.hour, time.minute, time.second)
	    
	    if i_time.minute >= 60:
	        i_time.minute -= 60
	        i_time.hour +=1
		     
	    i_time.hour = i_time.hour % 24
		    
	    if i_time.hour < 24 and i_time.minute < 60 and i_time.second < 60:    
	        return i_time
	    else:
	        print (i_time.hour, i_time.minute, i_time.second, '\nThere something wrong!')
	     
	print_time(increment(time, 360000))
## 16.4 原型和计划
### 刚才展示的开发计划称为“原型和补丁”
#### 对每个函数，编写一个可以进行基本计算的原型，测试它发现错误并打补丁
#### 在不熟悉问题时很有效，但增量地修正可能会导致代码过度复杂
### 另一种方法：*有规划开发*
### 练习 16-5
	def time_to_int(time):
	    minutes = time.hour * 60 +time.minute
	    seconds = minutes * 60 +time.second
	    return seconds

	def int_to_time(seconds):
	    time = Time()
	    minutes, time.second = divmod(seconds, 60)
	    time.hour, time.minute = divmod(minutes, 60)
	    return time
	    
	def increment(time, seconds):   
	    i_time = Time()
	    i_seconds = time_to_int(time) + seconds
	    i_time = int_to_time(i_seconds)
		    
	    if i_time.hour < 24 and i_time.minute < 60 and i_time.second < 60:    
	        return i_time
	    else:
	        print (i_time.hour, i_time.minute, i_time.second, '\nThere something wrong!')
	     
	print_time(increment(time_t, 3600))
#### 这个程序并不能处理超过一天的时间，因为超过一天之后就不再只是60进制数了
### 有时候把一个问题弄得更难（更通用），反而会让它更简单（因为特殊情况更少，以及更少的出错机会）
## 16.5 调试
### 当minute和second的值在0到60（不包含）之间以及hour为正时，是合法的。允许second拥有小数值，这种需求称为*不变式*，因为它们应当总是为真，不为真时必定有地方出错。
### 可以编写一种检查错误的函数
	def valid_time(time):
		if time.hour < 0 or time.minute < 0 or time.second < 0:
			return False
		if time.minute >= 60 or time.second >= 60:
			return False
		return True
### 可以放在每个函数的开头检查参数
	def add_time(t1, t2)：
		if not valid(t1) or not valid_time(t2):
			raise ValueError, 'invaild Time object in add_time'
		seconds = time_to_int(t1) + time_to_int(t2)
		return int_to_time(seconds)
### 或者使用*assert语句*，它会检查一个给定的不变式，当检查失败时抛出异常：
	def add_time(t1, t2)：
		assert valid(t1) and valid_time(t2)
		seconds = time_to_int(t1) + time_to_int(t2)
		return int_to_time(seconds)
### assert语句区分处理了普通条件的代码和检查错误的代码
## 16.6 术语表
## 16.7 练习
# 第17章 类和方法
## 17.1 面向对象特性
### 面向对象编程
#### 1. 程序由对象定义和函数定义组成，大部分计算都是用对象操作来表达
#### 2. 每个对象定义对应真实世界的某些对象或概念，并且操作那个对象的函数对应真实世界中对象之间的交互方式
### 每个函数都至少接受一个对象作为参数，这是*方法*的由来；
### 一个方法，即和某个特定类相关联的函数
### 方法和函数在语义上是一样的，但是在语法上有区别：
#### 1. 方法定义写在类定义之中，更明确的表示类和方法的关联
#### 2. 调用方法和调用函数的语法形式不同
## 17.2 打印对象
	class Time(object):
		def print_time(self): # 方法的第一个形参用self是惯例
			print '%.2d:%.2d:%.2d' % (self.hour, self.minute, self.second)
### 这种惯例的原因是一个隐喻：
#### 1. 函数调用的语法，print_time(start)，暗示函数是活动主体
#### 2. 面向对象编程中，对象是活动主体，start.print_time()
### 练习 17-1
	class Time(object):
    	def time_to_int(self):
       		minutes = 60 * self.hour + self.minute
       		seconds = 60 * minutes + self.second
       		return seconds
## 17.3 另一个示例
	def int_to_time(seconds):
    	time = Time()
	    minutes, time.second = divmod(seconds, 60)
	    time.hour, time.minute = divmod(minutes, 60)
	    return time
    
	class Time(object):
	    def print_time(self):
	        print ('%.2d:%.2d:%.2d' % (self.hour, self.minute, self.second))
	        
	    def time_to_int(self):
	        minutes = 60 * self.hour + self.minute
	        seconds = 60 * minutes + self.second
	     	return seconds
	       
	    def increment(self, seconds):
	        seconds += self.time_to_int()
	        return int_to_time(seconds)
## 17.4 一个更加复杂的示例
	def int_to_time(seconds):
	    time = Time()
	    minutes, time.second = divmod(seconds, 60)
	    time.hour, time.minute = divmod(minutes, 60)
	    return time
	    
	class Time(object):
	    def print_time(self):
	        print ('%.2d:%.2d:%.2d' % (self.hour, self.minute, self.second))
	        
	    def time_to_int(self):
	        minutes = 60 * self.hour + self.minute
	        seconds = 60 * minutes + self.second
        return seconds
       
    	def increment(self, seconds):
	        seconds += self.time_to_int()
	        return int_to_time(seconds)
	    
	    def is_after(self, other):
	        return self.time_to_int() > other.time_to_int()

	>>> end.is_after(start)
	True # 读起来像英语一样
## 17.5 __init__方法 (特殊方法1)
### 练习 17-2
	class Point(object):
	    def __init__(self, x=0, y=0):
    	    self.x = x
	        self.y = y

	point = Point(1, 2)
## 17.6 __str__方法 (特殊方法2)
### 练习 17-3
	class Point(object):
	    def __init__(self, x=0, y=0):
    	    self.x = x
	        self.y = y
	    
	    def __str__(self):
	        return '%d, %d' % (self.x, self.y)
        
	point = Point(1, 2)
	print (point)
### 编写新类时，可以先写__init__，再写__str__，以便调试
## 17.7 操作符重载
### 练习 17-4
	class Point(object):
	    def __init__(self, x=0, y=0):
	        self.x = x
	        self.y = y
	    
	    def __str__(self):
	        return '%d, %d' % (self.x, self.y)
	    
	    def __add__(self, other):
	        point_add = Point()
	        point_add.x = self.x + other.x
	        point_add.y = self.y + other.y
	        return point_add
        
        
	point1 = Point(1, 2)
	point2 = Point(2, 3)
	print (point1 + point2)
## 17.8 基于类型的分发
### 练习 17-5
	class Point(object):
	    def __init__(self, x=0, y=0):
    	    self.x = x
    	    self.y = y
    	
    	def __str__(self):
    	    return '%d, %d' % (self.x, self.y)
    	
    	def __add__(self, other):
    	    point_add = Point()
    	    if isinstance(other, Point):
    	        point_add.x = self.x + other.x
    	        point_add.y = self.y + other.y
    	        return point_add
    	    else:
    	        point_add.x = self.x + other[0]
    	        point_add.y = self.y + other[1]
    	        return point_add
               
	point1 = Point(1, 2)
	point2 = Point(2, 3)

	print (point1 + (2, 3))
	print (point1 + point2)
## 17.9 多态
### 可以处理多个类型的函数称为*多态(polymorphic)*
### 如果函数内部的所有操作都支持某种类型，那么这个函数就可以用作某种类型
### 多态可以促进代码复用
	# sum 对所有其元素支持加法的序列都适用
	>>> t1 = Time(7, 43)
	>>> t2 = Time(7, 41)
	>>> t3 = Time(7, 37)
	>>> total = sum([t1, t2, t3]) # 由于时间对象提供了add方法，则可以使用sum
	>>> print total
	23:01:00
## 17.10 调试
### 在__init__中初始化对象的全部属性是个好习惯
### 如果并不清楚一个对象是否拥有某属性，可以使用*hasattr*
### 另一种访问对象的属性方法是通过特别属性*__dict__*，将属性名称(str形式)映射到属性值：
	>>> p = Point(2, 3)
	>>> print p.__dict__
	{'y': 3, 'x': 2}
	
	def print_attributes(obj):
		"""接受一个对象obj,返回其拥有的属性，以及属性的值"""
		for attr in obj.__dict__:
			print attr, getattr(obj, attr) # getattr接受一个对象和属性名称(str形式),并返回属性的值
### 为了调试方便print_attibutes()会很好用
## 17.11 接口和实现
### 面向对象设计的目标之一就是提高软件的可维护性
### 练习 17-6
## 17.12 术语表
## 17.13 练习
# 第18章 继承
## 18.1 卡片对象
	class Card(object):
    	"""Represents a standard playing card."""
    
    	def __init__(self, suit=0, rank=2):
        	self.suit = suit
        	self.rank = rank
## 18.2 类属性
### suit_names、rank_names被称为*类属性*，suit、name被称为*实例属性*
	    suit_names = ['Clubs', 'Diamonds', 'Hearts', 'Spades']
    	rank_names = [None, 'Ace', '2', '3', '4', '5', '6', '7',
        	          '8', '9', '10', 'Jack', 'Queen', 'King']    
    
    	def __str__(self):
    	    return '%s of %s' % (Card.rank_names[self.rank], 
    	                         Card.suit_names[self.suit])
## 18.3 对比卡牌
    	def __cmp__(self, other):
        	t1 = self.suit, self.rank
        	t2 = other.suit, other.rank
	        return cmp(t1, t2)
### 练习 18-1
	class Time(object):

    	def __init__(self, hour=0, minute=0, second=0):
	        self.hour = hour
    	    self.minute = minute
	        self.second = second

	    def __str__(self):
	        return '%.2d:%.2d:%.2d' % (self.hour, self.minute, self.second)

	    def __cmp__(self, other):
	        t1 = self.hour, self.minute, self.second
	        t2 = other.hour, other.minute, other.second
	        return cmp(t1, t2)

	time1 = Time(1, 2, 3)
	time2 = Time(2, 3, 4)
	print time1 < time2
## 18.4 牌组
	class Card(object):
	    """Represents a standard playing card."""
    
	    def __init__(self, suit=0, rank=2):
	        self.suit = suit
	        self.rank = rank
	
	    suit_names = ['Clubs', 'Diamonds', 'Hearts', 'Spades']
	    rank_names = [None, 'Ace', '2', '3', '4', '5', '6', '7',
	                  '8', '9', '10', 'Jack', 'Queen', 'King']    
    
	    def __str__(self):
	        return '%s of %s' % (Card.rank_names[self.rank], 
	                             Card.suit_names[self.suit])
    
	    def __cmp__(self, other):
	        t1 = self.suit, self.rank
	        t2 = other.suit, other.rank
	        return cmp(t1, t2)
	
	class Deck(object):
	
	    def __init__(self):
	        self.cards = []
	        for suit in range(4):
	            for rank in range(1, 14):
	                card = Card(suit, rank)
	                self.cards.append(card)
## 18.5 打印牌组                
	    def __str__(self):
	        res = []
	        for card in self.cards:
	            res.append(str(card))
	        return '\n'.join(res)

	deck = Deck()
	print deck
# 18.6 添加、删除、洗牌和排序
	class Deck(object):

    	def __init__(self):
    	    self.cards = []
    		for suit in range(4):
    	        for rank in range(1, 14):
    	   	        card = Card(suit, rank)
        	        self.cards.append(card)
                
    	def __str__(self):
	        res = []
	        for card in self.cards:
	            res.append(str(card))
	        return '\n'.join(res)
	
	    def pop_card(self):
	        return self.cards.pop()
	
	    def add_card(self, card):
	        self.cards.append(card) # 调用另一个函数却不做其他工作，称为饰面(veneer)
	
	    def shuffle(self):
	        random.shuffle(self.cards)
# 18.7 继承
	class Deck(object):

    	def __init__(self):
        	self.cards = []
        	for suit in range(4):
        	    for rank in range(1, 14):
        	        card = Card(suit, rank)
        	        self.cards.append(card)
                
    	def __str__(self):
	        res = []
	        for card in self.cards:
	            res.append(str(card))
	        return '\n'.join(res)
	
	    def pop_card(self):
	        return self.cards.pop()
	
	    def add_card(self,card):
	        return self.cards.append(card)
	
	    def move_cards(self, hand, num):
	        for i in range(num):
	            hand.add_card(self.pop_card())
		
		def deal_cards(self, hands_num, num):
     	    for i in range(hands_num):
         	   handname = 'hand' + str(i + 1)
         	   hand = Hand(handname)
         	   self.move_cards(hand, num)
            

        return hand

	class Hand(Deck):
	    """Represents a hand of playing cards."""
	    def __init__(self, label=''):
	        self.cards = []
	        self.label = label

	hand = Hand('new hand')
	
	deck = Deck()
	card = deck.pop_card()
	hand.add_card(card)
	
	deck.deal_cards 
	print hand
## 18.8 类图
### 1. 一个类的对象可能包含对其他类的对象的引用；*HAS-A*(有一个)
### 2. 一个类可能继承自另一个类；*IS-A*(是一个)
### 3. 一个类可能依赖于另一个类。
	# 空心三角箭头  IS-A
	# 标准箭头     HAS-A
	# （*）     关联重数标记（数字，范围，*）
## 18.9 调试
	def find_defining_class(obj, meth_name):
		for ty in type(obj).mro(): # MRO: method resolution order
			if meth_name in ty.__dict__:
				return ty
	>>> hand = Hand()
	>>> print find_defining_class(hand, 'shuffle')
	<class 'Card.Deck'>
### 每当你重载一个方法的时候，新方法的接口应当和旧方法一致。
### 1. 接收同样的参数
### 2. 返回相同的类型
### 3. 服从同样的前置条件与后置条件
## 18.10 数据封装
### 1. 从编写函数、（如果需要的话）读写全局变量开始
### 2. 一旦你的程序能够正确运行，查看全局变量与使用它们的函数的关联
### 3. 将相关的变量封装成为对象的属性
### 4. 将相关的函数转换为这个新类的方法
## 18.11 术语表
## 18.12 练习
# 第19章 案例研究：Tkinter
## 19.1 GUI
	from Gui import *

	g = Gui()
	g.title('Gui')
	g.mainloop()

	button = g.bu(text = 'Press me.')
### 按钮(button)：控制
### 画布(canvas)：图形
### 输入框(entry)：输入
### 滚动条(scrollbar)：显示
### 画面框(frame)：本体(载基)
## 19.2 按钮和回调
	
	from Gui import *

	g = Gui()
	g.title('Gui')


	button = g.bu(text = 'Press me.')

	label = g.la(text = 'Press the button')

	def make_label():
	    g.la(text = 'Thank you!')
	
	# command后的选项被称为回调，典型的事件驱动编程
	button2 = g.bu(text = 'No, press me!', command = make_label)

	g.mainloop()
### 练习 19-1
	from Gui import *

	g = Gui()
	g.title('Gui')

	def make_button():
	    g.bu(text = 'Press me, too!', command = make_label)
    
	def make_label():
	    g.la(text = 'Well done!')
	
	button = g.bu(text = 'Press me.', command = make_button)

	g.mainloop()
## 19.3 画布部件
### 练习 19-2
	from Gui import *

	g = Gui()
	g.title('Gui')

	def make_button():
	    g.bu(text = 'Press me, too!', command = make_label)
	    
	def make_label():
	    g.la(text = 'Well done!')
	
	button = g.bu(text = 'Press me.', command = make_button)
	
	g.mainloop()
## 19.4 坐标序列
	# 对角定点的方式称为边界盒
	convas.rectangle([0, 0], [200, 100],
					fill = 'blue', outline = 'orange', width = 10)
	convas.oval([0, 0], [200, 100],
				fill = 'blue', outline = 'orange', width = 10)	
	convas.line([0, 0], [100, 200], [200, 100]
				, width = 10)
	convas.polygon([0, 0], [100, 200], [200, 100]
					fill = 'blue', outline = 'orange', width = 10)
## 19.5 更多部件
