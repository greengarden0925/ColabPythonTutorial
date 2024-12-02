# Python 入門教學
# 目錄
- [1. Python 簡介](#1-python-簡介)
  - [歷史](#歷史)
  - [特點](#特點)
  - [示例程式碼](#示例程式碼打印-hello-world)
- [2. 基本語法](#2-基本語法)
  - [資料型別與變數](#資料型別與變數)
  - [示例程式碼](#示例程式碼定義變數並打印)
- [3. 控制結構](#3-控制結構)
  - [條件語句](#條件語句)
  - [示例程式碼](#示例程式碼判斷數字是否為偶數)
- [4. 函式與模組](#4-函式與模組)
  - [函式](#函式)
  - [示例程式碼](#示例程式碼計算兩個數字的和)
- [5. 資料結構](#5-資料結構)
  - [列表操作](#列表操作)
  - [示例程式碼](#示例程式碼操作列表)

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

### 條件語句
Python 使用 `if`、`elif` 和 `else` 來實現條件分支。

### 示例程式碼：判斷數字是否為偶數
```python
# 判斷數字是否為偶數
number = 4
if number % 2 == 0:
    print(f"{number} is even.")
else:
    print(f"{number} is odd.")
```

#### 註解說明：
- `number % 2 == 0`：判斷數字是否能被 2 整除。
- `f"{number}"`：格式化字串，用於動態插入變數值。

### 練習題：
1. 編寫程式碼判斷一個數字是否為正數、負數或零。

#### 提示：
- 使用多個條件分支。

#### 標準答案：
```python
number = -5
if number > 0:
    print("Positive number")
elif number < 0:
    print("Negative number")
else:
    print("Zero")
```

# 控制結構教案

本教案適合大學生學習 Python 中的控制結構，涵蓋條件語句、迴圈、以及循環控制語句的基礎應用。

---

## 1. 條件語句（if、elif、else）

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

## 2. 迴圈（for 和 while）

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

## 3. 循環控制語句（break、continue、pass）

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
# 控制結構教案

本教案適合大學生學習 Python 中的控制結構，涵蓋條件語句、迴圈、以及循環控制語句的基礎應用。

---

## 1. 條件語句（if、elif、else）

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

## 2. 迴圈（for 和 while）

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

## 3. 循環控制語句（break、continue、pass）

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

希望這份教案能幫助學生理解並掌握控制結構的基本概念與應用！ 🎓


---

## 4. 函式與模組

### 函式
函式是一段可以重複使用的代碼，使用 `def` 關鍵字定義。

### 示例程式碼：計算兩個數字的和
```python
# 定義函式
def add_numbers(a, b):
    return a + b

# 呼叫函式並打印結果
result = add_numbers(3, 5)
print("Sum:", result)
```

#### 註解說明：
- `def add_numbers(a, b):`：定義一個接受兩個參數的函式。
- `return`：將計算結果返回給調用者。

### 練習題：
1. 編寫函式計算一個數的平方，並測試該函式。

#### 提示：
- 使用 `return` 返回結果。

#### 標準答案：
```python
# 定義函式
def square_number(x):
    return x ** 2

# 測試函式
result = square_number(4)
print("Square:", result)
```

---

## 5. 資料結構

### 列表操作
列表（`list`）是 Python 中的可變序列，用於存儲多個值。

### 示例程式碼：操作列表
```python
# 定義列表
fruits = ["apple", "banana", "cherry"]

# 添加元素
fruits.append("date")

# 刪除元素
fruits.remove("banana")

# 打印列表
print("Fruits:", fruits)
```

#### 註解說明：
- `append()`：在列表末尾添加元素。
- `remove()`：移除指定的元素。

### 練習題：
1. 定義一個包含五個數字的列表，計算列表中所有數字的總和。

#### 提示：
- 使用 `sum()` 函式計算總和。

#### 標準答案：
```python
numbers = [1, 2, 3, 4, 5]
total = sum(numbers)
print("Total:", total)
```
