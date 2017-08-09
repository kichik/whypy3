---
title: Advanced unpacking
repl: https://repl.it/KDQ3/3
---
{% highlight python %}
a, b, *rest = range(10)
print(a)     # prints 0
print(b)     # prints 1
print(rest)  # prints [2, 3, 4, 5, 6, 7, 8, 9]

# or even

a, *rest, b = range(10)
print(rest)  # prints [1, 2, 3, 4, 5, 6, 7, 8]
{% endhighlight %}
