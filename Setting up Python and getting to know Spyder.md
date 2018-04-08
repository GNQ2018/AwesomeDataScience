# Set up Anaconda and Spyder

1.  Download the [Anaconda Python distribution](https://www.continuum.io/downloads) (we recommend the commandline version)
2.  Install Anaconda
3.  Follow these instructions to install Caiman [here](https://github.com/simonsfoundation/CaImAn#installation)

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#python-environments)Python _environments_

Environments are a very useful Python feature. They make it easy to work with different versions of Python and Packages without interference ([cheatsheet](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/)).

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#installing-packages)Installing packages

One can install packages with either _conda_ or with _pip_. When software is available in each, it is preferable to use the version in conda, and use pip as a fallback option (as pip is not very aware of Conda). As an example:

```
conda install tifffile
Fetching package metadata .......
Solving package specifications: .
PackageNotFoundError: Package not found: '' Package missing in current osx-64 channels: 
  - tifffile

You can search for that package on anaconda.org with

    anaconda search -t conda tifffile
```

If you can't find it in conda:

```
pip install tifffile
```

(if it is not available in conda or pip, you may need to manually install it)

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#the-pythonpath-variable)The PYTHONPATH variable

This tells Python where to find installed packages if they're not installed in the standard (system) places.
For example, to use CaImAn, we need to set this variable every time we launch a new shell or terminal:

```
export PYTHONPATH="/path/to/caiman:$PYTHONPATH"
```

# [<svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg>](https://github.com/flatironinstitute/CaImAn/wiki/Setting-up-Python-and-getting-to-know-Spyder#spyder)Spyder

Spyder is an interactive programming environment with several similarities to MATLAB. Spyder has an editor and an interactive shell. It also has an interface for debugging, inspectors for objects and documentation, and variable and folder explorers.

To launch Spyder, after activating your environment and updating the PYTHONPATH variable, type

```
spyder
```

Spyder will launch.

There are some settings you'll probably want to change after you launch it for the first time.
Go to Preferences -> IPython Console -> Graphics and select Backend:Qt5. Restart Spyder. This will prevent inline figure plotting (displaying plots in a separate window).

Once launched, go to the editor and type

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

Each of the "#%%" defines a code block, similarly to cells (%%) in MATLAB. In order to run each of the cells press Control-Enter. If you want to run and then move to the next cell, press Control-Shift-Enter.
