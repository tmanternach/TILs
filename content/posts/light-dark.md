+++
title = "light-dark css property"
date = "2024-10-26T07:41:10-06:00"
description = "An easy way to support dark modes on your site."
showFullContent = true
readingTime = false
hideComments = false
+++

There is a new-ish [CSS function](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/light-dark) that simplifies creating different light and dark stylesheets for your site. It's called `light-dark` and here are some quick steps to use it:

First, you need to define your `color-scheme` at the `:root` or `html` level of your CSS.

```
:root {
  color-scheme: light dark;
}
```

Now, wherever you set any color in the rest of your CSS, you can instead use `light-dark` to define 2 colors. The first color in the function is for the light color scheme; the second is for the dark scheme. It's that easy!

```
body {
  color: light-dark(black, white);
  background-color: light-dark(white, black);
}
```

I just implemented on this new TIL site by editing my (already custom) terminal.css stylesheet. You can view it [here](/terminal.css). I learned this today thanks to [this post](https://css-tricks.com/come-to-the-light-dark-side/) from CSS-Tricks.