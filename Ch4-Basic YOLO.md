# YOLO 影像辨識基礎應用（使用 YOLOv8 或 YOLOv9）
---

## **1. YOLO 模型簡介**

### **1.1 YOLO 演算法基礎與應用概述**（10 分鐘）  

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

### **1.2 安裝與設置 YOLOv8 或 YOLOv9**（15 分鐘）

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

### **2.1 透過 Colab 加載預訓練模型**（20 分鐘）

#### **步驟 1：下載範例檔案**
使用網路上提供的開放資料集，以下是範例圖片的下載指令：
```bash
!wget https://ultralytics.com/images/bus.jpg -O bus.jpg
!wget https://ultralytics.com/images/zidane.jpg -O zidane.jpg
```

#### **步驟 2：加載預訓練模型**
使用 YOLOv8 的預訓練權重進行物件檢測：
```python
from ultralytics import YOLO

# 加載預訓練模型
model = YOLO('yolov8s.pt')  # 使用 YOLOv8 的 Small 模型

# 檢測圖片
results = model('bus.jpg', conf=0.4)

# 顯示檢測結果
results.show()
```

#### **步驟 3：保存檢測結果**
將檢測結果保存為圖片：
```python
results.save(save_dir='runs/detect/exp')  # 檢測結果保存於目錄下
```

---

### **2.2 使用 YOLOv8 進行影像物件辨識**（20 分鐘）

#### **步驟 1：檢測多張圖片**
一次處理多張影像：
```python
results = model(['bus.jpg', 'zidane.jpg'], conf=0.5)
results.show()
```

#### **步驟 2：下載檢測結果**
檢測結果將保存於 `runs/detect/exp` 目錄下，以下代碼可下載結果：
```python
from google.colab import files

files.download('runs/detect/exp/bus.jpg')
files.download('runs/detect/exp/zidane.jpg')
```

---

### **2.3 實現即時影像辨識**（25 分鐘）

#### **步驟 1：即時影像檢測**
啟用攝影機進行即時檢測（需本地執行環境支持攝影機）：
```python
results = model(source=0, conf=0.4)
results.show()
```

#### **步驟 2：檢測影片**
使用範例影片進行物件檢測，以下指令可下載測試影片：
```bash
!wget https://github.com/ultralytics/yolov5/releases/download/v1.0/bus.mp4 -O bus.mp4
```
執行影片檢測：
```python
results = model('bus.mp4', conf=0.4)
results.show()
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
results.save(save_dir='runs/detect/exp')

# 2. 檢測影片
results = model('bus.mp4', conf=0.4)
results.save(save_dir='runs/detect/exp_video')

# 3. 即時影像辨識
results = model(source=0, conf=0.4)
results.show()
```

---
