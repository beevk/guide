---
title: Apply a Style Until a Condition is Met with @while
---
## Apply a Style Until a Condition is Met with @while

`@while` directive has similar functionality to `while` loop in JavaScript.

Start by declaring a variable to use in `@while` directive.
```javascript
$x: 1;
```

Next, declare a `@while` directive. Here, the loop would run until the given condition is met. i.e. `$x <= 10`

```javascript
@while $x <= 10 {
  // Do sth. here
}
```

Inside this `@while` directive, you have to perform all your css operations. You'll also need to update the value of `$x` in each loop.

```javascript
.text-#{$x} { font-size: 5px * $x;}
$x: $x + 1;
```

So, the complete solution would be:

```html
<style type='text/sass'>
```
```javascript

$x: 1;
@while $x <= 10 {
  .text-#{$x} { font-size: 5px * $x;}
  $x: $x + 1;
}

```
```HTML
</style>

<p class="text-1">Hello</p>
<p class="text-2">Hello</p>
<p class="text-3">Hello</p>
<p class="text-4">Hello</p>
<p class="text-5">Hello</p>
<p class="text-6">Hello</p>
<p class="text-7">Hello</p>
<p class="text-8">Hello</p>
<p class="text-9">Hello</p>
<p class="text-10">Hello</p>
```

You can refer [this](https://sass-lang.com/documentation/at-rules/control/while) link to learn more about `@while` directives.
