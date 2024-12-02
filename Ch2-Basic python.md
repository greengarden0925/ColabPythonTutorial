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
