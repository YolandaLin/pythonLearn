# 第 4 週作業：函式與問題拆解

## 本週目標

學會把會重複使用的程式整理成函式。函式不是為了讓程式變難，而是讓程式可以「取名字、重複用、比較好測」。

## 本週主題

- `def`：定義函式
- 參數：函式需要的輸入
- `return`：把結果交回去
- `print()` 和 `return` 的差異
- 用多組資料測試同一個函式

## 範例 1：沒有函式的寫法

```python
c = 30
f = c * 9 / 5 + 32
print(f)
```

## 範例 2：整理成函式

```python
def c_to_f(celsius):
    return celsius * 9 / 5 + 32

print(c_to_f(30))
print(c_to_f(0))
```

函式的好處是：公式只要寫一次，可以測很多組資料。

## 必做作業

### hw1：問候函式

建立 `greeting.py`。

寫一個函式：

```python
def say_hello(name):
    return f"你好，{name}"
```

請用三個不同名字測試它。

### hw2：溫度轉換

建立 `temperature.py`。

請寫兩個函式：

- `c_to_f(celsius)`：攝氏轉華氏
- `f_to_c(fahrenheit)`：華氏轉攝氏

README 請測試：

- `c_to_f(0)` 應該是 32
- `c_to_f(100)` 應該是 212
- `f_to_c(32)` 應該是 0

### hw3：數字工具

建立 `number_tools.py`。

請寫三個函式：

- `is_even(number)`：偶數回傳 `True`，奇數回傳 `False`
- `max_of_two(a, b)`：回傳兩個數中比較大的
- `score_passed(score)`：分數大於等於 60 回傳 `True`，否則回傳 `False`

每個函式至少測試三組資料。

### hw4：簡答題

請寫在 `learning-log.md`：

1. 什麼情況適合寫成函式？
2. 參數是什麼？請用生活例子解釋。
3. `print()` 和 `return` 有什麼不同？
4. 你覺得哪一個函式名稱最清楚？為什麼？

## 繳交內容

請建立一個 `week4` 資料夾，至少包含：

- `greeting.py`
- `temperature.py`
- `number_tools.py`
- `README.md`：貼上每個函式的測試資料與結果。
- `learning-log.md`

## 自我檢測

- [ ] 我能用 `def` 定義函式。
- [ ] 我知道參數是函式的輸入。
- [ ] 我知道 `return` 是把結果交回呼叫函式的地方。
- [ ] 我能用三組資料測試同一個函式。
- [ ] 我不會把所有程式都塞進同一個大函式。

## 挑戰題

建立 `bmi_function.py`，把 BMI 計算整理成函式：

```python
def calculate_bmi(height_m, weight_kg):
    # 回傳 BMI
```

再用 `print()` 印出三組測試結果。