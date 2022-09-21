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

- Normal git command inside Ipython. Most of the Unix commands can be used this way
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

- Display all the content of the external file as its output
````bash
%pycat foo.py
````

- List commands
````bash
lsmagic
````

- Shows how much time a code needs to run
````bash
%time a = some_function()  #Return the running time on this line

%timeit a = some_function() #Return more details, such number of loops

%%time	#Return the running time about all the code below
a = some_funtion()
b = some_another_function()
````

- Shows the list of variables in your environment
````bash
%who_ls 		#Outputs a list of all interactive variables in your environment

%who_ls function	#Reduces the output to interactive variables of type "function"
````
