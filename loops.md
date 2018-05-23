# Loops
A loop statement allows us to excecute a statement or multiple statements multiple times

## for loop
Executes a sequence of statements multiple times and abbreviates the code that manages the loop variable.

syntax
```
for iterating_var in sequence:
   statements(s)
```
Example
```
for letter in 'Python':     # First Example
   print 'Current Letter :', letter

fruits = ['banana', 'apple',  'mango']
for fruit in fruits:        # Second Example
   print 'Current fruit :', fruit

print "Good bye!"
```
 - iterating by sequence
```
fruits = ['banana', 'apple',  'mango']
for index in range(len(fruits)):
   print 'Current fruit :', fruits[index]

print "Good bye!
```
## while loop
Repeats a statement or group of statements while a given condition is TRUE. It tests the condition before executing the loop body.

Syntax
```
while expression:
   statement(s)
```
Example
```
count = 0
while (count < 9):
   print 'The count is:', count
   count = count + 1

print "Good bye!"
```
 - Infinite loop

A loop becomes infinite loop if a condition never becomes FALSE. 
```
var = 1
while var == 1 :  # This constructs an infinite loop
   num = raw_input("Enter a number  :")
   print "You entered: ", num

print "Good bye!"
```
 - single statement suites
```
flag = 1
while (flag): print 'Given flag is really true!'
print "Good bye
```