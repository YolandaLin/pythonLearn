# 第 14 週自我檢討：物件導向入門

## 交作業前檢查

- [ ] `Student` 有 `name`、`score`、`is_passing()`、`summary()`。
- [ ] `Pet` 有 energy，而且 feed/play 會改變 energy。
- [ ] `characters.py` 有把多個角色物件放進 list。
- [ ] README 有貼上執行結果。

## 常見錯誤

### 1. 忘記 self

```python
class Student:
    def is_passing():
        return self.score >= 60
```

方法裡通常要把 `self` 放在第一個參數：

```python
class Student:
    def is_passing(self):
        return self.score >= 60
```

### 2. 建立物件時參數數量不對

如果 `__init__` 需要 name 和 score：

```python
Student("小明", 85)
```

就不能只寫：

```python
Student("小明")
```

### 3. 把 class 當成 dict 使用

class 物件通常用點號取資料：

```python
student.name
```

不是：

```python
student["name"]
```

### 4. 方法沒有真的改到狀態

`feed()` 應該改變 `self.energy`，不是只印出「餵食了」。

## 修正方向

1. 先建立最小 class，只放 name。
2. 確認可以建立物件後，再加方法。
3. 每呼叫一次方法，就印出狀態確認是否有改變。
4. 不要一開始就寫互動選單，先用固定流程測試。

## 延伸練習

替 `Character` 加上 `attack(other)` 方法，讓一個角色攻擊另一個角色並扣血。