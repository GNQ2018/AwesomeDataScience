[原文地址](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html)

---

[Hans Fangohr](http://www.southampton.ac.uk/~fangohr), University
of Southampton, UK, 2013

Spyder has developed into a fairly mature and very productive tool;
here I try to provide a tutorial. This documentation is motivated by
training courses in Python and computational modelling for students at
the University of Southampton (see [historical note](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#historical-note) for more
detail).

This blog entry has been integrated into Spyder as the
_Tutorial_. Once Spyder has started, the most up-to-date version of
this tutorial can be found under 
<tt class="docutils literal">Help</tt> -> 
<tt class="docutils literal">Spyder tutorial</tt>.

Outline

* [1   First steps with Spyder](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#first-steps-with-spyder)
    * [1.1   Execute a given program](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-a-given-program)
        * [1.1.1   Start IPython](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#start-ipython)
        * [1.1.2   Background information: What happens when you execute the program?](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#background-information-what-happens-when-you-execute-the-program)
    * [1.2   Call existing function objects from the command line](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#call-existing-function-objects-from-the-command-line)
    * [1.3   Inspecting objects](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#inspecting-objects)
    * [1.4   Updating objects](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#updating-objects)
        * [1.4.1   Simple strategy: re-execute whole program](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#simple-strategy-re-execute-whole-program)
        * [1.4.2   Looking at the details](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#looking-at-the-details)
* [2   Recommended first steps for Python beginners](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#recommended-first-steps-for-python-beginners)
    * [2.1   Switch to an IPython console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#switch-to-an-ipython-console)
    * [2.2   Reset the name space](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#reset-the-name-space)
    * [2.3   Strive for PEP8 Compliance](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#strive-for-pep8-compliance)
* [3   Selected Preferences](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#selected-preferences)
    * [3.1   Where are the preferences?](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#where-are-the-preferences)
    * [3.2   Change Spyder settings to always start with an IPython shell](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#change-spyder-settings-to-always-start-with-an-ipython-shell)
    * [3.3   Warn if PEP8 coding guidelines are violated](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#warn-if-pep8-coding-guidelines-are-violated)
    * [3.4   No convenience imports in Python Console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#no-convenience-imports-in-python-console)
    * [3.5   No convenience imports in IPython Console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#no-convenience-imports-in-ipython-console)
    * [3.6   Automatic Symbolic Python](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#automatic-symbolic-python)
* [4   Shortcuts for useful functions](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#shortcuts-for-useful-functions)
* [5   Run Settings](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#run-settings)
    * [5.1   Execute in current Python or IPython interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-in-current-python-or-ipython-interpreter)
        * [5.1.1   Persistence of objects I (after code execution)](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#persistence-of-objects-i-after-code-execution)
        * [5.1.2   Persistence of objects II (from before code execution)](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#persistence-of-objects-ii-from-before-code-execution)
    * [5.2   Execute in new dedicated Python interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-in-new-dedicated-python-interpreter)
    * [5.3   How to double check your code executes correctly "on its own"](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#how-to-double-check-your-code-executes-correctly-on-its-own)
    * [5.4   Recommendation](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#recommendation)
* [6   Other observations](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#other-observations)
    * [6.1   Multiple windows](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#multiple-windows)
    * [6.2   Environment variables](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#environment-variables)
    * [6.3   Reset all customisation](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#reset-all-customisation)
    * [6.4   Objects in the variable explorer](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#objects-in-the-variable-explorer)
* [7   Docstring formatting](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#docstring-formatting)
* [8   Debugging in the Ipython Debugger](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#debugging-in-the-ipython-debugger)
    * [8.1   Line by line step execution of code](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#line-by-line-step-execution-of-code)
    * [8.2   Debugging once an exception has occured](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#debugging-once-an-exception-has-occured)
* [9   Plotting](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#plotting)
* [10   Historical note](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#historical-note)
* [11   Versions](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#versions)
    * [11.1   Spyder version](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#spyder-version)
    * [11.2   Changes](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#changes)

---

## [1   First steps with Spyder](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id1)

### [1.1   Execute a given program](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id2)

* Get the hello world file into the Spyder editor window by either
    * Download [hello.py](http://www.southampton.ac.uk/~fangohr/blog/code/python/spyder/hello.py) and save as

        <tt class="docutils literal">hello.py</tt>. (You download the file by right-clicking on the
        link in your browser, then select 

        <tt class="docutils literal">Save Target As</tt> or 

        <tt class="docutils literal">Save
        Download as</tt>), and then

    * Open the file 

        <tt class="docutils literal">hello.py</tt> via the 

        <tt class="docutils literal">File</tt> menu, then select

        <tt class="docutils literal">Open</tt>. We express this as 

        <tt class="docutils literal">File <span class="pre">-&gt;</span> Open</tt> in short.

    or
    * click on [hello.py](http://www.southampton.ac.uk/~fangohr/blog/code/python/spyder/hello.py) to see the source code in
        the webbrowser, then copy the whole code
    * navigate to the editor window in spyder and paste the code. Then
        save the file as 

        <tt class="docutils literal">hello.py</tt>.

* To execute the program, select 
    <tt class="docutils literal">Run <span class="pre">-&gt;</span> Run</tt> (or press F5), and
    confirm the 
    <tt class="docutils literal">Run settings</tt> if required.

    You should see output like:

    <pre class="literal-block">
    Hello World
    >>>
    </pre>

    or (the particular path will depend on where you have saved the
    file, but this is inserted by Spyder automatically):

    <pre class="literal-block">
    >>> runfile('/Users/fangohr/Desktop/hello.py', wdir=r'/Users/fangohr/Desktop')
    Hello World
    >>>
    </pre>

    If so, then you have just run your first Python program - well done.

#### [1.1.1   Start IPython](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id3)

Before we proceed, please

* [Switch to an IPython console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#switch-to-an-ipython-console)

    The IPython console can do a little more than the standard Python
    console, and we suggest to use it as the default console here.

    In the IPython interpreter session that we have just started, you can use 
    <tt class="docutils literal"><span class="pre">Run-&gt;Run</span></tt> (as
    before) to execute 
    <tt class="docutils literal">hello.py</tt> and you should see:

    <pre class="literal-block">
    In [1]: runfile('/Users/fangohr/Desktop/hello.py', wdir='/Users/fangohr/Desktop')
    Hello World
    </pre>

#### [1.1.2   Background information: What happens when you execute the program?](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id4)

* Python reads the file line by line, ignoring comments

* when it comes across the 
    <tt class="docutils literal">def</tt> keyword, it knows that a function is DEFined in this and the next (one or more) lines. In the 
    <tt class="docutils literal">hello.py</tt> file, Python thus creates a _function object_ with name 
    <tt class="docutils literal">hello</tt>. All _indented_ lines following 
    <tt class="docutils literal">def <span class="pre">hello():</span></tt> belong to the function body.

    Note that the function object is just created at this point in the file, but the function is not yet called (i.e. not executed).

* when Python comes across commands (other than 
    <tt class="docutils literal">def ...</tt> and a few other keywords) that are written in the left-most column, it will execute these immediately. In the 
    <tt class="docutils literal">hello.py</tt> file this is only the line reading 
    <tt class="docutils literal">hello()</tt> which will actually call (i.e. _execute_) the function with name 
    <tt class="docutils literal">hello</tt>.

    If you remove the line 
    <tt class="docutils literal">hello()</tt> from the program and run the whole file
    again (by pressing F5, or selecting 
    <tt class="docutils literal">run <span class="pre">-&gt;</span> run</tt>), nothing will be
    printed (because the function 
    <tt class="docutils literal">hello</tt> is defined, but not called,
    i.e. not executed).

Now you should know how to execute a Python program that you have in
the editor window in Spyder using the Python Console, and the more
sophisticated IPython Console.

If you are just starting to learn Python, this is probably a good
point to return to your text book / course and look at more basic
examples.

The next section gives more detailed information how you can execute
_parts_ of the code in the editor in the Python console, and thus
update parts of your definitions in the editor. This is a more
advanced technique but can be very useful. (You may also be interested
in the option to execute chunks (so-called "cells") of code that are
seperated by delimiters -- see [Shortcuts for useful functions](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#shortcuts-for-useful-functions).)

### [1.2   Call existing function objects from the command line](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id5)

Once you have executed the 
<tt class="docutils literal">hello.py</tt> program, the function object 
<tt class="docutils literal">hello</tt> is defined and known at the Python prompt. We can thus call the function from the Python prompt:

* Call the 
    <tt class="docutils literal">hello()</tt> function from the Python prompt, i.e. type
    <tt class="docutils literal">hello()</tt> in the Python Shell window (the Python prompt shows as
    <tt class="docutils literal">&gt;&gt;&gt;</tt>, or as 
    <tt class="docutils literal">In <span class="pre">[?]</span></tt> if we use the IPython session where the
    question mark can be any positive integer number.), and press the
    return key.

    You should find that the 
    <tt class="docutils literal">hello()</tt> function is executed again,
    i.e. 
    <tt class="docutils literal">Hello World</tt> is printed again. Your function call at the
    Python prompt together with the output should look like this:

    <pre class="literal-block">
    In [ ]: hello()
    Hello World
    </pre>

* Can you see how this differs from executing the whole program again?

    When we execute the whole program (by pressing F5), Python goes
    through the file, creates the 
    <tt class="docutils literal">hello</tt> function object (overriding
    the previous object), reaches the main program and calls the
    function.

    When we call 
    <tt class="docutils literal">hello()</tt> from the Python prompt, we only call the
    function objects 
    <tt class="docutils literal">hello</tt> that has been defined in the (I)Python
    console when we executed the whole 
    <tt class="docutils literal">hello.py</tt> file earlier (by
    pressing 
    <tt class="docutils literal">F5</tt>).

    This will become clearer over time and also when we work with
    slightly larger examples. You may want to return to this tutorial at
    a slightly later stage.

### [1.3   Inspecting objects](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id6)

* Python provides a function that displays all known objects (in the
    current name space). It is called 
    <tt class="docutils literal">dir()</tt>: when you type 
    <tt class="docutils literal">dir()</tt>
    at the prompt, you get a list of known objects. Ignore everything
    starting with an underscore for now. Can you see 
    <tt class="docutils literal">hello</tt> in the
    list?

    (If you get a long list of defined objects, then Spyder may have
    done some convenience imports for you already. To address this you
    may want to:
    * [Reset the name space](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#reset-the-name-space) (you may want to follow instructions
        at [No convenience imports in IPython Console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#no-convenience-imports-in-ipython-console) to change the
        default settings)
    * execute the file 

        <tt class="docutils literal">hello.py</tt> again by pressing F5

    Then run 
    <tt class="docutils literal">dir()</tt> as suggested above.
    )

* Once an object is visible in the current name space (as is 
    <tt class="docutils literal">hello</tt>
    in this example), we can use the 
    <tt class="docutils literal">help</tt> function as follows to
    learn about it: Type 
    <tt class="docutils literal">help(hello)</tt> at the Python prompt, you
    should see output like this:

    <pre class="literal-block">
    In [ ]: help(hello)
    Help on function hello in module __main__:

    hello()
        Print "Hello World" and return None
    </pre>

    Where does Python take the information from? Some of it (like the
    number of input arguments and names of those variables; here we have
    no input arguments) Python can find through inspecting its objects,
    additional information comes from the documentation string provided
    for the function object 
    <tt class="docutils literal">hello</tt>. The documentation string is the
    first string immediately below the line 
    <tt class="docutils literal">def <span class="pre">hello():</span></tt>.

* The Spyder environment also provides a panel in the top right corner
    (by default) which is the 
    <tt class="docutils literal">Object inspector</tt>. If you type
    <tt class="docutils literal">hello</tt> into the empty line in the Object inspector window, it
    will also provide the help string.![Object explorer shows docstring](http://www.southampton.ac.uk/~fangohr/blog/images/spyder-hello-docstring.png)

### [1.4   Updating objects](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id7)

#### [1.4.1   Simple strategy: re-execute whole program](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id8)

* In the Editor window, change the function 
    <tt class="docutils literal">hello</tt> so
    that it prints 
    <tt class="docutils literal">Good Bye World</tt> rather than 
    <tt class="docutils literal">Hello World</tt>.

* Press F5 (to execute the whole program) and check that the output of the program is now:

    <pre class="literal-block">
    Good Bye World
    </pre>

What has happened when you pressed F5 is this: Python has gone through
the 
<tt class="docutils literal">hello.py</tt> file and created a new function object 
<tt class="docutils literal">hello</tt>
(overriding the function object 
<tt class="docutils literal">hello</tt> we had defined before) and
then executed the function.

#### [1.4.2   Looking at the details](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id9)

We need to start with a clearly defined state. To do this, please
change the function 
<tt class="docutils literal">hello()</tt> back so that it prints 
<tt class="docutils literal">Hello World</tt>
(i.e. use the original [hello.py](http://www.southampton.ac.uk/~fangohr/blog/code/python/spyder/hello.py) file), then press F5 to
run the whole program and check that it prints 
<tt class="docutils literal">Hello World</tt>.

* Call the function 
    <tt class="docutils literal">hello()</tt> from the command prompt (as described
    in [Call existing function objects from the command line](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#call-existing-function-objects-from-the-command-line)). You
    should see 
    <tt class="docutils literal">Hello World</tt> printed.

* Now change the function definition so that it would print 
    <tt class="docutils literal">Laters
    World</tt>, and save the file (but do NOT execute the program, i.e. do
    NOT press F5 yet).

* Call the function 
    <tt class="docutils literal">hello()</tt> from the command prompt again. You
    should find that the text printed reads 
    <tt class="docutils literal">Hello World</tt>, like here

    <pre class="literal-block">
    In [ ]: hello()
    Hello World
    </pre>

    Why is this so? Because the 
    <tt class="docutils literal">hello</tt> function object in the Python
    _interpreter_ is the old one which prints 
    <tt class="docutils literal">Hello World</tt>. So far, we
    have changed the file 
    <tt class="docutils literal">hello.py</tt> (and replaced 
    <tt class="docutils literal">Hello World</tt> in
    there with 
    <tt class="docutils literal">Laters World</tt>) in the editor but this has not affected the objects
    that have previously been created in the Python interpreter.

Here are two possibilities to use our modified version of the 
<tt class="docutils literal">hello</tt> function:

* Option 1: execute the whole file 
    <tt class="docutils literal">hello.py</tt> again by pressing F5:
    this creates a new function object 
    <tt class="docutils literal">hello</tt> (and overrides the old
    one). You should find that if you press F5, and then call
    <tt class="docutils literal">hello()</tt> at the prompt, the new text 
    <tt class="docutils literal">Laters World</tt> is printed.

* Option 2: select the region you have changed (in this case the whole
    function 
    <tt class="docutils literal">hello</tt>, starting from the line 
    <tt class="docutils literal">def <span class="pre">hello():</span></tt> down to
    <tt class="docutils literal">return None</tt>, and then select 
    <tt class="docutils literal">Run <span class="pre">-&gt;</span> Run selection</tt>.

    This will update the 
    <tt class="docutils literal">hello</tt> object in the interpreter without
    having to execute the whole 
    <tt class="docutils literal">hello.py</tt> file:

    <pre class="literal-block">
    In [ ]: def hello():
       ...:     """Print "Hello World" and return None"""
       ...:     print("Laters world")
       ...:
    </pre>

    If we now type 
    <tt class="docutils literal">hello()</tt>, we see the update response:

    <pre class="literal-block">
    In [ ]: hello()
    Laters world
    </pre>

The ability to execute _parts of the code_ to update some objects in
the interpreter (in the example above, we updated the function object
<tt class="docutils literal">hello</tt>), is of great use when developing and debugging more complex
codes, and when creating objects/data in the interpreter session take
time. For example, by modifying only the functions (or
classes/objects, etc) that we are actually developing or debugging, we
can keep re-using the data structures etc that are defined in the
interpreter session.

## [2   Recommended first steps for Python beginners](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id10)

To teach Python programming and computational modelling, we recommend
to (i) use IPython instead of the normal Python interpreter and (ii)
not use any convenience imports. This accepts IPython as the de-facto
standard and helps to better understand namespaces.

Spyder tries to help more advanced users by importing a number of modules into the main
name space. Type 
<tt class="docutils literal">scientific</tt> in the command prompt to see the
details. This behaviour may change in future Spyder releases.

While these convenience imports are very useful for more experienced
programmers, they can be confusing (if not misleading) for beginners. We
thus recommend to 
<tt class="docutils literal">undo</tt> these imports to fulfil our requirements
outline above and to (i) [switch to an IPython console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#switch-to-an-ipython-console), and (ii)
issue the 
<tt class="docutils literal">%reset</tt> command to [reset the name space](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#reset-the-name-space). Both steps are
explained in more detail in the next section.

### [2.1   Switch to an IPython console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id11)

In the console window (lower right corner by default), you see by
default a prompt with three greater than signs, i.e. 
<tt class="docutils literal">&gt;&gt;&gt;</tt>. This
shows that we are using the 
<tt class="docutils literal">console</tt> -- basically a normal Python
interpreter session (with some added functionality from Spyder).

Instead, we would like to use an _Interactive Python_ shell, short
_IPython_ from the [ipython project](http://www.ipython.org/). To do this, select 
<tt class="docutils literal">Interpreters</tt> -> 
<tt class="docutils literal">Open an IPython
Console</tt>.

You should see in the consolse window a new shell appearing, and the
IPython prompt 
<tt class="docutils literal">In [</tt>**1**
<tt class="docutils literal">]:</tt> should be displayed.

See also: [Change Spyder settings to always start with an IPython shell](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#change-spyder-settings-to-always-start-with-an-ipython-shell)

### [2.2   Reset the name space](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id12)

The name space can be cleared in IPython using the 
<tt class="docutils literal">%reset</tt>
command. Type 
<tt class="docutils literal">%reset</tt> and press return, then confirm with 
<tt class="docutils literal">y</tt>:

<pre class="literal-block">
In [1]: %reset

Once deleted, variables cannot be recovered. Proceed (y/[n])? y

In [2]:
</pre>

That's all.

We discuss this a little further, but you can skip the following if
you are not interested: After issuing the 
<tt class="docutils literal">%reset</tt> command, we
should have only a few objects defined in the namespace of that
session. We can list all of them using the 
<tt class="docutils literal">dir()</tt> command:

<pre class="literal-block">
In [2]: dir()
Out[2]:
['In',
 'Out',
 '__builtin__',
 '__builtins__',
 '__name__',
 '_dh',
 '_i',
 '_i2',
 '_ih',
 '_ii',
 '_iii',
 '_oh',
 '_sh',
 'exit',
 'get_ipython',
 'help',
 'quit']
</pre>

Finally, if you like to skip the confirmation step of the 
<tt class="docutils literal">reset</tt>
command, use can use 
<tt class="docutils literal">%reset <span class="pre">-f</span></tt> instead of 
<tt class="docutils literal">%reset</tt>.

### [2.3   Strive for PEP8 Compliance](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id13)

In addition to the Syntax that is enforced by Python, there are
additional conventions regarding the layout of sourcecode, in
particular the [Style Guide for Python source code](http://www.python.org/dev/peps/pep-0008/) knows as "PEP8".

You should change Spyders settings to [Warn if PEP8 coding guidelines are violated](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#warn-if-pep8-coding-guidelines-are-violated).

## [3   Selected Preferences](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id14)

### [3.1   Where are the preferences?](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id15)

A lot of Spyder's behaviour can be configured through it's
Preferences. Where this is located in the menu depends on your
operating system:

* On Windows and Linux, go to 

    <tt class="docutils literal">Tools <span class="pre">-&gt;</span> Preferences</tt>

* On Mac OS, go to 

    <tt class="docutils literal">Python <span class="pre">-&gt;</span> Preferences</tt>

### [3.2   Change Spyder settings to always start with an IPython shell](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id16)

Go to 
<tt class="docutils literal">Preferences <span class="pre">-&gt;</span> IPython console <span class="pre">-&gt;</span> Startup</tt> and
select the tickbox next to 
<tt class="docutils literal">Open an IPython console at
startup</tt>. Then click the 
<tt class="docutils literal">OK</tt> button.

The next time Spyder starts, it will show the IPython console
automatically.

### [3.3   Warn if PEP8 coding guidelines are violated](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id17)

Go to 
<tt class="docutils literal">Preferences <span class="pre">-&gt;</span> Editor <span class="pre">-&gt;</span> Code
Introspection/Analysis</tt> and
select the tickbox next to 
<tt class="docutils literal">Style analysis (PEP8)</tt>

### [3.4   No convenience imports in Python Console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id18)

To avoid any 'magic' when the console is started, go to

<tt class="docutils literal">Preferences <span class="pre">-&gt;</span> Console <span class="pre">-&gt;</span> Advanced Settings <span class="pre">-&gt;</span> PYTHONSTARTUP
replacement</tt>
and select 
<tt class="docutils literal">Default PYTHONSTARTUP script</tt> (and restart Spyder).

(This magic, amongst other things, runs the 
<tt class="docutils literal">from __future__ import
division</tt> command.)

The [default settings may change](https://groups.google.com/forum/#!topic/spyderlib/yTm4j9madZM)
for this in the next major release.

### [3.5   No convenience imports in IPython Console](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id19)

To avoid import of all objects from 
<tt class="docutils literal">pylab</tt> and 
<tt class="docutils literal">numpy</tt> into the
current name space in the IPython Console, go to
<tt class="docutils literal">Preferences <span class="pre">-&gt;</span> IPython console <span class="pre">-&gt;</span> Graphics</tt> and
deselect the tickbox next to 
<tt class="docutils literal">Automatically load Pylab and NumPy
modules</tt> and also deselect 
<tt class="docutils literal">Activate support</tt>.

The [default settings may change](https://groups.google.com/forum/#!topic/spyderlib/yTm4j9madZM)
for this in the next major release.

### [3.6   Automatic Symbolic Python](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id20)

Through 
<tt class="docutils literal">Preferences <span class="pre">-&gt;</span> IPython console <span class="pre">-&gt;</span> Advanced Settings <span class="pre">-&gt;</span> Use
symbolic math</tt> we can activate IPython's symbolic python mode. This
will allow nicely rendered sympy output (latex style) and also imports
some sympy objects automatically when the IPython console starts, and
reports what it has done.

<pre>
Thesecommands wereexecuted:
>>> from __future__ import division
>>> from sympy import \*
>>> x, y, z, t = symbols('x y z t')
>>> k, m, n = symbols('k m n', integer=True)
>>> f, g, h = symbols('f g h', cls=Function)
</pre>

We can then use the variables 
<tt class="docutils literal">x</tt>, 
<tt class="docutils literal">y</tt>, for example like this:![Rendered Sympy output](http://www.southampton.ac.uk/~fangohr/blog/images/spyder-sympy-example.png)

## [4   Shortcuts for useful functions](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id21)

* F5 executes the current buffer

* F9 executes the currently highlighted chunk of code: this is very
    useful to update definitions of functions (say) in the interpreter session without
    having to run the whole file again

* <tt class="docutils literal">CTRL + &lt;RETURN&gt;</tt> executes the current cell (menu enty 
    <tt class="docutils literal">Run <span class="pre">-&gt;</span> Run cell</tt>). A cell is defined as the
    code between two lines which start with the agreed tag 
    <tt class="docutils literal">#%%</tt>.

* <tt class="docutils literal">SHIFT + &lt;RETURN&gt;</tt> executes the current cell and advances the
    cursor to the next cell (menu entry 
    <tt class="docutils literal">Run <span class="pre">-&gt;</span> Run cell and
    advance</tt>).

    Cells are useful to execute a large file/code segment in smaller
    units. (It is a little bit like a cell in an IPython notebook, in
    that chunks of code can be run independently.)

* <tt class="docutils literal">ALT + &lt;CURSOR UP&gt;</tt> moves the current line up. If multiple lines are
    highlighted, they are moved up together. 
    <tt class="docutils literal"><span class="pre">ALT+&lt;CURSOR</span> DOWN&gt;</tt>
    works correspondingly moving line(s) down.

* Right clicking on a function/method in the source, opens a new
    editor windows showing the definition of that function.

* <tt class="docutils literal">SHIFT+CTRL+ALT+M</tt> maximises the current window (or changes the
    size back to normal if pressed in a maximised window)

* <tt class="docutils literal">SHIFT+CTRL+F</tt> activates the search across all files.

* On Mac OS X: 
    <tt class="docutils literal">CMD</tt> + 
    <tt class="docutils literal">+</tt> will increase the font size in the editor,
    <tt class="docutils literal">CMD</tt> + 
    <tt class="docutils literal">-</tt> decrease. Also works in the IPython Console.

    The font size for the object explorer, the Python console etc can be set
    individually via 
    <tt class="docutils literal">Preferences <span class="pre">-&gt;</span> Object explorer</tt> etc.

    I couldn't find a way of changing the font size in the variable explorer.

* <tt class="docutils literal">CTRL+SPACE</tt> autocompletes commands, function names, variable
    names, methods; very useful.

* <tt class="docutils literal">CMD+s</tt> (on Mac OS X) and 
    <tt class="docutils literal">CTRL+s</tt> (otherwise) _in the editor_
    window saves the file
    currently being edited. This also forces various warning triangles
    in the left column of the editor to be updated (otherwise they
    update every 2 to 3 seconds by default).

* <tt class="docutils literal">CMD+s</tt> (on Mac OS X) and 
    <tt class="docutils literal">CTRL+s</tt> (otherwise) _in the IPython console_
    window saves the current IPython session as an HTML file, including
    any figures that may be displayed inline. This is useful as a quick
    way of recording what has been done in a session.

    (It is not
    possible to load this saved record back into the session - if you
    need functionality like this, look for the IPython Notebook.)

* <tt class="docutils literal">CMD+i</tt> (on Mac OS X) and 
    <tt class="docutils literal">CTRL+i</tt> (otherwise) when pressed
    while the cursor is on an object, opens documentation for that
    object in the object inspector.

## [5   Run Settings](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id22)

These are the settings that define how the code in the editor is
executed if we select 
<tt class="docutils literal">Run <span class="pre">-&gt;</span> Run</tt> or press F5.

By default, the settings box will appear the first time we try to execute a
file. If we want to change the settings at any other time, they can be
found under 
<tt class="docutils literal">Run <span class="pre">-&gt;</span> Configure</tt> or by pressing F6.

There are three choices for the interpreter to use, of which I'll
discuss the first two. Let's assume we have a program 
<tt class="docutils literal">hello.py</tt> in the editor
which reads

<pre>
def hello(name):
    """Given an object 'name', print 'Hello ' and the object."""
    print("Hello {}".format(name))

i = 42
if __name__ == "__main__":
    hello(i)
</pre>

### [5.1   Execute in current Python or IPython interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id23)

This is the default suggestion, and also generally a good choice.

#### [5.1.1   Persistence of objects I (after code execution)](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id24)

Choosing 
<tt class="docutils literal">Execute in current Python or IPython interpreter
setting</tt> under 
<tt class="docutils literal">Run <span class="pre">-&gt;</span> Configure</tt> means that

1.  When the execution of 
    <tt class="docutils literal">hello.py</tt> is completed, we can interact
    with the interpreter in which the program ran, and we can use the
    convenient IPython interpreter for this (rather than the default
    Python interpreter).

    In particular,

2.  we can inspect and interact with objects that the execution of
    our program created, such as 
    <tt class="docutils literal">i</tt> and 
    <tt class="docutils literal">hello()</tt>.

This is generally very useful for incremental coding, testing and
debugging: we can call 
<tt class="docutils literal">hello()</tt> directly from the interpreter
prompt, and don't need to execute the whole 
<tt class="docutils literal">hello.py</tt> for this
(although if we change the function 
<tt class="docutils literal">hello()</tt>, we need to execute
the buffer, or at least the function definition, to make the new
version of 
<tt class="docutils literal">hello()</tt> visible at the interpreter; either by
executing the whole buffer or via 
<tt class="docutils literal">Run <span class="pre">-&gt;</span> Run Selection</tt>.)

#### [5.1.2   Persistence of objects II (from before code execution)](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id25)

However, executing the code in the editor in the current interpreter
also means that

1.  the code that executes can see other (global) objects that were
    defined in the interpreter session.

_This_ persistence of objects is easily forgotton and usually not
required when working on small programs (although it can be of great
value occasionally). These objects could come from previous execution
of code, from interactive work in the interpreter, or from convenience
imports such as 
<tt class="docutils literal">from pylab import *</tt> (Spyder may do some of those
convenience imports automatically).

This visibility of objects in the interpreter global name space to the
code we execute may also result in coding mistakes if the code
inadvertently relies on these objects.

Here is an example: imagine that

* we run the code 

    <tt class="docutils literal">hello.py</tt>. Subsequently, the variable 

    <tt class="docutils literal">i</tt>
    is known in the interpreter as a global variable.

* we edit the 

    <tt class="docutils literal">hello.py</tt> source and accidentally delete the line 

    <tt class="docutils literal">i = 42</tt>

* we execute the buffer containing 

    <tt class="docutils literal">hello.py</tt> again. At this
    point, the call of 

    <tt class="docutils literal">hello(i)</tt> will _not_ fail because the
    interpreter has an object of name 

    <tt class="docutils literal">i</tt> defined, although this is
    not defined in the source of 

    <tt class="docutils literal">hello.py</tt>.

At this point, we could save 
<tt class="docutils literal">hello.py</tt> and (falsely) think it
would execute correctly. However, running it in a new python
interpreter session (or via 
<tt class="docutils literal">python hello.py</tt>, say) would result
in an error, because 
<tt class="docutils literal">i</tt> is not defined.

The problem arises because the code makes use of an object (here
<tt class="docutils literal">i</tt>) without creating it. This also affects importing of modules: if
we had imported 
<tt class="docutils literal">pylab</tt> at the IPython prompt, then our program will
see that when executed in this IPython interpreter session.

To learn how we can double check that our code does not depend on such
existing objects, see [How to double check your code executes correctly "on its own"](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#how-to-double-check-your-code-executes-correctly-on-its-own) .

### [5.2   Execute in new dedicated Python interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id26)

Choosing 
<tt class="docutils literal">Execute in new dedicated Python interpreter</tt> under 
<tt class="docutils literal">Run
<span class="pre">-&gt;</span> Configure</tt> will start _a new Python interpreter everytime_ the
<tt class="docutils literal">hello.py</tt> program is executed. The major advantage of this mode
over [Execute in current Python or IPython interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-in-current-python-or-ipython-interpreter) is that we
can be certain that there are no global objects defined in this
interpreter which originate from debugging and repeated execution of
our code: every time we run the code in the editor, the python
interpreter in which the code runs is restarted.

This is a safe option, but provides less flexibility and cannot use
the IPyton interpreter.

### [5.3   How to double check your code executes correctly "on its own"](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id27)

Assuming you have chosen for your code to [Execute in current Python or IPython interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-in-current-python-or-ipython-interpreter),
then you two options to check that our code does work on its own
(i.e. it does not depend on undefined variables, unimported modules
and commands etc.)

1.  Switch from [Execute in current Python or IPython interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-in-current-python-or-ipython-interpreter)
    to [Execute in new dedicated Python interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-in-new-dedicated-python-interpreter),
    and execute the code in the editor in this dedicated Python interpreter.

    Alternatively, if you want to stay with the current IPython
    interpreter, you can

2.  Use IPython's magic 
    <tt class="docutils literal">%reset</tt> command which will remove all
    objects (such as 
    <tt class="docutils literal">i</tt> in the example above) from the current name
    space, and then execute the code in the editor.

### [5.4   Recommendation](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id28)

My recommendation for beginners would be to [Execute in current Python or IPython interpreter](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#execute-in-current-python-or-ipython-interpreter), _and_
to chose the IPython interpreter for this (see also [Change Spyder settings to always start with an IPython shell](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#change-spyder-settings-to-always-start-with-an-ipython-shell)).

Once you have completed a piece of code, double check that it executes
independently using one of the options explained in
[How to double check your code executes correctly "on its own"](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#how-to-double-check-your-code-executes-correctly-on-its-own).

## [6   Other observations](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id29)

### [6.1   Multiple windows](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id30)

When multiple files are opened in the editor, the
corresponding tabs at the top of the window area are arranged in
alphabetical order of the filename from left to right.

On the left of the tabs, there is as icon that shows 
<tt class="docutils literal">Browse tabs</tt>
if the mouse hovers over it. It is useful to jump to a particular
file directly, if many files are open.

### [6.2   Environment variables](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id31)

Environment variables can be displayed from the Console window (bottom right window in
default layout). Click on the 
<tt class="docutils literal">Options</tt> icon (the tooltip is
<tt class="docutils literal">Options</tt>), then select 
<tt class="docutils literal">Environment variables</tt>.

### [6.3   Reset all customisation](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id32)

All customisation saved on disk can be reset by calling spyder from
the command line with the switch 
<tt class="docutils literal"><span class="pre">--reset</span></tt>, i.e. a command like
<tt class="docutils literal">spyder <span class="pre">--reset</span></tt>.

### [6.4   Objects in the variable explorer](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id33)

Right-clicking on arrays in the variable explorer gives options to
plot and analyse these further.

Double clicking on a dictionary object opens a new window that
displays the dictionary nicely.

Presumably there is other 'hidden' capability for some other data types.

## [7   Docstring formatting](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id34)

There are some conventions assumed regarding documentation strings
written in restructured text. If we follow those guidelines, we can
obtain beautifully formated documentation strings in Spyder.

For example, to get our 
<tt class="docutils literal">average()</tt> function look like this in the
Spyder Object explorer:![Rendering of docstring](http://www.southampton.ac.uk/~fangohr/blog/images/spyder-nice-docstring-rendering.png)

We need to format the documentation string as follows

<pre>
def average(a, b):
    """
    Given two numbers a and b, return their average value.

    Parameters
    ----------
    a : number
      A number
    b : number
      Another number

    Returns
    -------
    res : number
      The average of a and b, computed using 0.5*(a + b)

    Example
    -------
    >>> average(5, 10)
    7.5

    """

    return (a + b) \* 0.5
</pre>

What matters here, is that the word 
<tt class="docutils literal">Parameters</tt> is used, and
underlined. The line 
<tt class="docutils literal">a : number</tt> shows us that the type of the
parameter 
<tt class="docutils literal">a</tt> is 
<tt class="docutils literal">number</tt>. In the next line, which is indented, we
can write a more extended explanation what this variable represents,
what conditions the allowed types have to fulfil etc.

The same for all Parameters, and also for the returned value.

Often it is a good idea to include an example as shown.

## [8   Debugging in the Ipython Debugger](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id35)

### [8.1   Line by line step execution of code](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id36)

Activating the debug mode (
<tt class="docutils literal">Debug <span class="pre">-&gt;</span> Debug</tt>) starts the IPython
debugger (ipdb) in the IPython console. This is operated as normal,
but the editor display window highlights the line that is about to be
executed, and the variable explorer displays variables in the current
context of the point of program execution. (It only displays
'numerical' variables, i.e. not function objects etc.)

The key commands within the IPython debugger are indivdual keystrokes:

* <tt class="docutils literal">s</tt> to Step into the current statement. If this is a function
    call, step into that function.
* <tt class="docutils literal">n</tt> move to the Next statement. If the current statement is a
    function, do not step into that function, but execute it completely
    before returning control to the interactive debugger prompt.
* <tt class="docutils literal">r</tt> complete all statements in the current function and Return
    from that function before returning control.
* <tt class="docutils literal">p</tt> Print allows to display values of variables, for example

    <tt class="docutils literal">p x</tt> will print the value of the variable 

    <tt class="docutils literal">x</tt>.

Note that at the ipdb, you can also _change_ values of variable. For
example, to modify a valiable 
<tt class="docutils literal">x</tt>, you can say 
<tt class="docutils literal">ipdb &gt; x = 42</tt>
and the debugger will carry on with 
<tt class="docutils literal">x</tt> being bound to 
<tt class="docutils literal">42</tt>. You
can also call functions, and do many others things.

To leave the debugging mode, you can type 
<tt class="docutils literal">exit</tt> or select from the
menu 
<tt class="docutils literal">Debug <span class="pre">-&gt;</span> Debugging Control <span class="pre">-&gt;</span> Exit</tt>

### [8.2   Debugging once an exception has occured](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id37)

In the IPython console, we can call 
<tt class="docutils literal">%debug</tt>
straight after an exception has been raised: this will start the
IPython debug mode, and allows inspection of local variables at the
point where the exception occurred as described above. This is a lot
more efficient than adding 
<tt class="docutils literal">print</tt> statements to the code an
running it again.

If you use this, you may also want to use the commands 
<tt class="docutils literal">up</tt> and
<tt class="docutils literal">down</tt> which navigate the inspection point up and down the
stack. (Up the stack means to the functions that have called the
current function; down is the opposite direction.)

## [9   Plotting](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id38)

Assuming we use an IPython console with version >= 1.0.0, we can
decide whether figures created with matplotlib/pylab will show

1.  _inline_, i.e. inside the IPython console, or whether they should
2.  appear inside a new window.

Option 1 is convenient to save a record of the interactive session
(section [Shortcuts for useful functions](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#shortcuts-for-useful-functions) lists a shortcut to save
the IPython console to an html file).

Option 2 allows to interactively zoom into the figure, manipulate it a little, and
save the figure to different file formats via the menu.

The command to get the figures to appear _inline_ in the IPython
console is
<tt class="docutils literal">%matplotlib inline</tt>.

The command to get figures appear in their own window (which
technically is a QT windown) is 
<tt class="docutils literal">%matplotlib qt</tt>.

The Spyder preferences can be used to customise the default behaviour
(in particular 
<tt class="docutils literal">Preferences <span class="pre">-&gt;</span> IPython Console <span class="pre">-&gt;</span> Graphics <span class="pre">-&gt;</span>
Activate Support</tt> to switch into inline plotting).

## [10   Historical note](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id39)

This tutorial is based on [notes](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html)
by [Hans Fangohr](http://www.southampton.ac.uk/~fangohr), that are
used at the [University of Southampton](http://www.soton.ac.uk/) to
[teach Python for computational modelling](http://www.southampton.ac.uk/~fangohr/teaching/python.html) to undegraduate
engineers and postgraduate PhD students for the
[Next Generation Computational Modelling](http://ngcm.soton.ac.uk/)
doctoral training centre.

## [11   Versions](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id40)

### [11.1   Spyder version](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id41)

The notes above have been created in September 2013 with Spyder 2.2.14
on Mac OS, installed via Anaconda.

Additions after 18 October 2013 tested with Spyder 2.2.4 and IPython 1.0.0.

### [11.2   Changes](http://www.southampton.ac.uk/~fangohr/blog/spyder-the-python-ide.html#id42)

22 September 2013: Update location of preferences, add notes on debugger and
variable explorer.

23 September 2013: Add section on run settings.

30 September 2013: How to avoid automatic imports and other magic in
Python and IPython console added.

18 October 2013: Add 
<tt class="docutils literal">%matplotlib</tt> command, and shortcuts for
executing a cell.

21 October 2013: Adding 
<tt class="docutils literal">%debug</tt> after exception, Adding section "first steps", adding numbering of sections

29 December 2013: Reviewed for inclusion into Spyder, minor fixes and improvements.
