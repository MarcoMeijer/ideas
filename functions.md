# Functions

```ruby
def sum(int x, int y) -> int {
    return x + y;
}
```

You can also omit return and instead remove the semicolon from the last line.

```ruby
def sum(int x, int y) -> int {
    x + y
}
```

You can omit types.

```ruby
def sum(x, y) {
    x + y
}
```

Functions are first class citizens:

```
def apply((int) -> int f, int x) {
    return f(x);
}
```

## Compile time arguments

```ruby
def factorial<int x> {
    if x == 0 {
        return 1;
    }
    factorial<x - 1> * x
}
```

## Named arguments

Ordered arguments come first and then named arguments will come inside curly braces.

```ruby
def solve(int n, {bool first}) {
    # ...
}

solve(n, first: true);
```

## Default values

Each named argument can get a default value. A suffix of ordered arguments can get a default value.

```ruby
def f()
```

## Anonymous functions

```ruby

sum = |int x, int y| -> int {
    return x + y;
};

# without types, implicit return

sum = |x, y| {
    x + y
};

# one-liner

sum = |x, y| x + y;

v = [1, 3, 5, 2, 4];
v.sort |a, b| a > b;
```