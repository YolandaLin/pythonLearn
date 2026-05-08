# 第 11 週自我檢討：資料分析入門

## 交作業前檢查

- [ ] `survey.csv` 放在 `data` 資料夾裡。
- [ ] `analyze_survey.py` 可以成功讀取 CSV。
- [ ] 有印出前 5 筆、欄位名稱、資料筆數。
- [ ] 有回答平均睡眠、喜歡 Python 人數、各社團人數。
- [ ] learning-log.md 有至少兩個資料觀察。

## 常見錯誤

### 1. pandas 沒安裝

如果看到 `ModuleNotFoundError: No module named 'pandas'`，代表目前環境沒有 pandas。先執行：

```powershell
pip install pandas
```

### 2. 路徑錯誤

如果程式是：

```python
df = pd.read_csv("data/survey.csv")
```

請確認終端機目前位置在 `week11`。

### 3. 欄位名稱打錯

`likes_python` 和 `like_python` 是不同欄位。請先印出：

```python
print(df.columns)
```

### 4. 只貼結果，沒有解釋

資料分析不是只有程式輸出。請用自己的話寫觀察，例如「這份資料中音樂社有 3 位，是最多人的社團之一」。

## 修正方向

1. 先確認 pandas 能 import。
2. 再確認 CSV 路徑正確。
3. 先用 `print(df.head())` 看資料長什麼樣。
4. 每回答一個問題，就在 learning-log.md 寫一句中文解釋。

## 延伸練習

把 `likes_python` 的 yes/no 統計成比例，例如喜歡 Python 的人佔全部幾成。