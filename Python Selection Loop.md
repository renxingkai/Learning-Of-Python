# �����ж�

* ���������ж����:

 1. ����ѡ��:
  ```python
    age = 3
    if age >= 18:
        print('your age is', age)
        print('adult')
    else:
        print('your age is', age)
        print('teenager')
 ```
 2.����ѡ��:
 ```python
    if <�����ж�1>:
        <ִ��1>
    elif <�����ж�2>:
        <ִ��2>
    elif <�����ж�3>:
        <ִ��3>
    else:
        <ִ��4>
 ```

* ע�ⲻҪ��д��ð��`:`��


# ѭ��


&ensp; &ensp; 1.`for...in`ѭ�����:
 
```python
names = ['Michael', 'Bob', 'Tracy']
for name in names:
    print(name)
```
 
&ensp; &ensp; &ensp;ִ�к�Ľ��:
 
```python
Michael
Bob
Tracy
```

&ensp; &ensp; &ensp;����ִ��1+2+3+...+100:

```python
sum = 0
for x in range(101):
    sum = sum + x
print(sum)

5050
```

&ensp; &ensp; 2.`while`ѭ�����:

&ensp; &ensp; &ensp;�����������ͻ�һֱִ�С�

```python
sum = 0
n = 99
while n > 0:
    sum = sum + n
    n = n - 2
print(sum)

2500
```

* `break`��������ѭ��������ֱ���˳�ѭ������`continue`��������ǰ��������ѭ������ֱ�ӿ�ʼ��һ��ѭ�������������ͨ�����������`if`���ʹ�á�
