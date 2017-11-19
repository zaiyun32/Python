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

### 用strftime()方法, 將datetime及date轉成字串.

#### (2)程式範例

```python
#--------------------------------------------------
# 從datetime模組中, 匯入datetime, date類別
#--------------------------------------------------
from datetime import datetime, date

#--------------------------------------------------
# 取得現在的日期時間(轉成字串)
#--------------------------------------------------
now = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
print('現在的日期時間--用datetime()')
print(type(now))
print(now)
print('-'*30)

print('現在的日期')
today = datetime.now().strftime("%Y-%m-%d")
print(type(today))
print(today)
print('-'*30)

print('現在的時間')
time = datetime.now().strftime("%H:%M:%S")
print(type(time))
print(time)
print('='*30)

#--------------------------------------------------
# 取得今天的日期(轉成字串)
#--------------------------------------------------
today = date.today().strftime("%Y/%m/%d")
print('今天的日期--用today()')
print(type(today))
print(today)
print('-'*30)
```



### 用timedelta計算日期

#### (3)程式範例

```python
#--------------------------------------------------
# 從datetime模組中, 匯入date, timedelta類別
#--------------------------------------------------
from datetime import date, timedelta

#--------------------------------------------------
# 取得今天的日期
#--------------------------------------------------
today = date.today()
print('今天的日期')
print(today)
print('-'*30)


#--------------------------------------------------
# 用datetime模組中的timedelta取得明天的日期
#--------------------------------------------------
tomorrow = today + timedelta(days=1)
print('明天的日期')
print(tomorrow)
print('-'*30)
```

執行結果:
```
今天的日期
2017-11-19
------------------------------
明天的日期
2017-11-20
------------------------------
```
