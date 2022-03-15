# Z Language (Zlang)

Z language (or Zlang) is a embeddable programming language inspired by Haskell and APL derivatives (mostly Q and K).

## Primitive data types
Int: 				 `100`
Float: 			  `20.2`
String: 		 `"Hello world!"`
List: 			  `1 "juan" 4.20 5`
Dict: 			  `{:a 50; :b 20}`

## Some examples

Simple math operators:

```k
z) 10 + 20 , This is a comment btw.
30
z) 10 + 40 50 60 , Do array operators just like APL
50 60 70
z) 20 - 10 , Minus
10
z) 30 * 2 , Multiply
60
z) 10 / 2 , Divide
5.0
z) 10 % 2 , Modulo
0
z) 10 // 2 , Divide, but the result is an int
5
```

Define variables:

```
z) a -> 10 , Define a to be 10
z) a
10
z) a + 10
20
z) nums -> 1 2 3 4 5 , Define a list (and basically any data type) is also the same
z) sum nums , The sum of 'nums'
15
z) +/nums , Another way to write the sum of 'nums'
15
```

List operators:

```
z) a -> 10 21 10 35 41 42 41
z) uniq a , Similar to 'distinct'
10 21 35 41 42
z) reverse a , Reverse the list
41 42 41 35 10 21 10
z) count a , See the length of the list
7
z) a ++ 13 , Concat with a number
10 21 10 35 41 42 41 13
z) a -- 10 , Remove the first '10' element that it found in 'a'
z) a
21 10 35 41 42 41 13
z) pop a , Pops out the last element
13
z) a
10 21 10 35 41 42 41
z) each a , Loop through a
<Generator or something like that here>
z) b -> a "abc" , List of lists
z) count each b
7
3
```

Define functions:

```
z) add -> {[a; b] a + b} , Define a function in Z is pretty similar to K
z) add 50 50
100
```

Comparison operators:

```
z) a -> 10
z) b -> 20
z) a = b , Equal
1				 , 1 means false, 0 means true
z) a > b , Greater than
1
z) a < b , Less than
0
z) a >= b , Greater or equal
1
z) a <= b , Less or equal
0
z) a != 0 , Not equal
0
z) !a     , Not
1				  , If a != 0, then 1, else 0
z) a -> 0
z) !a
0
z) a -> 10
z) a & b  , And
1
z) b -> 10
z) a & b
0
```