# Flammen - A programming language that compiles to `bash`

`Hello world!`:

```
hello = ->
  echo "Hello world!"

hello
```

`Define variables`:

```
# Set normal variables
a = 10
b = 20
# Set environment variables
env PATH = "ADD:$PATH"
```

`Condition flow`:

```
# If
x = 10
if x == 10
  print "x == 10"
else
  print "x != 10"
```
