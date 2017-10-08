# Python������������

## ����

* Python���Դ��������С����������Ȼ�������������ڳ����еı�ʾ��������ѧ�ϵ�д��һģһ�������磺`1`��`100`��`-8080`��`0`���ȵȡ�

* ���������ʹ�ö����ƣ����ԣ���ʱ����ʮ�����Ʊ�ʾ�����ȽϷ��㣬ʮ��������`0x`ǰ׺��`0-9`��`a-f`��ʾ�����磺`0xff00`��`0xa5b4c3d2`���ȵȡ�

## ������

* ������Ҳ����С����֮���Գ�Ϊ������������Ϊ���տ�ѧ��������ʾʱ��һ����������С����λ���ǿɱ�ģ����磬`1.23x109`��`12.3x108`����ȫ��ȵġ���������������ѧд������`1.23`��`3.14`��`-9.01`���ȵȡ����Ƕ��ںܴ���С�ĸ��������ͱ����ÿ�ѧ��������ʾ����`10`��`e`�����`1.23x109`����`1.23e9`������`12.3e8`��`0.000012`����д��`1.2e-5`���ȵȡ�

* �����͸������ڼ�����ڲ��洢�ķ�ʽ�ǲ�ͬ�ģ�����������Զ�Ǿ�ȷ�ģ������ѵ�Ҳ�Ǿ�ȷ�ģ��ǵģ���������������������ܻ��������������

## �ַ���

* �ַ������Ե�����`'`��˫����`"`�������������ı�������`'abc'`��`"xyz"`�ȵȡ���ע�⣬`''`��`""`����ֻ��һ�ֱ�ʾ��ʽ�������ַ�����һ���֣���ˣ��ַ���`'abc'`ֻ��`a`��`b`��`c`��3���ַ������`'`����Ҳ��һ���ַ����ǾͿ�����`""`������������`"I'm OK"`�������ַ���`I`��`'`��`m`��`�ո�`��`O`��`K`��6���ַ���

* ����ַ����ڲ��Ȱ���`'`�ְ���`"`��ô�죿������ת���ַ�`\`����ʶ�����磺

```python
'I\'m \"OK\"!'
```

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;��ʾ���ַ�������Ϊ:

```python
I'm "OK"!
```

* ת���ַ�`\`����ת��ܶ��ַ�������`\n`��ʾ���У�`\t`��ʾ�Ʊ������ַ�`\`����ҲҪת�壬����`\\`��ʾ���ַ�����`\`��������Python�Ľ���ʽ��������`print()`��ӡ�ַ���������

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

* ����ַ��������кܶ��ַ�����Ҫת�壬����Ҫ�Ӻܶ�`\`��Ϊ�˼򻯣�Python��������`r''`��ʾ`''`�ڲ����ַ���Ĭ�ϲ�ת�壬

```python
>>> print('\\\t\\')
\       \
>>> print(r'\\\t\\')
\\\t\\
```

## ����ֵ

* һ������ֵֻ��`True`��`False`����ֵ������:

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

* ����ֵ��`��`��`��`��`��`�����Ϊ`and`��`or`��`not`��

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

## ����

* ���������淶:������������`��СдӢ��`��`���ֺ�_`����ϣ���`���������ֿ�ͷ`

## ����

* ��python��ͨ����`ȫ����д�ı�����`����ʾ������

```python
PI = 3.14159265359
```

## ��������

* ��python�У������ֳ���:һ����`/`������Ľ���Ǹ�����

```python
>>> 10 / 3
3.3333333333333335
```

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;���ھ������⣬����3.33333333333

* ��һ�ֳ�����`//`����Ϊ�ذ��,���������ĳ�����Ȼ������������:

```python
>>> 10 // 3
3
```

* ȡ������ʹ��`%`�����

## ��ϰ

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
```