# Javascript Notes

## How to swap variables

A nice way of swaping variables using destructuting and avoiding creating a temporary variable is the following:

```javascript
[x, y] = [y, x];
```

## How to set a variable with a default value

Instead of the most common way of doing this using `||` (which doesn't work for falsy values) we can use `??`:

```javascript
let variable = arg.method() ?? default
```
