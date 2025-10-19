# 2.1 变量 Varible
可以通过加入变量的方式，对程序进行输出
```python
#eg 2.1
message="Hello World"
print(message)
```
其中，message为变量
## 2.1.1 变量命名使用规则
- 变量名只能包含字母、数字以及下划线，但不能以数字打头
- 变量名不能包含空格
- 不得将python关键字以及函数名用作变量名
- 慎用小写字母$l$与大写字母$O$，易被看作1和0
## 2.1.2 避免变量命名错误
$$善用Traceback$$
## 2.1.3 变量是标签
变量是可被赋值的标签，指向特定量
# 2.2 字符串 String
字符串就是一系列字符，python中用引号引起的都是字符串，可以是单引号也可以是双引号
```python
#eg 2.2
"This is string."
'This is also string.'
```

这样，string中可包含'与"

```python
#eg 2.3
'I told my friend, "python is my favorite language!"'
"The laguage 'Python' is named after Monty Python,not the snake."
```
## 2.2.1 使用方法修改字符串的单词大小写
首字母大写
```python
#eg 2.4
name="ada lovelace"
print(name.title())#输出结果为Ada Lovelace
```
下面将介绍全字段小写、全字段大写程序
```python
#eg 2.5
name="Ada Lovelace"
print(name.upper())#全字段大写，输出结果为ADA LOVELACE
print(name.lower())#全字段小写，输出结果为ada lovelace
```
## 2.2.2 在字符串中使用变量
```python
#eg 2.6
first_name="keelyn"
last_name="tse"
full_name=f"{first_name} {last_name}"
print(full_name)
```
这类字符串称为**f字符串**，f means format.可通过f字符串显示问候用户信息，如：
```python
#eg 2.7
print(f"Hello,{full_name.title()}!")
```
在eg 2.6当中，往后加入eg 2.7中的代码，输出效果为：
```python
Hello,Keelyn Tse!
```
或者可以2.7当中的将输出语句赋值给变量，再进行输出，格式如下：
```python
#eg 2.8
message=f"Hello,{full_name.title()}!"
printf(message)
```
## 2.2.3 使用制表符或换行符添加空白
>编程当中，空白泛指任意非打印字符，如空格、制表符与换行符，可适时选用以提高文档可阅读性。

在字符串中添加**制表符**，可用字符组合\t
```python
#eg 2.9
print("Python")
#输出为Python
print("\tPython")
#输出为    Python
```
字符串中添加**换行符**，可用字符组合\n
```python
#eg 2.10
print("Languages：\nPython\nC\nJavaScript")
```
同一个字符串可以同时包含换行符与制表符
```python
#eg 2.11
print("Languages：\n\tPython\n\tC\n\tJavaScript")
```
## 2.2.4 删除空白
可使用rstrip()方法确保输出字符串右端不存在空白，使用示例如下：
```python
#eg 2.12
learning_language='python '
print(learning_language.rstrip())
#输出为python，变量值为'python '
```
但是，上述方法逻辑为在输出内存单元中分配一个新单元存储删除空格后进行输出
想要永久删除空格，应renew原有变量值
```python
#eg 2.13
learning_language='python '
learning_language=learning_language.rstrip()
print(learning_language)
#输出为python，且变量值为'python'
```
同上述使用方法，lstrip()为删除字符串左边空白，strip()为删除字符串两端空白
## 2.2.5 删除前缀
假定一个URL包含常见前缀https://，但是使用中不想保留，可使用removeprefix()方法
```python
#eg 2.14
a_url='https://markdown.com.cn/'
print(a_url.removeprefix('https://'))
#输出结果为markdown.com.cn/
```
同eg2.12，操作不覆盖原有值，如想彻底删除应renew原有变量值
## 2.2.6 删除后缀
参考2.2.5内容，删除后缀方法为removesuffix()
## 2.2.7 在使用字符串避免语法错误
$$注意单双引号内容，注意查看Traceback$$

# 2.3 数Number
## 2.3.1 整数
- Python终端当中，可以对整数[^1]进行加（+）减（-）乘（*）除（/）运算，乘方用（**）表示
- 空格不影响计算顺序
- 加括号可指定运算顺序（与四则运算相同）
[^1]:整数，integer，常简写为int
## 2.3.2 浮点数
带小数点的数即为**浮点数（float）**
## 2.3.3 整数和浮点数
- 任意两个数相除，结果总数浮点数[^2]
- 任何运算过程中，如果一个操作数为浮点数，其结果仍然为浮点数
[^2]:整数与整数相除也是如此
## 2.3.4 数中的下划线
在书写很大的数字时，可使用下划线将数字进行分组，使其更加简单易读
```python
#eg 2.15
universe_age=14_000_000_000
print(universe_age)
#输出结果为14000000000
```
python将自动忽略其中的下划线，既适用于整数也适用于浮点数
## 2.3.5 同时给多个变量赋值
可在一行代码中为多个变量赋值，将变量名与变量使用逗号进行分隔即可
```python
#将x,y,z赋0为初始值
x,y,z=0,0,0
```
## 2.3.6 常量
Python无内置常量，Python程序员会通过写全大写字母来表征不变量，如下：
```python
MAX_CONNECTIONS=5000
```
# 2.4 Python之禅
在Python终端中输入import this，将会得到Python之禅，可看作一个彩蛋，介绍了编写优秀Python代码的指导原则，其全文如下：
>The Zen of Python, by Tim Peters
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!