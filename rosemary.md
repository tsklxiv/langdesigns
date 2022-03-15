# Rosemary - A boring scripting language

`Simple example`:

```
a: + 10 20
print a
```

[`Truth machine`](https://esolangs.org/wiki/Truth-machine):

```
// Ask for input
// Btw this is a comment
input: cast_int (ask "")
// If-then-else
// [...] are list (used as arguments in here)
// {...} are code blocks
// & are while loops
? [
  input = 0;
  { print "0" };
  { & { print "1" } };
]
```

`Factorial`:

```
// Function
// 'x', 'y', 'z' are implicit argument,
// but to clarify it, we will define the argument 'x'
fact: {[x]
  ?[> x 0; * x fact [- x 1]; 1]
}

// For loop
// For loop has implicit argument 'i', but here we will use 'n'
^ [
  n;
  1..19;
  { print ["Factorial of " n " = " fact n] };
]
```

`Numbers`:

```
a: 10 // Int
b: 3.14 // Float
c: 0xFF // Hex
d: 10e10 // 'E'
```

`Strings`:

```
s1: "This is a string"
s2: `
  This is
  a multi-line string.
  It remains exactly as the original.
`
```

`Characters`:

```
ch: 'c' // Char
ch_val: cast_int 'c' // ASCII value
```

`Arrays`:

```
d: [1 2.0 "aaa"]
```

`Dictionaries`:

```
e: #[
  name "Tuan"
  surname "Hoang"
  age 20
  likes ["pizza" "spagetti"]
]
```

`Logical values`:

```
t: true
f: false
```

`case statements`:

```
// $ is a simple version of "self" or "it"
@[
  1; // The value to check
  ?[= $ 10; { print "1 = 10, what?"}]; // Case 1
  ?[= $ 20; { print "1 = 20, what????"}]; // Case 2
  { print "Here we are" }; // Case 3, "Here we are"
]
```

`Loop through a dictionary`:

```
// Each key-value pair are break by a newline/2 spaces
dict: #[a 10  b 20  c 30]

^ [
  [key value];
  dict;
  { print [key " = " value] };
]
```

`Infinite/while loop`:

```
// Infinite loop
& {
  print "You are an idiot!"
}

// While loop
i: 0
& [
  <= i 10; // Condition
  {
    print ["i = " i]
    inc i
  }
]

// For loop
^ [
  i;
  0..10;
  { print i };
]
```

`Array indexing`:

```
arr: [1 2 3 4 5 6 7 8 9 10]
print arr!0 // 1
print first arr // 1
print arr!-1 // 10
print last arr // 10
arr!0: 2
print arr // 2 2 3 4 5 6 7 8 9 10
```
