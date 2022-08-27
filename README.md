# Resolution aware product preview card solution with Material Design inspired theming

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).
For more designs - check out [my profile](https://www.frontendmentor.io/profile/Fobya7) there!

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Solution

Live Site URL: [Check out my design!](https://fobya7.github.io/product-preview-card-component-main/)

<table>
  <tr>
    <th>Desktop</th>
    <th>Mobile</th>
  </tr>
  <tr>
    <td width="72%"> <img src="readme/screenshot-desktop.jpeg"> </td>
    <td width="28%"> <img src="readme/screenshot-mobile.jpeg"> </td>
  </tr>
</table>

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

- Encapsulating an image in it's own div makes controlling it's size way easier.

```html
<div class="product-preview-image">
  <img class="product-preview-image" src="images/image-product-desktop.jpg">
</div>
```

- You should start your stylesheet by declaring color variables for your theme. It makes it easier to refrence colors while you're working.

```css
:root
{
    --color-background: hsl(30, 38%, 92%);
    --color-surface: hsl(0, 0%, 100%);
    --color-on-surface: hsl(228, 12%, 48%);
    --color-primary: hsl(158, 36%, 37%);
    --color-on-primary: hsl(0, 0%, 100%);
    --color-secondary: hsl(212, 21%, 14%);
}
```

- Making a website look great both in mobile & desktop requires seperate styling.
```css
@media only screen and ( max-width: 700px )
{ /* for mobile */
  .product-preview
  {
      width: 100%;
      flex-direction: column;
  }
}
@media only screen and ( min-width: 701px )
{ /* for desktop */
  .product-preview
  {
      width: 50%;
      flex-direction: row;
  }
}
```

- I really like this part. First I learned about [selectors](https://www.w3schools.com/cssref/sel_hover.asp) and then about [darkening color](https://stackoverflow.com/questions/1625681/dynamically-change-color-to-lighter-or-darker-by-percentage-css) without declaring additional variables.

```css
button.add-to-cart:hover
{
    filter: brightness(85%);
}
```

### Continued development

- **workflow** - Which part of the assignment tackle first? And also doing documentation throughout, not scrambling for details after finishing the project.

### Useful resources

- Material Design [typography](https://material.io/design/typography/the-type-system.html) and [colors](https://material.io/design/color/the-color-system.html) - helped me with mentally organizing the theme and naming its parts,
- MDN's [Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries) - helped me with controlling components based on screen resolution.
