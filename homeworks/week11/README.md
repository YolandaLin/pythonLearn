# 第 11 週作業：資料分析入門

## 本週目標

用 Python 讀表格，回答一個具體問題。這是進階應用週，重點不是背 pandas，而是學會「先問問題，再用資料回答」。

## 本週主題

- CSV 表格資料
- pandas DataFrame
- 讀取 CSV
- 查看前幾筆資料
- 選欄位
- 計算平均與人數
- 用文字寫觀察

## 安裝提醒

這週需要 pandas：

```powershell
pip install pandas
```

如果安裝卡住，請先記錄錯誤訊息，老師可以協助處理。不要把環境問題和資料分析問題混在一起。

## 建議資料夾結構

```text
week11/
├── analyze_survey.py
├── data/
│   └── survey.csv
├── README.md
└── learning-log.md
```

## 範例資料

建立 `data/survey.csv`：

```csv
name,grade,sleep_hours,club,likes_python
小明,高一,6,籃球,yes
小華,高一,7,音樂,yes
小美,高二,5,美術,no
小安,高二,8,籃球,yes
小君,高三,6,科學,no
小杰,高一,7,音樂,yes
小婷,高二,6,美術,yes
小宇,高三,5,籃球,no
小萱,高一,8,科學,yes
小哲,高三,7,音樂,no
```

## 必做作業

### hw1：讀取資料

建立 `analyze_survey.py`，讀取 `data/survey.csv`，印出：

- 前 5 筆資料
- 所有欄位名稱
- 總共有幾筆資料

### hw2：回答三個問題

用 pandas 回答：

1. 平均睡眠時數是多少？
2. 喜歡 Python 的人有幾位？
3. 每個社團各有幾位學生？

### hw3：寫資料觀察

在 `learning-log.md` 寫出至少兩個觀察，例如：

- 這份資料中，高一學生有幾位。
- 睡眠時數最高是多少。
- 喜歡 Python 的比例大約是多少。

### hw4：簡答題

請寫在 `learning-log.md`：

1. DataFrame 可以想像成什麼？
2. 什麼是欄位？什麼是一列資料？
3. 為什麼資料分析要先問問題？
4. 你覺得這份資料有哪些限制？

## 繳交內容

請建立一個 `week11` 資料夾，至少包含：

- `analyze_survey.py`
- `data/survey.csv`
- `README.md`：貼上分析結果。
- `learning-log.md`

## 自我檢測

- [ ] 我能用 pandas 讀取 CSV。
- [ ] 我能印出前 5 筆資料。
- [ ] 我能選出單一欄位。
- [ ] 我能計算平均或人數。
- [ ] 我能用文字說明資料觀察，而不是只貼程式輸出。

## 挑戰題

新增一欄 `study_hours`，記錄每天讀書時數，分析睡眠和讀書時數是否看起來有關係。只需要描述觀察，不需要做統計推論。