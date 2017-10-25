s = Hello

 H  e  l  l  o
 0  1  2  3  4
-5 -4 -3 -2 -1

s[1:4] is 'ell' - chars starting at index 1 and extending up to but not including index4.
s[1:] is 'ello' - omitting either index defaults to the start or end of the string.
s[:1] is 'H' - start from the beggining and stop at index 1
s[:] is 'Hello' - omitting both always gives us a copy of the whole thing.(this is the pythonic way to copy a sequence like a string or list)
s[1:100] is 'ello' - char starting at index 1 to the end of the string.

s[-1] is 'o' - last char(1st from the end)
s[-4] is 'e' - 4th from the end.
s[:-3] is 'He' - going up to but not including the last 3 chars(exclude last 3 chars).
s[-3:] is 'llo' - starting with the 3rd char from the end and extending to the end of the string(last 3 char).

s[:1] + s[1:] == s # True