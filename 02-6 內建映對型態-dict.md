# 02-6 Python內建映對(map)型態-dict

#### 在Python中宣告一個dict(字典)變數, 可由一對大括號, 其中包括多組成對資料, 每組資料由冒號隔開組成. dict是mutable物件, 內容可在設定後再增減. 


## 1. dict(字典)

#### (1)程式範例
```python
# 建立一個dict物件
departments={'1':'會資系', '2':'財金系', '3':'財稅系', '4':'商務系', '5':'企管系', '6':'資管系', '7':'應外系'}

print(departments)
print(type(departments))
print('-'*30)

# 印出dict內的所有鍵及值(方法1)
for key in departments:
    print('鍵:', key, '=> 值:', departments[key])
    
print('-'*30) 


# 印出dict內的所有鍵及值(方法2)
for key, value in departments.items():
    print('鍵:', key, '=> 值:', value)
    
print('-'*30)  
```

執行結果:
```
{'1': '會資系', '2': '財金系', '3': '財稅系', '4': '商務系', '5': '企管系', '6': '資管系', '7': '應外系'}
<class 'dict'>
------------------------------
鍵: 1 => 值: 會資系
鍵: 2 => 值: 財金系
鍵: 3 => 值: 財稅系
鍵: 4 => 值: 商務系
鍵: 5 => 值: 企管系
鍵: 6 => 值: 資管系
鍵: 7 => 值: 應外系
------------------------------
鍵: 1 => 值: 會資系
鍵: 2 => 值: 財金系
鍵: 3 => 值: 財稅系
鍵: 4 => 值: 商務系
鍵: 5 => 值: 企管系
鍵: 6 => 值: 資管系
鍵: 7 => 值: 應外系
------------------------------
```


#### (2)程式範例
```python
# 建立一個dict物件
departments={'1':'會資系', '2':'財金系', '3':'財稅系', '4':'商務系', '5':'企管系', '6':'資管系', '7':'應外系'}

print(departments)
print(type(departments))
print('-'*30)


# 以鍵值取出資料
print(departments['1'])
print(departments['5'])   
print('-'*30)   


# 以鍵值取出資料(錯誤處理)
try:
    print(departments['8'])   
except KeyError:    
    print('沒有對應資料')
    
print('-'*30) 
```

執行結果:
```
{'1': '會資系', '2': '財金系', '3': '財稅系', '4': '商務系', '5': '企管系', '6': '資管系', '7': '應外系'}
<class 'dict'>
------------------------------
會資系
企管系
------------------------------
沒有對應資料
------------------------------
```




## 2. 可以操作在映對型態的運算

#### 完整資料建議查看Python文件
```
len(d)
d[key]
d[key] = value
del d[key]
key in d
key not in d
iter(d)
clear()
copy()
classmethod fromkeys(seq[, value])
fromkeys()
get(key[, default])
items()
keys()
pop(key[, default])
popitem()
setdefault(key[, default])
update([other])
values()
```

#### (1)程式範例
```python
# 建立一個dict物件
departments={'1':'會資系', '2':'財金系', '3':'財稅系', '4':'商務系', '5':'企管系', '6':'資管系', '7':'應外系'}

print(departments)
print(type(departments))
print('-'*30)


# 加入其他內容
departments['A']='商設系'
departments['B']='商創系'   
departments['C']='數媒系'


# 印出dict內的所有鍵及值
for key in departments:
    print('鍵:', key, '=> 值:', departments[key])
    
print('-'*30)  
```

執行結果:
```
{'1': '會資系', '2': '財金系', '3': '財稅系', '4': '商務系', '5': '企管系', '6': '資管系', '7': '應外系'}
<class 'dict'>
------------------------------
鍵: 1 => 值: 會資系
鍵: 2 => 值: 財金系
鍵: 3 => 值: 財稅系
鍵: 4 => 值: 商務系
鍵: 5 => 值: 企管系
鍵: 6 => 值: 資管系
鍵: 7 => 值: 應外系
鍵: A => 值: 商設系
鍵: B => 值: 商創系
鍵: C => 值: 數媒系
------------------------------
```



#### (2)程式範例
```python
# 建立一個dict物件
departments={'1':'會資系', '2':'財金系', '3':'財稅系', '4':'商務系', '5':'企管系', '6':'資管系', '7':'應外系'}

print(departments)
print(type(departments))
print('-'*30)


# 判斷是否有鍵值
print('是否有鍵值1 ?', '1' in departments)
print('是否有鍵值D ?', 'D' in departments)
print('-'*30)   


# 刪除內容
del departments['1']

print(departments)
print('-'*30)
```

執行結果:
```
{'1': '會資系', '2': '財金系', '3': '財稅系', '4': '商務系', '5': '企管系', '6': '資管系', '7': '應外系'}
<class 'dict'>
------------------------------
是否有鍵值1 ? True
是否有鍵值D ? False
------------------------------
{'2': '財金系', '3': '財稅系', '4': '商務系', '5': '企管系', '6': '資管系', '7': '應外系'}
------------------------------
```
