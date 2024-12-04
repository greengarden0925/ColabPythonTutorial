# YOLO 影像辨識基礎應用（使用 YOLOv8 或 YOLOv9）
---
## 目錄
1. [YOLO 模型簡介](#1-yolo-模型簡介)  
   - [1.1 YOLO 演算法基礎與應用概述](#11-yolo-演算法基礎與應用概述)  
     - [什麼是 YOLO？](#什麼是-yolo)  
     - [應用場景](#應用場景)  
   - [1.2 安裝與設置 YOLOv8 或 YOLOv9](#12-安裝與設置-yolov8-或-yolov9)  
     - [步驟 1：安裝 YOLOv8](#步驟-1安裝-yolov8)  

2. [YOLO 實作應用](#2-yolo-實作應用)  
   - [2.1 透過 Colab 加載預訓練模型](#21-透過-colab-加載預訓練模型)  
     - [步驟 1：下載範例檔案](#步驟-1下載範例檔案)  
     - [步驟 2：加載預訓練模型](#步驟-2加載預訓練模型)  
     - [步驟 3：保存檢測結果](#步驟-3保存檢測結果)  
   - [2.2 使用 YOLOv8 進行影像物件辨識](#22-使用-yolov8-進行影像物件辨識)  
     - [步驟 1：檢測多張圖片](#步驟-1檢測多張圖片)  
     - [步驟 2：下載檢測結果](#步驟-2下載檢測結果)  
   - [2.3 實現即時影像辨識](#23-實現即時影像辨識)  
     - [步驟 1：即時影像檢測](#步驟-1即時影像檢測)  
     - [步驟 2：檢測影片](#步驟-2檢測影片)  
   - [綜合練習](#綜合練習)  

---
## **1. YOLO 模型簡介**

### **1.1 YOLO 演算法基礎與應用概述**  

#### **什麼是 YOLO？**
- YOLO（**You Only Look Once**）是一種實時物件檢測演算法。
- **YOLOv8/YOLOv9** 是最新版本，具有更高準確率和更快的檢測速度。
  - **YOLOv8/YOLOv9 優勢**：
    - 更高的計算效能，支持更大的模型和多樣的應用場景。
    - 提供對 CPU 和 GPU 的高效支持。

#### **應用場景**
- **安防監控**：人物與車輛辨識。
- **醫療影像**：腫瘤檢測。
- **零售業務**：商品追蹤與統計。
- **智慧城市**：車輛流量分析。

---

### **1.2 安裝與設置 YOLOv8 或 YOLOv9**

#### **步驟 1：安裝 YOLOv8**
1. 在 [Google Colab](https://colab.research.google.com) 中執行以下指令：
   ```bash
   !pip install ultralytics
   ```
   YOLOv8 安裝完成後，`ultralytics` 提供完整的模型支援。

2. 驗證安裝：
   ```python
   from ultralytics import YOLO
   print("YOLOv8 已安裝成功！")
   ```

---

## **2. YOLO 實作應用**

### **2.1 透過 Colab 加載預訓練模型**

#### **步驟 1：下載範例檔案**
使用網路上提供的開放資料集，以下是範例圖片的下載指令：
```bash
!wget https://ultralytics.com/images/bus.jpg -O bus.jpg
!wget https://ultralytics.com/images/zidane.jpg -O zidane.jpg

#顯示圖片
import matplotlib.pyplot as plt
import cv2
def show_image(image_path):
    image = cv2.imread(image_path)
    image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
    plt.imshow(image)
    plt.axis('off')  # Hide axis
    plt.show()

show_image('bus.jpg')
show_image('zidane.jpg')

```

#### **步驟 2：加載預訓練模型**
使用 YOLOv8 的預訓練權重進行物件檢測：
```python
from ultralytics import YOLO
from google.colab.patches import cv2_imshow

# 加載預訓練模型
model = YOLO('yolov8s.pt')  # 使用 YOLOv8 的 Small 模型

# 檢測圖片
results = model('bus.jpg', conf=0.4)

# 顯示檢測結果
cv2_imshow(results[0].plot())
```
建立圖片偵測函示
```python
#建立輸入圖片判斷物件並顯示的函示
def detectShow(image_path,conf):
  results = model(image_path, conf=conf, stream=False)  # Modified to return a single Results object
  cv2_imshow(results[0].plot())

detectShow("zidane.jpg",conf=0.8)
```


### **2.2 使用 YOLOv8 進行影像物件辨識**

#### **步驟 1：檢測多張圖片**
一次處理多張影像：
```python
results = model(['bus.jpg', 'zidane.jpg'], conf=0.5)
cv2_imshow(results[0].plot())
cv2_imshow(results[1].plot())
```
---

### **2.3 影像辨識**

#### **步驟 1：下載影片**
使用範例影片進行物件檢測，以下指令可下載測試影片：
```bash
#從google drive共享連結下載mp4檔案
!pip install gdown
import gdown

url = 'https://drive.google.com/uc?id=1BtSAUp92j1VkrNYTXvEW0dNSAdiUiYPn'

# 設定儲存的檔案路徑
output = 'input_video.mp4'

# 下載檔案
gdown.download(url, output, quiet=False)

#查看影片
import IPython.display as display
display.Video('input_video.mp4', embed=True)
```
#### **步驟 2：檢測影片**
執行影片檢測：
```python
# 輸入影片路徑
input_video = 'input_video.mp4'  # 替换为你上传的视频文件名

# 進行影片檢測
results = model(source=input_video)
```

查看影格
```python
cv2_imshow(results[10].plot())
cv2_imshow(results[180].plot())
```
---

### **綜合練習**

**問題：** 使用 YOLOv8 完成以下任務：
1. 上傳多張圖片進行檢測，嘗試調整 `conf` 值。
2. 下載並檢測範例影片，將檢測結果保存。
3. 實現即時影像辨識。

**標準答案：**
```python
# 1. 檢測多張圖片
results = model(['bus.jpg', 'zidane.jpg'], conf=0.5)

# 2. 檢測影片
results = model('input_video.mp4', conf=0.4)

```

---
