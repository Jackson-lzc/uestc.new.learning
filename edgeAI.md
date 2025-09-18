# ***嵌入式AI学习***
## 9.9Markdown
学习了一天markdown，感觉不如自己上手写这篇文章，不得不逼自己去写一些语法，背诵起来更牢了（ps:以后#与标题间一定打空格）。但在vscode上转为pdf，还有这个导入图片不显示真的挺麻烦的。
## 9.10人工智能，机器学习，深度学习的区别
1.在我的映像里一直把这三个归为这样的一个关系：人工智能是通过机器学习，深度学习创造出来的，但实际呢，如Xmind所示吧![区别]("C:\Users\hp\Desktop\edgeAI\三个的区别.png" "区别")
ps：机器学习还有很多未解之谜，嵌入式AI：顾名思义，即嵌入式，与AI，前面研究硬件嵌入，后面研究人工智能，相结合而成。

2.嵌入式AI发展方向：（询问了下Deepseek）嵌入式AI，本质上是让我们身边的事物充满“智能”，比如家里用的智能汽车，小爱音响，将AI嵌入硬件之中发挥作用，有芯片与硬件，算法与模型，开发模式与工具，应用场景等领域。

嵌入式AI无需依赖云端服务器（应该就是网络啥的），实现本地化运行，可以保护用户隐私，同时由于嵌入的机械一般体型较小，嵌入式AI具有低功耗与轻量化的特点。对于延迟敏感地场景，要求算法在毫秒级，此时网络可就用不了了，需要嵌入式AI

应用也很广泛，就像我之前提到的，小爱音响，其实就是智能硬件与消费电子的一种（人家总结的好到位）；同时还可以用于工业与智能制造，比如工业机器人；还可以用于汽车与自动驾驶，比如特斯拉？；最后还可以用于医疗与健康，比如推测癌症？（吴恩达课程）

未来趋势可以进行类脑芯片研发（从芯片根本上改造），复杂任务调用云端算力(就是遇到困难时连网)，还可以在线学习(这有点强大了，以后带它去上课)。

我自己的想法：嵌入式AI就是把智能赋予各种机器，小到音响洗碗机，大到工业机器，都有嵌入式AI的影子，我们创造了人式的机器。未来所有物体都可以拥有自己的那一套“想法”，只要我们愿意投入功夫与足够的精力去完成。
##9.10配置好python
什么都不会，上b站！

一个小时把conda装好了，准备学习安装各个库

图书馆要关门了明天再装
## 9.11安装anaconda+学习python
1.学习了虚拟环境的配置，并配置了python=3.11版本，并用prompt安装了所用的几个库，由于notebook安装失败了在vscode上安装了插件，也可以用。
matplotlib  3.10.6
pandas      2.3.2
python      3.11.13
torch       2.8.0（pytorch与torch一样吗）
notebook    7.4.5
[version]("C:\Users\hp\Desktop\edgeAI\version.png" "version")

顺便下载了git，创建了github账号
2.学习python:第一步先打出Hello world
数字类型一共7种，数字，字符串，布尔，列表，元组，集合，字典
数字有浮点，整型，布尔，复数（这个后面是j，或者complex（a，b）表示），其中bool是int的子型？！？，用type（）来看形式，True False可以与数字想加
/相除得浮点数，//得整数（好像是向下取整），**乘方，%取模
对于字符串，也是第一个字符用0代表，\n转义，前面加r取消转移,注意索引时【0：9】才是123456789的整个打印，【1，9】会省略1，如果打印末尾的话用list[0：]，不需要写数字

## 9.12 pythom语言学习+吴恩达课程
1.列表：特别注意最后一个元素不会被取到，同时python列表支持不同的数据类型，可以嵌套

2.截取步长：如list[1：4：2]，即从第一位元素开始，走两步，到第三个元素，即打印1，3元素，当第三位为-2时反向，记录一下实例：

inputWords[-1::-1] 有三个参数
    第一个参数 -1 表示最后一个元素
    第二个参数为空，表示移动到列表末尾
    第三个参数为步长，-1 表示逆向，最后达到反向的效果
    索引时注意：
    str[:]表示所有，str[:3]，引用前三个，str[1：4]引用下标为1~3的字符

3.元组：与列表相似，但元素不能修改，写在小括号里用逗号隔开，记录实例：
    tup1 = ()    # 空元组
    tup2 = (20,) # 一个元素，需要在元素后添加逗号

4.集合：用{}来创建用于存储唯一的元素，但空集用()，与数学中的集合基本一样，运算也一样。也可以使用 set() 函数创建集合

5.字典：字典是一种映射类型，字典用 { } 标识，它是一个无序的 键(key) : 值(value) 的集合（真的不知道字典的用途是什么qwq）
记下一个例子：tinydict = {'name': 'runoob','code':1, 'site': 'www.runoob.com'}，这是一种定义方式。

6.bytes：一种二进制类型，bytes 类型中的元素是整数值（0 到 255 之间的整数），常用于处理二进制数据，比如图像文件、音频文件、视频文件等等（开眼界了），也可以使用 bytes() 函数将其他类型的对象转换为 bytes 类型。bytes() 函数的第一个参数是要转换的对象，第二个参数是编码方式，如果省略第二个参数，则默认使用 UTF-8 编码。
最常见的方式是使用 b 前缀，比如x=b“hello”，x就变成了一个byte类型的字符。
必须记下一个例子：x = bytes("hello", encoding="utf-8")

7.数据类型转化：
1）隐式类型转换 - 自动完成，显式类型转换 - 需要使用类型函数来转换，主要应该学习显式（毕竟数据转换挺重要的）

2）隐式类型转化：较低数据类型（比如整数）就会转换为较高数据类型（比如浮点数），但整型与字符串不能通过隐式类型转化计算

3）显式类型转化：float() 强制转换为浮点型，str() 强制转换为字符串类型 ，chr()整数转化为字符，ord()字符转化为整数,hex()转化为16进制，oct()转化为8进制

8.注释：
多行注释：‘‘‘，或者”””，但不可以嵌套
单行注释：#，推荐使用，很方便

9.运算符：
普通的运算符与c语言一模一样，但记一下赋值运算符(因为没有学过)
c = a + b 将 a + b 的运算结果赋值为 c
c += a 等效于 c = c + a
c -= a 等效于 c = c - a
c *= a 等效于 c = c * a
c /= a 等效于 c = c / a（除法）
c %= a 等效于 c = c % a（取模）
c **= a 等效于 c = c ** a（幂乘）
c //= a 等效于 c = c // a（取整除）
:=	海象运算符，这个运算符的主要目的是在表达式中同时进行赋值和返回赋值的值。（很good）记下一个例子：
    if (n := 10) > 5:：这是使用海象运算符（:=）的写法。海象运算符在表达式中进行赋值操作。
    (n := 10)：将变量 n 赋值为 10，同时返回这个赋值结果。

10.位运算符：
没办法，记吧
&	按位与运算符：参与运算的两个值,如果两个相应位都为1,则该位的结果为1,否则为0	
|	按位或运算符：只要对应的二个二进位有一个为1时，结果位就为1。
^	按位异或运算符：当两个数位置对应的二进位相异时，结果为1	
~	按位取反运算符：对数据的每个二进制位取反,即把1变为0,把0变为1。~x 类似于 -x-1
<<	左移动运算符：运算数的各二进位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补0。	
/     >>右移动运算符：把">>"左边的运算数的各二进位全部右移若干位，">>"右边的数指定移动的位数
ps：这个位运算在实际中应该不常用吧（感觉好烧脑）

11.逻辑运算符：
and，x and y ,如果 x 为 False，x and y 返回 x 的值，否则返回 y 的计算值。
or,  x or y,如果 x 是 True，它返回 x 的值，否则它返回 y 的计算值。
not, not x,如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。

12.成员运算符：
in	//如果在指定的序列中找到值返回 True，否则返回 False。
not in	//如果在指定的序列中没有找到值返回 True，否则返回 False。
比如： a in list

13.身份运算符：（截取python3的话记忆吧）
is	//is 是判断两个标识符是不是引用自一个对象	x is y, 类似 id(x) == id(y) , 如果引用的是同一个对象则返回 True，否则返回 False
is not	//is not 是判断两个标识符是不是引用自不同对象	x is not y ， 类似 id(x) != id(y)。如果引用的不是同一个对象则返回结果 True，否则返回 False。
14.数字
一些公式(ctrlC了)记忆吧没办法，但给出用的场景

abs(x)	返回数字的绝对值，如abs(-10) 返回 10   //挺常用的
ceil(x)	返回数字的上入整数，如math.ceil(4.1) 返回 5  //感觉没啥用
exp(x)	返回e的x次幂(ex),如math.exp(1) 返回2.718281828459045  //没啥用
fabs(x)	以浮点数形式返回数字的绝对值，如math.fabs(-10) 返回10.0  //和abs感觉差不多，不如都用fabs
floor(x)	返回数字的下舍整数，如math.floor(4.9)返回 4  //呃呃呃，不知道干嘛的
log(x)	如math.log(math.e)返回1.0,math.log(100,10)返回2.0  //看出来是log运算了
log10(x)	返回以10为基数的x的对数，如math.log10(100)返回 2.0  //看出来是lg
max(x1, x2,...)	返回给定参数的最大值，参数可以为序列。  //感觉非常有用
min(x1, x2,...)	返回给定参数的最小值，参数可以为序列。  //感觉也非常有用
modf(x)	返回x的整数部分与小数部分，两部分的数值符号与x相同，整数部分以浮点型表示。  //怎么说感觉有点想分离整数
pow(x, y)	x**y 运算后的值。  //直接打不好吗
round(x [,n])返回浮点数 x 的四舍五入值，如给出 n 值，则代表舍入到小数点后的位数。其实准确的说是保留值将保留到离上一位更近的一端。//保留
sqrt(x)	返回数字x的平方根。  //取根运算，那取三次根咋办呢

当资料查阅

随机数：
choice(seq)	从序列的元素中随机挑选一个元素，比如random.choice(range(10))，从0到9中随机挑选一个整数。
randrange ([start,] stop [,step])	从指定范围内，按指定基数递增的集合中获取一个随机数，基数默认值为 1 //没看懂
random()	随机生成下一个实数，它在[0,1]范围内。//@计算器
seed([x])	改变随机数生成器的种子seed。如果你不了解其原理，你不必特别去设定seed，Python会帮你选择seed。//好的
shuffle(lst)	将序列的所有元素随机排序//乱序了
uniform(x, y)	随机生成下一个实数，它在[x,y]范围内。//感觉非常有用

三角函数：
acos(x)	返回x的反余弦弧度值。
asin(x)	返回x的反正弦弧度值。
atan(x)	返回x的反正切弧度值。
atan2(y, x)	返回给定的 X 及 Y 坐标值的反正切值。
cos(x)	返回x的弧度的余弦值。
hypot(x, y)	返回欧几里德范数 sqrt(x*x + y*y)。
sin(x)	返回的x弧度的正弦值。
tan(x)	返回x弧度的正切值。
degrees(x)	将弧度转换为角度,如degrees(math.pi/2) ， 返回90.0
radians(x)	将角度转换为弧度
三角函数在机器学习这方面作用不是很大
常量pi和e也要记住

15.转义字符：在需要在字符中使用特殊字符时，python 用反斜杠 \ 转义字符。
\ (在行尾时)	续行符	
\\ 反斜杠符号	
\'	单引号	
\"	双引号	
\a	响铃执行后电脑有响声。
\b	退格(Backspace)	
Hello World!
\000	空	
\n	换行	
\v	纵向制表符	
print("Hello \v World!")
Hello 
       World!
\t	横向制表符	
print("Hello \t World!")
Hello      World!
\r	回车，将 \r 后面的内容移到字符串开头，并逐一替换开头部分的字符，直至将 \r 后面的内容完全替换完成。	
print('google runoob taobao\r123456')
123456 runoob taobao
\f	换页	
print("Hello \f World!")
Hello 
       World!
ps：由于本人c语言不是很懂，所以把横向纵向制表符号给记录下来了

16.字符串格式化
诶呀，就是c语言的%d，%f啥的，语法一模一样

### 吴恩达机器学习换个脑子：图书馆怎么全**是人，都不睡觉的吗（生气
1.监督学习概述：学习X到Y的映射，或输入到输出的算法，我们给定输入X的正确输出是Y，然后算法会学习“正确答案”，最终在没有输出标签的情况下，在监督学习之后，给出期望结果（好神奇）。这个可以应用于广告推送：比如分析用户在什么类型广告上停留最久，最感兴趣，判断你是否会点击。机器在分析XY的输入输出之中，会给出最佳预测（比如回归预测，算出拟合曲线）。

但这并不只限于回归预测，还有分析数据集的分析，指离散分析，分类算法预测（判断图片是狗还是猫猫），后者预测更准
当我们给出的X到Y映射种类越多时，预测会越准确（显而易见）

2.无监督学习（其实是9.13号，暂时放这里吧）
与监督学习相比，只有输入X，我们不要求机器输出正确答案Y，但在整个数据中发现了一些结构或者模式。
比如说聚类计算，将数据放入不同的组中，比如说相似文章推送，但我们没有告诉机器哪些应该放一组，应该分几组，但机器会自动分标签
再比如异常检查，在金融中有应用
再比如学习降维，可以将大数据集压缩为小数据集

## 9.13线性回归模型+python学习
1.列表：
列表可以从前面索引，第一位为0，也可以从后面索引，第一位为-1，第二位为-2，之前好像记过一些
append用来加入数据，比如list1.append（''）然后默认加在最后一位，更换元素比如更换第三个元素要用list[2]=，因为序号从0，1，2开始标
del删除与更新是一个道理

如果要进行脚本操作与正常的差不多，就是*4表示重复，+表示相加，还有for x in...表示迭代
此外列表还支持嵌套

1）	list.append(obj)
在列表末尾添加新的对象
2）	list.count(obj)
统计某个元素在列表中出现的次数
3）	list.extend(seq)
在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表）
4）	list.index(obj)
从列表中找出某个值第一个匹配项的索引位置
5）	list.insert(index, obj)
将对象插入列表
6）	list.pop([index=-1])
移除列表中的一个元素（默认最后一个元素），并且返回该元素的值
7）	list.remove(obj)
移除列表中某个值的第一个匹配项
8）	list.reverse()
反向列表中元素
9）	list.sort( key=None, reverse=False)
对原列表进行排序
10）	list.clear()
清空列表
11）	list.copy()
复制列表
（一些常用公式）

2.元组
元组中元素不可修改（非常重要），所以不能用append，并且在使用del时只能删除整个元组，其余与列表非常相似，元组也用圆括号

3.字典
（最不熟悉的一种，所以多加记笔记）字典是另一种可变容器模型，且可存储任意类型对象。字典的每个键值 key=>value 对用冒号 : 分割，每个对之间用逗号(,)分割，整个字典包括在花括号 {} 中 ,格式如下所示d = {key1 : value1, key2 : value2, key3 : value3 }
其中见键不可变，可以使用内部函数dict来创建字典

""访问时将键放入方括号中""（非常重要！）

更新与修改字典中的值与列表相似。
键必须不可变，所以可以用数字，字符串或元组充当，而用列表就不行。
1）	dict.clear()
删除字典内所有元素
2）	dict.copy()
返回一个字典的浅复制
3）	dict.fromkeys()
创建一个新字典，以序列seq中元素做字典的键，val为字典所有键对应的初始值
4）	dict.get(key, default=None)
返回指定键的值，如果键不在字典中返回 default 设置的默认值
5）	key in dict
如果键在字典dict里返回true，否则返回false
6）	dict.items()
以列表返回一个视图对象
7）	dict.keys()
返回一个视图对象
8）	dict.setdefault(key, default=None)
和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default
9）	dict.update(dict2)
把字典dict2的键/值对更新到dict里
10）	dict.values()
返回一个视图对象
11）	dict.pop(key[,default])
删除字典 key（键）所对应的值，返回被删除的值。
12）	dict.popitem()
返回并删除字典中的最后一对键和值
（一些不知道怎么用的公式）

4.集合：
s.add( x )用来添加元素，s.update( x )，也可以添加元素
s.remove( x )移除元素，s.discard( x )，也可以移除元素
s.pop() 随机删除一个元素，原理是先随机排序，再删除最左边的那个元素
len(s)，用来计算集合中元素个数
s.clear()，清空集合
x in s 判断元素x是否在集合s中

5.终于到了干货条件控制了，先ctrl v一个例子
if condition_1:
    statement_block_1
elif condition_2:
    statement_block_2
else:
    statement_block_3
如果 "condition_1" 为 True 将执行 "statement_block_1" 块语句
如果 "condition_1" 为False，将判断 "condition_2"
如果"condition_2" 为 True 将执行 "statement_block_2" 块语句
如果 "condition_2" 为False，将执行"statement_block_3"块语句
值得注意的是，必须加上：，并且使用缩进来分割语句块
还可以有嵌套if哦
对于3.10版本以后的（我用的是3.11，可以有match case语句）
match 后的对象会依次与 case 后的内容进行匹配，如果匹配成功，则执行匹配到的表达式，否则直接跳过，_ 可以匹配一切。

语法格式如下：

match subject:
    case <pattern_1>:
        <action_1>
    case <pattern_2>:
        <action_2>
    case <pattern_3>:
        <action_3>
    case _:
        <action_wildcard>

6.干货：循环
while for循环基本和c语言差不多，同时可以通过while来实现无限循环，就是while后面的条件永远不为假，然后用ctrl c 退出循环
while后面还可以加else语句，当while后面语句不为真时执行

for语句：for 啥 in 啥：加个陈述，然后else：加个陈述，用于在循环后执行某个操作
遇到break就跳出循环，如果遇到continue就继续，但跳过输出

range函数：range（开始，结束，步长），其中不包含结束的值，要到结束值把后面改成-1

pass 不做任何事情，一般用做占位语句。

7.python编程第一步！（好耶！）
python推导式（什么鬼东西），先学个基础的吧：列表的推导式[表达式 for 变量 in 列表] 或者[表达式 for 变量 in 列表 if 条件]，先循环，在判断，最后把表达式组成一个新的列表。
本质上感觉就是一种简化代码行数的方法，但用多了自己会看不懂。

8.迭代器与生成器（越来越看不懂了）
迭代器有两个基本的方法：iter() 和 next()
创建一个列表（可迭代对象）
my_list = [1, 2, 3]
用 iter() 函数把它变成一个迭代器
my_iterator = iter(my_list)

用 next() 函数从迭代器里一个一个取值
print(next(my_iterator)) # 输出：1
print(next(my_iterator)) # 输出：2
print(next(my_iterator)) # 输出：3
print(next(my_iterator)) # 报错！因为已经没有数据了

这个deepseek给出的例子太好了

生成器：
在 Python 中，使用了 yield 的函数被称为生成器（generator）。yield 是一个关键字，用于定义生成器函数，生成器函数是一种特殊的函数，可以在迭代过程中逐步产生值，而不是一次性返回所有结果。
跟普通函数不同的是，生成器是一个返回迭代器的函数，只能用于迭代操作，更简单点理解生成器就是一个迭代器。
当在生成器函数中使用 yield 语句时，函数的执行将会暂停，并将 yield 后面的表达式作为当前迭代的值返回。
然后，每次调用生成器的 next() 方法或使用 for 循环进行迭代时，函数会从上次暂停的地方继续执行，直到再次遇到 yield 语句。这样，生成器函数可以逐步产生值，而不需要一次性计算并返回所有结果。
调用一个生成器函数，返回的是一个迭代器对象。

deepseek在这方面就是yyds

def countdown(n):
    while n > 0:
        yield n
        n -= 1
 
创建生成器对象
generator = countdown(5)
 
通过迭代生成器获取值
print(next(generator))  # 输出: 5
print(next(generator))  # 输出: 4
print(next(generator))  # 输出: 3
 
使用 for 循环迭代生成器
for value in generator:
    print(value)  # 输出: 2 1

### 回归模型&分类模型
1.回归模型：给出一条直线与数据集吻合（与高中时候的线性方程相似），属于一种监督学习，并且用来预测数据，因为已经给出了正确答案。
回归模型一般会有上万个输出，同时需要有个**训练集**，用来训练数据，而要预测的数据不在数据集中。
验证集即我们给定正确的x-y的映射，用于调整参数和模型选择。而测试集仅用于最总评估，不用作参量调整和模型训练，是衡量泛化能力的
过拟合即模型在训练集上表现很好，但测试集非常糟糕

对于这个训练集，我们用x表示输入变量(输入特征)，y为目标变量(输出变量)，一个（x，y）是一个训练样本，用m表示训练样本的总数，用上标表示不同训练样本。我们将数据集输入到监督学习算法中，然后这个算法会生成一些函数f，f的职责是为了接受新的输入集并输出一个估计值或者预测值(y-hat)，这个f就是模型。

难点：f的生成，在线性回归中f(x)=wx+b，线性回归比较简单（先比较与曲线），有单变量线性和多变量线性

成本函数（代价函数）：J（w，b）=1/2m ∑（y-y^）**2，和高中残差的实质是一样的，也有其他的成本函数，但这种是用最小二乘法来确定J（w）的最小值
一个以x为自变量，一个以w为自变量，成本函数是一条抛物线，我们应该选择顶点作为w的值，此时J（w）最小。

在三维弓形曲面图中，三个变量，w，b，J，形成一个碗型的3D图，同样的取纵轴最低的点

## 9.14 python学习＋吴恩达课程

1.with语句
with expression [as variable]:
expression 返回一个支持上下文管理协议的对象
as variable 是可选的，用于将表达式结果赋值给变量
代码块执行完毕后，自动调用清理方法

记下一个例子with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
但是真的不会创立上下文管理器

2。函数
def 函数名（参数列表）:
    函数体
    然后加了星号 * 的参数会以元组(tuple)的形式导入，存放所有未命名的变量参数。
    加了两个星号 ** 的参数会以字典的形式导

return表达式用于退出函数，不带return视作返回none

匿名函数：lambda      lambda arguments: expression
arguments 是参数列表，可以包含零个或多个参数，但必须在冒号(:)前指定。
expression 是一个表达式，用于计算并返回函数的结果。
比如：sum = lambda arg1, arg2: arg1 + arg2
 print ("相加后的值为 : ", sum( 10, 20 ))
 print ("相加后的值为 : ", sum( 20, 20 ))

3.三维弓形曲面图可视化
见using.py代码

4.梯度下降
1.梯度下降是一种可以用来尝试最小化任何函数的算法，不仅限于线性回归函数的代数函数
对于线性回归函数的代价函数，先将w，b初始化为0，然后在梯度下降运算中，每次小幅度改变w，b的值，尝试价绍J，最后让J达到最小值
（有些模型有不同的最小值点，所以有不同顶点）梯度下降算法是算最速降线，在某一点上，360°环顾一周，选择最快的下降地方，下降一点点，再重复上述操作。这会导致出现局部最小值（很重要）

w'=w-a*dJ(w,b)/dw，=为赋值运算,b'=b-a*dJ(w,b)/dw,w，b随时同时更新,再进行下一轮计算，即递归。其中a为学习率。

2.dJ(w,b)/dw的意义，先确定b的值
由于a一直>0，更新的斜率绝对值会越来越小，最终找到曲线的顶点

如何选择a呢？如果过小，比如0.0000001，下降非常小，迭代次数会变多，学习时间显著增加；如果过大，会导致w超过0，导致发生震荡，即发散

如果J（w）已经到达了局部最小值，根据梯度下降，此时导数为0，w不再改变，同时我们能注意到斜率变化率的变化率会下降，即二阶导

## 9.15线性回归

1.线性回归模型的梯度下降
J（w，b）=1/2m ∑（y-y^）**2，y^=w*x+b,再w'=w-a*dJ(w,b)/dw，b'=b-a*dJ(w,b)/dw，可以得到w=w-a/m *∑i=1,m  (f(xi)-yi)*xi
b=b-a/m *∑i=1,m  (f(xi)-yi).
对于有多个最小值，我们将它解剖为一个个凸函数，再求每一个的局部最小值

这种成为批量梯度下降，即每次都查看所有训练集（还有其他种类）
实现代码：
import math, copy
import numpy as np
import matplotlib.pyplot as plt
plt.style.use('./deeplearning.mplstyle')
from lab_utils_uni import plt_house_x, plt_contour_wgrad, plt_divergence, plt_gradients

#Load our data set
x_train = np.array([1.0, 2.0])   # features
y_train = np.array([300.0, 500.0])   #target value

#Function to calculate the cost
def compute_cost(x, y, w, b):
   
    m = x.shape[0] 
    cost = 0
    
    for i in range(m):
        f_wb = w * x[i] + b
        cost = cost + (f_wb - y[i])**2
    total_cost = 1 / (2 * m) * cost

    return total_cost

def compute_gradient(x, y, w, b): 
    # Number of training examples
    m = x.shape[0]    
    dj_dw = 0
    dj_db = 0
    
    for i in range(m):  
        f_wb = w * x[i] + b 
        dj_dw_i = (f_wb - y[i]) * x[i] 
        dj_db_i = f_wb - y[i] 
        dj_db += dj_db_i
        dj_dw += dj_dw_i 
    dj_dw = dj_dw / m 
    dj_db = dj_db / m 
        
    return dj_dw, dj_db


def gradient_descent(x, y, w_in, b_in, alpha, num_iters, cost_function, gradient_function): 
    w = copy.deepcopy(w_in) # avoid modifying global w_in
    # An array to store cost J and w's at each iteration primarily for graphing later
    J_history = []
    p_history = []
    b = b_in
    w = w_in
    
    for i in range(num_iters):
        # Calculate the gradient and update the parameters using gradient_function
        dj_dw, dj_db = gradient_function(x, y, w , b)     

        # Update Parameters using equation (3) above
        b = b - alpha * dj_db                            
        w = w - alpha * dj_dw                            

        # Save cost J at each iteration
        if i<100000:      # prevent resource exhaustion 
            J_history.append( cost_function(x, y, w , b))
            p_history.append([w,b])
        # Print cost every at intervals 10 times or as many iterations if < 10
        if i% math.ceil(num_iters/10) == 0:
            print(f"Iteration {i:4}: Cost {J_history[-1]:0.2e} ",
                  f"dj_dw: {dj_dw: 0.3e}, dj_db: {dj_db: 0.3e}  ",
                  f"w: {w: 0.3e}, b:{b: 0.5e}")
 
    return w, b, J_history, p_history #return w and J,w history for graphing

#initialize parameters
w_init = 0
b_init = 0
#some gradient descent settings
iterations = 10000
tmp_alpha = 1.0e-2
#run gradient descent
w_final, b_final, J_hist, p_hist = gradient_descent(x_train ,y_train, w_init, b_init, tmp_alpha, 
                                                    iterations, compute_cost, compute_gradie
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/wayyzzww/article/details/146297436

但是在运行时还是有问题qwq因为我没有deeplearning的正版文件夹
但是可以删除库，就没有图像了

2.多元线性回归
还是举房价的例子，现在有地段，年代，大小等多个特征
xj为第i个特征代码（即房价），n为特征总数，xi为第i个数据列表（即100w的房子100平方，在市中心......）

先在f(w,b)x=w1x1+w2x2+w3x3+......+wnxn+b，定义向量**w**=[w1,w2,.....wn],**x**=[x1,x2,x3.....xn],f(w,b)=**w** * **x**+b
在python中可以用下面代码表示：

第一种向量组

import numpy as np
w=np.array([1.0,2.5,-3.3])
b=4
x=np.array([10,20,30])
f=w[0]*x[0]+......  numpy就是数值线性代数库，可以通过w[0],x[2]等来索引，（注意索引从0开始）

第二种方法，不用向量，而用求和

f=0
for j in range(0,n):##这里到n-1，其中0可以省略
    f=f+w[j]*x[j]
f=f+b

第三种向量化

import numpy as np
f=np.dot(w,x)+b

当然三种都要先定义向量组

向量化实际上会简化算法，让算法高效执行，原理如下：
对于for循环（没有向量化）会一步步索引，就是从0开始执行15步终止；对于numpy库，实际上是直接向量并行执行，即只执行一步将其全部算出来

对于代价函数J(w,b)=J(**w**,b),然后对每一个wi求偏导，其余相同，对每一个wi都要求偏导

另一种线性回归的算法：正规方程算法，方便但不能推广，且n很大时速度很慢，一般不用

3.特征缩放

特征的变化范围比较大时，wi会较小，反之会较大。因为特征变化范围较大时，影响程度很大。所以我们需要对x1，x2等进行放缩，将x1，x2尽量范围放缩到一致，代价函数的等高线更接近一个椭圆，增加运算速度。
如何实现：

可以对x1/1000，或者x2*5等类似的改变。或者找出x1（特征代码）的平均值为mu，然后（x1=x1-u）/（xmax-xmin），即均值归一化

Z分数归一化：计算均值mu和每个特征的标准差s（方差的算数平方根），然后xi=（xi-mu）/s

不管怎样建议先进行特征放缩

4.检查梯度下降是否收敛

对学习率a的选择：画出J(w,b)关于下降次数的图像（学习曲线），这条学习曲线应该是下降的，并且找到最后趋于水平的线，即收敛
对于迭代次数很难确定什么时候数据会收敛，可以设定一个收敛参数进行自动收敛测试，比如0.001，当J小于0.001时收敛，但不准（不准确）

有拐点就不收敛，可以将a设为非常小的值来看是否收敛比如0.001-0003-0.01，然后慢慢确定梯度下降最佳的值。

## 9.17 机器学习
1.选择合适特征（特征工程）
比如，一座房子：x1=地块前沿，x2=深度，f=w1x1+w2x2+b
定义x3=x1x2，表示面积，f=w1x1+w2x2+w3x3+b，x3就是新特征，通过组合或改变已有变量（通过现有知识）

2.多项式回归拟合非线性方程
可以将f扩展为变量的多项式，此时必须使用特征放缩


3.先把最后一个任务做了yolo！
这个包给我下载半天，最后用指令下载pip install 包名 -i https://pypi.tuna.tsinghua.edu.cn/simple --trusted-host pypi.tuna.tsinghua.edu.cn
然后就在我的conda activate two里面执行了好久，感觉显卡在燃烧
Speed: 0.9ms preprocess, 65.8ms inference, 0.0ms loss, 1.7ms postprocess per image
Results saved to C:\Users\hp\Desktop\edgeAI\runs\detect\train
(two) PS C:\Users\hp\Desktop\edgeAI> 
[yolo]("C:\Users\hp\Desktop\edgeAI\yolo.png" "yolo")
终于下载好了，好神奇
这非常显然是一个分类模型，迭代了一百次




## 9.18 逻辑回归（分类算法）
1.预期变量是“是”或者“否”，即一种二元分类在计算机中为0（负类），1（正类）

逻辑回归用于分类，而非回归。**Sigmoid**函数，即逻辑函数，起着重要作用（看起来像反余切）实际上g(z)=1/(1+e**-z)，逻辑回归只会输出0或1
z=f(x)=w*x+b w，x为向量，然后带入g(z)中

回到判断肿瘤的例子：
x=肿瘤大小，y=0/1，如果输出0.7，即患者患肿瘤概率为70% 

2.决策边界
设定一个阈值，高于阈值为1，低于阈值为0，对于0，1保持中立的线为决策边界，即z=0，如果w'b等参数不同的话决策边界为变
决策边界可能是直线可能是曲线

3.训练
逻辑回归有多个特征变量，对于这个二元集，输出结果为0或1.
如何选择w，b：
如果J(w,b)代价函数与线性回归一样，平方误差代价函数会形成多个局部最小值
J(**w**,b)=1/m ∑1/2(f(x)-y)**2
内部为单个样本损失：(f(x)-y)**2
L=-log(f(x)),if y==1,-log(1-f(x))，if y==0，此时L为损失函数，L越接近0越准确。y与x的差值就是损失。
此时代价函数可以进行梯度下降

同样用m表示特征变量数量，或者L(f(x),y)=-ylog(f(x))-(1-y)log(1-f(x))其中，x为xi，y为yi，与上面分段函数相同

这个就是极大似然估计，似然就是从结果推测参量的概率

4.如何选择w，b
先申明：梯度算法下降的公式与线性回归一样wj'=wj-a*dJ(w,b)/dwj,b'=b-a*dJ(w,b)/dw(j=1,2,....n)
再对损失函数求偏导：
dJ(w,b)/dwj=1/m ∑(f(x)-y)xj   这里的f(x)就是上述的g(z)，即g(x)=1/(1+e**-w*x+b)
监督与向量化与特征放缩依旧和线性回归一样可以类似实现