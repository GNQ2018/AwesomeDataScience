# AwesomeDataScience
 帅气的数据科学

## Python


### 安装 Python

1. Windows 安装

2. MacOS 安装

3. Linux 安装


### 查看 Python 版本


## [Anaconda Python 数据科学平台](https://www.anaconda.com/)

## [Anaconda 下载安装](https://www.anaconda.com/download/)


Have you correctly installed Python IDE and can successfully run the two test programs?

1. Install Python 3.x IDE (It is recommended to install Anaconda only)

IDLE url：https://python.org

Anaconda url：https://www.continuum.io/downloads

2. Test the use of IDE(using Spyder of Anaconda)

(1)

```
import numpy as np
from scipy.cluster.vq import vq, kmeans, whiten
list1 = [88.0, 74.0, 96.0, 85.0]
list2 = [92.0, 99.0, 95.0, 94.0]
list3 = [91.0, 87.0, 99.0, 95.0]
list4 = [78.0, 99.0, 97.0, 81.0]
list5 = [88.0, 78.0, 98.0, 84.0]
list6 = [100.0, 95.0, 100.0, 92.0]
data = np.array([list1,list2,list3,list4,list5,list6])
whiten = whiten(data)
centroids,_ = kmeans(whiten, 2)
result,_= vq(whiten, centroids)
print(result)      # [0 1 1 1 0 1] or other similar list

```

(2)

```

import numpy as np
import matplotlib.pyplot as plt
t=np.arange(0.,4.,0.1)
plt.plot(t,t,t,t+2,t,t**2)
#I am a picture, I am a picture, I am a picture.

```

![输出](https://user-images.githubusercontent.com/11325103/38465879-a676f90c-3b53-11e8-9dec-fb63f0589837.png)


## [🙃Spyder 官方的求助信](https://github.com/spyder-ide/spyder/wiki/Anaconda-stopped-funding-Spyder)


## 
