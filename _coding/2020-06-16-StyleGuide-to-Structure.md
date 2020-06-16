---
layout: post
title: Taking a Styleguide and making a working Structure in SASS
---

When looking at the [https://sass-guidelin.es/#the-7-1-pattern](https://sass-guidelin.es/#the-7-1-pattern), I am not inclined to use it exactly.

My designer, [Marlowe Wakeman](https://marlowexperience.com/about/), gave me a Base color palette, Color Allocations, and Element States.  So, I am implementing this pattern.

- sass
  - base
    - _palette.scss
  - element
    - _page.scss
    - _button.scss
    - _form.scss
    - _card.scss
  - main.scss

Where I am placing the Base color palette in `sass/base/_palette.scss` and specifying the use by elements.


In `sass/base/_palette.scss`, I declare the variable as rbga to allow for better intention to be shown.  So that when I overwrite the "alpha" or transparency later, it will be more clear. But, I also leave a comment with the Designers color code for reference.:
```
$lightBlue: rgba(182, 212, 221, 1);  // #B6D4DD
```

In `sass/element/_page.scss`, I will import the pallette:
```
@import "../base/palette";

$pageBackgroundColor: $lightBlue;
```

Now, in the `sass/main.scss`, I will use the `<body>` element to set the background to all the web pages:
```
@import "./element/page";

body {
  background-color: $pageBackgroundColor;
}
```
