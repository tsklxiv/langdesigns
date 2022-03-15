# Lushie - A Q-style, interpreted programming language, just for fun.

Lushie is a interpreted language. It has a syntax inflenced by J and Q.

## Examples

`Hello world!`:

```
print "Hello world!"
```

`Operators`:

```
, Arithmetic
  1 + 1
  2 - 2
  3 * 4
  40 / 5
, Multiple numbers
  10 20 30 * 3
30 60 90
, Comparisons
  10 < 15
0 , 0 is true, 1 is false
  10 20 60 < 50
0 0 1
```

`Functions`:

```
  square:{x*x} , 'x' is implicit argument
  square 5
25
  value square , Check the value of 'square'
{x*x}
```

`Errors`:

```
, Errors in Lushie are concise, just like in Q.
  10 20 30 + 10 20
length! , Wrong length
  2 + "aa"
type! , Wrong type
```

`Bulitins`:

```
  x: 1 2 3 4 5
  len x , Checks length of x
5
  value x , Checks the value of x
1 2 3 4 5
  sum x , Sum x
15
```
