# 第 10 週作業：模組、套件與虛擬環境

## 本週目標

開始使用 Python 內建工具，理解「別人已經寫好的功能可以 import 進來」。這週以標準函式庫為主，第三方套件和虛擬環境先理解概念，不要求做很複雜的安裝。

## 本週主題

- `import`
- 標準函式庫：`random`、`datetime`、`math`
- 第三方套件是什麼
- `pip` 是什麼
- `venv` 為什麼存在
- `requirements.txt` 記錄專案需要的套件

## 範例 1：random

```python
import random

choices = ["讀 20 分鐘書", "整理桌面", "散步 10 分鐘"]
print(random.choice(choices))
```

## 範例 2：datetime

```python
from datetime import date

today = date.today()
print(today)
```

## 必做作業

### hw1：幸運任務抽籤

建立 `lucky_task.py`。

建立一個 list，放入至少 6 個小任務，例如讀書、運動、整理書包。使用 `random.choice()` 隨機抽出一個任務。

### hw2：猜數字隨機版

建立 `random_guess.py`。

把第 3 週的猜數字改成答案隨機產生，範圍是 1 到 100。

### hw3：倒數日工具

建立 `days_until.py`。

使用 `datetime` 計算今天距離某個固定日期還有幾天，例如段考、生日、畢業日。

先把目標日期寫在程式裡，不需要讓使用者輸入日期。

### hw4：環境紀錄

建立 `environment.md`。

請記錄：

1. 你的 Python 版本。
2. 什麼是標準函式庫？
3. 什麼是第三方套件？
4. `pip` 的用途是什麼？
5. `venv` 想解決什麼問題？

### hw5：requirements.txt

建立 `requirements.txt`。

如果本週沒有使用第三方套件，請保持空白，或寫註解說明：

```text
# 本週只使用 Python 標準函式庫，沒有第三方套件
```

## 繳交內容

請建立一個 `week10` 資料夾，至少包含：

- `lucky_task.py`
- `random_guess.py`
- `days_until.py`
- `environment.md`
- `requirements.txt`
- `README.md`：貼上執行結果。
- `learning-log.md`

## 自我檢測

- [ ] 我知道 `import` 是把別的工具拿進來用。
- [ ] 我能分辨標準函式庫和第三方套件。
- [ ] 我知道本週不一定需要安裝套件。
- [ ] 我知道 `requirements.txt` 是給專案環境使用的紀錄。
- [ ] 我知道 `venv` 可以避免不同專案套件互相影響。

## 挑戰題

建立一個虛擬環境並在 README 記錄你執行過的指令。若電腦環境卡住，可以先寫下卡在哪一步，不強迫完成。