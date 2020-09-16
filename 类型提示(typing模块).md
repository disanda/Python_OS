# 类型提示


## 1.动态类型 (dynamic typing)
Python是一种动态类型语言，这意味着Python解释器只在该段代码运行时才会检查变量类型

- case1
```py
if False:
  1+'two' #这段代码不会运行，所以也就不会报错
else:
  1+2

1+'two' #这段代码会 raise TypeError
```
- case2
```py
>>>thing = 'hello'
>>>type(thing)
<class 'str'>

>>>thing = 28
>>>type(thing)
<clas 'float'>
```
>python变量可以改变类型

## 2.静态类型 (Static Typing)

静态类型会在代码执行前检查类型，类型不对就会报错.

比如 Java和C,就是静态类型编码，变量赋值时需要声明类型，在编码时就会检查类型.

静态类型一般不充许类型转换，尽管存在类型强制转换的语法.

## 3.鸭类型 (Duck Typing)
是动态类型相关的概念，涉及面向对象时，类型指代的类。

比如一个类有默认的方法，当子类覆盖了这个方法时，那么子类的方法就是可以执行的.

## 4.类型提示

```py

def headline(text, align=True):
  if align:
    return f"{text.title()}\n{'-'* len(text)}"
  else:
    return f"{text.title()}".center(50,"0") #文本居中两边是'o'

def headline(text: str, align: bool = Ture) -> str:
    ....
```

以上类型提示: 

- text参数类型为 str
- align参数类型为Ture
- 函数返回值类型为str

注意类型提示不是强制性的，就是说函数实现时类型与类型提示不符，程序也不会报错

## 注解 (Annotations)

## 集合型数据 (composite types)

```py

name: list = ['a','b','c']
nums: tuple = (3, 7, 1)
dicts: dict = {1:False, 2:True}

from typing import Dict, List, Tuple

name: List = ['a','b','c']
nums: Tuple = [3, 7, 1]
dicts: Dict = {1:False, 2:True}
nested: List[Tuple[str,str]] #规定了列表，以及列表中元素的类型
```








## reference
- realpython.com/python-type-checking
