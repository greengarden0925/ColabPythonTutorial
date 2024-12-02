# Python 入門教學
---
1. [Python 簡介](#1-python-簡介)
-1.1 [歷史](#歷史)
-1.2 [特點](#特點)
-1.3 [示例程式碼：打印-Hello-World](#示例程式碼打印-hello-world)
-1.4 [練習題](#練習題)

## 2. [基本語法](#2-基本語法)
### 2.1 [資料型別與變數](#資料型別與變數)
### 2.2 [示例程式碼：定義變數並打印](#示例程式碼定義變數並打印)
### 2.3 [練習題](#練習題)

## 3. [控制結構](#3-控制結構)
### 3.1 [條件語句（if、elif、else）](#31-條件語句ifelifelse)
### 3.2 [迴圈（for 和 while）](#32-迴圈for-和-while)
### 3.3 [循環控制語句（break、continue、pass）](#33-循環控制語句breakcontinuepass)

## 4. [函式與模組](#4-函式與模組)
### 4.1 [函式的定義與調用（def 和 return）](#41-函式的定義與調用def-和-return)
### 4.2 [匯入模組與使用內建函式](#42-匯入模組與使用內建函式)
### 4.3 [自訂模組的創建與使用](#43-自訂模組的創建與使用)

## 5. [資料結構](#5-資料結構)
### 5.1 [列表（list）操作：新增、刪除、排序](#51-列表list操作新增刪除排序)
### 5.2 [字典（dict）操作：鍵值對管理](#52-字典dict操作鍵值對管理)
### 5.3 [集合（set）與元組（tuple）的使用場景](#53-集合set與元組tuple的使用場景)

## 6. [檔案操作](#6-檔案操作)
### 6.1 [打開、讀取、寫入文件](#61-打開讀取寫入文件)
### 6.2 [檔案處理的錯誤捕捉](#62-檔案處理的錯誤捕捉)

## 7. [異常處理](#7-異常處理)
### 7.1 [使用 try、except 捕捉錯誤](#71-使用-tryexcept-捕捉錯誤)
### 7.2 [finally 處理資源釋放](#72-finally-處理資源釋放)

## 8. [物件導向程式設計 (OOP)](#8-物件導向程式設計-oop)
### 8.1 [類與物件的概念](#81-類與物件的概念)
### 8.2 [定義類與方法](#82-定義類與方法)
### 8.3 [繼承與多型](#83-繼承與多型)

## 9. [常用函式庫](#9-常用函式庫)
### 9.1 [數學運算（math 模組）](#91-數學運算math-模組)
### 9.2 [隨機生成（random 模組）](#92-隨機生成random-模組)
### 9.3 [日期與時間處理（datetime 模組）](#93-日期與時間處理datetime-模組)
### 9.4 [數據處理（numpy 和 pandas）](#94-數據處理numpy-和-pandas)

---
## 1. Python 簡介

Python 是一種廣泛使用的高階程式語言，具有簡潔的語法和強大的功能，適合新手和專業開發者。

### 歷史
Python 由 Guido van Rossum 在 1989 年創立，第一版於 1991 年釋出。它的名字來自 BBC 的喜劇節目《蒙提·派森的飛行馬戲團》（Monty Python's Flying Circus）。

重要的里程碑包括：
- **1991**：Python 1.0 發佈，包含簡單的模組系統與內建資料型別。
- **2000**：Python 2.0 發佈，引入垃圾回收與列表推導式。
- **2008**：Python 3.0 發佈，改善了語法一致性，但與 Python 2 不完全兼容。

### 特點
- 易於學習和使用。
- 支持多種編程範式（如物件導向、函數式編程）。
- 擁有龐大的社群和豐富的函式庫。

### 示例程式碼：打印 "Hello, World!"
```python
# 打印基本信息
print("Hello, World!")
```

#### 註解說明：
- `print()`：Python 中的輸出函數，用於將內容打印到控制台。

### 練習題：
1. 修改程式碼打印 "Welcome to Python!"。

#### 提示：
- 將 `"Hello, World!"` 替換為 `"Welcome to Python!"`。

#### 標準答案：
```python
print("Welcome to Python!")
```

---

## 2. 基本語法

### 資料型別與變數
Python 提供多種資料型別，如整數（int）、浮點數（float）、字串（str）、布林值（bool）等。

### 示例程式碼：定義變數並打印
```python
# 定義不同型別的變數
integer_var = 10  # 整數
float_var = 3.14  # 浮點數
string_var = "Python"  # 字串
boolean_var = True  # 布林值

# 打印變數
print("Integer:", integer_var)
print("Float:", float_var)
print("String:", string_var)
print("Boolean:", boolean_var)
```

#### 註解說明：
- `integer_var = 10`：定義一個整數變數並賦值為 10。
- `print()`：輸出變數內容到控制台。

### 練習題：
1. 定義一個變數 `name`，其值為你的名字，並打印 "Hello, [name]!"。

#### 提示：
- 使用 `+` 拼接字串。

#### 標準答案：
```python
name = "John"  # 將名字替換為你的名字
print("Hello, " + name + "!")
```

---

## 3. 控制結構

### 3.1. 條件語句（if、elif、else）

### 說明  
條件語句用於根據條件的真假來執行不同的程式碼區塊。

### 範例程式碼

```python
# 判斷一個數字是否為正、負或零
number = int(input("請輸入一個數字： "))

if number > 0:
    print("這是一個正數。")  # 當數字大於 0 時執行
elif number < 0:
    print("這是一個負數。")  # 當數字小於 0 時執行
else:
    print("這是零。")  # 當數字等於 0 時執行
```

### 練習題  
**問題：** 寫一段程式，判斷輸入的年齡是否為青少年（13 到 19 歲之間）。  

**提示：** 使用 `if` 和 `elif` 檢查條件範圍。

**標準答案：**
```python
age = int(input("請輸入年齡： "))

if 13 <= age <= 19:
    print("你是一名青少年。")
else:
    print("你不是青少年。")
```

---

### 3.2 迴圈（for 和 while）

### 說明  
迴圈用於重複執行某段程式碼，直到條件不成立。`for` 適合用於迭代結構，`while` 用於條件控制。

### 範例程式碼

#### `for` 迴圈
```python
# 使用 for 迴圈計算 1 到 5 的總和
total = 0
for i in range(1, 6):  # range(1, 6) 產生數字 1 到 5
    total += i  # 將每次迭代的數字累加到 total
print("總和是：", total)
```

#### `while` 迴圈
```python
# 使用 while 迴圈找出小於 10 的偶數
number = 0
while number < 10:
    if number % 2 == 0:  # 判斷是否為偶數
        print(number)
    number += 1  # 每次迭代增加 1
```

### 練習題  
**問題 1：** 使用 `for` 迴圈印出 1 到 10 的所有奇數。  
**提示：** 使用 `if` 判斷數字是否為奇數。  

**標準答案：**
```python
for i in range(1, 11):
    if i % 2 != 0:  # 判斷是否為奇數
        print(i)
```

**問題 2：** 使用 `while` 迴圈計算 1 到 100 的總和。  
**提示：** 設置初始值，並在每次迴圈增加計數器。  

**標準答案：**
```python
total = 0
number = 1

while number <= 100:
    total += number  # 將當前數字加入總和
    number += 1  # 增加計數器
print("總和是：", total)
```

---

### 3.3 循環控制語句（break、continue、pass）

### 說明  
- **`break`**：結束整個迴圈。  
- **`continue`**：跳過當前迭代，繼續下一次迭代。  
- **`pass`**：不執行任何操作，用作佔位符。

### 範例程式碼

#### 使用 `break`
```python
# 找到第一個大於 50 的偶數
for i in range(100):
    if i > 50 and i % 2 == 0:  # 判斷條件
        print("找到：", i)
        break  # 結束迴圈
```

#### 使用 `continue`
```python
# 跳過所有小於 5 的數字
for i in range(10):
    if i < 5:
        continue  # 跳過當前迭代
    print(i)
```

#### 使用 `pass`
```python
# 用 pass 保留未完成的功能
for i in range(5):
    if i == 3:
        pass  # 暫時不執行任何操作
    print(i)
```

### 練習題  
**問題 1：** 使用 `break` 迴圈找到並印出 1 到 100 中第一個可以被 7 整除的數字。  
**提示：** 使用 `if` 檢查條件，並在符合條件時中斷迴圈。  

**標準答案：**
```python
for i in range(1, 101):
    if i % 7 == 0:  # 判斷是否能被 7 整除
        print("找到的數字是：", i)
        break
```

**問題 2：** 使用 `continue` 實現，只印出 1 到 10 之間的奇數。  
**提示：** 在偶數條件下跳過當前迭代。  

**標準答案：**
```python
for i in range(1, 11):
    if i % 2 == 0:  # 判斷是否為偶數
        continue
    print(i)
```

---

## 4. 函式與模組
### 4.1 函式的定義與調用（`def` 和 `return`）

### 說明  
函式是一段可重複執行的代碼，通過 `def` 關鍵字定義，可以使用 `return` 傳回結果。

### 範例程式碼

#### 定義與調用函式
```python
# 定義一個函式計算兩數之和
def add_numbers(a, b):
    """
    接收兩個數字，返回它們的和
    """
    return a + b  # 返回計算結果

# 調用函式並顯示結果
result = add_numbers(5, 3)
print("兩數之和是：", result)
```

### 練習題  
**問題：** 定義一個函式 `is_even`，檢查一個數字是否為偶數，並返回布林值（`True` 或 `False`）。  

**提示：** 使用模數運算符 `%` 判斷是否可被 2 整除。  

**標準答案：**
```python
def is_even(number):
    """
    判斷數字是否為偶數
    """
    return number % 2 == 0

# 測試函式
print(is_even(4))  # True
print(is_even(7))  # False
```

---

### 4.2 匯入模組與使用內建函式（如 `math`、`random`）

### 說明  
模組是包含 Python 代碼的文件，可以透過 `import` 將模組功能匯入程式中。

### 範例程式碼

#### 使用 `math` 模組
```python
# 計算平方根和圓的面積
import math

# 計算 16 的平方根
sqrt_result = math.sqrt(16)
print("16 的平方根是：", sqrt_result)

# 計算半徑為 5 的圓面積
radius = 5
circle_area = math.pi * (radius ** 2)  # 使用 math.pi 提供的圓周率
print("圓的面積是：", circle_area)
```

#### 使用 `random` 模組
```python
# 隨機生成一個 1 到 10 的整數
import random

random_number = random.randint(1, 10)
print("隨機生成的數字是：", random_number)
```

### 練習題  
**問題 1：** 使用 `math` 模組計算一個數字的自然對數。  
**提示：** 使用 `math.log()` 函數。  

**標準答案：**
```python
import math

number = 10
log_result = math.log(number)
print(f"{number} 的自然對數是：", log_result)
```

**問題 2：** 使用 `random` 模組生成 5 個介於 1 到 100 之間的隨機數，並印出它們的平均值。  
**提示：** 使用迴圈和累加計算平均值。  

**標準答案：**
```python
import random

total = 0
for _ in range(5):
    num = random.randint(1, 100)
    total += num
    print("生成的數字：", num)
average = total / 5
print("平均值是：", average)
```

---

### 4.3 自訂模組的創建與使用

### 說明  
可以將函式存儲在一個 `.py` 文件中作為模組，然後在其他程式中匯入使用。

### 範例程式碼

#### 創建自訂模組
1. 創建一個名為 `my_module.py` 的檔案，內容如下：
```python
# my_module.py

def greet(name):
    """
    返回歡迎信息
    """
    return f"你好，{name}！歡迎學習 Python！"

def square(number):
    """
    返回一個數字的平方
    """
    return number ** 2
```

2. 在主程式中匯入並使用模組：
```python
# 匯入自訂模組
import my_module

# 使用模組的函式
print(my_module.greet("大學生"))  # 調用 greet 函式
print("4 的平方是：", my_module.square(4))  # 調用 square 函式
```

### 練習題  
**問題：** 創建一個名為 `math_utils.py` 的模組，其中包含以下函式：  
- `factorial(n)`：計算並返回 n 的階乘。  
- `is_prime(n)`：判斷 n 是否為質數。

在主程式中匯入該模組，測試這兩個函式。

**提示：** 階乘可以用遞迴或迴圈實現，質數判斷可以用除法測試。

**標準答案：**

#### `math_utils.py` 模組內容：
```python
# math_utils.py

def factorial(n):
    """
    計算並返回 n 的階乘
    """
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)

def is_prime(n):
    """
    判斷 n 是否為質數
    """
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True
```

#### 主程式內容：
```python
# 匯入自訂模組
import math_utils

# 測試階乘函式
print("5 的階乘是：", math_utils.factorial(5))  # 120

# 測試質數判斷函式
print("7 是否為質數？", math_utils.is_prime(7))  # True
print("10 是否為質數？", math_utils.is_prime(10))  # False
```
---

## 5. 資料結構
---

### 5.1 列表（`list`）操作：新增、刪除、排序

### 說明  
列表是可變的有序集合，用於存儲多個值，可以新增、刪除、或排序元素。

### 範例程式碼

#### 新增元素
```python
# 使用 append() 方法新增元素
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")  # 新增一個元素到列表末尾
print(fruits)  # ['apple', 'banana', 'cherry', 'orange']

# 使用 insert() 方法在指定位置新增元素
fruits.insert(1, "kiwi")  # 在索引 1 插入 'kiwi'
print(fruits)  # ['apple', 'kiwi', 'banana', 'cherry', 'orange']
```

#### 刪除元素
```python
# 使用 remove() 方法刪除指定值
fruits.remove("banana")  # 刪除 'banana'
print(fruits)  # ['apple', 'kiwi', 'cherry', 'orange']

# 使用 pop() 方法刪除指定位置的元素
removed_fruit = fruits.pop(2)  # 刪除索引 2 的元素
print(removed_fruit)  # 'cherry'
print(fruits)  # ['apple', 'kiwi', 'orange']
```

#### 排序
```python
# 使用 sort() 方法排序
numbers = [5, 2, 9, 1]
numbers.sort()  # 升序排序
print(numbers)  # [1, 2, 5, 9]

# 使用 sorted() 函數返回新排序列表
numbers_desc = sorted(numbers, reverse=True)  # 降序排序
print(numbers_desc)  # [9, 5, 2, 1]
```

### 練習題  
**問題：** 創建一個學生分數的列表，新增一個分數，刪除最低分數，並將列表按升序排序後打印。  

**提示：** 使用 `append()`、`min()` 和 `sort()`。  

**標準答案：**
```python
scores = [85, 92, 78, 90]
scores.append(88)  # 新增一個分數
scores.remove(min(scores))  # 刪除最低分數
scores.sort()  # 排序
print("更新後的分數列表：", scores)  # [85, 88, 90, 92]
```

---

### 5.2 字典（`dict`）操作：鍵值對管理

### 說明  
字典是一種無序的鍵值對集合，用於快速查找、添加、或刪除資料。

### 範例程式碼

#### 新增或修改鍵值對
```python
# 新增鍵值對
student = {"name": "Alice", "age": 20}
student["grade"] = "A"  # 新增 'grade' 鍵
print(student)  # {'name': 'Alice', 'age': 20, 'grade': 'A'}

# 修改鍵值對
student["age"] = 21  # 修改 'age' 的值
print(student)  # {'name': 'Alice', 'age': 21, 'grade': 'A'}
```

#### 刪除鍵值對
```python
# 使用 pop() 方法刪除鍵
removed_value = student.pop("grade")  # 刪除 'grade'
print(removed_value)  # 'A'
print(student)  # {'name': 'Alice', 'age': 21}

# 使用 del 關鍵字刪除鍵值對
del student["age"]
print(student)  # {'name': 'Alice'}
```

#### 遍歷字典
```python
# 遍歷鍵與值
for key, value in student.items():
    print(f"{key}: {value}")
```

### 練習題  
**問題：** 創建一個包含 3 位學生及其分數的字典，新增一位學生及其分數，刪除分數最低的學生。  

**提示：** 使用 `min()` 尋找分數最低的鍵值。  

**標準答案：**
```python
students = {"Alice": 85, "Bob": 92, "Charlie": 78}
students["David"] = 88  # 新增學生
lowest_score = min(students, key=students.get)  # 找到最低分的學生
del students[lowest_score]  # 刪除最低分學生
print("更新後的學生列表：", students)  # {'Alice': 85, 'Bob': 92, 'David': 88}
```

---

### 5.3 集合（`set`）與元組（`tuple`）的使用場景

### 集合（`set`）

#### 說明  
集合是無序且不重複的元素集合，適合用於快速測試是否存在某元素或去重操作。

#### 範例程式碼
```python
# 去重
numbers = [1, 2, 2, 3, 4, 4]
unique_numbers = set(numbers)  # 去除重複元素
print(unique_numbers)  # {1, 2, 3, 4}

# 集合運算
set_a = {1, 2, 3}
set_b = {2, 3, 4}
print(set_a & set_b)  # 交集：{2, 3}
print(set_a | set_b)  # 聯集：{1, 2, 3, 4}
print(set_a - set_b)  # 差集：{1}
```

### 元組（`tuple`）

#### 說明  
元組是不可變的有序集合，適合存儲不變的數據（如座標）。

#### 範例程式碼
```python
# 創建元組
point = (2, 3)
print("x 坐標是：", point[0])  # 訪問元組的元素

# 元組的解包
x, y = point
print(f"x: {x}, y: {y}")
```

### 練習題  

#### 集合題目  
**問題：** 給定兩個班級的學生名單，找出同時參加兩個班級的學生。  

**提示：** 使用集合的交集運算。  

**標準答案：**
```python
class_a = {"Alice", "Bob", "Charlie"}
class_b = {"Bob", "David", "Charlie"}
common_students = class_a & class_b
print("同時參加兩個班級的學生：", common_students)  # {'Bob', 'Charlie'}
```

#### 元組題目  
**問題：** 創建一個元組存放 3 個城市的經緯度，並打印每個城市的經緯度。  

**提示：** 使用迴圈解包元組內容。  

**標準答案：**
```python
cities = [("Taipei", 25.0330, 121.5654), ("Tokyo", 35.6895, 139.6917), ("Seoul", 37.5665, 126.9780)]

for city, lat, lon in cities:
    print(f"{city} 的經緯度是：({lat}, {lon})")
```

---
## 6. 檔案操作
---

### 6.1 檔案操作：打開、讀取、寫入文件（`open()`、`read()`、`write()`）

### 說明  
檔案操作是程式處理數據的重要部分，通過 `open()` 打開文件，並使用 `read()` 讀取或 `write()` 寫入內容。

### 範例程式碼

#### 打開與讀取文件
```python
# 讀取文件內容
try:
    with open("example.txt", "r") as file:  # 使用 "r" 模式打開文件
        content = file.read()  # 讀取整個文件內容
        print("文件內容：")
        print(content)
except FileNotFoundError:
    print("文件不存在，請檢查文件名稱。")
```

#### 寫入文件
```python
# 寫入新內容到文件
with open("example.txt", "w") as file:  # 使用 "w" 模式覆蓋寫入
    file.write("這是一個新的檔案內容。\n")
    file.write("學習 Python 的檔案操作！")
print("內容已寫入 example.txt")
```

#### 附加寫入文件
```python
# 附加內容到文件
with open("example.txt", "a") as file:  # 使用 "a" 模式附加內容
    file.write("\n這是附加的內容。")
print("附加內容已添加到 example.txt")
```

### 練習題  
**問題：** 創建一個名為 `students.txt` 的文件，寫入 3 位學生的姓名，然後讀取並打印文件內容。  

**提示：** 使用 `write()` 和 `read()` 操作。  

**標準答案：**
```python
# 寫入學生姓名
with open("students.txt", "w") as file:
    file.write("Alice\n")
    file.write("Bob\n")
    file.write("Charlie\n")

# 讀取文件內容
with open("students.txt", "r") as file:
    content = file.read()
print("文件內容：")
print(content)
```

---

### 6.2 檔案處理的錯誤捕捉

### 說明  
在檔案操作中可能會發生文件不存在、讀寫權限不足等錯誤，這些問題可以通過異常處理來應對。

### 範例程式碼

#### 捕捉文件錯誤
```python
try:
    with open("nonexistent_file.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("錯誤：文件不存在。")
except PermissionError:
    print("錯誤：無法讀取文件，權限不足。")
```

### 練習題  
**問題：** 實現一個程式，嘗試讀取用戶指定的文件，如果文件不存在，提示用戶重新輸入文件名稱。  

**提示：** 使用 `while` 迴圈和 `try-except` 捕捉錯誤。  

**標準答案：**
```python
while True:
    filename = input("請輸入文件名稱： ")
    try:
        with open(filename, "r") as file:
            content = file.read()
        print("文件內容：")
        print(content)
        break
    except FileNotFoundError:
        print("文件不存在，請再試一次。")
```

---
## 7. 異常處理
---

### 7.1 異常處理：使用 `try`、`except` 捕捉錯誤

### 說明  
異常處理幫助程式在錯誤發生時不中斷，並能執行相應的應對措施。

### 範例程式碼

#### 捕捉通用錯誤
```python
try:
    result = 10 / 0  # 會引發 ZeroDivisionError
except ZeroDivisionError:
    print("錯誤：除以零。")
```

#### 捕捉多種類型錯誤
```python
try:
    value = int(input("請輸入一個整數： "))
    result = 10 / value
    print("計算結果：", result)
except ValueError:
    print("錯誤：輸入的不是整數。")
except ZeroDivisionError:
    print("錯誤：不能除以零。")
```

---

### 7.2 使用 `finally` 處理資源釋放

### 說明  
`finally` 區塊中的程式碼無論是否發生異常都會執行，適合用於釋放資源，如關閉文件。

### 範例程式碼

#### 使用 `finally`
```python
try:
    file = open("example.txt", "r")
    content = file.read()
    print("文件內容：")
    print(content)
except FileNotFoundError:
    print("文件不存在。")
finally:
    if 'file' in locals() and not file.closed:
        file.close()  # 確保文件被關閉
        print("文件已關閉。")
```

### 練習題  
**問題：** 實現一個程式，嘗試讀取一個文件，如果發生錯誤，打印錯誤訊息，無論是否成功都需打印 "操作結束"。  

**提示：** 使用 `try-except-finally` 處理錯誤並打印訊息。  

**標準答案：**
```python
try:
    with open("example.txt", "r") as file:
        content = file.read()
        print("文件內容：")
        print(content)
except FileNotFoundError:
    print("錯誤：文件不存在。")
finally:
    print("操作結束。")
```
---
## 8. 物件導向程式設計(Object-oriented programming, OOP) 
---
### 8.1 類與物件的概念

### 說明  
- **類（Class）** 是對物件的抽象描述，定義了物件的屬性和行為。  
- **物件（Object）** 是類的實例，是具有具體值和狀態的存在。  

### 範例程式碼
```python
# 定義一個簡單的類與物件
class Dog:
    """
    定義狗的類，包含屬性和方法
    """
    def __init__(self, name, age):  # 初始化方法
        self.name = name  # 名字屬性
        self.age = age  # 年齡屬性

    def bark(self):  # 方法
        print(f"{self.name} 說：汪汪！")

# 創建物件
my_dog = Dog("Lucky", 3)
print(f"我的狗叫 {my_dog.name}，今年 {my_dog.age} 歲。")
my_dog.bark()  # 呼叫物件的方法
```

### 練習題  
**問題：** 創建一個名為 `Car` 的類，該類具有 `brand` 和 `speed` 屬性，以及一個方法 `drive()` 用於打印車輛行駛的訊息。  

**提示：** 使用 `__init__` 初始化屬性，並定義方法打印消息。  

**標準答案：**
```python
class Car:
    def __init__(self, brand, speed):
        self.brand = brand
        self.speed = speed

    def drive(self):
        print(f"{self.brand} 以 {self.speed} km/h 的速度行駛中。")

# 創建物件
my_car = Car("Toyota", 120)
my_car.drive()
```

---

### 8.2 定義類（`class`）與方法

### 說明  
類可以包含屬性（變數）和方法（函式），通過定義方法來描述物件的行為。

### 範例程式碼

#### 屬性與方法
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"大家好，我是 {self.name}，我今年 {self.age} 歲。")

# 創建物件並調用方法
person = Person("Alice", 25)
person.greet()
```

#### 修改屬性
```python
# 修改屬性值
person.age = 26  # 修改年齡
print(f"{person.name} 的新年齡是 {person.age} 歲。")
```

### 練習題  
**問題：** 定義一個類 `Rectangle`，用於表示長方形，包含長（`length`）和寬（`width`）屬性，以及計算面積的 `area()` 方法和計算周長的 `perimeter()` 方法。  

**提示：** 面積公式為 `length * width`，周長公式為 `2 * (length + width)`。  

**標準答案：**
```python
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

    def perimeter(self):
        return 2 * (self.length + self.width)

# 創建物件並測試
rect = Rectangle(5, 3)
print("面積是：", rect.area())
print("周長是：", rect.perimeter())
```

---

### 8.3 繼承與多型

### 說明  
- **繼承（Inheritance）**：允許新類別基於現有類別創建，繼承父類的屬性和方法。  
- **多型（Polymorphism）**：允許不同類型的物件使用相同的方法，但表現出不同的行為。

### 範例程式碼

#### 繼承
```python
# 定義父類
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("動物發出聲音。")

# 定義子類
class Cat(Animal):
    def speak(self):
        print(f"{self.name} 說：喵喵！")

# 創建子類物件
cat = Cat("Kitty")
cat.speak()  # 調用子類的方法
```

#### 多型
```python
# 多型例子
class Dog(Animal):
    def speak(self):
        print(f"{self.name} 說：汪汪！")

# 測試多型行為
animals = [Cat("Kitty"), Dog("Buddy")]

for animal in animals:
    animal.speak()  # 根據物件類型調用相應的方法
```

### 練習題  
**問題：** 定義一個父類 `Shape`，包含一個方法 `area()`（默認返回 0），然後定義子類 `Circle` 和 `Square`，分別實現 `area()` 方法計算圓形和正方形的面積。  

**提示：** 圓形面積公式為 `pi * r^2`，正方形面積公式為 `side^2`。  

**標準答案：**
```python
import math

class Shape:
    def area(self):
        return 0

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return math.pi * (self.radius ** 2)

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side ** 2

# 創建物件並測試
circle = Circle(3)
square = Square(4)

print("圓的面積是：", circle.area())  # 圓的面積
print("正方形的面積是：", square.area())  # 正方形的面積
```

---
## 9. 常用函式庫
---
本教案介紹 Python 的常用函式庫，包括數學運算、隨機生成、日期與時間處理，以及數據處理工具 `numpy` 和 `pandas` 的基礎應用。
---

### 9.1 數學運算（`math` 模組）

### 說明  
`math` 模組提供了常用的數學函數和常數，如平方根、對數、三角函數、圓周率等。

### 範例程式碼

#### 基本數學運算
```python
import math

# 計算平方根
print("16 的平方根是：", math.sqrt(16))

# 計算對數
print("10 的自然對數是：", math.log(10))

# 使用圓周率計算圓面積
radius = 5
area = math.pi * radius ** 2
print(f"半徑為 {radius} 的圓面積是：", area)
```

#### 三角函數
```python
# 計算三角函數值
angle = math.radians(30)  # 將角度轉為弧度
print("sin(30°) 的值是：", math.sin(angle))
print("cos(30°) 的值是：", math.cos(angle))
```

### 練習題  
**問題：** 計算一個三角形的斜邊長，已知兩直角邊分別為 3 和 4。  

**提示：** 使用勾股定理公式，斜邊長為 `sqrt(a^2 + b^2)`。  

**標準答案：**
```python
import math

a = 3
b = 4
hypotenuse = math.sqrt(a ** 2 + b ** 2)
print("三角形的斜邊長是：", hypotenuse)
```

---

### 9.2 隨機生成（`random` 模組）

### 說明  
`random` 模組用於生成隨機數或隨機選擇元素。

### 範例程式碼

#### 隨機數生成
```python
import random

# 生成 1 到 10 的隨機整數
print("隨機整數：", random.randint(1, 10))

# 生成 0 到 1 的隨機浮點數
print("隨機浮點數：", random.random())
```

#### 隨機選擇與打亂
```python
# 隨機選擇
choices = ["apple", "banana", "cherry"]
print("隨機選擇的水果：", random.choice(choices))

# 打亂列表順序
random.shuffle(choices)
print("打亂後的列表：", choices)
```

### 練習題  
**問題：** 模擬擲 6 面骰子 10 次，並打印每次的結果。  

**提示：** 使用 `randint(1, 6)` 模擬骰子擲出結果。  

**標準答案：**
```python
import random

for _ in range(10):
    print("骰子結果：", random.randint(1, 6))
```

---

### 9.3 日期與時間處理（`datetime` 模組）

### 說明  
`datetime` 模組用於處理日期與時間，支援格式化和計算。

### 範例程式碼

#### 獲取當前時間
```python
from datetime import datetime

now = datetime.now()
print("當前日期與時間：", now)
```

#### 日期格式化
```python
# 格式化為自定義格式
formatted_date = now.strftime("%Y-%m-%d %H:%M:%S")
print("格式化日期：", formatted_date)
```

#### 日期計算
```python
from datetime import timedelta

# 計算 7 天後的日期
future_date = now + timedelta(days=7)
print("7 天後的日期是：", future_date)
```

### 練習題  
**問題：** 計算用戶的生日距離今天還有多少天。  

**提示：** 使用 `datetime.strptime` 解析生日，並與當前日期相減。  

**標準答案：**
```python
from datetime import datetime

birthday = input("請輸入生日 (格式：YYYY-MM-DD)： ")
birthday_date = datetime.strptime(birthday, "%Y-%m-%d")
today = datetime.now()

days_left = (birthday_date - today).days
print(f"距離你的生日還有 {days_left} 天。")
```

---

### 9.4 數據處理（`numpy` 和 `pandas`）

### 說明  
- **`numpy`**：數值計算工具，適合處理多維數據和矩陣操作。  
- **`pandas`**：數據分析工具，提供強大的數據結構（如 `DataFrame`）。

---

### 使用 `numpy`

#### 範例程式碼
```python
import numpy as np

# 創建數組
array = np.array([1, 2, 3, 4])
print("數組：", array)

# 基本運算
print("數組的平方：", array ** 2)
```

#### 矩陣操作
```python
# 創建矩陣
matrix = np.array([[1, 2], [3, 4]])
print("矩陣：")
print(matrix)

# 矩陣的轉置
print("矩陣的轉置：")
print(matrix.T)
```

### 使用 `pandas`

#### 範例程式碼
```python
import pandas as pd

# 創建 DataFrame
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35],
    "Score": [85, 90, 95]
}
df = pd.DataFrame(data)
print("數據表：")
print(df)

# 選取列
print("選取 'Age' 列：")
print(df["Age"])
```

### 練習題  

#### `numpy` 練習  
**問題：** 創建一個長度為 10 的數組，所有元素為 0，然後將第 5 個元素設為 1。  

**標準答案：**
```python
import numpy as np

array = np.zeros(10)  # 創建全為 0 的數組
array[4] = 1  # 將第 5 個元素設為 1
print("數組：", array)
```

#### `pandas` 練習  
**問題：** 創建一個包含 3 位學生的 DataFrame，並計算分數的平均值。  

**標準答案：**
```python
import pandas as pd

data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Score": [85, 90, 95]
}
df = pd.DataFrame(data)
average_score = df["Score"].mean()
print("分數的平均值是：", average_score)
```

---


