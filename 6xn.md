# 6xn (6 by n) - A prototype

6xn (or 6 by n) is a succesor to 3xn, but instead of limited to 3 chars/line of code, 6xn extends to 6 chars/line of code.

## :question: Instructors

<dl>
  <dt><markdown>`+`, `-`, `*`, `/`, `%`, `^`</markdown></dt>
  <dd>Arithmetic operators</dd>

  <dt><markdown>`n` with `n` = `[0-9]`</markdown></dt>
  <dd>Push a number to stack</dd>

  <dt><markdown>`nnnnn.`</markdown></dt>
  <dd>Push the number `nnnnn` to stack</dd>

  <dt><markdown>`.` or ` ` (*space*)</markdown></dt>
  <dd>No-op</dd>

  <dt><markdown>`@`</markdown></dt>
  <dd>Sum/concat</dd>

  <dt><markdown>`,`</markdown></dt>
  <dd>Pop with no print</dd>

  <dt><markdown>`?`</markdown></dt>
  <dd>Get user input and then push it to the stack as number</dd>

  <dt><markdown>`!`</markdown></dt>
  <dd>Pop the last element and print to the output</dd>

  <dt><markdown>`$`</markdown></dt>
  <dd>Pop a number, cast it to string, and then push back</dd>

  <dt><markdown>`1:a`</markdown></dt>
  <dd>Assign a number to a variable (identifier is 2 chars max)</dd>

  <dt><markdown>`:a`</markdown></dt>
  <dd>The same as above, but pop the last element of the stack and then assign it to a</dd>

  <dt><markdown>`=j`</markdown></dt>
  <dd>Jump to line `j + 1` of the code</dd>

  <dt><markdown>`(...)`</markdown></dt>
  <dd>While loop (until the first element is 0)</dd>

  <dt><markdown>`'aaaaa`</markdown></dt>
  <dd>Push the string `aaaaa` to stack</dd>

  <dt><markdown>`&a`</markdown></dt>
  <dd>Load the value of `a` to stack</dd>

  <dt><markdown>`_`</markdown></dt>
  <dd>Halt. Stop reading the rest of the line of code, useful if you don't want to put `...` at the end of your code</dd>
</dl>

## Comments

In 6xn, use `#...#` for multi-line commenting (Note that it is not nestable), e.g.

```
#
  Never gonna give you up.
  Never gonna let you down.
  Never gonna go around and desert you.
  Never gonna make you cry.
  Never gonna say goodbye.
  Never gonna tell a lie.
  And hurt you.
#
```

And `_...` for single-line commenting, e.g.

```
_ I thought it is a halt!
```

## :book: Example

Hello world:

```
'Hello
' worl
'd'_
++!_
```

Simple counter:

```
1_ Push 1 to stack
(   # Start while loop #
1:a_ Assign 1 to a
&a_ Load a to stack
1+_ Push one to stack and then 1 + a
:a_ Store the last element to a again
) # The cycle continues #
```
