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