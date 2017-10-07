#Python输入输出语法

##输出

* 用print()在括号中加上字符串，就可以向屏幕上输出指定的文字。比如输出`hello,world`,用代码实现如下:

```python
>>>print("hello,world")
hello,world
或
>>>print('hello,world')
hello,world
```

* print()函数也可以接受多个字符串，用逗号`","`隔开，就可以连成一串输出:

```pythton
>>>print('The quick brown fox','jumps over','the lazy dog')
The quick brown fox jumps over the lazy dog
```

* print()也可以打印整数,或者计算结果:

```python
>>>print(300)
300
>>>print(100+200)
300
```

* 同时，我们可以把计算`100+200`的结果打印得漂亮一点:

```python
>>>print('100+200=',100+200)
100+200=300
```
注意，对于`100+200`，Python解释器自动计算出结果`300`，但是，`'100+200='`是字符串而非数学公式，Python把它视为字符串。

##输入

* Python提供了一个`input()`，可以让用户输入字符串，并且存放到一个变量里。比如输入用户的名字:

```python
>>>name=input()
Michael
>>>name
'Michael'
```

* 也可以用`print()`函数打印name值

```python
>>>print(name)
Michael
```

* 如果需要程序在输入时，存在用户提示，`input()`也可以来显示一个字符串来提示用户，于是我们把代码改为:

```python
>>>name=input('please enter your name:')
please enter your name:Michael
>>>print('hello,',name)
hello,Michael
```