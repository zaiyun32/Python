# 07-2 類別(class)-@property


### 直接取用屬性值的寫法, 比寫getter及setter方便, 也是比較推薦的作法. 這種成員存放名稱在前方加上一個_(底線), 在設定值的函式前加上@property的修飾, 在取出值的函式前加上@成員名稱.setter的修飾.
之前加上底線的成員名稱, 是為了和設定及取用的方法名稱有所區別.

#### (1)程式範例

##### ntub.py
```python
#------------------------------------------------
# 定義學生類別
#------------------------------------------------
class Student():
    #------------------------------       
    # 建構元
    # 性別的實際存放名稱為 _gender
    #------------------------------   
    def __init__(self, stuNo, stuName, gender=None):
        self.stuNo=stuNo
        self.stuName=stuName
        self._gender=gender

    #----------------------------------    
    # 取出性別的方法
    # 直接用 [...=實例名稱.gender] 即可
    #---------------------------------- 
    @property
    def gender(self):
        if self._gender=='M':
            return '男'
        elif self._gender=='F':
            return '女'
        else:
            return None

    #----------------------------------    
    # 設定性別的方法
    # 直接用 [實例名稱.gender=...] 即可
    #---------------------------------- 
    @gender.setter
    def gender(self, gender):
        if gender=='M' or gender=='F':
            self._gender=gender
        else:
            self._gender=None
    

    #-------------------    
    # 取出學制的方法
    #-------------------
    def division(self):
        if self.stuNo[0]=='N':
            return '進修推廣部'
        else:
            return '日間部'    
```

##### main.py
```python
#--------------------------------------------
# 匯入ntub模組
#--------------------------------------------
import ntub

#--------------------------------------------
# 生成實例
#--------------------------------------------
s1=ntub.Student('1056001', '王小明', 'M')
s2=ntub.Student('1056002', '陳小華')

#--------------------------------------------
# 呼叫實例的方法
#-------------------------------------------- 
print('學號:{}  姓名:{}  性別:{}  學制:{}'.format(s1.stuNo, s1.stuName, s1.gender, s1.division()))
print('學號:{}  姓名:{}  性別:{}  學制:{}'.format(s2.stuNo, s2.stuName, s2.gender, s2.division()))
```


執行結果:
```
學號:1056001  姓名:王小明  性別:男  學制:日間部
學號:1056002  姓名:陳小華  性別:None  學制:日間部
```


