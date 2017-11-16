# 01-2 Python內建型態轉換(int, float, str)

#### 內建型態int, float及str之間可以使用內建函式(Built-in Functions)相互轉換. 


## 1. 數字間轉換

#### 程式範例
```python
# 宣告一個整數
a=100
print(a)
print(type(a))
print('-'*30)


# 將整數轉為浮點數
# float()是內建函式
b=float(a) 
print(b)
print(type(b))
print('-'*30)


# 宣告一個浮點數
c=123.56
print(c)
print(type(c))
print('-'*30)


# 將浮點數轉為整數
# 小數捨去, int()是內建函式
e=int(c)
print('小數捨去:', e)
print(type(e))
print('-'*30)


# 將浮點數轉為整數
# 四捨五入, round()是內建函式
f=round(c)
print('四捨五入:', f)
print(type(f))
print('-'*30)
```

執行結果:
```
100
<class 'int'>
------------------------------
100.0
<class 'float'>
------------------------------
123.56
<class 'float'>
------------------------------
小數捨去: 123
<class 'int'>
------------------------------
四捨五入: 124
<class 'int'>
------------------------------
```


## 2. 數字及文字間轉換

#### 程式範例
```python
# 宣告一個整數
a=100
print(a)
print(type(a))
print('-'*30)


# 將整數轉為字串
# str()是內建函式
b=str(a)
print(b)
print(type(b))
print('-'*30)


# 將浮點數轉為字串
c=123.4567
d=str(c)
print(d)
print(type(d))
print('-'*30)


# 將字串轉為整數
e = '123'
f=int(e)
print(f)
print(type(f))
print('-'*30)


# 將字串轉為整數(錯誤處理)
e = 'abc'
try:
    f=int(e)
    print(f)
    print(type(f))
    print('-'*30)
except ValueError:
    print('轉換錯誤')
    print('-'*30)    
```

執行結果:
```
100
<class 'int'>
------------------------------
100
<class 'str'>
------------------------------
123.4567
<class 'str'>
------------------------------
123
<class 'int'>
------------------------------
轉換錯誤
------------------------------
```
