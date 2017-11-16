# 03-3 Python的內建函式-filter


### 1. 範例使用了lambda. 如有需要, 請參考03-2的lambda說明. 



### 2. filter()將一個可迭代物件的每個元素進行條件比對, 得到一個filter物件, 內容為通過過濾條件的元素. 



#### (1)程式範例
```python
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


#### (2)程式範例(filter物件內容只能取出一次)
```python
# 建立一個函式
fn=lambda x: x>=60

# 建立一個list
data=[81, 43, 95, 72, 35, 67]

# 建立一個filter
myFilter=filter(fn, data)


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
[81, 95, 72, 67]
------------------------------
------------------------------
```
