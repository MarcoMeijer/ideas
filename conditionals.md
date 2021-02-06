# Conditionals

## If

```ruby
if condition {

} else if condition2 {

} else {

}
```

## One lined if

After `if` and `else` write a `do` to explicitly tell Bullet that you only want to use one line.

```ruby
if condition do stuff();
if condition do stuff(); else if condition2 do stuff2(); else do stuff3();
```

## One lined reversed if

Sometimes it's nice to write the if the other way around!

```ruby
stuff() if condition else otherstuff();
break if condition;
continue if condition;
```

## If expression

```ruby
a = if x > 5 {
    "big"
} else {
    "small"
};

b = "big" if x > 5 else "small"; # python-esque.
c = x > 5 ? "big" : "small"; # ternary operator.
```