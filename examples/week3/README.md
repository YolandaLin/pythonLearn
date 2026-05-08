# 第 3 週自我檢討：迴圈與重複工作

## 交作業前檢查

- [ ] `countdown.py` 輸入 `5` 時會從 5 印到 1。
- [ ] `stars.py` 輸入 `3` 時會印出 3 行星星。
- [ ] `sum_to_n.py` 已測試 `1`、`5`、`10`。
- [ ] `guess.py` 猜大、猜小、猜對都有不同回應。
- [ ] README 有貼上執行指令與測試結果。

## 常見錯誤

### 1. range 結尾不包含最後一個數

```python
for i in range(1, 5):
    print(i)
```

會印出 1、2、3、4，不會印出 5。

如果要印 1 到 n，通常會寫：

```python
for i in range(1, n + 1):
    print(i)
```

### 2. 忘記更新 while 條件

```python
number = 1
while number <= 5:
    print(number)
```

這會一直印 1，因為 `number` 沒有改變。要記得：

```python
number = number + 1
```

### 3. 累加器放錯位置

`total = 0` 應該放在迴圈外面。如果放在迴圈裡，每一圈都會重新變成 0。

### 4. 還沒轉成整數就拿來比較

`input()` 拿到的是字串，要先 `int()` 才能做數字比較。

## 修正方向

1. 先手寫迴圈表格：第幾圈、變數值、total 值。
2. 如果 while 停不下來，先檢查停止條件有沒有機會變成 False。
3. 寫猜數字時，先固定答案，不要一開始就加 random。
4. 測試資料先小一點，例如 `3`、`5`，方便自己追蹤。

## 延伸練習

把 `sum_to_n.py` 改成只加偶數，並在 learning-log.md 寫下你怎麼判斷偶數。