# 条件判断

* 常用条件判断语句:

 1. 二重选择:
  ```python
    age = 3
    if age >= 18:
        print('your age is', age)
        print('adult')
    else:
        print('your age is', age)
        print('teenager')
 ```
 2.多重选择:
 ```python
    if <条件判断1>:
        <执行1>
    elif <条件判断2>:
        <执行2>
    elif <条件判断3>:
        <执行3>
    else:
        <执行4>
 ```

* 注意不要少写了冒号`:`。


# 循环


&ensp; &ensp; 1.`for...in`循环语句:
 
```python
names = ['Michael', 'Bob', 'Tracy']
for name in names:
    print(name)
```
 
&ensp; &ensp; &ensp;执行后的结果:
 
```python
Michael
Bob
Tracy
```

&ensp; &ensp; &ensp;再如执行1+2+3+...+100:

```python
sum = 0
for x in range(101):
    sum = sum + x
print(sum)

5050
```

&ensp; &ensp; 2.`while`循环语句:

&ensp; &ensp; &ensp;满足条件，就会一直执行。

```python
sum = 0
n = 99
while n > 0:
    sum = sum + n
    n = n - 2
print(sum)

2500
```

* `break`语句可以在循环过程中直接退出循环，而`continue`语句可以提前结束本轮循环，并直接开始下一轮循环。这两个语句通常都必须配合`if`语句使用。
