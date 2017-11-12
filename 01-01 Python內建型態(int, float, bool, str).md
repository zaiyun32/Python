# 01-01 Python內建型態(int, float, bool, str)

#### 內建型態(Built-in Types)可以在Python程式中直接使用, 不必預先import模組. 在 Python 中宣告變數後可直接指定一個特定值, 其變數型態自動設定為設定值的型態. 


## int (整數)

### (1)
```javascript
# 宣告一個整數
a=100
print(a)
print('型態:', type(a))
print('-'*30)

# 宣告另一個整數
b=200
print(b)
print('型態:', type(b))
print('-'*30)

print('a和b是否同一物件?', a is b)
```

執行結果:
```
100
型態: <class 'int'>
------------------------------
200
型態: <class 'int'>
------------------------------
a和b是否同一物件? False
```

### (2)
```javascript
import sys

# 宣告一個整數
a=1234567890123
print(a)
print('型態:', type(a))
print('物件大小:', sys.getsizeof(a))
print('-'*30)


# 宣告一個整數
b=123456789012345678901234567
print(b)
print('型態:', type(b))
print('物件大小:', sys.getsizeof(b))
print('-'*30)
```

執行結果:
```
1234567890123
型態: <class 'int'>
物件大小: 32
------------------------------
123456789012345678901234567
型態: <class 'int'>
物件大小: 36
------------------------------
```


## float (浮點數)

### (1)
```javascript
import sys

# 宣告一個浮點數
a=100.1234
print(a)
print('型態:', type(a))
print('物件大小', sys.getsizeof(a))
print('-'*30)

# 宣告另一個浮點數
b=1234567890123456789012345.1234567890123456789012345
print(b)
print('型態:', type(b))
print('物件大小', sys.getsizeof(b))
print('-'*30)
```

執行結果:
```
100.1234
型態: <class 'float'>
物件大小 24
------------------------------
1.2345678901234568e+24
型態: <class 'float'>
物件大小 24
------------------------------
```

### (2)
```javascript
import sys

# 宣告一個浮點數
a=100.5678
print(a)
print('型態:', type(a))
print('物件大小', sys.getsizeof(a))
print('-'*30)

# 產生一個整數
b=int(a)
print(b)
print('型態:', type(b))
print('物件大小', sys.getsizeof(b))
print('-'*30)
```

執行結果:
```
100.5678
型態: <class 'float'>
物件大小 24
------------------------------
100
型態: <class 'int'>
物件大小 28
------------------------------
```



## str

在 Python 宣告字串可以使用 `單引號` 或 `雙引號`, 以下是一個例子:

### (1)
```javascript
# 宣告一個字串
a='Hello'
print(a)
print(type(a))
print('-'*30)


# 宣告另一個字串
b="你好"
print(b)
print(type(b))
print('-'*30)


# 字串相加
c=a+b
print(c)
print('-'*30)
```

執行結果:
```
Hello
<class 'str'>
------------------------------
你好
<class 'str'>
------------------------------
Hello你好
------------------------------
```

### (2)
```javascript
# 宣告一個字串
a='Hello'
print(a)
print(type(a))
print('-'*30)


# 用迭代取出每個長度為1的子字串
for c in a:
    print(c)

print('-'*30)


# 切割字串
print(a[1:4])
print('-'*30)
```

執行結果:
```
Hello
<class 'str'>
------------------------------
H
e
l
l
o
------------------------------
ell
------------------------------
```


## bool

在 Python 宣告布林值可設定為 `True` 或 `False`, 或是一個邏輯運算結果, 以下是一個例子:

```javascript
# 宣告一個布林
a = True
print(a)
print(type(a))
print('-'*30)

# 宣告另一個布林
b = False
print(b)
print(type(b))
print('-'*30)

# 一個邏輯運算結果
c = 10>20 or 20<=30
print(c)
print('-'*30)
```

以下是執行結果:
```
True
<class 'bool'>
------------------------------
False
<class 'bool'>
------------------------------
True
------------------------------
```
