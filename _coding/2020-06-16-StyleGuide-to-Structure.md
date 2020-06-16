---
layout: post
title: Taking a Styleguide and making a working Structure in SASS
---

When looking at the [https://sass-guidelin.es/#the-7-1-pattern](https://sass-guidelin.es/#the-7-1-pattern), I am not inclined to use it exactly.

My designer gave me a Base color palette, Color Allocations, and Element States.  So, I am implementing this pattern.

- sass
  - base
    - palette.scss
  - element
    - page.scss
    - button.scss
    - form.scss
    - card.scss
  - main.scss

Where I am placing the Base color palette in `sass/base/palette.scss` and specifying the use by elements.


In `sass/element/page.scss`, I will import the pallette:
```
@import "../
