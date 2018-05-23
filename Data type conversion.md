# Data type Conversions

|**Function**|**Description**|**Example**|
|----|:----:|--:--|
|int(x [,base])|Converts x to an integer. base specifies the base if x is a string.|int('12')|
|float(x)|Converts x to a floating-point number.|float(65464)|
|complex(real [,imag])|Creates a complex number.|complex(65465)|
|str(x)|Converts object x to a string representation.|str(456)|
|repr(x)|Converts object x to an expression string.|repr(465)|
|eval(str)|Lets a python program run a python code within itself.|>>>a = 234; eval('a')|
|tuple(s)|Converts s to a tuple.|tuple('monkey'). PS. Int objects are not iterable|
|list(s)|Converts s to a list.|list('funky monkey')|
|set(s)|Converts strings,lists to a set.|list_a = 'asdf', 'qwer', 'zxcv', 'asdf'; set(list_a)|
|dict(d)|Creates a dictionary. d must be a sequence of (key,value) tuples and list.|l = [1, 2, 3, 4]; dict_a = dict(l[i:i+2] for i in range(0, len(l), 2))|
|frozenset(s)|Converts s to a frozen set.|list_a = ('asdf', 'qwer', 'zxcv', 'asdf'); frozenset(list_a)|
|chr(x)|Converts an integer to a character.|chr(1000)|
|ord(x)|Converts a single character to its integer value.|ord('a')|
|hex(x)|Converts an integer to a hexadecimal string.|hex(254)|
|oct(x)|Converts an integer to an octal string.|oct(254)|
