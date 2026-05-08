# 第 2 週自我檢討：條件判斷

## 交作業前檢查

- [ ] `umbrella.py` 輸入 `yes`、`no`、其他文字時都有合理回應。
- [ ] `adult.py` 已測試 `17`、`18`、`19`。
- [ ] `password.py` 有測試正確密碼與錯誤密碼。
- [ ] `grade.py` 已測試 `-1`、`0`、`59`、`60`、`89`、`90`、`101`。
- [ ] README 有貼上測試資料與執行結果。
- [ ] learning-log.md 有回答簡答題。

## 常見錯誤

### 1. 把 `=` 和 `==` 搞混

錯誤寫法：

```python
if password = "python123":
    print("登入成功")
```

比較是否相等要用 `==`：

```python
if password == "python123":
    print("登入成功")
```

### 2. 忘記把輸入轉成數字

```python
age = input("年齡：")
if age >= 18:
    print("已成年")
```

`input()` 拿到的是字串，要先轉成整數：

```python
age_text = input("年齡：")
age = int(age_text)
if age >= 18:
    print("已成年")
```

### 3. 邊界值寫錯

如果成年規則是「18 歲以上」，條件應該是：

```python
if age >= 18:
```

不是：

```python
if age > 18:
```

因為 `> 18` 不包含剛好 18 歲。

### 4. `elif` 順序錯誤

成績判斷建議從高分往低分寫：

```python
if score > 100 or score < 0:
    print("分數範圍錯誤")
elif score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
elif score >= 60:
    print("D")
else:
    print("F")
```

如果順序亂掉，可能 95 分不會進到 A。

### 5. 縮排不一致

Python 用縮排判斷哪些程式屬於 `if`。建議每一層固定使用 4 個空白，不要混用 Tab 和空白。

## 修正方向

1. 先用最簡單資料測，例如 `18`、正確密碼、`yes`。
2. 再測邊界資料，例如 `17`、`18`、`19`。
3. 每次新增一個 `elif`，就重新執行一次。
4. README 要保留測試資料，因為測試資料能證明你的條件有處理到。

## 延伸練習

把 `grade.py` 加上更清楚的回應，例如：

```text
你的分數是 85，等第是 B
```

如果學生已經穩定完成，再挑戰 `ticket.py` 的多區間判斷。