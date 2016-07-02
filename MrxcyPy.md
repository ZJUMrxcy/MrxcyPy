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
