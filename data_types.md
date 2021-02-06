# Data Types

Basic data types in Bullet are all 3 lettered to make them faster to type.

## Booleans

```ruby
a = true;
b = false;

bit c = a && b; # false
```

## Characters

```ruby
a = 'a';
b = 'b';

chr c = 'c'; 
```

## Integers

```ruby
a = 2;
b = -3;

int c = a + b; # -1
```

## Floating point numbers

```ruby
a = 2.3;
b = 4.5;

num c = a + b; # 6.8
```

## Strings

```ruby
a = "Hello,";
b = " World!";

str c = a + b; # "Hello, World!"
```

## Tuples

```ruby
t0 = (1, 1.2); # infers that it's tup<int, num>
tup t1 = (1, 1.2); # infers that it's <int, num>
tup<int, num> t2 = (1, 1.2); # explicit type

t2[1]; # 1.2
```

## Maps

```ruby
m0 = {"Hello": "World"}; # infers that it's map<str, str>
map m1 = {"Hello": "World"}; # infers that it's <str, str>
map<str, str> m2 = {"Hello": "World"} # explicit type

m0["Hello"]; # "World"
```

## Sets

```ruby
s0 = {1, 2, 3}; # infers that it's set<int>
set s1 = {1, 2, 3}; # infers that it's <int>
set<int> s2 = {1, 2, 3}; # explicit type
s0.add(4);
```

## Arrays

```ruby
arr<int, 3> a0 = [1, 2, 3];
```

## Vectors

```ruby
v0 = [1, 2, 3]; # infers that it's vec<int>
vec v1 = [1, 2, 3]; # infers that it's <int>
vec<int> v2 = [1, 2, 3]; # explicit type
v0.pushb(4);
puts(v0[-1]); # 4
```

## Queues

```ruby
que<int> q;
q.push(1);
puts(q.pop()); # 1
```

## Double-Ended Queues

```ruby
deq<int> d;
d.pushb(1);
d.pushf(2);
2.times do puts(d.popb());
```

## Common methods
* `.size` gets the size of the container.