### [GDB](https://www.gnu.org/software/gdb/) commands

#### General
- Start GDB
````bash
gdb [program]
````
- Running
````bash
run [args]
````
- Kill the running;
````bash
kill
````
#### Breakpoints
- Set a breakpoint
````bash
break [where (e.g., function, line)]
````
- Remove a breakpoint
````bash
delete [breakpoint#]
````
- Remove all breakpoints
````bash
clear
````
- Enable a disabled breakpoint
````bash
enable [breakpoint#]
````
- Disable a breakpoint
````bash
disable [breakpoint#]
````
#### Examining the stack
- Show call stack
````bash
backtrace
````
- Show current line
````bash
frame
````
#### Stepping 
- Go to the next instruction, but don't dive into functions
````bash
next
````
-  Go to the next instruction, diving into function
````bash
step
````
- Continue norma execution
````bash
continue
````
- Continue until the current function returns
````bash
finish
````
#### Variables and memory
- Print content of variable/memory location/register
````bash
print [something (e.g., variable)]
````
#### Threads
- Chose thread to operate on
````bash
thread [thread#]
````
#### Manipulating the program
- Change the content of a variable to the given value
````bash
set var [variable_name]=[value]
````
- Force the current function to return immdiately, passing the given value
````bash
return [expression]
````
#### Sources
- Shows the current or given source context
````bash
list
list [filename]:[function]
list [filename]:[line number]
list [first line],[last line]
````
#### Informations
- Print arguments to the function of the current stack frame 
````bash
info args
````
- Print informations about the breakpoints
````bash
info breakpoints
````
- Print the local variables in the currently selected stack frame
````bash
info locals
````
- List loaded shared libraries 
````bash
info sharedlibrary
````
- List all threads
````bash
info threads
````
- Print type of named variable
````bash
whatis [variable_name]
````

