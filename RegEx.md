### What is Regular Expression?
>Regular expression is a set of characters used to check pattern in strings. 
>
>They're also known as RegEXP or RegEX

### Basic RegEx are:-
```
tr
sed
vi
grep
```
### Symbols and Description
```
. - Replaces any characters
^ - Matches start of String
$ - Matches end of string
* - Matches zero or more preceding charaters
\ - Represents special characters
() - Group removal expression
? - Matches exactly one characters
```
### Interval RegEx
```
{n} - Matches the preceding character appearing 'n' times exactly.
{n,m} - Matches the preceding character appearing 'n' times but not more than 'm'.
{n, } - Matches preceding character only when it appears 'n' times.
```

### Extended RegEx
```
\+ - Matches one or more occurrence of previous characters
\? - Matches zero or one occurrence of previous characters
```
###### EXAMPLE
```
grep "a\+t"
output: bat, hat, cat.
```

### Brace Expansion
```
Sequence - {0..10}
         - {a..z}
Comma separated list - {aa, bb, cc}
``` 
###### EXAMPLES
```
echo {aa, bb, cc} = aa bb cc
echo {a..b} = a b c d e f g h i j k l m n o p q r s t u v w x y z
echo {0..9} = 0 1 2 3 4 5 6 7 8 9
echo a{0..5}b = a0b a1b a2b a3b a4b a5b 
```


RESOURCES

![Youtube reference](https://youtu.be/mpyCeSvGh-M)    

[Python RegEx](https://docs.python.org/3/howto/regex.html)


