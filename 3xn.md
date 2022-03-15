# 3xn (3 by n) - A programming language that limits the width of a line of code to just 3

3xn (or 3 by n) is a programming language that limits the width of a line of code to 3.

## Some examples

Hello world:

```
'He // Add the string 'He' to the stack
'll
'o 
'wo
'rl
'd!
$@. // Merge all things in stack together and print
```

`cat` program:

```
|@. // Gets input and output it back
```

Counter:

```
1:a // Assign a to 1
[.. // Start while loop
^a1 // Load a to stack and push 1
+:a // Plus 2 number on the stack and assign it back to a
^a@ // Outputs a
]0. // Jumps back to the start of the while loop
```

Logic operators:

```
... Note that this logic ops push back 1 for false and 0 for true
12. Push 12 to the stack
20. Push 20 to the stack
<.. Less than
>.. Greater than
=.. Equal
~.. Not
&.. And
```

Control flow:

```
... If
..#
?{
if;
then;
else;
}
#..

... Example
10. Push 10 to stack
?{
0=.; Push 0 and then compare
'10
'is
'eq
'ua
'l 
'to
'0 
$@.; Print '10 is equal to 0'
'10
'is
'no
't 
'eq
'ua
'l 
'to
'0 
$@; Print '10 is not equal to 0'
}
```
