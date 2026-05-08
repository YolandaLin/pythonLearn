# 第 14 週作業：物件導向入門

## 本週目標

理解 class 可以把「資料」和「行為」放在一起。這週不追求完整物件導向設計，只要知道 class 適合描述有狀態、會做事的東西，例如學生、寵物、遊戲角色。

## 本週主題

- class
- `__init__`
- 屬性
- 方法
- `self`
- 物件清單
- dict 和 class 的差異

## 範例：從 dict 到 class

dict 寫法：

```python
student = {"name": "小明", "score": 85}
```

class 寫法：

```python
class Student:
    def __init__(self, name, score):
        self.name = name
        self.score = score

    def is_passing(self):
        return self.score >= 60

student = Student("小明", 85)
print(student.name)
print(student.is_passing())
```

## 必做作業

### hw1：Student class

建立 `student_class.py`。

建立 `Student` class，包含：

- `name`
- `score`
- `is_passing()`：分數大於等於 60 回傳 True
- `summary()`：回傳一段學生摘要文字

請建立至少 3 位學生並印出摘要。

### hw2：Pet class

建立 `pet.py`。

建立 `Pet` class，包含：

- `name`
- `energy`，初始值 50
- `feed()`：energy 增加 10，最高不超過 100
- `play()`：energy 減少 15，最低不低於 0
- `status()`：回傳目前狀態文字

請示範餵食、玩耍與印出狀態。

### hw3：角色清單

建立 `characters.py`。

建立一個 `Character` class，包含姓名與血量 hp。建立至少 3 個角色，放進 list，印出每個角色的狀態。

### hw4：簡答題

請寫在 `learning-log.md`：

1. class 和 dict 都能放資料，差別在哪？
2. `self` 可以怎麼理解？
3. 方法和一般函式有什麼相似與不同？
4. 什麼生活物件適合用 class 描述？

## 繳交內容

請建立一個 `week14` 資料夾，至少包含：

- `student_class.py`
- `pet.py`
- `characters.py`
- `README.md`：貼上執行結果。
- `learning-log.md`

## 自我檢測

- [ ] 我能建立 class。
- [ ] 我能用 `__init__` 設定初始資料。
- [ ] 我知道 `self` 代表目前這個物件。
- [ ] 我能呼叫物件方法。
- [ ] 我能把多個物件放進 list。

## 挑戰題

把 `Pet` 改成互動版，讓使用者輸入 `feed`、`play`、`status`、`quit` 來照顧寵物。