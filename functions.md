# Function
A function is a block of organized, reusable code that is used to perform a single, related action.

Syntax
```
def functionname( parameters ):
   "function_docstring"
   function_suite
   return [expression]
```
Example
```
# Function definition is here
def changeme( mylist ):
   "This changes a passed list into this function"
   mylist.append([1,2,3,4]);
   print "Values inside the function: ", mylist
   return

# Now you can call changeme function
mylist = [10,20,30];
changeme( mylist );
print "Values outside the function: ", mylist
```

## dir()
Returns a sorted list of strings containing the names defined by a module

Example
```
#!/usr/bin/python

# Import built-in module math
import math
print dir(math)
```