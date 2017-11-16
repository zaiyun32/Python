# 03-9 Python的內建函式-input


### 用input()處理鍵盤輸入. 



#### (1)程式範例
```python
w=input('寬(公分):')
h=input('高(公分):')

try:
    width=float(w)
    height=float(h)
    
    area=width*height
    print('面積={}平分公分'.format(area))
except ValueError:
    print('輸入有誤')              
```


執行結果:
```
寬(公分): 20
高(公分): 30
面積=600.0平分公分
```
