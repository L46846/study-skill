# Python 基础语法学习笔记


## 1. 变量与数据类型
### 1.1 变量命名规则
- 只能包含字母、数字和下划线，**不能以数字开头**。
- 区分大小写（`name` 与 `Name` 不同）。
- 避免使用 Python 关键字（如 `if`、`for`、`while`）。

### 1.2 常见数据类型
Python 中最常用的数据类型有以下几种：

| 数据类型 | 描述 | 典型示例 |
| :--- | :--- | :--- |
| **int** | 整数 | `age = 18` |
| **float** | 浮点数（小数） | `score = 98.5` |
| **str** | 字符串（文本） | `name = "Alice"` |
| **bool** | 布尔值（真假） | `is_student = True` |
| **list** | 列表（有序序列） | `nums = [1, 2, 3]` |

### 1.3 代码示例
```python
# 1. 定义不同类型的变量
name = "Alice"       # 字符串
age = 20             # 整数
height = 175.5       # 浮点数
is_adult = True      # 布尔值

# 2. 查看变量类型
print(type(name))    # 输出: <class 'str'>
print(type(age))     # 输出: <class 'int'>

# 3. 类型转换
num_str = "123"
num_int = int(num_str)  # 把字符串转为整数
print(num_int + 1)      # 输出: 1242. 输入与输出
 
2.1 输出 ( print )
 
用于在控制台显示内容，是代码与人交互的基础方式。
 
python
  
# 1. 基础输出
print("Hello, Python!")

# 2. 多内容输出（逗号分隔，自动加空格）
print("姓名:", "Alice", "年龄:", 20)

# 3. 格式化输出（f-string 最推荐，写法简单直观）
name = "小明"
age = 18
score = 95.5
print(f"我叫{name}，今年{age}岁，考试分数是{score}分。")
# 输出: 我叫小明，今年18岁，考试分数是95.5分。
 
 
2.2 输入 ( input )
 
用于获取用户的键盘输入，默认返回字符串类型，如需计算必须手动转换。
 
python
  
# 1. 基础输入
username = input("请输入你的名字: ")
print(f"你好, {username}! 欢迎学习Python！")

# 2. 输入数字（必须转换类型）
age_str = input("请输入你的年龄: ")
age = int(age_str)  # 把字符串转为整数
print(f"明年你就{age + 1}岁啦！")
 
 
 
 
3. 基本运算符
 
3.1 算术运算符
 
python
  
a = 10
b = 3
print(a + b)  # 加法: 13
print(a - b)  # 减法: 7
print(a * b)  # 乘法: 30
print(a / b)  # 除法: 3.333...（结果永远是浮点数）
print(a // b) # 整数除法: 3（只取整数部分）
print(a % b)  # 取余: 1（求余数）
print(a ** b) # 幂运算: 1000（10的3次方）
 
 
3.2 比较运算符（结果为布尔值）
 
python
  
a = 5
b = 3
print(a > b)   # 大于: True
print(a < b)   # 小于: False
print(a == b)  # 等于: False
print(a != b)  # 不等于: True
print(a >= b)  # 大于等于: True
print(a <= b)  # 小于等于: False
 
 
3.3 逻辑运算符
 
python
  
# and（与）: 两个条件都满足才为True
print(5 > 3 and 10 > 8)  # True
print(5 > 3 and 2 > 8)   # False

# or（或）: 只要一个条件满足就为True
print(5 > 3 or 2 > 8)    # True
print(1 > 3 or 2 > 8)    # False

# not（非）: 取反
print(not 5 > 3)         # False
print(not 1 > 3)         # True
 
 
 
 
4. 流程控制语句
 
4.1 单分支  if 
 
满足条件就执行缩进内的代码，不满足则跳过。
 
python
  
score = 85
if score >= 60:
    print("恭喜你，及格了！")
    print("可以去玩啦！")
# 注意：Python用缩进（4个空格）区分代码块，必须严格遵守
 
 
4.2 双分支  if-else 
 
满足条件执行 if 内代码，不满足执行 else 内代码。
 
python
  
age = 15
if age >= 18:
    print("你是成年人")
else:
    print("你是未成年人")
 
 
4.3 多分支  if-elif-else 
 
按顺序判断多个条件，满足一个就执行对应代码，后续不再判断。
 
python
  
score = 82
if score >= 90:
    print("等级: A (优秀)")
elif score >= 80:
    print("等级: B (良好)")
elif score >= 60:
    print("等级: C (及格)")
else:
    print("等级: D (不及格)")
 
 
 
 
5. 循环语句
 
5.1  for  循环（已知循环次数，最常用）
 
用于遍历序列（列表、字符串、range等），重复执行代码。
 
python
  
# 1. 用range()生成数字序列，循环5次（0到4）
for i in range(5):
    print(f"当前计数: {i}")

# 2. 遍历列表
fruits = ["苹果", "香蕉", "橘子", "葡萄"]
for fruit in fruits:
    print(f"我想吃: {fruit}")

# 3. 遍历字符串
for char in "Python":
    print(f"当前字符: {char}")
 
 
5.2  while  循环（未知循环次数，满足条件就执行）
 
只要条件为 True ，就一直循环，直到条件为 False 停止。
 
python
  
# 计算1到100的和
sum_num = 0
i = 1
while i <= 100:
    sum_num += i  # 等价于 sum_num = sum_num + i
    i += 1        # 等价于 i = i + 1
print("1到100的和是:", sum_num)  # 输出: 5050
 
 
5.3 循环控制关键字
 
python
  
# continue: 跳过本次循环，直接进入下一次
for i in range(10):
    if i == 3:
        continue  # 遇到3就跳过，不执行后面的print
    print(i)
# 输出: 0 1 2 4 5 6 7 8 9

# break: 直接终止整个循环
for i in range(10):
    if i == 6:
        break     # 遇到6就直接结束循环
    print(i)
# 输出: 0 1 2 3 4 5
 
 
 
 
6. 列表与字典常用操作
 
6.1 列表（ list ）
 
有序、可变的序列，可存储不同类型数据。
 
python
  
# 1. 创建列表
fruits = ["苹果", "香蕉", "橘子"]
nums = [1, 2, 3, 4, 5]

# 2. 访问元素（索引从0开始）
print(fruits[0])  # 输出: 苹果
print(fruits[-1]) # 输出: 橘子（-1代表最后一个元素）

# 3. 添加元素
fruits.append("葡萄")  # 在末尾添加
print(fruits)  # 输出: ['苹果', '香蕉', '橘子', '葡萄']

# 4. 删除元素
fruits.remove("香蕉")  # 删除指定元素
print(fruits)  # 输出: ['苹果', '橘子', '葡萄']

# 5. 列表长度
print(len(fruits))  # 输出: 3
 
 
6.2 字典（ dict ）
 
无序、可变的键值对集合，通过键快速查找值。
 
python
  
# 1. 创建字典
student = {"name": "Alice", "age": 20, "major": "计算机"}

# 2. 访问值（通过键）
print(student["name"])  # 输出: Alice
print(student.get("age"))  # 输出: 20（get方法更安全，键不存在不会报错）

# 3. 添加/修改键值对
student["gender"] = "女"  # 键不存在则添加
student["age"] = 21       # 键存在则修改
print(student)

# 4. 删除键值对
del student["major"]
print(student)

# 5. 遍历字典
for key, value in student.items():
    print(f"{key}: {value}")
 
 
 
 
7. 函数
 
7.1 函数定义与调用
 
把重复使用的代码打包，方便复用，提高效率。
 
python
  
# 1. 定义函数（def关键字）
def say_hello(name):
    """这是一个打招呼的函数（文档注释，说明函数功能）"""
    print(f"你好, {name}! 欢迎学习Python！")

# 2. 调用函数
say_hello("小明")
say_hello("小红")

# 3. 带返回值的函数
def add(a, b):
    """计算两个数的和"""
    return a + b  # return返回结果

result = add(10, 20)
print(result)  # 输出: 30
 
 
 
 
8. 入门练习题（附答案）
 
8.1 基础题
 
1. 定义变量存储你的姓名、年龄、身高，用 print 格式化输出。
2. 用 input 获取用户输入的两个数字，计算它们的和、差、积、商并输出。
3. 用 for 循环打印1到100之间所有的偶数。
4. 用 while 循环计算1到10的阶乘（1×2×3×…×10）。
5. 定义一个列表存储5个同学的名字，遍历列表并打印每个同学的名字。
 
8.2 参考答案
 
python
  
# 1. 变量与输出
name = "张三"
age = 19
height = 178.5
print(f"姓名: {name}, 年龄: {age}, 身高: {height}cm")

# 2. 输入与计算
num1 = float(input("请输入第一个数字: "))
num2 = float(input("请输入第二个数字: "))
print(f"和: {num1 + num2}")
print(f"差: {num1 - num2}")
print(f"积: {num1 * num2}")
print(f"商: {num1 / num2}")

# 3. for循环打印偶数
for i in range(1, 101):
    if i % 2 == 0:
        print(i)

# 4. while循环计算阶乘
result = 1
i = 1
while i <= 10:
    result *= i
    i += 1
print(f"10的阶乘是: {result}")

# 5. 列表遍历
students = ["小明", "小红", "小刚", "小丽", "小强"]
for student in students:
    print(f"同学姓名: {student}")