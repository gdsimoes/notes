# Some CSS tricks

## How to make elements stay still

Just use

```
position: fixed;
```

or

```
position: sticky;
```

To see the difference between them and more go to [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/position).

## Control which element is on top

Just use the `z-index` property. I believe that with `z-index` and `position: fixed` we can create those interesting background images that seem to move with the page like the scenery on a window.

## Hiding and element

Just add:

```
visibility: hidden;
```

This is very useful in the browser inspector.
