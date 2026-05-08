# 第 13 週作業：API 與網路資料

## 本週目標

理解程式可以讀取 JSON 資料，也可以從網路 API 取得資料。完全初學者先從本地 JSON 開始，再進到網路，避免被網路連線問題卡住。

## 本週主題

- request 與 response
- HTTP 狀態碼
- JSON
- Python 的 dict / list
- `requests` 第三方套件
- API key 安全觀念

## 安裝提醒

這週若要呼叫網路 API，需要 requests：

```powershell
pip install requests
```

## 建議資料夾結構

```text
week13/
├── json_viewer.py
├── public_api.py
├── data/
│   └── profile.json
├── README.md
└── learning-log.md
```

## 必做作業

### hw1：讀取本地 JSON

建立 `data/profile.json`：

```json
{
  "name": "小明",
  "grade": "高一",
  "skills": ["Python", "資料整理", "簡報"],
  "favorite_subject": "數學"
}
```

建立 `json_viewer.py`，讀取這個 JSON，輸出：

- 姓名
- 年級
- 最喜歡的科目
- 所有技能

### hw2：觀察 JSON 結構

在 `learning-log.md` 寫：

1. JSON 的 `{}` 讀進 Python 後像什麼？
2. JSON 的 `[]` 讀進 Python 後像什麼？
3. `skills` 這個欄位為什麼適合用 list？

### hw3：呼叫免 key API

建立 `public_api.py`。

使用一個不需要 API key 的公開 API，例如 GitHub 使用者 API：

```text
https://api.github.com/users/octocat
```

程式要印出：

- status code
- login
- public_repos
- html_url

如果網路失敗，請在 README 記錄錯誤，不要硬改到看不懂。

### hw4：簡答題

請寫在 `learning-log.md`：

1. request 和 response 是什麼？
2. HTTP 200 大概代表什麼？404 大概代表什麼？
3. 為什麼不能把 API key commit 到 GitHub？
4. 本地 JSON 和網路 API 的資料格式有什麼相似處？

## 繳交內容

請建立一個 `week13` 資料夾，至少包含：

- `json_viewer.py`
- `public_api.py`
- `data/profile.json`
- `README.md`：貼上執行結果或網路錯誤紀錄。
- `learning-log.md`

## 自我檢測

- [ ] 我能讀取本地 JSON。
- [ ] 我知道 JSON object 讀進 Python 後像 dict。
- [ ] 我知道 JSON array 讀進 Python 後像 list。
- [ ] 我知道 request 與 response 的基本概念。
- [ ] 我知道不要公開 API key。

## 挑戰題

讓使用者輸入 GitHub username，再查詢該使用者資料。請處理查不到使用者時的 404 狀態。