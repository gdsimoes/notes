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

## The initial value of a property

The initial value of a property belongs only to that property and not to any element type. By this, I mean that, for example, the following code will not set the text to bold:

```CSS
strong {
    font-weight: initial;
}
```

The value we usually get for 'font-weight in 'strong' elements is defined in the user-agent stylesheet and is not the so-called 'initial' value of font-weight (which is the same regardless of the element type).

## Position: relative and absolute

If you want an element with the property `position: absolute` to have its width, height, and position set relative to its parent container, then use `position: relative` in the parent container.

## CSS Remedy behavior

If you are using [CSS Remedy](https://github.com/jensimmons/cssremedy) (which I usually am), then remember that you might be surprised by some CSS behavior. For example, all images by default will only have 100% of the width.

The browser inspector is a great to help understand what is going on.

## The function `translateY` is moving an element horizontally?

Let's look at the following code from a recent project of mine:

```CSS
#officeWorker {
    /* ... */
    transform: translate(-50%, -50%);
}
```

Later I tried changing the position of the image:

```CSS
@media screen and (min-width: 1000px) {
    /* ... */
    #woman {
        /*  */
        transform: translateY(-50%);
    }
}
```

I was surprised to see that when I added the `translateY` line the image moved horizontally. This happened because the first value of transformed (which moved the image in both dimensions) was replaced by the following one, creating the impression of a horizontal movement caused by `translateY`.

Once again, I was saved by Firefox's inspector DOM and style inspector.
