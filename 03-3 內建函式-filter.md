# 03-3 Python的內建函式-filter.md


## 1. 關於lambda

#### 關於lambda的說明, 請參考03-2. 



## 2. 內建函式filter()

#### filter()將一個可迭代物件的每個元素進行條件比對, 得到一個filter物件, 內容為通過過濾條件的迭代物件. 



#### (1) 程式範例
```javascript
# 建立一個函式
fn=lambda x: x>=60

# 建立一個list
data=[81, 43, 95, 72, 35, 67]


# 進行list元素的過濾(filter), 並印出結果
print([c for c in filter(fn, data)])
print('-'*30)


# 進行list元素的過濾, 並印出結果
for c in filter(fn, data):
    print(c)

print('-'*30)
```

執行結果:
```
[81, 95, 72, 67]
------------------------------
81
95
72
67
------------------------------
```


#### (2) 程式範例(filter物件內容只能取出一次.)
```javascript
# 建立一個函式
fn=lambda x: x>=60

# 建立一個list
data=[81, 43, 95, 72, 35, 67]

# 建立一個filter
myFilter=filter(fn, data)
print(myFilter)
print(type(myFilter))
print('-'*30)


# 進行list元素的過濾(filter), 並印出結果
print([c for c in myFilter])
print('-'*30)


# 進行list元素的過濾, 並印出結果(沒有資料)
for c in myFilter:
    print(c)

print('-'*30)
```

執行結果:
```
<filter object at 0x7f77e8566f28>
<class 'filter'>
------------------------------
[81, 95, 72, 67]
------------------------------
------------------------------
```
