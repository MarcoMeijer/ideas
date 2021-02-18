# Loops

## Times

Sometimes you just want to repeat something a few times. Like when you want to repeat the program for t test cases.

```ruby
get<int>.times {
    # your code here
}
```

Also:
```ruby
get<int>.times |i| {
    # you can use i here
}
```

## Each

```ruby
(1:10:2).each |i| {
    puts(i);
}

# or omit the block
(1:10:2).each |i| puts(i);
```

## For

```ruby
for i in 1:10 {
    put(i); # prints 1 2 ... 9
}

for i in 9:0:-1 {
    put(i); # prints 9 8 ... 1
}

for i in :10 { # Empty argument will default to zero
    put(i) # prints 0 1 ... 9
}
```

## C-Style For

Sometimes this is still the easiest way to write your code:

```ruby
for i = 0; i < 10; ++i {
    put(i); # prints 0 1 ... 9
}
```

## While and do while

```ruby
while condition {
    # ...
}

do {
    # ...
} while condition;
```

## One lined loops

Unlike C and C++, you need to use curly braces for loops. If you don't want to curly braces and have only a line inside the body you have to explicitly write `do` keyword.

```ruby
for i in :10 do put(i);
while condition do stuff();
do stuff(); while condition;
10.times do stuff();
10.times |i| stuff(i); # no `do` here because we're passing an anonymous function to times method.
```

## Control flow statements

```ruby
for i in :n {
    break; # breaks from the loop
    continue; # goes to the next i immediately 
}

for i in :n {
    for j in i:n {
        break 2 if i * j > 100; # break 2 will break from both for loops.
    }
}
```
