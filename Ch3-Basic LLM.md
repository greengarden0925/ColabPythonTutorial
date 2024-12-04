# 大型語言模型 (LLM) 入門
---
## 目錄
1. [大型語言模型基礎概念](#1-大型語言模型基礎概念)  
   - [1.1 大型語言模型的介紹及用途](#11-大型語言模型的介紹及用途10-分鐘)  
     - [什麼是大型語言模型（LLM）？](#什麼是大型語言模型llm)  
     - [用途與應用場景](#用途與應用場景)  
   - [1.2 OpenAI GPT API 的基本架構與申請流程](#12-openai-gpt-api-的基本架構與申請流程15-分鐘)  
     - [API 架構](#api-架構)  
     - [申請 OpenAI API 流程](#申請-openai-api-流程)  

2. [實作應用](#2-實作應用)  
   - [2.1 使用 Python 與 Colab 連接 OpenAI API](#21-使用-python-與-colab-連接-openai-api20-分鐘)  
     - [步驟 1：設定環境](#步驟-1設定環境)  
     - [步驟 2：連接 API](#步驟-2連接-api)  
   - [2.2 簡單文本生成應用](#22-簡單文本生成應用20-分鐘)  
     - [範例應用：自動文案生成](#範例應用自動文案生成)  
   - [2.3 簡易問答系統開發與調整](#23-簡易問答系統開發與調整15-分鐘)  
     - [步驟 1：設計問答系統](#步驟-1設計問答系統)  
     - [步驟 2：改進問答系統](#步驟-2改進問答系統)  
   - [綜合練習](#綜合練習)  

---
## **1. 大型語言模型基礎概念**  

### **1.1 大型語言模型的介紹及用途**（10 分鐘）  

#### **什麼是大型語言模型（LLM）？**
- LLM 是基於深度學習技術的自然語言處理模型，擁有數十億參數，能理解和生成自然語言。
- 其主要能力包括：
  - **文本生成**：撰寫文章、故事或對話。
  - **問答系統**：解答問題。
  - **文本摘要**：提取關鍵內容。
  - **翻譯**：多語言文本轉換。

#### **用途與應用場景**
- **商業應用**：
  - 客服系統。
  - 市場文案生成。
- **教育與學術**：
  - 自動批改作業。
  - 知識問答與輔導。
- **科技開發**：
  - 原型設計。
  - API 集成。

---

### **1.2 OpenAI GPT API 的基本架構與申請流程**（15 分鐘）  

#### **API 架構**
- **端點（Endpoint）**：通過 API 請求的 URL。
  - 常用端點如 `https://api.openai.com/v1/chat/completions`。
- **請求參數**：
  - **`model`**：選擇 GPT 模型（如 `gpt-4` 或 `gpt-3.5-turbo`）。
  - **`messages`**：對話上下文，包括角色與消息內容。
  - **`temperature`**：控制生成的隨機性（0-1 範圍）。
- **返回值**：
  - 模型生成的文本與相關元數據。

#### **申請 OpenAI API 流程**
1. 訪問 [OpenAI 官網](https://platform.openai.com/)。
2. 註冊帳戶，完成驗證。
3. 進入管理界面，生成 API 金鑰。
   - **注意：** 保管好金鑰，切勿公開分享。

---

## **2. 實作應用**  

### **2.1 使用 Python 與 Colab 連接 OpenAI API**（20 分鐘）  

#### **步驟 1：設定環境**
1. 打開 [Google Colab](https://colab.research.google.com/)。
2. 安裝 OpenAI Python 客戶端：
   ```bash
   !pip install openai
   ```

#### **步驟 2：連接 API**
```python
import os
from openai import OpenAI

client = OpenAI(
    api_key="你的_API_金鑰",  # This is the default and can be omitted
)

# 測試請求
response = openai.ChatCompletion.create(
    model="gpt-3.5-turbo",
    messages=[
        {"role": "system", "content": "你是一個友好的助理。"},
        {"role": "user", "content": "你好！"}
    ]
)

print("回應：", response["choices"][0]["message"]["content"])
```

---

### **2.2 簡單文本生成應用**（20 分鐘）  

#### **範例應用：自動文案生成**
1. 輸入主題關鍵詞，生成廣告文案：
```python
def generate_ad_copy(topic):
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[
            {"role": "system", "content": "你是一個專業的文案撰寫助理。"},
            {"role": "user", "content": f"幫我為 {topic} 撰寫一段廣告文案。"}
        ]
    )
    return response["choices"][0]["message"]["content"]

# 測試文案生成
topic = "環保飲品"
print(generate_ad_copy(topic))
```

---

### **2.3 簡易問答系統開發與調整**（15 分鐘）  

#### **步驟 1：設計問答系統**
```python
def chatbot(user_input):
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[
            {"role": "system", "content": "你是一個博學的助手。"},
            {"role": "user", "content": user_input}
        ]
    )
    return response["choices"][0]["message"]["content"]

# 測試問答
question = "Python 的主要用途是什麼？"
print("回答：", chatbot(question))
```

#### **步驟 2：改進問答系統**
- **添加上下文**：將之前的對話記錄傳入 `messages`。
- **控制生成品質**：調整 `temperature`。

---

### **綜合練習**
**問題：** 開發一個簡易的問答應用，允許用戶輸入問題並獲取模型的回答，並加入提示引導功能。  

**標準答案：**
```python
def interactive_chatbot():
    print("歡迎使用簡易問答系統！輸入 '退出' 結束對話。")
    while True:
        user_input = input("你問：")
        if user_input.lower() == "退出":
            print("感謝使用，再見！")
            break
        response = chatbot(user_input)
        print("助理回答：", response)

interactive_chatbot()
```

---

