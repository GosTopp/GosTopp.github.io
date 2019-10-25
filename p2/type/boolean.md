# 布尔值与逻辑运算

程序里，一个语句只要涉及判断，就会产生结果，这个结果就是布尔值（True/False）。

## 1. True or False

我们来看几个程序里涉及判断的语句。

```python
1==2 # 结果为 False
2>1 # 结果为 True
1+2 < 5 # 结果为 True
'Bob'=='bob' # 结果为 False
len('abc')==1 # len(）函数用来计算数据的长度，结果为 False
'd' in ['a','b','c'] # 'd' 在列表里，结果为 False
```

得到一个布尔值有什么用？我们来看一段代码，其中`elif`对应 else if ，就是“如果”的意思，表示条件分支。

```python
x=18

if x<14:    # 不符合条件，x<14 为假，下述代码跳过不执行
    y='Children'
    print(y)
elif x<24:    # 符合条件，x<24 为真，执行下述代码
    y='Youth'
    print(y)
elif x<64:    # 未执行
    y='Adults'
    print(y)
else:        # 未执行
    y='Seniors'
    print(y)
```

在上述的条件分支中，从上往下依次检查判断语句的真假，我们发现当进行到`x<24`时，语句为真，于是就执行了`y='Youth'`和`print(y)`，最终会在屏幕上打印出`Youth`。

  
由此可以看出，通过布尔值（True/False）我们可以控制一段程序的运行逻辑，判定代码块是否执行，这在后面深入学习条件语句、循环语句和流程控制会频繁使用。

## 2. 逻辑运算

多个布尔值通过逻辑运算符连接，也可以进行逻辑运算。 在自然语言中，我们同时陈述两个判断时，中间通常会有语法连接词\(grammatical conjunction\)，如下面[例子](https://en.wikipedia.org/wiki/Logical_connective)：

1. Jack went up the hill.
2. Jill went up the hill.
3. Jack went up the hill **and** Jill went up the hill.
4. Jack went up the hill **so** Jill went up the hill.

在3的语句中, and 是逻辑连接符号，因为当1和2同时为真时，语句3必为真。 而4的语句中, so 不是逻辑连接符号，因为当1和2同时为真时，语句4未必为真。

可以看出，逻辑连接符是那些可以通过判定子句真假而得到整句真假的语法链接符，比如: `and`和`or`。

```python
True and True # 两个判断同时为真，and 连接
>>> True # 结果为真

True and False # 两个判断一真一假，and 连接
>>> False # 结果为假


True or False # 两个判断一真一假，or 连接
>>> True # 结果为真
```

除了上述`and`和`or`可以作为逻辑连接符, `not`可以对布尔值做反向操作

```python
not True
>>> False

not False
>>> True
```

## 3. 算术运算

在 Python 里，布尔值也可以做算术运算，也就是常见的`+ - * /`，在做算术计算时，True 代表 1， False 代表 0。

```python
True+True
>>> 2

True+False
>>> 1

False+False
>>> 0
```

