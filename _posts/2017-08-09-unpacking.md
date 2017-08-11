---
title: Advanced unpacking
repl: https://repl.it/KDQ3/20
---
{% highlight python %}
# easily split lists or iterators into variables

a, b, *rest = range(10)
print(a)     # prints 0
print(b)     # prints 1
print(rest)  # prints [2, 3, 4, 5, 6, 7, 8, 9]

# or even

a, *rest, b = range(10)
print(rest)  # prints [1, 2, 3, 4, 5, 6, 7, 8]

# in python 2 it's a lot more verbose

l = list(range(10))
a = l[0]
rest = l[1:-1]
b = l[-1]
{% endhighlight %}
