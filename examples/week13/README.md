# 第 13 週自我檢討：API 與網路資料

## 交作業前檢查

- [ ] `json_viewer.py` 能讀取 `data/profile.json`。
- [ ] `public_api.py` 有印出 status code。
- [ ] README 有貼上 API 回傳重點，或記錄網路錯誤。
- [ ] learning-log.md 有說明 request、response、200、404。

## 常見錯誤

### 1. JSON 格式少逗號或多逗號

JSON 格式比 Python 嚴格。每個欄位之間要有逗號，最後一個欄位後面不要多逗號。

### 2. 忘記 import json 或 requests

讀本地 JSON 需要：

```python
import json
```

呼叫網路 API 通常需要：

```python
import requests
```

### 3. 網路失敗不等於程式邏輯錯

API 可能因為網路、伺服器、限制次數而失敗。請先印出 status code 和錯誤訊息。

### 4. 直接假設欄位一定存在

API 回傳資料可能沒有你想要的欄位。可以先 print 整份資料，確認欄位名稱。

## 修正方向

1. 先完成本地 JSON，再做網路 API。
2. 每次讀到資料，先觀察型態是 dict 還是 list。
3. 呼叫 API 後先檢查 status code。
4. 不要把 token、API key、密碼貼到 README 或 GitHub。

## 延伸練習

把 GitHub API 回傳的資料整理成一段自我介紹文字。