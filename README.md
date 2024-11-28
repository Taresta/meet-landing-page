# Frontend Mentor - Meet landing page solution

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Desktop](./assets/desktop/Desktop.png)

![Mobile](./assets/mobile/Mobile.png)


### Links

- Solution URL: [Solution URL](https://taresta.github.io/meet-landing-page/)
- Live Site URL: [Live URL](https://taresta.github.io/meet-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- SASS

### What I learned
I had learned more properties of SASS. As this been a project focused on responsive design, I learned how setting a width on the child element can effect its parent element's size as well. In my picture element, I had initially did not set any width for the image element present inside it, which makes the parent grow along with its child element. However, on setting a fixed width for the child element, the picture element's width became unaffected by the width of the child, and was governed by the properties of its parent flex container. It might seem like something obvious, but it did make me spend quite some time in aligning my header's hero images properly according to the deisgn.

I also learned the use of SASS mixin functions. It helps a lot in consolidating many lines of code and reduce redundancies. 
I was also a bit at loss for giving a proper width to the footer button element as it was a child of the flexbox, but that got resolved when I found out that it can be done by setting its flex-shrink to 0, this was the text inside the button element did not get wrapped to the next line and I was able to make it look similar to the design.

```css
@mixin text-preset($preset) {
    @if $preset != null {
      font-weight: map-get($preset, weight);
      font-size: map-get($preset, size);
      line-height: map-get($preset, line-height);
      font-family: map-get($preset, family);
    } @else {
      @warn "Invalid preset passed to text-preset mixin!";
    }
}

@mixin hero-background($url) {
  background: linear-gradient(0deg, rgba($cyan-600, 0.85), rgba($cyan-600, 0.85)), 
  url($url) no-repeat center/cover;
}

```

### Continued development
 I would like to continue to work on my responsive design techniques, and continue to improve my understanding of SASS.

### Useful resources

- [SASS Official Documentation](https://sass-lang.com/) - This is the prefect resource for learning and improving one's understanding of SASS.


## Author

- Website - [GitHub Website](https://github.com/Taresta)
- Frontend Mentor - [Paradox](https://www.frontendmentor.io/profile/Taresta)

## Acknowledgments
Thanks to my teacher, all the amazing resources and all the people who encourage me to continue imprving and moving forward.
