# Tsuki - A concatenative (stack-based) programming language that compiles to C

`Hello world!`:

```
main func
  "Hello world!" print
  0 return
end
```

`Hello #{user}!`:

```
# Entry point function
main func
  "What is your name? " ask # Ask the user
  name store # Store the user name to "name"
  [ "Hello, " name "!" ] concat print # Print "Hello, #{name}!"
  # Another one: "Hello, #{name}!" print (With no concat)
  0 return
end
```

`Defines`:

```
name store # Pop, then store to "name"
name load # Load "name" to stack
```

`Condition flow`:

```
{ 10 15 > } if # The { ... } is lambda
  "15 > 10!" print
{ 20 20 = } elif # Else-if
  "20 == 20!" print
else
  "We're doomed!" print
end

# `match`
10 name store # name = 10
name match
  { "10 is 10" print } 10 # 10 -> print "10 is 10"
  { "Wait, what?" print } else # else -> print "Wait, what?"
end
```
