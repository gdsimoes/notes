# Some CSS tricks

## How to make elements stay still

Just use

```CSS
position: fixed;
```

or

```CSS
position: sticky;
```

To see the difference between them and more go to [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/position).

## Control which element is on top

Just use the `z-index` property. I believe that with `z-index` and `position: fixed` we can create those interesting background images that seem to move with the page like the scenery on a window.

## Hiding and element

Here we have two options:

```CSS
visibility: hidden;
display:none;
```

This is very useful in the browser inspector. The difference between the two is that if you use visibility, space is still allocated for the element, while in the display case, it isn't.

## Make in-page navigation smoother

The default behavior when a user clicks on a link that leads to another section on the same page is for the browser to "teleport" the user to given section. To make this transition smoother use:

```CSS
html {
    scroll-behavior: smooth;

}
```
