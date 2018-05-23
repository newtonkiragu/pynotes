# Basic Operators
Operators are the constructs which can manipulate the value of operands.
Python has the following operators
 - <a name='aro'>Arithmetic operators</a>
 - <a name='co'>Comparison (relational) operators</a>
 - <a name='aso'>Assignment operators</a>
 - <a name='lo'>Logical operators</a>
 - <a name='bo'>Bitwise operators</a>
 - <a name='mo'>Membership operators</a>
 - <a name='io'>Identity operators</a>

Assume `a = 10`, `b = 20`.
## [Arithmetic operators](#aro)
|**Operator**|**Description**|**example**|
|:----|:----|:----|
|+ Addition|adds values on either sides of the operator|a+b = 30|
|- Subtraction|subtracts right hand operand from left hand operand|b-a = 10|
|* Multiplication|multiplies values on either side of operator|a*b = 200|
|/ Division|divides left hand operand from right hand operand|a/b = 0.5|
|% Modulus|divides left hand operand from right hand operand and returns remainder|a%b = 10|
|** Exponent|performs and exponential(power) calculation on operands|a**b = 100000000000000000000|
|// Floor division| The division of operands where the result is the quotient in which the digits after the decimal point are removed. But if one of the operands is negative, the result is floored, i.e., rounded away from zero (towards negative infinity)|b//a = 2|

## [Comparison operators](#co) 
|**Operator**|**Description**|**example**|
|:----|:----|:----|
|==|if the value of operands are equal, then the condition becomes true.| (a==b) is not true|
|!=|if the values of the operands are not equal, then the condition becomes true|(a!=b) is true|
|>|If the value of left operand is greater than the value of right operand, then condition becomes true.|a>b is False|
|<|If the value of left operand is less than the value of right operand, then condition becomes true.|a\<b is True|
|>=|If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.|a>=b is False|
|<=|If the value of left operand is less than or equal to the value of right operand, then condition becomes true.|a<=b is True|

## [Assignment operators](#aso) 
|**Operator**|**Description**|**example**|
|:----|:----|:----|
|+ ADD|Assigns values from right side operands to left side operand|c = a + b assigns value of a + b into c|
|+= ADD AND|It adds right operand to the left operand and assign the result to left operand|c += a is equivalent to c = c + a|
|-= Subtract AND|It subtracts right operand from the left operand and assign the result to left operand|c -= a is equivalent to c = c - a|
|*= Multiply AND|It multiplies right operand with the left operand and assign the result to left operand|c *= a is equivalent to c = c * a|
|/= Divide AND|It divides left operand with the right operand and assign the result to left operand|c /= a is equivalent to c = c / ac /= a is equivalent to c = c / a|
|%= Modulus AND|It takes modulus using two operands and assign the result to left operand|c %= a is equivalent to c = c % a|
|**= Exponential AND|Performs exponential (power) calculation on operators and assign value to the left operand|c **= a is equivalent to c = c ** a|
|//= FLoor division|	It performs floor division on operators and assign value to the left operand|c //= a is equivalent to c = c // a|


## [Membership operators](#mo) 
Python’s membership operators test for membership in a sequence, such as strings, lists, or tuples.
|**Operator**|**Description**|**example**|
|:----|:----|:----|
|in|Evaluates to true if it finds a variable in the specified sequence and false otherwise.|x in y, here in results in a 1 if x is a member of sequence y.|
|not in|Evaluates to true if it does not finds a variable in the specified sequence and false otherwise.|x not in y, here not in results in a 1 if x is not a member of sequence y.|


## [Identity operators](#i0) 
Identity operators compare the memory locations of two objects
|**Operator**|**Description**|**example**|
|:----|:----|:----|
|is|Evaluates to true if the variables on either side of the operator point to the same object and false otherwise.|a is b returns false|
|is not|Evaluates to false if the variables on either side of the operator point to the same object and true otherwise.|a is not b returns ture|

