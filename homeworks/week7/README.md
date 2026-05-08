# 第 7 週作業：Dictionary 與結構化資料

## 本週目標

學會用 key-value 表示一筆有欄位的資料。list 適合放一串同類資料，dict 適合描述「一個東西有哪些屬性」，例如一位學生的姓名、座號、分數。

## 本週主題

- dict 建立
- key 與 value
- 新增、修改、刪除欄位
- `in` 判斷 key 是否存在
- `items()` 走訪 key-value
- list + dict 表示多筆資料

## 範例 1：學生資料卡

```python
student = {
    "name": "小明",
    "seat": 12,
    "score": 85
}

print(student["name"])
print(student["score"])
```

## 範例 2：走訪 dict

```python
for key, value in student.items():
    print(f"{key}: {value}")
```

## 必做作業

### hw1：學生資料卡

建立 `student_card.py`。

建立一個 dict，包含：

- 姓名
- 年級
- 座號
- 最喜歡的科目
- 本週 Python 分數

程式要輸出一段完整摘要，例如：

```text
小明是高一學生，座號 12，最喜歡數學，本週 Python 分數是 85。
```

### hw2：通訊錄查詢

建立 `contacts.py`。

建立一個 dict，key 是姓名，value 是電話或 email。讓使用者輸入姓名：

- 如果查得到，印出聯絡方式。
- 如果查不到，印出 `查無此人`。

請至少放 3 筆資料。

### hw3：多位學生最高分

建立 `student_scores.py`。

使用 list + dict 表示多位學生：

```python
students = [
    {"name": "小明", "score": 85},
    {"name": "小華", "score": 92},
    {"name": "小美", "score": 78}
]
```

程式要找出最高分學生並印出姓名與分數。

### hw4：簡答題

請寫在 `learning-log.md`：

1. list 和 dict 適合存什麼不同資料？
2. dict 裡的 key 有什麼用途？
3. 為什麼查詢 dict 前可以先用 `in`？
4. 什麼情況會適合用 list + dict？

## 繳交內容

請建立一個 `week7` 資料夾，至少包含：

- `student_card.py`
- `contacts.py`
- `student_scores.py`
- `README.md`：貼上測試資料與執行結果。
- `learning-log.md`

## 自我檢測

- [ ] 我知道 dict 用 `{}` 表示。
- [ ] 我知道 key 是用來查 value 的名字。
- [ ] 我能用 `in` 判斷 key 是否存在。
- [ ] 我能用 `items()` 走訪 dict。
- [ ] 我知道多筆結構化資料可以用 list + dict。

## 挑戰題

把 `contacts.py` 改成可以新增一筆聯絡人，再查詢剛剛新增的人。