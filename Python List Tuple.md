# 列表和元组

## 列表list

* Python内置的一种数据类型是列表：`list`。`list`是一种有序的集合，可以随时添加和删除其中的元素。

* 比如列出班里同学名字:

```python
>>> classmates = ['Michael', 'Bob', 'Tracy']
>>> classmates
['Michael', 'Bob', 'Tracy']
```

* 变量`classmates`就是一个`list`。用`len()`函数可以获得`list`元素的个数：

```python
>>> len(classmates)
3
```

* 用索引来访问`list`中每一个位置的元素，记得索引是从0开始的，最后一个元素的索引是:`len(classmates)-1`。

* 同时，最后一个元素索引可以为-1，倒数第二个为-2，以此类推。

* list是一个可变的有序表，所以，可以往list中追加元素到末尾：

```python
>>> classmates.append('Adam')
>>> classmates
['Michael', 'Bob', 'Tracy', 'Adam']
```

* 也可以把元素插入到指定的位置，比如索引号为1的位置：

```python
>>> classmates.insert(1, 'Jack')
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy', 'Adam']
```

* 要删除`list`末尾的元素，用`pop()`方法：

```python
>>> classmates.pop()
'Adam'
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy']
```

* 要删除指定位置的元素，用`pop(i)`方法，其中`i`是索引位置：

```python
>>> classmates.pop(1)
'Jack'
>>> classmates
['Michael', 'Bob', 'Tracy']
```

* 要把某个元素替换成别的元素，可以直接赋值给对应的索引位置：

```python
>>> classmates[1] = 'Sarah'
>>> classmates
['Michael', 'Sarah', 'Tracy']
```

* `list`里面的元素的数据类型也可以不同，比如：

```python
>>> L = ['Apple', 123, True]
```

* `list`元素也可以是另一个`list`，比如：

```python
>>> s = ['python', 'java', ['asp', 'php'], 'scheme']
>>> len(s)
4
```


## 元组tuple

* 另一种有序列表叫元组:`tuple`。`tuple`和`list`非常类似，但是`tuple`一旦初始化就不能修改，比如同样是列出同学的名字：

```python
>>> classmates = ('Michael', 'Bob', 'Tracy')
```

* `tuple`没有`insert()`，`pop()`等方法。

* 如果只有1个元素的tuple定义时必须加一个逗号`','`，来消除歧义，否则编译器会认为tuple只有1这个数。Python在显示只有1个元素的tuple时，也会加一个逗号,，以免你误解成数学计算意义上的括号。

```python
>>> s=(1)
>>> s
1
>>> s=(1,)
>>> s
(1,)
```

* 如果需要让tuple可变，则可以:

```python
>>> t = ('a', 'b', ['A', 'B'])
>>> t[2][0] = 'X'
>>> t[2][1] = 'Y'
>>> t
('a', 'b', ['X', 'Y'])
```
