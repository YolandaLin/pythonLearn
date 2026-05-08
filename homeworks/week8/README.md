# 第 8 週作業：檔案讀寫與資料保存

## 本週目標

讓程式能把資料存起來，也能下次再讀回來。前幾週資料都只存在程式執行期間，程式關掉就消失；這週開始使用文字檔與 CSV。

## 本週主題

- 文字檔 `.txt`
- CSV 檔 `.csv`
- `with open(...)`
- 讀取模式 `r`
- 寫入模式 `w`
- 追加模式 `a`
- 相對路徑
- 檔案不存在時的錯誤

## 建議資料夾結構

請在 `week8` 裡建立：

```text
week8/
├── notes.py
├── read_notes.py
├── read_scores.py
├── data/
│   ├── notes.txt
│   └── scores.csv
├── README.md
└── learning-log.md
```

## 範例 1：寫入文字檔

```python
with open("data/notes.txt", "a", encoding="utf-8") as file:
    file.write("今天學會檔案寫入\n")
```

## 範例 2：讀取文字檔

```python
with open("data/notes.txt", "r", encoding="utf-8") as file:
    content = file.read()

print(content)
```

## 必做作業

### hw1：新增筆記

建立 `notes.py`。

讓使用者輸入一行學習筆記，追加寫入 `data/notes.txt`。

每次執行都不應該覆蓋舊筆記。

### hw2：讀取筆記

建立 `read_notes.py`。

讀取 `data/notes.txt`，印出所有筆記內容。

如果檔案不存在，請先手動建立空白的 `data/notes.txt`。

### hw3：讀取成績 CSV

建立 `data/scores.csv`，內容如下：

```csv
name,score
小明,80
小華,95
小美,70
```

建立 `read_scores.py`，讀取 CSV 並輸出：

- 每位學生姓名與分數
- 全班平均

可以先用 `split(",")` 處理，不需要使用 pandas。

### hw4：簡答題

請寫在 `learning-log.md`：

1. `r`、`w`、`a` 三種模式差在哪裡？
2. 為什麼建議使用 `with open(...)`？
3. 什麼是相對路徑？
4. 如果程式找不到檔案，你會先檢查哪三件事？

## 繳交內容

請建立一個 `week8` 資料夾，至少包含：

- `notes.py`
- `read_notes.py`
- `read_scores.py`
- `data/notes.txt`
- `data/scores.csv`
- `README.md`：貼上執行結果。
- `learning-log.md`

## 自我檢測

- [ ] 我知道 `w` 會覆蓋原本檔案。
- [ ] 我知道 `a` 會追加到檔案最後。
- [ ] 我能用 `encoding="utf-8"` 避免中文亂碼。
- [ ] 我知道相對路徑是從目前執行位置出發。
- [ ] 我能讀取 CSV 並拆出欄位。

## 挑戰題

把 `notes.py` 改成每一筆筆記前面加上日期。

提示：可以先查 Python 的 `datetime` 標準函式庫。