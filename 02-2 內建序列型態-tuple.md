# 02-2 Python內建序列型態-tuple

#### 在Python中宣告一個tuple, 可藉由一對小括號, 其中包括的多個由逗點隔開的元素組成. Tuple和list很像, 只不過tuple物件在設定初值後即不可再增減內容(immutable). 


## 1. tuple

#### 程式範例
```javascript
# 建立1個tuple物件
a=(2, 4, 5, 6, 2, 1, 4, 6, 8, 9)


# 印出a中的所有元素
for i in a:
    print(i)
    
print('-'*30)    


# 印出a中的index及元素(range也是Python的序列型態)
for j in range(len(a)):
    print('第', j, '個元素:', a[j])
    
print('-'*30) 
```

執行結果:
```
2
4
5
6
2
1
4
6
8
9
------------------------------
第 0 個元素: 2
第 1 個元素: 4
第 2 個元素: 5
第 3 個元素: 6
第 4 個元素: 2
第 5 個元素: 1
第 6 個元素: 4
第 7 個元素: 6
第 8 個元素: 8
第 9 個元素: 9
------------------------------
```


## 2. 可以操作在序列型別的運算

#### 完整資料建議查看Python文件
```
x in s                True if an item of s is equal to x, else False
x not in s            False if an item of s is equal to x, else True
s + t                 the concatenation of s and t
s * n or n * s        equivalent to adding s to itself n times
s[i]                  ith item of s, origin 0
s[i:j]                slice of s from i to j
s[i:j:k]              slice of s from i to j with step k
len(s)                length of s 
min(s)                smallest item of s 
max(s)                largest item of s 
s.index(x[, i[, j]])  index of the first occurrence of x in s (at or after index i and before index j)
s.count(x)            total number of occurrences of x in s
```

#### 程式範例
```javascript
# 建立一個tuple物件
a=(2, 4, 5, 6, 2, 1, 4, 6, 8, 9, 2)
print(a)
print('-'*30)

# 是否存在tuple中
print('10是否存在:', 10 in a)
print('-'*30)    


# 範圍
print('索引值 3, 4, 5 的元素:', a[3:6])
print('-'*30)  


# 長度
print('長度:', len(a))
print('-'*30) 


# 計算個數
print('2的個數:', a.count(2))
print('-'*30) 


print('tuple中的最大值:', max(a))
print('-'*30) 


print('兩個tuple相加:', a+a)
print('-'*30) 
```

執行結果:
```
(2, 4, 5, 6, 2, 1, 4, 6, 8, 9, 2)
------------------------------
10是否存在: False
------------------------------
索引值 3, 4, 5 的元素: (6, 2, 1)
------------------------------
長度: 11
------------------------------
2的個數: 3
------------------------------
tuple中的最大值: 9
------------------------------
兩個tuple相加: (2, 4, 5, 6, 2, 1, 4, 6, 8, 9, 2, 2, 4, 5, 6, 2, 1, 4, 6, 8, 9, 2)
------------------------------
```
