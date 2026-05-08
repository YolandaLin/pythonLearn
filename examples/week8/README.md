# 第 8 週自我檢討：檔案讀寫與資料保存

## 交作業前檢查

- [ ] `notes.py` 會把新筆記追加到 `data/notes.txt`。
- [ ] 重複執行 `notes.py` 不會清掉舊筆記。
- [ ] `read_notes.py` 可以印出所有筆記。
- [ ] `read_scores.py` 可以讀取 `data/scores.csv` 並算平均。
- [ ] README 有寫清楚檔案放在哪裡。

## 常見錯誤

### 1. 用 w 覆蓋檔案

```python
open("data/notes.txt", "w")
```

`w` 會覆蓋原本內容。要保留舊內容並加在最後，請用：

```python
open("data/notes.txt", "a")
```

### 2. 中文亂碼

讀寫中文檔案時建議加上：

```python
encoding="utf-8"
```

### 3. 找不到檔案

先檢查三件事：

1. 檔案是否真的存在。
2. 檔名是否完全一樣。
3. 終端機目前位置是否在 `week8`。

### 4. CSV 第一行是標題

`scores.csv` 第一行 `name,score` 是欄位名稱，不應該拿來計算平均。

## 修正方向

1. 先建立 `data` 資料夾，再執行程式。
2. 先用小檔案測試，不要一開始放大量資料。
3. 讀 CSV 時先逐行 print，確認自己讀到什麼。
4. 路徑錯誤時，先用 `dir` 看目前資料夾內容。

## 延伸練習

把 `read_scores.py` 改成找出最高分學生。