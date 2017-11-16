# 03-7 Python的內建函式-open


### open()可以開啟檔案. 



#### (1)程式範例
```python
# 開啟檔案(r:只讀)
file = open('data.txt','r')  

# 每行依次讀入
for line in file.readlines():  
    line = line.strip()  #去除頭尾空白及\n 
    print(line)

print('-'*30)

# 關閉檔案
file.close()                  
```


#### 測試檔案(data.txt)
```
1,男,46,56,42,48,37,10
2,男,48,51,39,48,43,10
3,男,50,52,47,41,42,8
4,女,40,56,45,46,45,8
5,男,43,41,29,35,34,10
6,女,44,52,50,41,46,8
7,女,44,56,47,46,41,8
8,男,50,56,47,46,35,8
9,男,56,60,30,48,41,8
10,男,43,55,49,36,50,10
```


執行結果:
```
1,男,46,56,42,48,37,10
2,男,48,51,39,48,43,10
3,男,50,52,47,41,42,8
4,女,40,56,45,46,45,8
5,男,43,41,29,35,34,10
6,女,44,52,50,41,46,8
7,女,44,56,47,46,41,8
8,男,50,56,47,46,35,8
9,男,56,60,30,48,41,8
10,男,43,55,49,36,50,10
------------------------------
```


#### (2)程式範例
```python
# 開啟檔案(r:只讀)
file = open('data.txt','r')  

# 每行依次讀入
for line in file.readlines():  
    line = line.strip()  #去除頭尾空白及\n 
    
    try:
        items = line.split(',')  #以逗號分隔資料
        num = items[0]
        gender = items[1]
        chi = int(items[2])
        eng = int(items[3])
        mat = int(items[4])
        soc = int(items[5])
        nat = int(items[6])
        lec = int(items[7])
    
        total=chi+eng+mat+soc+nat+lec
        print('序號:', num, '總分:', total)
    except ValueError:
        print('資料錯誤')

# 關閉檔案
file.close()              
```


#### 測試檔案(data.txt)
```
1,男,46,56,42,48,37,10
2,男,48,51,39,48,43,10
3,男,50,52,47,41,42,8
4,女,40,56,45,46,45,8
5,男,43,41,29,35,34,10
6,女,A,52,50,41,46,8
7,女,44,56,47,46,41,8
8,男,50,56,47,46,35,8
9,男,56,60,30,48,41,8
10,男,43,55,49,36,50,10
```


執行結果:
```
序號: 1 總分: 239
序號: 2 總分: 239
序號: 3 總分: 240
序號: 4 總分: 240
序號: 5 總分: 192
資料錯誤
序號: 7 總分: 242
序號: 8 總分: 242
序號: 9 總分: 243
序號: 10 總分: 243
------------------------------
```


#### (3)程式範例
```python
# 開啟檔案(r:只讀)
fr = open('in.txt','r')  
fw = open('out.txt','w')  

# 每行依次讀入
for line in fr.readlines():  
    line = line.strip()  #去除頭尾空白及\n 
    
    try:
        items = line.split(',')  #以逗號分隔資料
        num = items[0]
        gender = items[1]
        chi = int(items[2])
        eng = int(items[3])
        mat = int(items[4])
        soc = int(items[5])
        nat = int(items[6])
        lec = int(items[7])
    
        total=chi+eng+mat+soc+nat+lec
        print('序號:', num, '總分:', total)
        data=num+','+str(total)+'\n'
        fw.writelines(data)
    except ValueError:
        print('資料錯誤')
        data=num+','+'錯誤'+'\n'
        fw.writelines(data)

# 關閉檔案
fr.close()   
fw.close()            
```


#### 測試檔案(in.txt)
```
1,男,46,56,42,48,37,10
2,男,48,51,39,48,43,10
3,男,50,52,47,41,42,8
4,女,40,56,45,46,45,8
5,男,43,41,29,35,34,10
6,女,A,52,50,41,46,8
7,女,44,56,47,46,41,8
8,男,50,56,47,46,35,8
9,男,56,60,30,48,41,8
10,男,43,55,49,36,50,10
```


執行結果(out.txt)
```
1,239
2,239
3,240
4,240
5,192
6,錯誤
7,242
8,242
9,243
10,243
```



#### (4)程式範例
```python
# 開啟檔案(r:只讀)
fr = open('in.txt','r')  

# 一次全部讀入
data = fr.read()

# 刪除前後空白及\n
data=data.strip()  

# 將標點符號刪除
puncts=[',', '.', ';', '!', '?']

for punct in puncts:
    data=data.replace(punct, '')
    
print(data)
print('-'*30)

# 以空白分割單詞
vocs = data.split(' ')

print(vocs)
print('-'*30)

# 關閉檔案
fr.close()              
```


#### 測試檔案(in.txt)
```
With legacies as varied as its adventure landscape and spirited traditions thriving alongside the cream of Asian sophistication, Taiwan is a continent on one green island.
```


執行結果(out.txt)
```
With legacies as varied as its adventure landscape and spirited traditions thriving alongside the cream of Asian sophistication Taiwan is a continent on one green island
------------------------------
['With', 'legacies', 'as', 'varied', 'as', 'its', 'adventure', 'landscape', 'and', 'spirited', 'traditions', 'thriving', 'alongside', 'the', 'cream', 'of', 'Asian', 'sophistication', 'Taiwan', 'is', 'a', 'continent', 'on', 'one', 'green', 'island']
------------------------------
```
