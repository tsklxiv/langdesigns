# Totoro - A Lisp for Rust

## Examples:

Simple `Hello world!`

```rust
(fn main []
 (println! "Hello Rust from Totoro! :D"))
```

`Cursive` `Hello world!` example:

```rust
(use (cursive views '(Dialog TextView)))
(fn main []
  (mut root (:: cursive default '()))
  (.add_layer root
    (::around Dialog
      (
        (::new TextView "Hello world!")
        ($.title "Cursive")
        ($.button "Quit" (lambda s (.quit s '())))
      )
    )
  )
  (.run root ())
)
```

`Termion` color example:

```rust
(extern-crate termion)
(use (termion '(color style)))
(use (std io))

(fn main []
  (println! "{}Red" (::Fg color (::Red color)))
)
```

`Multiple dots`:

```rust
a.b().c;
```

Totoro:

```rust
(.c (.b a '()))
```

`if let`:

```rust
if let Ok(Some(pass)) = pass {
  stdout.write_all(pass.as_bytes()).unwrap();
  stdout.write_all(b"\n").unwrap();
} else {
  stdout.write_all(b"Error\n").unwrap();
}
```

Totoro:
```rust
(iflet (Ok (Some pass)) pass
  (do
    (.unwrap (.write_all stdout (.as_bytes pass '())))
    (.unwrap (.write_all stdout (byte "\n")))
  )
  (.unwrap (.write_all stdout (byte "Error\n")))
)
```

`Primitives`:

```rust
let x: i32 = 10
let y: i64 = 20
let z: f64 = 3.0
let k = 40
let k = 50 // Shadowing
let mut h = 50
h = 60
```

Totoro:

```rs
(let (x i32) 10)
(let (y i64) 20)
(let (z f64) 3.0)
(let k 40)
(let k 50) // Shadowing
(mut h 50)
(set h 60)
```

`Tuples`:

```rust
(10, 20.0, 30, 5050)
```

Totoro:

```rust
[10 20.0 30 5050]
```

`More complicated types`:

```rust
// Structs
struct Person {
  name: String,
  job: String,
  age: i8,
  id: i32,
}

// Enums
enum Msg {
  Hello(String),
  Destroy(Person),
  Craft(String, String, i8, i32),
  Nothing
}
```

Totoro:

```rust
;; Structs
(struct Person
  (name String)
  (job String)
  (age i8)
  (id i32)
)

;; Enums
(enum Msg
  (Hello String)
  (Destroy Person)
  (Craft String String i8 i32)
  (Nothing))
```

`Condition flow`:

```rust
if 10 == 10 {
  println!("A")
} else {
  println!("B")
}

let x = 10
match x {
  10 => println!("A"),
  20 => println!("B"),
  30 => {
    println!("Listen here you piece of sh-")
  }
}
```

Totoro:

```rust
;; If
(if (= 10 10)
  (println! "A")
  (println! "B"))

;; Match
(let x 10)
(match x
  '(10 (println! "A")) ;; Case 1
  '(20 (println! "B")) ;; Case 2
  '(30
    (do
      (println! "Listen here you piece of sh-")))) ;; Case 3
```
