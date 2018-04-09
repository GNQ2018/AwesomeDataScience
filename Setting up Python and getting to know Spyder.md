# 安装 Anaconda and Spyder

1.  下载 [Anaconda Python distribution](https://www.continuum.io/downloads) (we recommend the commandline version)
2.  安装 Anaconda
3.  做完上面的指令后安装 Caiman [here](https://github.com/simonsfoundation/CaImAn#installation)

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#python-environments)Python _environments_

Environments是一个非常有用的Python特点. 它让工作和不同的版本的Python和包没有打扰.([cheatsheet](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/)).

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#installing-packages)Installing packages

可以安装包通过 _conda_ 或 _pip_. 当软件时可用的, 更喜欢用conda版本, 并且使用 pip 作为一个fallback选项 (as pip is not very aware of Conda). 例:

```
conda install tifffile
Fetching package metadata .......
Solving package specifications: .
PackageNotFoundError: Package not found: '' Package missing in current osx-64 channels: 
  - tifffile

你能找到那个包在anaconda.org 通过

    anaconda search -t conda tifffile
```

你不能找到他在conda:

```
pip install tifffile
```

(如果在conda or pip都不可用, 你需要手动安装它)

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#the-pythonpath-variable)The PYTHONPATH variable

这事告诉Python去哪里找已安装的packages 如果他们没有安装到标准的(system)地方.
使用, 使用CaImAn, 我们需要去设置这个变量每次我们launch一个新的shell or terminal:

```
export PYTHONPATH="/path/to/caiman:$PYTHONPATH"
```

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#spyder)Spyder

Spyder是互动的编程环境,有些像MATLAB. Spyder有编辑器和交互的shell. 他也有一个interface可以debugging, 对象和文档的inspectors, 和变量和文件explorers.

为了launch Spyder, 你需要激活你的环境并更新PYTHONPATH变量,类型

```
spyder
```

Spyder将launch.

这有一些设置你想改的，在你首次launch它之后.
Go to Preferences -> IPython Console -> Graphics and select Backend:Qt5. 重启Spyder. 这将禁止inline figure plotting (displaying plots in a separate window).

launched之后, 去 editor and type

```
#%% DEFINES BLOCKS OF CODE
import numpy as np # math library
import scipy # scientific library
import pylab as pl # plotting library
#%% this will output some wisdom
print('Python and Calcium Imaging, a marriage made in heaven')
#%% this creates a random vector
a = np.random.random([10,10])
print(a)
#%% this will plot something
pl.imshow(a)

```

每一个 "#%%" 定义一个code block, 相当于cells (%%)在MATLAB. 为了运行每一个cells 按住Control-Enter. 如果你想运行，然后再移动到下一个cell,按住 Control-Shift-Enter.
