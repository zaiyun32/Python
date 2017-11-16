# 02-3 Python內建序列型態-range

#### 在Python中可以用range宣告一個數字範圍, 它通常用與迴圈敘述一起使用, 也可以用來生成一個特定大小的序列物件. range是建立後不可再增減內容的immutable物件.


## 1. range

#### 程式範例
```python
# 建立一個range物件
a=range(10)
print(a)
print('-'*30)

# 以迴圈逐個印出range所指的範圍內容, range(10)的範圍不包括10
for i in range(10):
    print(i)

print('-'*30) 


# 逐個印出(從1開始, 大於或等於10離開迴圈, 每次跳2), range範圍不包括10
for i in range(1, 10, 2):
    print(i)
    
print('-'*30)  


# 由range產生1個list
b=list(range(10))
print(b)
print(type(b))
print('-'*30)   
```

執行結果:
```
range(0, 10)
------------------------------
0
1
2
3
4
5
6
7
8
9
------------------------------
1
3
5
7
9
------------------------------
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
<class 'list'>
------------------------------
```
