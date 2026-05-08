# 第 9 週作業：錯誤處理與除錯

## 本週目標

學會讀錯誤訊息、定位問題，並讓程式遇到常見錯誤時不要直接中斷。這週不是要寫更難的功能，而是把前面寫過的程式變穩定。

## 本週主題

- traceback：錯誤訊息中的檔名與行號
- 常見錯誤：`SyntaxError`、`NameError`、`ValueError`、`ZeroDivisionError`、`FileNotFoundError`
- `try` / `except`
- `print()` 除錯
- 最小可重現範例
- 防呆輸入

## 範例 1：處理輸入非數字

```python
age_text = input("請輸入年齡：")

try:
    age = int(age_text)
    print(f"你明年 {age + 1} 歲")
except ValueError:
    print("請輸入整數")
```

## 範例 2：除以 0

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("不能除以 0")
```

## 必做作業

### hw1：錯誤訊息觀察

建立 `error_notes.md`。

請故意製造並記錄三種錯誤：

- `SyntaxError`
- `NameError`
- `ValueError`

每一種錯誤請寫：

1. 你寫了哪一小段錯誤程式。
2. 錯誤訊息中的檔名與行號在哪裡。
3. 錯誤原因是什麼。
4. 你怎麼修好。

### hw2：安全年齡輸入

建立 `safe_age.py`。

讓使用者輸入年齡，輸出明年幾歲。如果輸入不是整數，請印出 `請輸入整數年齡`。

README 請測試：`16`、`abc`、空白。

### hw3：安全除法

建立 `safe_divide.py`。

讓使用者輸入兩個數字，輸出相除結果。

需要處理：

- 使用者輸入非數字
- 除數是 0

### hw4：修好舊作業

從第 1-8 週挑一個自己寫過的程式，幫它加上至少一個錯誤處理，並在 README 說明你改了什麼。

### hw5：簡答題

請寫在 `learning-log.md`：

1. traceback 裡哪兩個資訊最重要？
2. `ValueError` 通常什麼時候會發生？
3. 為什麼不建議寫空白的 `except:`？
4. 什麼是最小可重現範例？

## 繳交內容

請建立一個 `week9` 資料夾，至少包含：

- `error_notes.md`
- `safe_age.py`
- `safe_divide.py`
- 一個修好的舊作業程式
- `README.md`：貼上測試資料與結果。
- `learning-log.md`

## 自我檢測

- [ ] 我能從 traceback 找到檔名與行號。
- [ ] 我知道 `ValueError` 和 `ZeroDivisionError` 的差別。
- [ ] 我知道不要用空白 `except:` 吃掉所有錯誤。
- [ ] 我能把問題縮小成一小段程式測試。
- [ ] 我會在 README 記錄錯誤輸入的測試結果。

## 挑戰題

把 `safe_age.py` 改成如果使用者輸入錯誤，就重複要求輸入，直到輸入正確整數為止。