#Python��������﷨

##���

* ��print()�������м����ַ������Ϳ�������Ļ�����ָ�������֡��������`hello,world`,�ô���ʵ������:

```python
>>>print("hello,world")
hello,world
��
>>>print('hello,world')
hello,world
```

* print()����Ҳ���Խ��ܶ���ַ������ö���`","`�������Ϳ�������һ�����:

```pythton
>>>print('The quick brown fox','jumps over','the lazy dog')
The quick brown fox jumps over the lazy dog
```

* print()Ҳ���Դ�ӡ����,���߼�����:

```python
>>>print(300)
300
>>>print(100+200)
300
```

* ͬʱ�����ǿ��԰Ѽ���`100+200`�Ľ����ӡ��Ư��һ��:

```python
>>>print('100+200=',100+200)
100+200=300
```
ע�⣬����`100+200`��Python�������Զ���������`300`�����ǣ�`'100+200='`���ַ���������ѧ��ʽ��Python������Ϊ�ַ�����

##����

* Python�ṩ��һ��`input()`���������û������ַ��������Ҵ�ŵ�һ����������������û�������:

```python
>>>name=input()
Michael
>>>name
'Michael'
```

* Ҳ������`print()`������ӡnameֵ

```python
>>>print(name)
Michael
```

* �����Ҫ����������ʱ�������û���ʾ��`input()`Ҳ��������ʾһ���ַ�������ʾ�û����������ǰѴ����Ϊ:

```python
>>>name=input('please enter your name:')
please enter your name:Michael
>>>print('hello,',name)
hello,Michael
```