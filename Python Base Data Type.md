# Python基础数据类型

## 整数

* Python可以处理任意大小的整数，当然包括负整数，在程序中的表示方法和数学上的写法一模一样，例如：`1`，`100`，`-8080`，`0`，等等。

* 计算机由于使用二进制，所以，有时候用十六进制表示整数比较方便，十六进制用`0x`前缀和`0-9`，`a-f`表示，例如：`0xff00`，`0xa5b4c3d2`，等等。

## 浮点数

* 浮点数也就是小数，之所以称为浮点数，是因为按照科学记数法表示时，一个浮点数的小数点位置是可变的，比如，`1.23x109`和`12.3x108`是完全相等的。浮点数可以用数学写法，如`1.23`，`3.14`，`-9.01`，等等。但是对于很大或很小的浮点数，就必须用科学计数法表示，把`10`用`e`替代，`1.23x109`就是`1.23e9`，或者`12.3e8`，`0.000012`可以写成`1.2e-5`，等等。

* 整数和浮点数在计算机内部存储的方式是不同的，整数运算永远是精确的（除法难道也是精确的？是的！），而浮点数运算则可能会有四舍五入的误差。

## 字符串

* 字符串是以单引号`'`或双引号`"`括起来的任意文本，比如`'abc'`，`"xyz"`等等。请注意，`''`或`""`本身只是一种表示方式，不是字符串的一部分，因此，字符串`'abc'`只有`a`，`b`，`c`这3个字符。如果`'`本身也是一个字符，那就可以用`""`括起来，比如`"I'm OK"`包含的字符是`I`，`'`，`m`，`空格`，`O`，`K`这6个字符。

* 如果字符串内部既包含`'`又包含`"`怎么办？可以用转义字符`\`来标识，比如：

```python
'I\'m \"OK\"!'
```

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;表示的字符串内容为:

```python
I'm "OK"!
```

* 转义字符`\`可以转义很多字符，比如`\n`表示换行，`\t`表示制表符，字符`\`本身也要转义，所以`\\`表示的字符就是`\`，可以在Python的交互式命令行用`print()`打印字符串看看：

```python
>>> print('I\'m ok.')
I'm ok.
>>> print('I\'m learning\nPython.')
I'm learning
Python.
>>> print('\\\n\\')
\
\
```

* 如果字符串里面有很多字符都需要转义，就需要加很多`\`，为了简化，Python还允许用`r''`表示`''`内部的字符串默认不转义，

```python
>>> print('\\\t\\')
\       \
>>> print(r'\\\t\\')
\\\t\\
```

* 对于单个字符的编码，Python提供了`ord()`函数获取字符的整数表示，`chr()`函数把编码转换为对应的字符：

```python
>>> ord('A')
65
>>> ord('中')
20013
>>> chr(66)
'B'
>>> chr(25991)
'文'
```

* Python对`bytes`类型的数据用带`b`前缀的单引号或双引号表示：

```python
x = b'ABC'
```

* 以`Unicode`表示的`str`通过`encode()`方法可以编码为指定的`bytes`，例如：

```python
>>> 'ABC'.encode('ascii')
b'ABC'
>>> '中文'.encode('utf-8')
b'\xe4\xb8\xad\xe6\x96\x87'
>>> '中文'.encode('ascii')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
UnicodeEncodeError: 'ascii' codec can't encode characters in position 0-1: ordinal not in range(128)
```

* 纯英文的`str`可以用`ASCII`编码为`bytes`，内容是一样的，含有中文的`str`可以用`UTF-8`编码为`bytes`。含有中文的`str`无法用`ASCII`编码，因为中文编码的范围超过了`ASCII`编码的范围，Python会报错。

* 如果我们从网络或磁盘上读取了字节流，那么读到的数据就是`bytes`。要把`bytes`变为`str`，就需要用`decode()`方法：

```python
>>> b'ABC'.decode('ascii')
'ABC'
>>> b'\xe4\xb8\xad\xe6\x96\x87'.decode('utf-8')
'中文'
```

* 要计算`str`包含多少个字符，可以用`len()`函数：

```python
>>> len('ABC')
3
>>> len('中文')
2
```

* `len()`函数计算的是`str`的字符数，如果换成`bytes`，`len()`函数就计算字节数：

```python
>>> len(b'ABC')
3
>>> len(b'\xe4\xb8\xad\xe6\x96\x87')
6
>>> len('中文'.encode('utf-8'))
6
```

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;可见，1个中文字符经过`UTF-8`编码后通常会占用3个字节，而1个英文字符只占用1个字节。

## 布尔值

* 一个布尔值只有`True`、`False`两种值，例如:

```python
>>> True
True
>>> False
False
>>> 3 > 2
True
>>> 3 > 5
False
```

* 布尔值的`与`、`或`、`非`运算符为`and`、`or`、`not`。

```python
>>> True or True
True
>>> True or False
True
>>> False or False
False
>>> 5 > 3 or 1 > 3
True
```

## 变量

* 变量命名规范:变量名必须是`大小写英文`、`数字和_`的组合，且`不能用数字开头`

## 常量

* 在python中通常用`全部大写的变量名`来表示常量。

```python
PI = 3.14159265359
```

## 除法运算

* 在python中，有两种除法:一种是`/`，计算的结果是浮点数

```python
>>> 10 / 3
3.3333333333333335
```

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;由于精度问题，并非3.33333333333

* 另一种除法是`//`，称为地板除,两个整数的除法仍然是整数，例如:

```python
>>> 10 // 3
3
```

* 取余运算使用`%`运算符


## 格式化

* 在Python中，采用的格式化方式和C语言是一致的，用`%`实现，举例如下：

```python
>>> 'Hello, %s' % 'world'
'Hello, world'
>>> 'Hi, %s, you have $%d.' % ('Michael', 1000000)
'Hi, Michael, you have $1000000.'
```

* 常见的占位符有：

- %d    整数
- %f	浮点数
- %s	字符串
- %x	十六进制整数

* 其中，格式化整数和浮点数还可以指定是否补0和整数与小数的位数：

```python
>>> '%2d-%02d' % (3, 1)
' 3-01'
>>> '%.2f' % 3.1415926
'3.14'
```

* 如果不确定用什么，`%s`永远起作用，它会把任何数据类型转换为字符串。

* 如果字符串里面的`%`一个普通字符怎么办？这个时候就需要转义，用`%%`来表示一个`%`



## 练习

```python
>>> s2 = 'Hello, \'Adam\''
>>> print(s2)
Hello, 'Adam'
>>> s3 = r'Hello, "Bart"'
>>> print(s3)
Hello, "Bart"
>>> s4 = r'''Hello,
Lisa!'''
>>> print(s4)
Hello,
Lisa!





>>> s1=72
>>> s2=85
>>> r=((85-72)/72)*100
>>> print('%2.1f%%'%r)
18.1%
```