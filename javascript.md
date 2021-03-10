# Javascript Notes

## How to swap variables

A nice way of swaping variables using destructuting and avoiding creating a temporary variable is the following:

```javascript
[x, y] = [y, x];
```

## How to set a variable with a default value

Instead of the most common way of doing this using `||` (which ignores not only null and undefined, but all falsy values) we can use `??`:

```javascript
let variable = arg.method() ?? default
```

## Some closures examples

A simple and (and somewhat simplistic) definition of closure is as follows:

Closure
: A closure is a function together with the references for the variables it uses.

There are some subtleties regarding how JavaScript deals with those variables, and the next two examples from Cay S. Horstmann's _Modern Javascript for the impacient_ illustrate that.

### First example:

```javascript
const sayLater = (text, when) => {
    let task = () => console.log(text);
    setTimeout(task, when);
};

sayLater("Hello", 1000);
sayLater("Goodbye", 10000);
```

This example shows that each version of 'task' uses its version of 'text.' It's very similar to how variables work in mathematics. You could search and replace 'text' with the strings 'Hello' and 'Goodbye,' and the result would be the same.

### Second example:

```javascript
let text = "Goodbye";
setTimeout(() => console.log(text), 10000);
text = "Hello";
```

This example shows that what is stored in the closure are not the values of the variables. If it were, this program would print 'Goodbye' instead of 'Hello.' What is stored in the closure are the references, and when the value of 'text' is changed, this affects the program's output.

## The '+' unary operator

The '+' unary operator evaluates to its operand, trying to convert it to a number if it isn't one:

```javascript
let number = "2.7";
console.log(typeof +number);
```

## How to time operations

```javascript
console.time("name");
doSomething();
console.timeLog("name");
doSomethingElse();
console.timeEnd("name");
```
