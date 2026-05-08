# 第 6 週作業：List 與資料集合

## 本週目標

學會把多筆資料放在同一個變數裡。以前一個變數只能放一個名字或一個分數，list 可以放一整串資料，例如全班分數、待辦事項、喜歡的歌曲。

## 本週主題

- list 建立與索引
- index 從 0 開始
- `append()`：新增資料
- `remove()` / `pop()`：移除資料
- 用 `for` 走訪 list
- `len()`、`sum()`、`max()`、`min()`
- 空 list 的處理

## 範例 1：固定清單

```python
subjects = ["國文", "英文", "數學"]
print(subjects[0])
print(subjects[1])
print(subjects[2])
```

請注意：第一個位置是 0，不是 1。

## 範例 2：走訪清單

```python
scores = [80, 95, 70]

for score in scores:
    print(score)
```

## 必做作業

### hw1：我的科目清單

建立 `subjects.py`。

建立一個 list，放入至少 5 個科目或社團活動。程式要印出：

- 第一個項目
- 最後一個項目
- 總共有幾個項目
- 用 `for` 一行一行印出所有項目

### hw2：成績統計

建立 `score_stats.py`。

先用固定 list：

```python
scores = [80, 95, 70, 60, 100]
```

程式要輸出：

- 最高分
- 最低分
- 平均分
- 有幾個人及格

完成固定 list 後，再挑戰讓使用者輸入多筆成績。

### hw3：待辦清單第一版

建立 `todo_list.py`。

先不用做互動選單。請用程式示範：

1. 建立空 list。
2. 新增三件待辦事項。
3. 印出所有待辦事項。
4. 刪除其中一件。
5. 再印出更新後的待辦事項。

### hw4：簡答題

請寫在 `learning-log.md`：

1. list 適合存什麼樣的資料？
2. 為什麼 index 從 0 開始容易出錯？
3. 空 list 不能直接做哪些事？
4. `append()` 和 `remove()` 各自做什麼？

## 繳交內容

請建立一個 `week6` 資料夾，至少包含：

- `subjects.py`
- `score_stats.py`
- `todo_list.py`
- `README.md`：貼上執行結果。
- `learning-log.md`

## 自我檢測

- [ ] 我知道 list 用 `[]` 表示。
- [ ] 我知道第一個 index 是 0。
- [ ] 我能用 `for` 處理 list 裡的每個元素。
- [ ] 我能算出最高、最低、平均。
- [ ] 我知道空 list 沒有第一個元素。

## 挑戰題

把 `score_stats.py` 改成讓使用者一直輸入分數，輸入 `done` 時結束並輸出統計結果。