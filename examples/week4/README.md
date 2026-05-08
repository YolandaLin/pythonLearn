# 第 4 週自我檢討：函式與問題拆解

## 交作業前檢查

- [ ] 每個函式名稱都能看出用途。
- [ ] 每個函式至少有一個 `return`。
- [ ] `temperature.py` 有測試 0 度、100 度、32 華氏。
- [ ] `number_tools.py` 每個函式至少測試三組資料。
- [ ] README 有貼上測試呼叫與輸出結果。

## 常見錯誤

### 1. 只 print，沒有 return

```python
def c_to_f(celsius):
    print(celsius * 9 / 5 + 32)
```

這樣函式只是印出結果，沒有把結果交回去。通常工具型函式應該：

```python
def c_to_f(celsius):
    return celsius * 9 / 5 + 32
```

### 2. 參數名稱不清楚

不建議：

```python
def c_to_f(x):
    return x * 9 / 5 + 32
```

比較清楚：

```python
def c_to_f(celsius):
    return celsius * 9 / 5 + 32
```

### 3. 忘記呼叫函式

定義函式不代表它會自動執行。你還需要：

```python
print(c_to_f(30))
```

### 4. 把 input 寫進每個函式

這週的重點是練習「函式收到參數、回傳結果」。先不要急著把 `input()` 放進函式裡。

## 修正方向

1. 先寫函式，再在下面用固定資料測試。
2. 測試資料要包含容易心算的值，例如 0、1、60、100。
3. 如果函式名稱看不懂，先改名稱，不要急著加註解。
4. 每個函式只做一件明確的事。

## 延伸練習

把 `number_tools.py` 多加一個 `is_passing(score)`，並測試 59、60、100。