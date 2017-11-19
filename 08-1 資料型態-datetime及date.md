# 08-1 資料型態(Data types)-datetime及date


### 在datetime模組(module)中, 有幾個與日期時間相關的類別(class), 包括date, time, datetime, timedelta, tzinfo及timezone.


#### (1)程式範例

```python
#--------------------------------------------------
# 從datetime模組中, 匯入datetime, date類別
#--------------------------------------------------
from datetime import datetime, date

#--------------------------------------------------
# 取得現在的日期時間
#--------------------------------------------------
now = datetime.now()
print('現在的日期時間')
print(type(now))
print(now)
print('-'*30)

#--------------------------------------------------
# 取得今天的日期
#--------------------------------------------------
today = date.today()
print('今天的日期')
print(type(today))
print(today)
print('-'*30)
```


執行結果:
```
現在的日期時間
<class 'datetime.datetime'>
2017-11-19 08:41:26.739404
------------------------------
今天的日期
<class 'datetime.date'>
2017-11-19
------------------------------
```

