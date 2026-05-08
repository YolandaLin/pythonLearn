# 第 6 週自我檢討：List 與資料集合

## 交作業前檢查

- [ ] `subjects.py` 有印出第一個、最後一個與總數。
- [ ] `score_stats.py` 有最高、最低、平均、及格人數。
- [ ] `todo_list.py` 有示範新增、列出、刪除。
- [ ] README 有貼上執行結果。

## 常見錯誤

### 1. index 從 1 開始想

```python
subjects[1]
```

這是第二個項目，不是第一個。第一個是：

```python
subjects[0]
```

### 2. 空 list 直接取第一個

```python
todos = []
print(todos[0])
```

會出錯，因為空 list 沒有第 0 個元素。

### 3. 平均忘記除以數量

```python
average = sum(scores) / len(scores)
```

如果 `scores` 是空 list，`len(scores)` 會是 0，不能拿來除。

### 4. remove 刪的是內容，不是位置

```python
todos.remove("寫作業")
```

這會刪掉內容是 `寫作業` 的項目。如果要刪位置，可以用 `pop(index)`。

## 修正方向

1. 先用固定 list，不要一開始就做複雜輸入。
2. 每次印出 list，看它是否真的有改變。
3. 走訪 list 時，變數名稱要用單數，例如 `for score in scores`。
4. 做平均前先確認 list 不是空的。

## 延伸練習

把 `subjects.py` 加上排序，印出排序前與排序後的清單。