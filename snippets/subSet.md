---
title: subSet
tags: array,intermediate
firstSeen: 2020-10-11T11:53:08+03:00
lastUpdated: 2020-10-22T20:24:30+03:00
---

Checks if the first iterable is a subset of the second one, excluding duplicate values.

- Use the `Set` constructor to create a new `Set` object from each iterable.
- Use `Array.prototype.every()` and `Set.prototype.has()` to check that each value in the first iterable is contained in the second one.

```js
const subSet = (a, b) => {
  const sA = new Set(a), sB = new Set(b);
  return [...sA].every(v => sB.has(v));
};
```

```js
subSet(new Set([1, 2]), new Set([1, 2, 3, 4])); // true
subSet(new Set([1, 5]), new Set([1, 2, 3, 4])); // false
```
