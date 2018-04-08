[原文地址](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html)

---

Contents

* [Introduction](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#introduction)
* [What is what: Python, Python packages, Spyder, Anaconda](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#what-is-what-python-python-packages-spyder-anaconda)
    * [Python](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#python)
    * [Python packages](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#python-packages)
    * [Spyder](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#spyder)
    * [Anaconda](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#anaconda)
* [Installation](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#installation)
* [Test your installation](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#test-your-installation)
    * [Running the tests with Spyder](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#running-the-tests-with-spyder)
    * [Running the tests from the console](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#running-the-tests-from-the-console)
    * [Missing packages](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#missing-packages)
* [Updating packages in the Anaconda installation](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#updating-packages-in-the-anaconda-installation)
* [Related tutorials](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#related-tutorials)

## [Introduction](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id1)

These notes are provided primarily for students at the
[University of Southampton](http://www.southampton.ac.uk/) (UK) in
undergraduate, postgraduate and [doctoral](http://ngcm.soton.ac.uk/)
studies to help them install Python 3 on their own
computers should they wish to do so, and to support their learning of
programming and computing, and subsequently their studies, in
particular in engineering, computer science and natural sciences.

**This is the most recent version** of the installation
instructions for the academic year 2016/2017.
(An older Version from 2014/2013, where we have used Python 2 (!) is available [here](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda-2014.html).)

In short, we suggest to use the
[Anaconda Python distribution](https://store.continuum.io/cshop/anaconda/).

By the nature of the information provided, the information is likely
to become partially outdated over time. For reference: this
mini-introduction was written in September 2016, where Anaconda 4.1
was available, and Python 3.5 is the default Python provided.

## [What is what: Python, Python packages, Spyder, Anaconda](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id2)

### [Python](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id3)

Python is

* a _programming language_ in which we write computer programs. These programs would be stored in text files that have the ending 
    <tt class="docutils literal">.py</tt>, for example 
    <tt class="docutils literal">hello.py</tt> which may contain:

    <pre class="literal-block">
    print("Hello World")
    </pre>

Python is also

* a _computer program_ (the technical term is ''interpreter'') which executes Python programs, such as 
    <tt class="docutils literal">hello.py</tt>. On windows, the Python interpeter is called 
    <tt class="docutils literal">python.exe</tt> and  from a command window we could execute the 
    <tt class="docutils literal">hello.py</tt> program by typing:

    <pre class="literal-block">
    python.exe hello.py
    </pre>

    On Linux and OS X operating systems, the Python interpreter program
    is called 
    <tt class="docutils literal">Python</tt>, so we can run the program 
    <tt class="docutils literal">hello.py</tt> as:

    <pre class="literal-block">
    python hello.py
    </pre>

    (This also works on Windows as the operating system does not need
    the 
    <tt class="docutils literal">.exe</tt> extension.)

### [Python packages](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id4)

For scientific computing and computational modelling, we need
additional libraries (so called _packages_) that are not part of the
Python standard library. These allow us, for example, to create plots,
operate on matricies, and use specialised numerical methods

The packages we generally need are

* <tt class="docutils literal">numpy</tt> (NUMeric Python): matrices and linear algebra
* <tt class="docutils literal">scipy</tt> (SCIentific Python): many numerical routines
* <tt class="docutils literal">matplotlib</tt>: (PLOTting LIBrary) creating plots of data

We also need for our teaching:

* <tt class="docutils literal">sympy</tt> (SYMbolic Python): symbolic computation
* <tt class="docutils literal">pytest</tt> (Python TESTing): a code testing framework

<!-- comment:
A package that allows to compute with numbers that have SI units
attached is

* ``physics`` : `computing with physical entities
  <physical-quantities-numerical-value-with-units-in-Python.html>`__ (numbers and units) -->

The packages 
<tt class="docutils literal">numpy</tt>, 
<tt class="docutils literal">scipy</tt> and 
<tt class="docutils literal">matplotlib</tt> are building
stones of computational work with Python and extremely widely spread.

<tt class="docutils literal">Sympy</tt> has a special role as it allows _SYMbolic_ computation
rather than numerical computation.

The 
<tt class="docutils literal">pytest</tt> package and tool supports regression testing and test
driven development -- this is generally important, and particularly so
in best practice software engineering for computational studies and
research.

<!-- comment:

The ``physics`` package is one
of several possibilities to carry out calculations where in addition
to the numerical value of an entity, we also carry along and process
the units of the entity. -->

### [Spyder](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id5)

Spyder ([home page](https://github.com/spyder-ide/spyder)) is s a powerful
interactive development environment for the Python language with
advanced editing, interactive testing, debugging and introspection
features. There is a separate blog entry providing a
[summary of key features of Spyder](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html),
which is also available as Spyder's tutorial from inside Spyder
(
<tt class="docutils literal">Help</tt> -> 
<tt class="docutils literal">Spyder tutorial</tt>).

The name SPyDER derives from "Scientific Python Development EnviRonment" (SPYDER).

We will use it as the main environment to learn about Python,
programming and computational science and engineering.

Useful features include

* provision of the IPython (Qt) console as an interactive prompt, which can display plots inline
* ability to execute snippets of code from the editor in the console
* continuous parsing of files in editor, and provision of visual warnings about potential errors
* step-by-step execution
* variable explorer

### [Anaconda](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id6)

[Anaconda](http://docs.continuum.io/anaconda/) is one of several
_Python distributions_. Python distributions provide the Python
interpreter, together with a list of Python packages and sometimes
other related tools, such as editors. The Anaconda Python distribution
was easiest to install on the University of Southampton student
computers, but other distributions provide similar functionality.

The [packages provide by the Anaconda Python distribution](https://docs.continuum.io/anaconda/pkg-docs.html) includes all of those
that we need, and for that reason we suggest to use Anaconda here.

A key part of the Anaconda Python distribution is [Spyder](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#spyder), an
interactive development environment for Python, including an editor.

## [Installation](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id7)

In general, the installation of the Python interpreter is fairly straightforward, but
installation of additional packages can be a bit tedious.

Instead of doing this manually, we suggest to install the [Anaconda](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#anaconda)
Python distribution using [these installation instructions](http://docs.continuum.io/anaconda/install.html), which provides the
Python interpreter itself and all packages we need.

The Anaconda Python distribution is available for [download](http://continuum.io/downloads) for
Windows, OS X and Linux operating systems (and free).

For Windows and OS X you are given a choice whether to download the
graphical installer or the next based installer. If you don't know
what the terminal (OS X) or command prompt (Windows) is, then you are
better advised to choose the graphical version. You want to install
the default suggestion (Python 3.5, 64bit).

Download the installer, start it, and follow instructions. Accept
default values as suggested.

(If you are using Linux and you are happy to use the package manager
of your distribution -- you will know who you are --, then you may be
better advised to install the required packages indivdually rather
than installing the whole Anaconda distribution.)

## [Test your installation](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id8)

Once you have installed [Anaconda](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#anaconda) or the Python distribution of your
choice, you can [download this testing programme](http://www.southampton.ac.uk/~fangohr/blog/code/python/soton-test-python-installation.py) and
execute it.

### [Running the tests with Spyder](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id9)

1.  Start Spyder

2.  Download the file
    [http://www.soton.ac.uk/~fangohr/blog/code/python/soton-test-python-installation.py](http://www.southampton.ac.uk/~fangohr/blog/code/python/soton-test-python-installation.py)

3.  Open the file in Spyder via 
    <tt class="docutils literal">File</tt> -> 
    <tt class="docutils literal">Open</tt>

4.  The execute the file via 
    <tt class="docutils literal">Run</tt> -> 
    <tt class="docutils literal">Run</tt>.

    If you get a pop up window, you can accept the default settings and
    click on the 
    <tt class="docutils literal">run</tt> button.

You should see output similar to this in the lower right window of
spyder (you may also see a plot appearing):

<pre class="literal-block">
Running using Python 3.5.1 |Anaconda 4.0.0 (x86_64)| (default, Dec  7 2015, 11:24:55)
[GCC 4.2.1 (Apple Inc. build 5577)]
Testing Python version-> py3.5 OK
Testing numpy...      -> numpy OK
Testing scipy ...     -> scipy OK
Testing matplotlib... -> pylab OK
Testing sympy         -> sympy OK
Testing pytest        -> pytest OK
</pre>

If the test program produces these outputs, there is a very good
chance that Python and the six listed packages are installed
correctly.

### [Running the tests from the console](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id10)

1.  Open a console:
    * Windows: type 

        <tt class="docutils literal">cmd</tt> in the search box

    * Mac OS X: Start the 

        <tt class="docutils literal">Terminal</tt> application that is located in
        the 

        <tt class="docutils literal">Utilities</tt> folder in 

        <tt class="docutils literal">Applications</tt>

    * Linux: start one of the shells you have available, or an xterm or
        so.

2.  Download the file
    [http://www.soton.ac.uk/~fangohr/blog/code/python/soton-test-python-installation.py](http://www.southampton.ac.uk/~fangohr/blog/code/python/soton-test-python-installation.py) onto your machine.

3.  Change directory into the folder you have downloaded the file to,
    and type:

    <pre class="literal-block">
    python soton-test-python-installation.py
    </pre>

If all the tests pass, you should see output similar to this:

<pre class="literal-block">
Running using Python 3.5.1 |Anaconda 4.0.0 (x86_64)| (default, Dec  7 2015, 11:24:55)
[GCC 4.2.1 (Apple Inc. build 5577)]
Testing Python version-> py3.5 OK
Testing numpy...      -> numpy OK
Testing scipy ...     -> scipy OK
Testing matplotlib... -> pylab OK
Testing sympy         -> sympy OK
Testing pytest        -> pytest OK
</pre>

### [Missing packages](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id11)

If you install Python in other ways than through the [Anaconda](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#anaconda)
distribution and, for example, you have only installed the 
<tt class="docutils literal">numpy</tt>,
<tt class="docutils literal">scipy</tt> and 
<tt class="docutils literal">matplotlib</tt> package, the program's output would be:

<pre class="literal-block">
Testing numpy...      -> numpy OK
Testing scipy...      -> scipy OK
Testing matplotlib... -> pylab OK
Testing sympy...      Could not import 'sympy' -> fail
Testing pytest...     Could not import 'pytest' -> fail
</pre>

## [Updating packages in the Anaconda installation](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id12)

To update, for example, spyder and python, follow these steps:

1.  Open a terminal (see step 1 in [Running the tests from the console](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#running-the-tests-from-the-console))

2.  Update the 
    <tt class="docutils literal">conda</tt> program (this manages the updating) by typing
    the  following command into the console:

    <pre class="literal-block">
    conda update conda
    </pre>

    Confirm updates if asked to do so. More than one package may be
    listed to be updated.

3.  Update individual packages, for example 
    <tt class="docutils literal">spyder</tt>:

    <pre class="literal-block">
    conda update spyder
    </pre>

    Other packages you may want to update include 
    <tt class="docutils literal">ipython</tt>,
    <tt class="docutils literal"><span class="pre">ipython-qtconsole</span></tt> and 
    <tt class="docutils literal"><span class="pre">ipython-notebook</span></tt>. The relevant command would
    be:

    <pre class="literal-block">
    conda update ipython ipython-qtconsole ipython-notebook
    </pre>

More details on using the conda package management system is available
in the [conda documentation page](http://conda.pydata.org/docs/).

## [Related tutorials](http://www.southampton.ac.uk/~fangohr/blog/installation-of-python-spyder-numpy-sympy-scipy-pytest-matplotlib-via-anaconda.html#id13)

Update 12 June 2015: If you prefer a video run through of an anaconda installation, check
[Steve Holden's post from June 2015](http://holdenweb.blogspot.co.uk/2015/02/how-to-get-almost-all-python-you-might.html)

<footer>

</footer>
