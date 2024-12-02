# 介紹 Google Colab
---
[111](#註解說明)
1. [Google Colab 功能概述](#1.Google-Colab-功能概述)  
   - [示例程式碼：檢查環境中的硬件加速](#示例程式碼檢查環境中的硬件加速)  
   - [練習題：檢查當前是否可用 TPU](#練習題檢查當前是否可用-tpu)  

2. [界面導覽與環境設定](#2-界面導覽與環境設定)  
   - [示例程式碼：安裝並使用外部函式庫](#示例程式碼安裝並使用外部函式庫)  
   - [練習題：生成隨機數陣列並計算平均值](#練習題生成隨機數陣列並計算平均值)  

3. [如何保存、分享和運行筆記本](#3-如何保存分享和運行筆記本)  
   - [示例程式碼：保存筆記本內容到 Google Drive](#示例程式碼保存筆記本內容到-google-drive)  
   - [練習題：將列表保存為文本文件到 Google Drive](#練習題將列表保存為文本文件到-google-drive)  

---
##  1.Google Colab 功能概述

Google Colab 是一個基於雲端的 Python 編輯環境，特別適合用於數據科學和機器學習。其主要功能包括：

- **免費提供 GPU 和 TPU 資源**，支持高效的深度學習訓練。
- **支持即時協作**，可以與其他用戶共同編輯筆記本。
- **內建與 Google Drive 集成**，方便存儲和管理文件。
- **支持安裝自定義庫**，可靈活使用多種 Python 函式庫。

### 示例程式碼：檢查環境中的硬件加速
```python
# 檢查當前是否可用 GPU
import tensorflow as tf

def check_gpu():
    if tf.config.list_physical_devices('GPU'):
        print("GPU is available!")
    else:
        print("GPU is not available.")

check_gpu()  # 呼叫函數來檢查 GPU 狀態
```

#### 註解說明：
- `import tensorflow as tf`：匯入 TensorFlow 函式庫。
- `tf.config.list_physical_devices('GPU')`：檢查當前環境是否有 GPU。
- `check_gpu()`：運行該函數即可顯示 GPU 狀態。

### 練習題：
1. 使用 Python 編寫一段程式碼來檢查當前是否可用 TPU。

#### 提示：
- 使用 `tf.config.list_physical_devices('TPU')`。

#### 標準答案：
```python
# 檢查當前是否可用 TPU
import tensorflow as tf

def check_tpu():
    if tf.config.list_physical_devices('TPU'):
        print("TPU is available!")
    else:
        print("TPU is not available.")

check_tpu()
```

---

## 2.界面導覽與環境設定

Google Colab 的界面包含以下主要部分：
- **左側面板**：顯示檔案、變數和資源使用情況。
- **筆記本編輯區域**：可執行的代碼和 Markdown 文本。
- **工具列**：提供運行、保存和其他常見操作的功能。

### 示例程式碼：安裝並使用外部函式庫
```python
# 安裝 matplotlib 函式庫
!pip install matplotlib

# 匯入並繪製簡單圖表
import matplotlib.pyplot as plt

# 繪製折線圖
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]
plt.plot(x, y, marker='o')
plt.title("Simple Line Chart")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.grid()
plt.show()
```

#### 註解說明：
- `!pip install matplotlib`：使用 `!` 命令在 Google Colab 中安裝外部函式庫。
- `plt.plot()`：用於繪製折線圖。
- `plt.show()`：顯示圖表。

### 練習題：
1. 安裝並使用 `numpy` 函式庫，生成一個包含 10 個隨機數的陣列，並計算其平均值。

#### 提示：
- 使用 `!pip install numpy` 安裝。
- 使用 `numpy.mean()` 計算平均值。

#### 標準答案：
```python
# 安裝 numpy 函式庫
!pip install numpy

# 匯入並計算隨機數平均值
import numpy as np

random_array = np.random.rand(10)  # 生成包含 10 個隨機數的陣列
mean_value = np.mean(random_array)  # 計算平均值
print("Random Array:", random_array)
print("Mean Value:", mean_value)
```

---

## 3.如何保存、分享和運行筆記本

在 Google Colab 中，可以方便地保存和分享筆記本：
1. **保存**：點擊左上角的文件 > 另存為 > 選擇保存到本地或 Google Drive。
2. **分享**：點擊右上角的分享按鈕，設置權限後即可生成共享連結。
3. **運行**：使用快捷鍵 `Shift+Enter` 運行當前單元格。

### 示例程式碼：保存筆記本內容到 Google Drive
```python
# 授權訪問 Google Drive
from google.colab import drive

drive.mount('/content/drive')  # 將 Google Drive 掛載到 /content/drive

# 創建一個文本文件並保存到 Google Drive
with open('/content/drive/My Drive/sample.txt', 'w') as file:
    file.write("Hello, Google Drive!")

print("File saved to Google Drive.")
```

#### 註解說明：
- `drive.mount('/content/drive')`：將 Google Drive 掛載到 Colab 環境。
- `open()`：創建或打開文件，並寫入數據。

### 練習題：
1. 編寫代碼將一個包含數字的列表保存為文本文件到 Google Drive。

#### 提示：
- 使用 `open()` 方法將數據寫入文件。

#### 標準答案：
```python
# 掛載 Google Drive
from google.colab import drive

drive.mount('/content/drive')

# 保存數字列表到文本文件
numbers = [1, 2, 3, 4, 5]
with open('/content/drive/My Drive/numbers.txt', 'w') as file:
    file.write(', '.join(map(str, numbers)))

print("Numbers saved to Google Drive.")
