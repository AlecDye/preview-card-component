# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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


## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![screenshot](./images/screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- GitHub URL: [Repo](https://github.com/AlecDye/preview-card-component)

## My process

- Create custom CSS variables with design specs to maintain the project
- Build the component for a mobile device first using flexbox
- Split the component into 2 main sections: image & text content
- Create an overlay on the image to try and match the design doc

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

The picture element allows sourcing differently sized images based on the viewport. This is handy but presents challenges during layout especially when combined with my solution with the transparent overlay.

```html
<div class="card-img">
  <div class="img-overlay"></div>
  <picture>
    <source media="(min-width:380px )" srcset="./images/image-header-desktop.jpg">
    <img src="/images/image-header-mobile.jpg" alt="">
  </picture>
</div>
```
```css
.img-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: var(--clr-accent);
  opacity: 0.4;
  z-index: 30;
}
```
### Continued development

- The picture element is tricky to use, it ended up causing layout headaches for me
- I could implement a better solution for the image overlay
- CSS custom variables are the way to go, very happy with their usage

### Useful resources

- [Ellen Macpherson's CSS image overlay](https://dev.to/ellen_dev/two-ways-to-achieve-an-image-colour-overlay-with-css-eio) - Blog post by Ellen Machpherson about a transparent color overlay for an image. Will try this out

## Author

- Frontend Mentor - [@AlecDye](https://www.frontendmentor.io/profile/alecdye)
- Twitter - [@alec_dye](https://www.twitter.com/alec_dye)