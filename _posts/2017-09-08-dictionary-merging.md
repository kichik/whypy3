---
title: dictionary merging
repl: https://repl.it/KDQ3/31
---
```python
# Given these three dictionaries, create one combined dict:

get = {'referrer': 'https://talkpython.fm', 'sort': 'newest'}
post = {'first': 'Tom', 'last': 'Jones', 'sort': 'popular'}
routes = {'action': 'snippets'}

all_inputs = {**get, **post, **routes}

import json
output = json.dumps(all_inputs, indent=True)
print(f'The merged dictionary is {output}.')

# Prints:
# The merged dictionary is {
#  "referrer": "https://talkpython.fm",
#  "sort": "popular",
#  "first": "Tom",
#  "last": "Jones",
#  "action": "snippets"
# }.
```
