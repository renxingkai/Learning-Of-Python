# �б��Ԫ��

## �б�list

* Python���õ�һ�������������б�`list`��`list`��һ������ļ��ϣ�������ʱ��Ӻ�ɾ�����е�Ԫ�ء�

* �����г�����ͬѧ����:

```python
>>> classmates = ['Michael', 'Bob', 'Tracy']
>>> classmates
['Michael', 'Bob', 'Tracy']
```

* ����`classmates`����һ��`list`����`len()`�������Ի��`list`Ԫ�صĸ�����

```python
>>> len(classmates)
3
```

* ������������`list`��ÿһ��λ�õ�Ԫ�أ��ǵ������Ǵ�0��ʼ�ģ����һ��Ԫ�ص�������:`len(classmates)-1`��

* ͬʱ�����һ��Ԫ����������Ϊ-1�������ڶ���Ϊ-2���Դ����ơ�

* list��һ���ɱ����������ԣ�������list��׷��Ԫ�ص�ĩβ��

```python
>>> classmates.append('Adam')
>>> classmates
['Michael', 'Bob', 'Tracy', 'Adam']
```

* Ҳ���԰�Ԫ�ز��뵽ָ����λ�ã�����������Ϊ1��λ�ã�

```python
>>> classmates.insert(1, 'Jack')
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy', 'Adam']
```

* Ҫɾ��`list`ĩβ��Ԫ�أ���`pop()`������

```python
>>> classmates.pop()
'Adam'
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy']
```

* Ҫɾ��ָ��λ�õ�Ԫ�أ���`pop(i)`����������`i`������λ�ã�

```python
>>> classmates.pop(1)
'Jack'
>>> classmates
['Michael', 'Bob', 'Tracy']
```

* Ҫ��ĳ��Ԫ���滻�ɱ��Ԫ�أ�����ֱ�Ӹ�ֵ����Ӧ������λ�ã�

```python
>>> classmates[1] = 'Sarah'
>>> classmates
['Michael', 'Sarah', 'Tracy']
```

* `list`�����Ԫ�ص���������Ҳ���Բ�ͬ�����磺

```python
>>> L = ['Apple', 123, True]
```

* `list`Ԫ��Ҳ��������һ��`list`�����磺

```python
>>> s = ['python', 'java', ['asp', 'php'], 'scheme']
>>> len(s)
4
```


## Ԫ��tuple

* ��һ�������б��Ԫ��:`tuple`��`tuple`��`list`�ǳ����ƣ�����`tuple`һ����ʼ���Ͳ����޸ģ�����ͬ�����г�ͬѧ�����֣�

```python
>>> classmates = ('Michael', 'Bob', 'Tracy')
```

* `tuple`û��`insert()`��`pop()`�ȷ�����

* ���ֻ��1��Ԫ�ص�tuple����ʱ�����һ������`','`�����������壬�������������Ϊtupleֻ��1�������Python����ʾֻ��1��Ԫ�ص�tupleʱ��Ҳ���һ������,��������������ѧ���������ϵ����š�

```python
>>> s=(1)
>>> s
1
>>> s=(1,)
>>> s
(1,)
```

* �����Ҫ��tuple�ɱ䣬�����:

```python
>>> t = ('a', 'b', ['A', 'B'])
>>> t[2][0] = 'X'
>>> t[2][1] = 'Y'
>>> t
('a', 'b', ['X', 'Y'])
```
