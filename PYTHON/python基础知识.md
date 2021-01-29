## 数据类型

![image-20200910211723231](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20200910211723231-1599748063175.png)

- 值类型

  字符串、元祖、数值(整型、浮点型、布尔型)

- 引用类型

  列表、字典、集合

## 输出

| 格式符号 |          转换          |
| :------: | :--------------------: |
|  **%s**  |         字符串         |
|  **%d**  |   有符号的十进制整数   |
|  **%f**  |         浮点数         |
|    %c    |          字符          |
|    %u    |    无符号十进制整数    |
|    %o    |       八进制整数       |
|    %x    | 十六进制整数（小写ox） |
|    %X    | 十六进制整数（大写OX） |
|    %e    | 科学计数法（小写'e'）  |
|    %E    | 科学计数法（大写'E'）  |
|    %g    |      %f和%e的简写      |
|    %G    |      %f和%E的简写      |

> 技巧

- %06d，表示输出的整数显示位数，不足以0补全，超出当前位数则原样输出
- %.2f，表示小数点后显示的小数位数。

```python
"""
    输出
"""
age = 18
name = "Tom"
weight = 75.5
studentId = 1
print("我的名字是%s" % name)

print("我的学号是%4d" % studentId)

print("我的体重是%.2f" % weight)
```

> f-格式化字符串是Python3.6中新增的格式化方法，该方法更简单易读。

### 转义字符

- `\n`：换行。
- `\t`：制表符，一个tab键（4个空格）的距离。

###  结束符

> 想一想，为什么两个print会换行输出？

```python
print('输出的内容', end="\n")
```

> 在Python中，print()， 默认自带`end="\n"`这个换行结束符，所以导致每两个`print`直接会换行展示，用户可以按需求更改结束符。

## 输入

- 输入功能
  - input('提示文字')
- 输入的特点
  - 一般将input接收的数据存储到变量
  - input接收的任何数据默认都是字符串数据类型

```python
password = input("请输入密码：")
print(f"你输入的密码是{password}")
```

## 数据类型转换

|         函数          |                        说明                         |
| :-------------------: | :-------------------------------------------------: |
|  **int(x [,base ])**  |                  将x转换为一个整数                  |
|     **float(x )**     |                 将x转换为一个浮点数                 |
| complex(real [imag ]) |        创建一个复数，real为实部，imag为虚部         |
|      **str(x )**      |                将对象 x 转换为字符串                |
|       repr(x )        |             将对象 x 转换为表达式字符串             |
|    **eval(str )**     | 用来计算在字符串中的有效Python表达式,并返回一个对象 |
|     **tuple(s )**     |               将序列 s 转换为一个元组               |
|     **list(s )**      |               将序列 s 转换为一个列表               |
|        chr(x )        |           将一个整数转换为一个Unicode字符           |
|        ord(x )        |           将一个字符转换为它的ASCII整数值           |
|        hex(x )        |         将一个整数转换为一个十六进制字符串          |
|        oct(x )        |          将一个整数转换为一个八进制字符串           |
|        bin(x )        |          将一个整数转换为一个二进制字符串           |

```python
num = input("请输入一个整数：")
print(type(num))

print(type(int(num)))

print(type(float(num)))

list1 = [1, 2, 3, 4]
print(type(tuple(list1)))

tuple1 = (1, 2, 3, 4)
print(type(list(tuple1)))

str1 = "10"
str2 = "[1, 2, 3]"
str3 = "(1, 2, 3)"

print(type(eval(str1)))
print(type(eval(str2)))
print(type(eval(str3)))
```

转换数据类型常用的函数

- int()
- float()
- str()
- list()
- tuple()
- eval()

## 运算符

### 运算符的分类

- 算数运算符
- 赋值运算符
- 复合赋值运算符
- 比较运算符
- 逻辑运算符

##### 算数运算符

| 运算符 |  描述  | 实例                                                  |
| :----: | :----: | ----------------------------------------------------- |
|   +    |   加   | 1 + 1 输出结果为 2                                    |
|   -    |   减   | 1-1 输出结果为 0                                      |
|   *    |   乘   | 2 * 2 输出结果为 4                                    |
|   /    |   除   | 10 / 2 输出结果为 5                                   |
|   //   |  整除  | 9 // 4 输出结果为2                                    |
|   %    |  取余  | 9 % 4 输出结果为 1                                    |
|   **   |  指数  | 2 ** 4 输出结果为 16，即 2 * 2 * 2 * 2                |
|   ()   | 小括号 | 小括号用来提高运算优先级，即 (1 + 2) * 3 输出结果为 9 |

> 注意：

- 混合运算优先级顺序：`()`高于 `**` 高于 `*` `/` `//` `%` 高于 `+` `-`

##### 赋值运算符

| 运算符 | 描述 | 实例                                |
| ------ | ---- | ----------------------------------- |
| =      | 赋值 | 将`=`右侧的结果赋值给等号左侧的变量 |

- 单个变量赋值

```python
num = 1
print(num)
```

- 多个变量赋值

```python
num1, float1, str1 = 10, 0.5, 'hello world'
print(num1)
print(float1)
print(str1)
```

- 多变量赋相同值

```python
a = b = 10
print(a)
print(b)
```

##### 复合赋值运算符

| 运算符 | 描述           | 实例                       |
| ------ | -------------- | -------------------------- |
| +=     | 加法赋值运算符 | c += a 等价于 c = c + a    |
| -=     | 减法赋值运算符 | c -= a 等价于 c = c- a     |
| *=     | 乘法赋值运算符 | c *= a 等价于 c = c * a    |
| /=     | 除法赋值运算符 | c /= a 等价于 c = c / a    |
| //=    | 整除赋值运算符 | c //= a 等价于 c = c // a  |
| %=     | 取余赋值运算符 | c %= a 等价于 c = c % a    |
| **=    | 幂赋值运算符   | c ** = a 等价于 c = c ** a |

```python
a = 100
a += 1
# 输出101  a = a + 1,最终a = 100 + 1
print(a)

b = 2
b *= 3
# 输出6  b = b * 3,最终b = 2 * 3
print(b)

c = 10
c += 1 + 2
# 输出13, 先算运算符右侧1 + 2 = 3， c += 3 , 推导出c = 10 + 3
print(c)
```



##### 比较运算符

比较运算符也叫关系运算符， 通常用来判断。

| 运算符 | 描述                                                         | 实例                                                        |
| ------ | ------------------------------------------------------------ | ----------------------------------------------------------- |
| ==     | 判断相等。如果两个操作数的结果相等，则条件结果为真(True)，否则条件结果为假(False) | 如a=3,b=3，则（a == b) 为 True                              |
| !=     | 不等于 。如果两个操作数的结果不相等，则条件为真(True)，否则条件结果为假(False) | 如a=3,b=3，则（a == b) 为 True如a=1,b=3，则(a != b) 为 True |
| >      | 运算符左侧操作数结果是否大于右侧操作数结果，如果大于，则条件为真，否则为假 | 如a=7,b=3，则(a > b) 为 True                                |
| <      | 运算符左侧操作数结果是否小于右侧操作数结果，如果小于，则条件为真，否则为假 | 如a=7,b=3，则(a < b) 为 False                               |
| >=     | 运算符左侧操作数结果是否大于等于右侧操作数结果，如果大于，则条件为真，否则为假 | 如a=7,b=3，则(a < b) 为 False如a=3,b=3，则(a >= b) 为 True  |
| <=     | 运算符左侧操作数结果是否小于等于右侧操作数结果，如果小于，则条件为真，否则为假 | 如a=3,b=3，则(a <= b) 为 True                               |

```python
a = 7
b = 5
print(a == b)  # False
print(a != b)  # True
print(a < b)   # False
print(a > b)   # True
print(a <= b)  # False
print(a >= b)  # True
```

##### 逻辑运算符

| 运算符 | 逻辑表达式 | 描述                                                         | 实例                                     |
| ------ | ---------- | ------------------------------------------------------------ | ---------------------------------------- |
| and    | x and y    | 布尔"与"：如果 x 为 False，x and y 返回 False，否则它返回 y 的值。 | True and False， 返回 False。            |
| or     | x or y     | 布尔"或"：如果 x 是 True，它返回 True，否则它返回 y 的值。   | False or True， 返回 True。              |
| not    | not x      | 布尔"非"：如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。 | not True 返回 False, not False 返回 True |

```python
a = 1
b = 2
c = 3
print((a < b) and (b < c))  # True
print((a > b) and (b < c))  # False
print((a > b) or (b < c))   # True
print(not (a > b))          # True
```

##### 拓展

数字之间的逻辑运算

``` python
a = 0
b = 1
c = 2

# and运算符，只要有一个值为0，则结果为0，否则结果为最后一个非0数字
print(a and b)  # 0
print(b and a)  # 0
print(a and c)  # 0
print(c and a)  # 0
print(b and c)  # 2
print(c and b)  # 1

# or运算符，只有所有值为0结果才为0，否则结果为第一个非0数字
print(a or b)  # 1
print(a or c)  # 2
print(b or c)  # 1
```

## 流程控制

### 条件语句

#### if

```python
# input接受用户输入的数据是字符串类型，条件是age和整型18做判断，所以这里要int转换数据类型
age = int(input('请输入您的年龄：'))

if age >= 18:
    print(f'您的年龄是{age},已经成年，可以上网')


print('系统关闭')
```

#### if...else...

```python
age = int(input('请输入您的年龄：'))

if age >= 18:
    print(f'您的年龄是{age},已经成年，可以上网')
else:
    print(f'您的年龄是{age},未成年，请自行回家写作业')

print('系统关闭')
```

#### 多重判断

```python
age = int(input('请输入您的年龄：'))
if age < 18:
    print(f'您的年龄是{age},童工一枚')
elif (age >= 18) and (age <= 60):
    print(f'您的年龄是{age},合法工龄')
elif age > 60:
    print(f'您的年龄是{age},可以退休')
```

#### 三目运算符

三目运算符也叫三元运算符。

语法如下：

``` python
值1 if 条件 else 值2
```

快速体验：

```python
a = 1
b = 2

c = a if a > b else b
print(c)
```

### 循环语句

在Python中，循环分为`while`和`for`两种，最终实现效果相同。

#### while

```python
# 重复打印9行表达式
j = 1
while j <= 9:
    # 打印一行里面的表达式 a * b = a*b
    i = 1
    while i <= j:
        print(f'{i}*{j}={j*i}', end='\t')
        i += 1
    print()
    j += 1
```

#### for

```python
str1 = 'helloWord'
for i in str1:
    print(i)
```

#### break

``` python
str1 = 'itheima'
for i in str1:
    if i == 'e':
        print('遇到e不打印')
        break
    print(i)
```

执行结果：

![image-20190104165242555](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190104165242555-6591962.png)

#### continue

```python
str1 = 'itheima'
for i in str1:
    if i == 'e':
        print('遇到e不打印')
        continue
    print(i)
```

执行结果：

![image-20190104165413160](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190104165413160-6592053.png)

## 数据序列

### 1、字符串

#### 一对引号字符串

```python
name1 = 'Tom'
name2 = "Rose"
```



#### 三引号字符串

```python
name3 = ''' Tom '''
name4 = """ Rose """
a = ''' i am Tom, 
        nice to meet you! '''

b = """ i am Rose, 
        nice to meet you! """
```



#### 字符串转义

```python
c = "I'm Tom"
d = 'I\'m Tom'
```

#### 字符串输出

```python
print('hello world')

name = 'Tom'
print('我的名字是%s' % name)
print(f'我的名字是{name}')
```

#### 字符串输入

```python
name = input('请输入您的名字：')
print(f'您输入的名字是{name}')
print(type(name))

password = input('请输入您的密码：')
print(f'您输入的密码是{password}')
print(type(password))
```

#### <font color='red'>下标</font>

```python
name = "abcdef"

print(name[1])
print(name[0])
print(name[2])
```

- 输出结果

![image-20190129174231104](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190129174231104.png)

#### <font color='red'>切片</font>

切片是指对操作的对象截取其中一部分的操作。**字符串、列表、元组**都支持切片操作。

##### 语法

``` python
序列[开始位置下标:结束位置下标:步长]
```

> 注意

   	1. 不包含结束位置下标对应的数据， 正负整数均可；
   	2. 步长是选取间隔，正负整数均可，默认步长为1。

```python
name = "abcdefg"

print(name[2:5:1])  # cde
print(name[2:5])  # cde
print(name[:5])  # abcde
print(name[1:])  # bcdefg
print(name[:])  # abcdefg
print(name[::2])  # aceg
print(name[:-1])  # abcdef, 负1表示倒数第一个数据
print(name[-4:-1])  # def
print(name[::-1])  # gfedcba
```

#### <font color='red'>查找</font>

所谓字符串查找方法即是查找子串在字符串中的位置或出现的次数。

- find()：检测某个子串是否包含在这个字符串中，如果在返回这个子串开始的位置下标，否则则返回-1。

##### 语法

``` python
字符串序列.find(子串, 开始位置下标, 结束位置下标)
```

> 注意：开始和结束位置下标可以省略，表示在整个字符串序列中查找。

快速体验

``` python
mystr = "hello world and itcast and itheima and Python"

print(mystr.find('and'))  # 12
print(mystr.find('and', 15, 30))  # 23
print(mystr.find('ands'))  # -1
```



- index()：检测某个子串是否包含在这个字符串中，如果在返回这个子串开始的位置下标，否则则报异常。

##### 语法

``` python
字符串序列.index(子串, 开始位置下标, 结束位置下标)
```

> 注意：开始和结束位置下标可以省略，表示在整个字符串序列中查找。

快速体验

``` python
mystr = "hello world and itcast and itheima and Python"

print(mystr.index('and'))  # 12
print(mystr.index('and', 15, 30))  # 23
print(mystr.index('ands'))  # 报错
```



- rfind()： 和find()功能相同，但查找方向为<font color='red'>右侧</font>开始。
- rindex()：和index()功能相同，但查找方向为<font color='red'>右侧</font>开始。
- count()：返回某个子串在字符串中出现的次数

##### 语法

``` python
字符串序列.count(子串, 开始位置下标, 结束位置下标)
```

> 注意：开始和结束位置下标可以省略，表示在整个字符串序列中查找。

快速体验

``` python
mystr = "hello world and itcast and itheima and Python"

print(mystr.count('and'))  # 3
print(mystr.count('ands'))  # 0
print(mystr.count('and', 0, 20))  # 1
```

#### <font color='red'>修改</font>

所谓修改字符串，指的就是通过函数的形式修改字符串中的数据。

- replace()：替换

1. 语法

``` python
字符串序列.replace(旧子串, 新子串, 替换次数)
```

> 注意：替换次数如果查出子串出现次数，则替换次数为该子串出现次数。

2. 快速体验

``` python
mystr = "hello world and itcast and itheima and Python"

# 结果：hello world he itcast he itheima he Python
print(mystr.replace('and', 'he'))
# 结果：hello world he itcast he itheima he Python
print(mystr.replace('and', 'he', 10))
# 结果：hello world and itcast and itheima and Python
print(mystr)
```

> 注意：数据按照是否能直接修改分为<font color='red'>可变类型</font>和<font color='red'>不可变类型</font>两种。字符串类型的数据修改的时候不能改变原有字符串，属于不能直接修改数据的类型即是不可变类型。

- split()：按照指定字符分割字符串。

1. 语法

``` python
字符串序列.split(分割字符, num)
```

> 注意：num表示的是分割字符出现的次数，即将来返回数据个数为num+1个。

2. 快速体验

``` python
mystr = "hello world and itcast and itheima and Python"

# 结果：['hello world ', ' itcast ', ' itheima ', ' Python']
print(mystr.split('and'))
# 结果：['hello world ', ' itcast ', ' itheima and Python']
print(mystr.split('and', 2))
# 结果：['hello', 'world', 'and', 'itcast', 'and', 'itheima', 'and', 'Python']
print(mystr.split(' '))
# 结果：['hello', 'world', 'and itcast and itheima and Python']
print(mystr.split(' ', 2))
```

> 注意：如果分割字符是原有字符串中的子串，分割后则丢失该子串。

- join()：用一个字符或子串合并字符串，即是将多个字符串合并为一个新的字符串。

1. 语法

``` python
字符或子串.join(多字符串组成的序列)
```

2. 快速体验

``` python
list1 = ['chuan', 'zhi', 'bo', 'ke']
t1 = ('aa', 'b', 'cc', 'ddd')
# 结果：chuan_zhi_bo_ke
print('_'.join(list1))
# 结果：aa...b...cc...ddd
print('...'.join(t1))
```



- capitalize()：将字符串第一个字符转换成大写。

``` python
mystr = "hello world and itcast and itheima and Python"

# 结果：Hello world and itcast and itheima and python
print(mystr.capitalize())
```

> 注意：capitalize()函数转换后，只字符串第一个字符大写，其他的字符全都小写。



- title()：将字符串每个单词首字母转换成大写。

``` python
mystr = "hello world and itcast and itheima and Python"

# 结果：Hello World And Itcast And Itheima And Python
print(mystr.title())
```



- lower()：将字符串中大写转小写。

``` python
mystr = "hello world and itcast and itheima and Python"

# 结果：hello world and itcast and itheima and python
print(mystr.lower())
```



- upper()：将字符串中小写转大写。

``` python
mystr = "hello world and itcast and itheima and Python"

# 结果：HELLO WORLD AND ITCAST AND ITHEIMA AND PYTHON
print(mystr.upper())
```



- lstrip()：删除字符串左侧空白字符。

![image-20190129213453010](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190129213453010.png)



- rstrip()：删除字符串右侧空白字符。

![image-20190129213558850](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190129213558850.png)



- strip()：删除字符串两侧空白字符。

![image-20190129213637584](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190129213637584.png)



- ljust()：返回一个原字符串左对齐,并使用指定字符(默认空格)填充至对应长度 的新字符串。

1. 语法

``` python
字符串序列.ljust(长度, 填充字符)
```

2. 输出效果

![image-20190130141125560](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190130141125560.png)



- rjust()：返回一个原字符串右对齐,并使用指定字符(默认空格)填充至对应长度 的新字符串，语法和ljust()相同。
- center()：返回一个原字符串居中对齐,并使用指定字符(默认空格)填充至对应长度 的新字符串，语法和ljust()相同。

![image-20190130141442074](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190130141442074.png)



#### <font color='red'>判断</font>

所谓判断即是判断真假，返回的结果是布尔型数据类型：True 或 False。

- startswith()：检查字符串是否是以指定子串开头，是则返回 True，否则返回 False。如果设置开始和结束位置下标，则在指定范围内检查。

1. 语法

``` python
字符串序列.startswith(子串, 开始位置下标, 结束位置下标)
```

2. 快速体验

``` python
mystr = "hello world and itcast and itheima and Python   "

# 结果：True
print(mystr.startswith('hello'))

# 结果False
print(mystr.startswith('hello', 5, 20))
```



- endswith()：：检查字符串是否是以指定子串结尾，是则返回 True，否则返回 False。如果设置开始和结束位置下标，则在指定范围内检查。

1. 语法

``` python
字符串序列.endswith(子串, 开始位置下标, 结束位置下标)
```

2. 快速体验

``` python
mystr = "hello world and itcast and itheima and Python"

# 结果：True
print(mystr.endswith('Python'))

# 结果：False
print(mystr.endswith('python'))

# 结果：False
print(mystr.endswith('Python', 2, 20))
```



- isalpha()：如果字符串至少有一个字符并且所有字符都是字母则返回 True, 否则返回 False。

``` python
mystr1 = 'hello'
mystr2 = 'hello12345'

# 结果：True
print(mystr1.isalpha())

# 结果：False
print(mystr2.isalpha())
```



- isdigit()：如果字符串只包含数字则返回 True 否则返回 False。

``` python
mystr1 = 'aaa12345'
mystr2 = '12345'

# 结果： False
print(mystr1.isdigit())

# 结果：False
print(mystr2.isdigit())
```



- isalnum()：如果字符串至少有一个字符并且所有字符都是字母或数字则返 回 True,否则返回 False。

``` python
mystr1 = 'aaa12345'
mystr2 = '12345-'

# 结果：True
print(mystr1.isalnum())

# 结果：False
print(mystr2.isalnum())
```



- isspace()：如果字符串中只包含空白，则返回 True，否则返回 False。

``` python
mystr1 = '1 2 3 4 5'
mystr2 = '     '

# 结果：False
print(mystr1.isspace())

# 结果：True
print(mystr2.isspace())
```

### 2、列表

#### 格式

```python
[数据1, 数据2, 数据3, 数据4......]
```

> 列表可以一次性存储多个数据，且可以为不同数据类型。

#### 常用操作

列表的作用是一次性存储多个数据，程序员可以对这些数据进行的操作有：增、删、改、查。

##### 查找

###### 下标

``` python
name_list = ['Tom', 'Lily', 'Rose']

print(name_list[0])  # Tom
print(name_list[1])  # Lily
print(name_list[2])  # Rose
```

###### 函数

- index()：返回指定数据所在位置的下标 。

1. 语法

``` python
列表序列.index(数据, 开始位置下标, 结束位置下标)
```

2. 快速体验

``` python
name_list = ['Tom', 'Lily', 'Rose']

print(name_list.index('Lily', 0, 2))  # 1
```

> 注意：如果查找的数据不存在则报错。

- count()：统计指定数据在当前列表中出现的次数。

``` python
name_list = ['Tom', 'Lily', 'Rose']

print(name_list.count('Lily'))  # 1
```

- len()：访问列表长度，即列表中数据的个数。

``` python
name_list = ['Tom', 'Lily', 'Rose']

print(len(name_list))  # 3
```



###### 判断是否存在

- in：判断指定数据在某个列表序列，如果在返回True，否则返回False

``` python
name_list = ['Tom', 'Lily', 'Rose']

# 结果：True
print('Lily' in name_list)

# 结果：False
print('Lilys' in name_list)
```



- not in：判断指定数据不在某个列表序列，如果不在返回True，否则返回False

``` python
name_list = ['Tom', 'Lily', 'Rose']

# 结果：False
print('Lily' not in name_list)

# 结果：True
print('Lilys' not in name_list)
```

- 体验案例

需求：查找用户输入的名字是否已经存在。

``` python
name_list = ['Tom', 'Lily', 'Rose']

name = input('请输入您要搜索的名字：')

if name in name_list:
    print(f'您输入的名字是{name}, 名字已经存在')
else:
    print(f'您输入的名字是{name}, 名字不存在')
```

##### 增加

作用：增加指定数据到列表中。

- append()：列表结尾追加数据。

1. 语法

``` python
列表序列.append(数据)
```

2. 体验

``` python
name_list = ['Tom', 'Lily', 'Rose']

name_list.append('xiaoming')

# 结果：['Tom', 'Lily', 'Rose', 'xiaoming']
print(name_list)
```

![image-20190130160154636](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190130160154636.png)

> 列表追加数据的时候，直接在原列表里面追加了指定数据，即修改了原列表，故列表为可变类型数据。

3. 注意点

如果append()追加的数据是一个序列，则追加整个序列到列表

``` python
name_list = ['Tom', 'Lily', 'Rose']

name_list.append(['xiaoming', 'xiaohong'])

# 结果：['Tom', 'Lily', 'Rose', ['xiaoming', 'xiaohong']]
print(name_list)
```



- extend()：列表结尾追加数据，如果数据是一个序列，则将这个序列的数据逐一添加到列表。

1. 语法

```python
列表序列.extend(数据)
```

2. 快速体验

   2.1 单个数据

```python
name_list = ['Tom', 'Lily', 'Rose']

name_list.extend('xiaoming')

# 结果：['Tom', 'Lily', 'Rose', 'x', 'i', 'a', 'o', 'm', 'i', 'n', 'g']
print(name_list)
```

​	2.2 序列数据

```python
name_list = ['Tom', 'Lily', 'Rose']

name_list.extend(['xiaoming', 'xiaohong'])

# 结果：['Tom', 'Lily', 'Rose', 'xiaoming', 'xiaohong']
print(name_list)
```



- insert()：指定位置新增数据。

1. 语法

``` python
列表序列.insert(位置下标, 数据)
```

2. 快速体验

``` python
name_list = ['Tom', 'Lily', 'Rose']

name_list.insert(1, 'xiaoming')

# 结果：['Tom', 'xiaoming', 'Lily', 'Rose']
print(name_list)
```

##### 删除

- del

1. 语法

``` python
del 目标
```

2. 快速体验

   2.1 删除列表

``` python
name_list = ['Tom', 'Lily', 'Rose']

# 结果：报错提示：name 'name_list' is not defined
del name_list
print(name_list)
```

​	2.2 删除指定数据

``` python
name_list = ['Tom', 'Lily', 'Rose']

del name_list[0]

# 结果：['Lily', 'Rose']
print(name_list)
```



- pop()：删除指定下标的数据(默认为最后一个)，并返回该数据。

1. 语法

``` python
列表序列.pop(下标)
```

2. 快速体验

``` python
name_list = ['Tom', 'Lily', 'Rose']

del_name = name_list.pop(1)

# 结果：Lily
print(del_name)

# 结果：['Tom', 'Rose']
print(name_list)
```



- remove()：移除列表中某个数据的第一个匹配项。

1. 语法

``` python
列表序列.remove(数据)
```

2. 快速体验

``` python
name_list = ['Tom', 'Lily', 'Rose']

name_list.remove('Rose')

# 结果：['Tom', 'Lily']
print(name_list)
```



- clear()：清空列表

``` python
name_list = ['Tom', 'Lily', 'Rose']

name_list.clear()
print(name_list) # 结果： []
```

##### 修改

- 修改指定下标数据

``` python
name_list = ['Tom', 'Lily', 'Rose']

name_list[0] = 'aaa'

# 结果：['aaa', 'Lily', 'Rose']
print(name_list)
```



- 逆置：reverse()

``` python
num_list = [1, 5, 2, 3, 6, 8]

num_list.reverse()

# 结果：[8, 6, 3, 2, 5, 1]
print(num_list)
```



- 排序：sort()

1. 语法

``` python
列表序列.sort( key=None, reverse=False)
```

> 注意：reverse表示排序规则，**reverse = True** 降序， **reverse = False** 升序（默认）

2. 快速体验

``` python
num_list = [1, 5, 2, 3, 6, 8]

num_list.sort()

# 结果：[1, 2, 3, 5, 6, 8]
print(num_list)
```

##### 复制

函数：copy()

``` python
name_list = ['Tom', 'Lily', 'Rose']

name_li2 = name_list.copy()

# 结果：['Tom', 'Lily', 'Rose']
print(name_li2)
```

#### 循环遍历

#### while

需求：依次打印列表中的各个数据。

- 代码

``` python
name_list = ['Tom', 'Lily', 'Rose']

i = 0
while i < len(name_list):
    print(name_list[i])
    i += 1
```

- 执行结果

![image-20190130164205143](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190130164205143.png)

#### for

- 代码

``` python
name_list = ['Tom', 'Lily', 'Rose']

for i in name_list:
    print(i)
```



- 执行结果

![image-20190130164227739](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190130164227739.png)

#### 列表嵌套

所谓列表嵌套指的就是一个列表里面包含了其他的子列表。

应用场景：要存储班级一、二、三三个班级学生姓名，且每个班级的学生姓名在一个列表。

``` python
name_list = [['小明', '小红', '小绿'], ['Tom', 'Lily', 'Rose'], ['张三', '李四', '王五']]
```

> 思考： 如何查找到数据"李四"？

``` python
# 第一步：按下标查找到李四所在的列表
print(name_list[2])

# 第二步：从李四所在的列表里面，再按下标找到数据李四
print(name_list[2][1])
```

### 3、元祖

#### 格式

```python
# 多个数据元组
t1 = (10, 20, 30)

# 单个数据元组
t2 = (10,)
```

#### 常见操作

元组数据不支持修改，只支持查找，具体如下：

- 按下标查找数据

``` python
tuple1 = ('aa', 'bb', 'cc', 'bb')
print(tuple1[0])  # aa
```



- index()：查找某个数据，如果数据存在返回对应的下标，否则报错，语法和列表、字符串的index方法相同。

``` python
tuple1 = ('aa', 'bb', 'cc', 'bb')
print(tuple1.index('aa'))  # 0
```



- count()：统计某个数据在当前元组出现的次数。

``` python
tuple1 = ('aa', 'bb', 'cc', 'bb')
print(tuple1.count('bb'))  # 2
```



- len()：统计元组中数据的个数。

``` python
tuple1 = ('aa', 'bb', 'cc', 'bb')
print(len(tuple1))  # 4
```

> 注意：元组内的直接数据如果修改则立即报错

``` python
tuple1 = ('aa', 'bb', 'cc', 'bb')
tuple1[0] = 'aaa'
```

> 但是如果元组里面有列表，修改列表里面的数据则是支持的，故自觉很重要。

``` python
tuple2 = (10, 20, ['aa', 'bb', 'cc'], 50, 30)
print(tuple2[2])  # 访问到列表

# 结果：(10, 20, ['aaaaa', 'bb', 'cc'], 50, 30)
tuple2[2][0] = 'aaaaa'
print(tuple2)
```

### 4、字典

#### 格式

字典特点：

- 符号为==大括号==
- 数据为==键值对==形式出现
- 各个键值对之间用==逗号==隔开

``` python
# 有数据字典
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}

# 空字典
dict2 = {}

dict3 = dict()
```

> 注意：一般称冒号前面的为键(key)，简称k；冒号后面的为值(value)，简称v。

#### 常见操作

##### 增

写法：字典序列[key] = 值

> 注意：如果key存在则修改这个key对应的值；如果key不存在则新增此键值对。

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}

dict1['id'] = 110

# {'name': 'Rose', 'age': 20, 'gender': '男', 'id': 110}
print(dict1)
```

> 注意：字典为可变类型。

##### 删

-  del：删除字典或删除字典中指定键值对。

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}

del dict1['gender']
# 结果：{'name': 'Tom', 'age': 20}
print(dict1)
```

- clear()：清空字典

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}

dict1.clear()
print(dict1)  # {}
```

##### 改

写法：字典序列[key] = 值

> 注意：如果key存在则修改这个key对应的值 ；如果key不存在则新增此键值对。

##### 查

###### key值查找

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
print(dict1['name'])  # Tom
print(dict1['id'])  # 报错
```

> 如果当前查找的key存在，则返回对应的值；否则则报错。

###### get()

- 语法

``` python
字典序列.get(key, 默认值)
```

> 注意：如果当前查找的key不存在则返回第二个参数(默认值)，如果省略第二个参数，则返回None。

- 快速体验

``` python 
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
print(dict1.get('name'))  # Tom
print(dict1.get('id', 110))  # 110
print(dict1.get('id'))  # None
```

###### keys()

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
print(dict1.keys())  # dict_keys(['name', 'age', 'gender'])
```

###### values()

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
print(dict1.values())  # dict_values(['Tom', 20, '男'])
```

###### items()

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
print(dict1.items())  # dict_items([('name', 'Tom'), ('age', 20), ('gender', '男')])
```

#### 字典的遍历

##### 遍历字典的key

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
for key in dict1.keys():
    print(key)
```

![image-20190212103905553](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190212103905553.png)



##### 遍历字典的value

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
for value in dict1.values():
    print(value)
```

![image-20190212103957777](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190212103957777.png)



#####  遍历字典的元素

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
for item in dict1.items():
    print(item)
```

![image-20190212104046564](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190212104046564.png)



##### 遍历字典的键值对

``` python
dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
for key, value in dict1.items():
    print(f'{key} = {value}')
```

![image-20190212104223143](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190212104223143.png)

### 5、集合

#### 格式

创建集合使用`{}`或`set()`， 但是如果要创建空集合只能使用`set()`，因为`{}`用来创建空字典。

``` python
s1 = {10, 20, 30, 40, 50}
print(s1)

s2 = {10, 30, 20, 10, 30, 40, 30, 50}
print(s2)

s3 = set('abcdefg')
print(s3)

s4 = set()
print(type(s4))  # set

s5 = {}
print(type(s5))  # dict
```

![image-20190318104620690](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190318104620690.png)

> 特点：
>
> 1. 集合可以去掉重复数据；
> 2. 集合数据是无序的，故不支持下标

#### 常见操作

##### 增

- add()

``` python
s1 = {10, 20}
s1.add(100)
s1.add(10)
print(s1)  # {100, 10, 20}
```

> 因为集合有去重功能，所以，当向集合内追加的数据是当前集合已有数据的话，则不进行任何操作。

- update(), 追加的数据是序列。

``` python
s1 = {10, 20}
# s1.update(100)  # 报错
s1.update([100, 200])
s1.update('abc')
print(s1)
```

![image-20190318121424514](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190318121424514.png)

##### 删

- remove()，删除集合中的指定数据，如果数据不存在则报错。

``` python
s1 = {10, 20}

s1.remove(10)
print(s1)

s1.remove(10)  # 报错
print(s1)
```



- discard()，删除集合中的指定数据，如果数据不存在也不会报错。

``` python
s1 = {10, 20}

s1.discard(10)
print(s1)

s1.discard(10)
print(s1)
```



- pop()，随机删除集合中的某个数据，并返回这个数据。

``` python
s1 = {10, 20, 30, 40, 50}

del_num = s1.pop()
print(del_num)
print(s1)
```

##### 查

- in：判断数据在集合序列
- not in：判断数据不在集合序列

``` python
s1 = {10, 20, 30, 40, 50}

print(10 in s1)
print(10 not in s1)
```

## 公共操作

### 运算符

| 运算符 |      描述      |      支持的容器类型      |
| :----: | :------------: | :----------------------: |
|   +    |      合并      |    字符串、列表、元组    |
|   *    |      复制      |    字符串、列表、元组    |
|   in   |  元素是否存在  | 字符串、列表、元组、字典 |
| not in | 元素是否不存在 | 字符串、列表、元组、字典 |

####  +

``` python
# 1. 字符串 
str1 = 'aa'
str2 = 'bb'
str3 = str1 + str2
print(str3)  # aabb


# 2. 列表 
list1 = [1, 2]
list2 = [10, 20]
list3 = list1 + list2
print(list3)  # [1, 2, 10, 20]

# 3. 元组 
t1 = (1, 2)
t2 = (10, 20)
t3 = t1 + t2
print(t3)  # (10, 20, 100, 200)
```

#### *

``` python
# 1. 字符串
print('-' * 10)  # ----------

# 2. 列表
list1 = ['hello']
print(list1 * 4)  # ['hello', 'hello', 'hello', 'hello']

# 3. 元组
t1 = ('world',)
print(t1 * 4)  # ('world', 'world', 'world', 'world')
```

#### in或not in

``` python
# 1. 字符串
print('a' in 'abcd')  # True
print('a' not in 'abcd')  # False

# 2. 列表
list1 = ['a', 'b', 'c', 'd']
print('a' in list1)  # True
print('a' not in list1)  # False

# 3. 元组
t1 = ('a', 'b', 'c', 'd')
print('aa' in t1)  # False
print('aa' not in t1)  # True
```

### 公共方法

| 函数                    | 描述                                                         |
| ----------------------- | ------------------------------------------------------------ |
| len()                   | 计算容器中元素个数                                           |
| del 或 del()            | 删除                                                         |
| max()                   | 返回容器中元素最大值                                         |
| min()                   | 返回容器中元素最小值                                         |
| range(start, end, step) | 生成从start到end的数字，步长为 step，供for循环使用           |
| enumerate()             | 函数用于将一个可遍历的数据对象(如列表、元组或字符串)组合为一个索引序列，同时列出数据和数据下标，一般用在 for 循环当中。 |

#### len()

``` python
# 1. 字符串
str1 = 'abcdefg'
print(len(str1))  # 7

# 2. 列表
list1 = [10, 20, 30, 40]
print(len(list1))  # 4

# 3. 元组
t1 = (10, 20, 30, 40, 50)
print(len(t1))  # 5

# 4. 集合
s1 = {10, 20, 30}
print(len(s1))  # 3

# 5. 字典
dict1 = {'name': 'Rose', 'age': 18}
print(len(dict1))  # 2
```

#### del()

``` python
# 1. 字符串
str1 = 'abcdefg'
del str1
print(str1)

# 2. 列表
list1 = [10, 20, 30, 40]
del(list1[0])
print(list1)  # [20, 30, 40]
```

#### max()

``` python
# 1. 字符串
str1 = 'abcdefg'
print(max(str1))  # g

# 2. 列表
list1 = [10, 20, 30, 40]
print(max(list1))  # 40
```

#### min()

``` python
# 1. 字符串
str1 = 'abcdefg'
print(min(str1))  # a

# 2. 列表
list1 = [10, 20, 30, 40]
print(min(list1))  # 10
```

#### range()

``` python
# 1 2 3 4 5 6 7 8 9
for i in range(1, 10, 1):
    print(i)

# 1 3 5 7 9
for i in range(1, 10, 2):
    print(i)

# 0 1 2 3 4 5 6 7 8 9
for i in range(10):
    print(i)
```

> 注意：range()生成的序列不包含end数字。

#### enumerate()

- 语法

``` python
enumerate(可遍历对象, start=0)
```

> 注意：start参数用来设置遍历数据的下标的起始值，默认为0。

- 快速体验

``` python
list1 = ['a', 'b', 'c', 'd', 'e']

for i in enumerate(list1):
    print(i)

for index, char in enumerate(list1, start=1):
    print(f'下标是{index}, 对应的字符是{char}')
```

![image-20190213115919040](python%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.assets/image-20190213115919040.png)

### 容器类型转换

#### tuple()

作用：将某个序列转换成元组

``` python
list1 = [10, 20, 30, 40, 50, 20]
s1 = {100, 200, 300, 400, 500}

print(tuple(list1))
print(tuple(s1))
```



#### list()

作用：将某个序列转换成列表

``` python
t1 = ('a', 'b', 'c', 'd', 'e')
s1 = {100, 200, 300, 400, 500}

print(list(t1))
print(list(s1))
```



#### set()

作用：将某个序列转换成集合

``` python
list1 = [10, 20, 30, 40, 50, 20]
t1 = ('a', 'b', 'c', 'd', 'e')

print(set(list1))
print(set(t1))
```

> 注意：

   	1. 集合可以快速完成列表去重
   	2. 集合不支持下标

## 推导式

### 列表推导式

#### 1.1 快速体验

需求：创建一个0-10的列表。

- while循环实现

``` python
# 1. 准备一个空列表
list1 = []

# 2. 书写循环，依次追加数字到空列表list1中
i = 0
while i < 10:
    list1.append(i)
    i += 1

print(list1)
```

- for循环实现

``` python
list1 = []
for i in range(10):
    list1.append(i)

print(list1)
```

- 列表推导式实现

``` python 
list1 = [i for i in range(10)]
print(list1)
```

#### 1.2 带if的列表推导式

需求：创建0-10的偶数列表

- 方法一：range()步长实现

``` python
list1 = [i for i in range(0, 10, 2)]
print(list1)
```

- 方法二：if实现

``` python
list1 = [i for i in range(10) if i % 2 == 0]
print(list1)
```

#### 1.3 多个for循环实现列表推导式

需求：创建列表如下：

``` html
[(1, 0), (1, 1), (1, 2), (2, 0), (2, 1), (2, 2)]
```

- 代码如下：

``` python
list1 = [(i, j) for i in range(1, 3) for j in range(3)]
print(list1)
```

### 字典推导式

思考：如果有如下两个列表：

``` python
list1 = ['name', 'age', 'gender']
list2 = ['Tom', 20, 'man']
```

如何快速合并为一个字典？

答：字典推导式

字典推导式作用：快速合并列表为字典或提取字典中目标数据。

#### 2.1 快速体验

1. 创建一个字典：字典key是1-5数字，value是这个数字的2次方。

``` python
dict1 = {i: i**2 for i in range(1, 5)}
print(dict1)  # {1: 1, 2: 4, 3: 9, 4: 16}
```



2. 将两个列表合并为一个字典

``` python 
list1 = ['name', 'age', 'gender']
list2 = ['Tom', 20, 'man']

dict1 = {list1[i]: list2[i] for i in range(len(list1))}
print(dict1)
```

3. 提取字典中目标数据

``` python
counts = {'MBP': 268, 'HP': 125, 'DELL': 201, 'Lenovo': 199, 'acer': 99}

# 需求：提取上述电脑数量大于等于200的字典数据
count1 = {key: value for key, value in counts.items() if value >= 200}
print(count1)  # {'MBP': 268, 'DELL': 201}
```

### 集合推导式

需求：创建一个集合，数据为下方列表的2次方。

``` python
list1 = [1, 1, 2]
```

代码如下：

``` python
list1 = [1, 1, 2]
set1 = {i ** 2 for i in list1}
print(set1)  # {1, 4}
```

> 注意：集合有数据去重功能。

## 函数

