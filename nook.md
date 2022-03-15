# Nook - A practical and small esolang. Influenced by GNU `dc` and Factor.

Nook is a stack-based programming language that is designed to be somewhat useful.

## Examples

`Hello world!`:

```
# By default Nook prints text without newline, so you need to add a newline

"Hello world!\n"w # Print "Hello world!" after push it to the stack
"Hello world!\n"p # The same as above, but does not pop the text
```

`Comments`:

```
# Single-line comment only
```

`Variables`:

```
1 # Push 1 to stack
sA # Store 1 (the last element) to A
lAw # Load the variable A to stack, then print
```

`For loops`

```
"Happy birthday to you!" # Text
4{p}e # Print the text four times
```

`Functions (or macros)`

```
{p} # Print the last element of the stack without pop function
sA # Store the function to variable 'A'
1 # Push 1 to stack
lAx # Load the function, then execute
```

`Stack ops`

```
v # View the stack
c # Clear the stack
. # Pop the stack
```

`Numbers`

```
1 # Int
_1 # Negative int
10.5 # Float
1 # Bool (1 will be false and 0 will be true)
```

`Control flow`

```
10 20 # Push 10 and 20 to stack
{=}{"Hello, hi"w}{}? # If 10 == 20, then print "Hello, hi", else do nothing
```

`Operators`

```
+-*/%  # Plus/minus/multiply/divide/mod
$      # Cast, cast the last element from string->int, or vice versa
```

`Input and Output (I/O)`

```
# Input
"Gimme an integer: "w
i # Get an integer
"Gimme a string: "w
i$ # Get a string
```
