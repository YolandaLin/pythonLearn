# 第 10 週自我檢討：模組、套件與虛擬環境

## 交作業前檢查

- [ ] `lucky_task.py` 每次執行可能抽到不同任務。
- [ ] `random_guess.py` 的答案是 1 到 100 的隨機數。
- [ ] `days_until.py` 能印出距離目標日期的天數。
- [ ] `environment.md` 有說明標準函式庫、第三方套件、pip、venv。
- [ ] `requirements.txt` 有正確說明本週是否使用第三方套件。

## 常見錯誤

### 1. 檔名和標準函式庫撞名

不要把檔案命名為 `random.py` 或 `datetime.py`，否則可能影響 import。

### 2. 忘記 import

使用 `random.choice()` 前要先：

```python
import random
```

### 3. 日期相減方向寫反

如果想算距離未來日期還有幾天，通常是：

```python
days = target_date - today
```

### 4. 以為所有東西都要 pip install

`random`、`datetime`、`math` 是標準函式庫，不需要安裝。

## 修正方向

1. 先確認檔名沒有和模組同名。
2. import 寫在檔案最上方。
3. 日期先用固定值，不要一開始就處理使用者輸入。
4. requirements.txt 只記錄第三方套件，不記錄標準函式庫。

## 延伸練習

把 `lucky_task.py` 改成抽完後問使用者是否再抽一次。