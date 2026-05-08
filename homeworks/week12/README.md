# 第 12 週作業：資料視覺化

## 本週目標

把資料變成圖，練習用圖表說故事。這週重點不是畫出很炫的圖，而是讓圖表清楚、誠實、看得懂。

## 本週主題

- matplotlib
- 折線圖：看趨勢
- 長條圖：比較類別
- 圖表標題
- x 軸與 y 軸標籤
- 儲存成 png 圖檔
- 圖表不要誤導讀者

## 安裝提醒

這週需要 matplotlib：

```powershell
pip install matplotlib
```

## 建議資料夾結構

```text
week12/
├── plot_sleep.py
├── plot_club.py
├── data/
│   ├── sleep.csv
│   └── club.csv
├── images/
├── README.md
└── learning-log.md
```

## 必做作業

### hw1：建立睡眠資料

建立 `data/sleep.csv`：

```csv
day,hours
Mon,6
Tue,7
Wed,5
Thu,6
Fri,7
Sat,8
Sun,8
```

### hw2：睡眠折線圖

建立 `plot_sleep.py`，讀取 `sleep.csv`，畫出一週睡眠時間折線圖，並儲存成：

```text
images/sleep_line.png
```

圖表至少要有：

- 標題
- x 軸名稱
- y 軸名稱

### hw3：社團人數長條圖

建立 `data/club.csv`：

```csv
club,count
籃球,12
音樂,8
美術,6
科學,10
```

建立 `plot_club.py`，畫出社團人數長條圖，儲存成：

```text
images/club_bar.png
```

### hw4：圖表觀察

請在 `learning-log.md` 寫：

1. 睡眠折線圖看起來哪一天最高？哪一天最低？
2. 社團長條圖中哪個社團最多人？
3. 折線圖適合看什麼？長條圖適合看什麼？
4. 如果 y 軸故意從 5 開始，圖表可能會怎麼誤導讀者？

## 繳交內容

請建立一個 `week12` 資料夾，至少包含：

- `plot_sleep.py`
- `plot_club.py`
- `data/sleep.csv`
- `data/club.csv`
- `images/sleep_line.png`
- `images/club_bar.png`
- `README.md`：貼上執行方式與圖檔說明。
- `learning-log.md`

## 自我檢測

- [ ] 我能產生 png 圖檔。
- [ ] 我的圖表有標題。
- [ ] 我的 x 軸和 y 軸有名稱。
- [ ] 我知道折線圖適合看趨勢。
- [ ] 我知道長條圖適合比較類別。
- [ ] 我能用文字描述圖表，而不是只貼圖。

## 挑戰題

把第 11 週的 `survey.csv` 拿來畫圖，例如各社團人數或各年級人數。