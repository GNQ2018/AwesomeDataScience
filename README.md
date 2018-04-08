# AwesomeDataScience
 帅气的数据科学

## Python


### 安装 Python

1. Windows 安装

2. MacOS 安装

3. Linux 安装


### 查看 Python 版本


## [Anaconda Python 数据科学平台](https://www.anaconda.com/)

---

# Anaconda: 最流行的Python数据科学平台

[(英文原文)](https://www.anaconda.com/what-is-anaconda/)

## <center> Anaconda Distribution </center>
    

拥有超过六百万的用户, 开源[Anaconda Distribution](https://www.anaconda.com/distribution/)是进行Python数据科学和机器学习最简单的方法. 它包括250多种流行的数据科学包(data science package)和conda包, 以及适用于Windowns, Linux和MacOS的conda包和虚拟环境管理器. Conda使安装,  运行, 和升级复杂的数据科学和机器学习环境(如Scikit-learn, TensorFlow, Scipy)变得快捷简单. Anaconda Distribution 是数百万的数据科学项目, 以及亚马逊Web服务的*机器学习AMI*，和*用于微软Azure和Windows的Anaconda*的基础. 


## <center> 可复制的数据科学和机器学习 </center>
在Anaconda 仓库(repository)中的Python和R conda包是在我们的安全环境中监管并编译的, 因此您能获得正好适用于您的系统的优化的二进制文档. 结合了conda的虚拟环境和深度依赖管理, 您能轻松地在Windows, Linux和MacOS系统之间复制完全相同的数据科学结果. Anaconda仓库中有超过1000的免费包供大家使用, 并且我们还在[anaconda.org](https://anaconda.org/conda-forge)上为conda包创建者们举办了一个[Conda Forge](https://conda-forge.org/)社区. 

## <center> Anaconda Enterprise(企业版) </center>
Anaconda的商业化产品, [Anaconda Enterprise](https://www.anaconda.com/enterprise/)是企业组织进行协作, 管理, 扩展和保护Python，R数据科学以及机器学习的软件. 完全版有基于目录的访问控制和版本控制，数据科学家可以在Notebook和模型上安全协作. IT可以操作自己的私有Python和R包仓库来镜像, 过滤并管理包, 以遵守其管理和安全方针. 快速部署ML模型, Live notebook以及仪表板到运行Docker/Kubernates, Hadoop和Spark的生产环境计算集群上. Anaconda企业版在您自己的数据中心以及AWS, Azure和Google Cloud平台上运行. 甚至可以在无网络接入的“空气间隙(Air－gapped)环境运行”. 

"通用电器数据科学专注于实时协作. 我们的团队分布于世界各地, 并且我们想要做到实时协作. 我们希望有一个每个人都能使用的通用机器学习平台, 进行现代分析, 并且制定每个人都能遵循的标准. Anaconda企业版让我们能够有效的做到这一点". 

-Girish Modgil，通用电器公司 数据&分析高级主管  



---

## [Anaconda 下载安装](https://www.anaconda.com/download/)



## 课程资料

### 1. Introduction to Python

### 2. The First Python Program  安装 Anaconda 后测试


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

### 3. Basics-of-python-syntax

![输出](https://user-images.githubusercontent.com/11325103/38465879-a676f90c-3b53-11e8-9dec-fb63f0589837.png)


## [🙃Spyder 官方的求助信](https://github.com/spyder-ide/spyder/wiki/Anaconda-stopped-funding-Spyder)


## 
