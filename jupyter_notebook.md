### [Jupyter Notebook](http://jupyter.org/) commands


#### Open Jupyter Notebook
````bash
jupyter-notebook
````

#### Open python
````bash
python
````

#### Ipython commands
- Open ipython
````bash
ipython
````

-  Show complete box
````bash
a<Tab>
````

- Shows info about variable, docstrings if it is function/class
````bash
a?
````

- Shows source code
````bash
a??
````

- normal git command inside Ipython. Most of the Unix commands can be used this way
````bash
!git
!ls -la
````

- Using debug
````bash
debug #just after exceptation
run -d foo.py #invoke debugger before excuting any code
````

- Profiling blocks of code
````bash
prun -l -s foo()
````

- Import code
````bash
import foo_lib
````

- Load code
````bash
load foo_lib.py
````

- Run a script. No need to import, just run
````bash
run foo.py
````

- Restart code
````bash
reload(foo_lib)
````

- List commands
````bash
lsmagic
````
