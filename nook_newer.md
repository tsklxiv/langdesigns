# Nook - A small, concatenative programming language, inspired by Factor and GNU `dc`. (The newer version)

Nook is a small, concatenative programming language, inspied by Factor and GNU `dc`.

`Hello world!`:

```
{Hello world!}w
{Hello world!}p # Does not pop the string
```

`FizzBuzz`:

```
100 # The range
{
  [$ 15 % 0 =]["FizzBuzz"w][]? # if i % 15 == 0 then print "FizzBuzz"
  [$ 3 % 0 =]["Fizz"w][]? # if i % 3 == 0 then print "Fizz"
  [$ 5 % 0 =]["Buzz"w][]? # if i % 5 == 0 then print "Buzz"
}e # Each
```

[`Truth machine`](https://esolangs.org/wiki/Truth-machine):

```
i d
{0 =}{0 w}{[1 w]t}?
# Pseudo code
# push input
# if input == 0: print 0
# else: loop "": print 1
# Note: `t` is short for `trap`, which is another name for `while`
# An empty string == infinite loop
```

[`iHateOddNumbers`](https://codegolf.stackexchange.com/questions/229052/ihateoddnumbers):

```
i # Get int input
{a}s # Store it to 'a'
{[a]l 2 % 0 =}{[a]l w}{[e]f}?
# Pseudo code
# get input
# store input -> a
# if a % 2 == 0,
#   write a
# else,
#   fail "e"
# end
```

`Variables`:

```
1 # Push 1 to stack
{a}s # Store 1 (the last element) to A
{a}l w # Load the variable A to stack, then print
```
