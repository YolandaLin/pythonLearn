# 第 1 週自我檢討：輸出、輸入與變數

## 交作業前檢查

- [ ] 我能用終端機執行 `python hello_me.py`。
- [ ] 我的檔名真的以 `.py` 結尾，不是 `.py.txt`。
- [ ] `name_card.py` 會詢問姓名、學校與興趣。
- [ ] `next_age.py` 輸入 `16` 時會輸出明年 `17` 歲。
- [ ] README 有貼上至少一組執行指令與執行結果。
- [ ] learning-log.md 有回答簡答題。

## 常見錯誤

### 1. 忘記加引號

錯誤寫法：

```python
print(你好)
```

Python 會以為 `你好` 是變數名稱。文字要加引號：

```python
print("你好")
```

### 2. 把數字當文字相加

```python
age = input("你今年幾歲？")
print(age + 1)
```

`input()` 拿到的是字串，所以要先轉成整數：

```python
age_text = input("你今年幾歲？")
age = int(age_text)
print(age + 1)
```

### 3. 終端機位置不對

如果出現找不到檔案，先用：

```powershell
dir
```

確認目前資料夾裡真的有你的 `.py` 檔。

### 4. 變數名稱太隨便

不建議：

```python
a = input("姓名：")
b = input("學校：")
```

比較好：

```python
name = input("姓名：")
school = input("學校：")
```

## 修正方向

1. 每次只改一個錯誤，改完重新執行。
2. 錯誤訊息先找自己的檔名和行號。
3. 變數名稱要讓一週後的自己也看得懂。
4. README 不只寫「完成」，要寫指令與輸出結果。

## 延伸練習

把 `name_card.py` 多加兩個欄位，例如喜歡的科目、最想做的 Python 作品。先不要追求畫面漂亮，重點是能正確輸入與輸出。