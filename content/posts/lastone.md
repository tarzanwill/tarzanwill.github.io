---
title: "Quick Sort Template"
date: 2022-04-25T22:18:25+08:00
tag: 1234, algo
description: 这里是一些废话
---

**Quick Sort**
---
```python3
def quick(q, l, r):
	if l >= r:
		return
	p, i, j = q[l + r >> 1], l - 1, r + 1
	while i < j:
		while 1:
			i += 1
			if q[i] >= p:
				break
		while 1:
			j -= 1
			if q[j] <= p:
				break
		if i < j:
			q[i], q[j] = q[j], q[i]
	quick(q, l, j)
	quick(q, j + 1, r)
```