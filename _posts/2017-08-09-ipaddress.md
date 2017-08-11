---
title: ipaddress
repl: https://repl.it/KDQ3/18
---
{% highlight python %}
# built-in ipaddress module that helps you easily deal with IP addresses
# check type, compare, check against subnets and more with both IPv4 and IPv6

from ipaddress import ip_address, ip_network

ip4 = ip_address('192.168.0.1')
print('packed', ip4.packed)
print('is private', ip4.is_private)

ip6 = ip_address('2001:db8::')
print('exploded', ip6.exploded)
print('is multicast', ip6.is_multicast)

net = ip_network('192.168.0.0/24')
print(f'{ip4} in {net} =', ip4 in net)
print(f'{ip6} in {net} =', ip6 in net)
{% endhighlight %}
