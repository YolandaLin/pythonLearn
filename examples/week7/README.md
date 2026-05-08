# 第 7 週自我檢討：Dictionary 與結構化資料

## 交作業前檢查

- [ ] `student_card.py` 有完整輸出學生摘要。
- [ ] `contacts.py` 查得到與查不到都有測試。
- [ ] `student_scores.py` 能找出最高分學生。
- [ ] README 有貼上測試資料與結果。

## 常見錯誤

### 1. key 寫錯就查不到

```python
student = {"name": "小明"}
print(student["Name"])
```

`name` 和 `Name` 不一樣。key 大小寫與文字都要完全相同。

### 2. 查不存在的 key 會出錯

```python
print(contacts["小王"])
```

如果沒有 `小王`，會出現 `KeyError`。可以先判斷：

```python
if name in contacts:
    print(contacts[name])
else:
    print("查無此人")
```

### 3. list 和 dict 混在一起時看不懂

看到：

```python
students[0]["name"]
```

先拆開想：`students[0]` 是第一位學生的 dict，`["name"]` 是拿這位學生的姓名。

### 4. dict 不是照座號排序的表格

dict 的重點是用 key 查資料，不是用第幾個位置查資料。需要順序時通常用 list。

## 修正方向

1. key 建議固定用英文小寫，例如 `name`、`score`。
2. 查詢前先用 `in`，避免 KeyError。
3. list + dict 看不懂時，先把其中一筆資料 print 出來。
4. 變數名稱要能看出資料型態，例如 `student`、`students`、`contacts`。

## 延伸練習

把 `student_scores.py` 改成同時算出平均分數。