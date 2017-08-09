---
title: ipaddress
repl: https://repl.it/KDQ3/6
---
{% highlight python %}
from ipaddress import ip_address
ip4 = ip_address('192.168.0.1')
print('packed', ip4.packed)
print('is private', ip4.is_private)
ip6 = ip_address('2001:db8::')
print('exploded', ip6.exploded)
print('is multicast', ip6.is_multicast)
{% endhighlight %}
