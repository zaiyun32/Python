# 02-5 Python內建集合型態-frozenset

#### 在Python中宣告一個frozenset(集合)物件, 可由frozenset()函式建立, 傳入set或list資料內容皆可. 在frozenset中的元素不會重覆, 而frozenset物件內容不可在設定後再增減(immutable). 


## 1. frozenset(集合)

#### 程式範例
```python
# 建立一個set物件
a=frozenset({2, 4, 5, 6, 2, 1, 4, 6, 8, 9})


# 印出a中的所有元素(沒有重覆內容)
for i in a:
    print(i)
    
print('-'*30) 
```

執行結果:
```
1
2
4
5
6
8
9
------------------------------
```


## 2. 可以操作在集合型態的運算, 包括set(mutable)及frozenset(immutable)

#### 完整資料建議查看Python文件
```
len(s)
x in s
x not in s
isdisjoint(other)
issubset(other)
set <= other
set < other
issuperset(other)
set >= other
set > other
union(*others)
set | other | ...
intersection(*others)
set & other & ...
difference(*others)
set - other - ...
symmetric_difference(other)
set ^ other
copy()
```

#### (1)程式範例
```python
# 建立一個set物件
a=frozenset({2, 4, 5, 6, 2, 1, 4, 6, 8, 9})

print(a)
print('-'*30)

# 是否存在set中
print('10是否存在:', 10 in a)
print('-'*30) 

print('5是否存在:', 5 in a)
print('-'*30) 

# 長度
print('長度:', len(a))
print('-'*30) 
```

執行結果:
```
frozenset({1, 2, 4, 5, 6, 8, 9})
------------------------------
10是否存在: False
------------------------------
5是否存在: True
------------------------------
長度: 7
------------------------------
```



#### (2)程式範例
```python
# 建立2個set物件
a=frozenset({5, 6, 8, 9, 3, 1, 8, 7, 5})
b=frozenset({5, 6, 12, 18, 20})

print('a集合:', a)
print('b集合:',b)
print('-'*40)

print('a,b交集', a & b)
print('a,b聯集', a | b)
print('a,b差集', a - b)
print('-'*40)
```

執行結果:
```
a集合: frozenset({1, 3, 5, 6, 7, 8, 9})
b集合: frozenset({5, 6, 12, 18, 20})
----------------------------------------
a,b交集 frozenset({5, 6})
a,b聯集 frozenset({1, 3, 5, 6, 7, 8, 9, 12, 18, 20})
a,b差集 frozenset({1, 3, 7, 8, 9})
----------------------------------------
```



## 3. frozenset沒有mutable運算

#### frozenset是immutable型態, 生成物件設定初值後, 其內容就不可再變動.
