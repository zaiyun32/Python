# 用 matplotlib 顯示圖表 


```
import numpy as np
import matplotlib.pyplot as plt

# 產生常態分配亂數成績
chi01=np.random.randn(100)*15+65
eng01=np.random.randn(100)*15+65

chi02=np.random.randn(100)*10+40
eng02=np.random.randn(100)*10+40

# 修正資料
chi01=chi01.clip(0, 100)
eng01=eng01.clip(0, 100)
chi02=chi02.clip(0, 100)
eng02=eng02.clip(0, 100)

# 設定字型及大小
plt.rcParams['font.sans-serif']=['SimHei']
plt.rcParams['font.size'] = 14

# 設定圖標題
plt.title('國文-英文成績分佈(依入學方式分別)')

# 設定x軸及y軸標題
plt.xlabel('國文成績')
plt.ylabel('英文成績')

# 資料表內的grid
plt.grid(True)

# 設定x軸及y軸的尺規範圍
plt.axis([-5, 105, -5, 105])

# 繪製資料
plt.plot(chi01, eng01, 'ro', chi02, eng02, 'bd')

# 設定資料說明
plt.legend(['推甄生', '分發生'], numpoints=1, loc='upper left')

# 顯示圖表
plt.show()
```

以下是執行結果:<p>
![GitHub Logo](/images/fig7-6.jpg)
