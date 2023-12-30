# Frontend Mentor - Results summary component solution

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page
- **Bonus**: Use the local JSON data to dynamically populate the content

### Screenshot

![Desktop](./design/Desktop.png)
![Active_State](./design/Active%20State.png)
![Mobile](./design/Mobile.png)

### Links

- Solution URL: [GitHub](https://github.com/LySabrina/Results-Summary)
- Live Site URL: [Live Site](https://lysabrina.github.io/Results-Summary/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

During this project, I used many flexbox on multiple elements. So there's flexbox within a flexbox. I mainly used it to center the containers.

I had difficulties structuring my HTML at first because the score has a circle so I was deciding whether to use

```html
<h1>76 <span> 86 </span> / 100</h1>
```

with some CSS styling but this way did not help me. I mainly use ems for the width and height but this may not be a good use as the user's font size may be different to 16px. Thus, it may change the entire look of the circle.

Thus, I opted to use the following:

```html
<div class="score">
  <h1>76</h1>
  <p>of 100</p>
</div>
```

I will now use the div to create the circle and use two block elements ( `<h1>` and `<p>`). This makes it easy to style and they are on their own separate line by default.

While I was working on the Desktop view, I had issues on getting the `results-container` and `summary-container` to be equal widths of the parent container. I wanted to use `width: 50%` but it did not seem to work. I was stumped on this but solved it using `flex:1' which will allow each container to grow equally inside the parent container. Now they will be each half of the parent's container.

Now the next issue was that `results-container` did not stretch the whole height of the parent container. The issues was I was using: `height:40%` which forces the height of the `results-container` to be that exact 40% width. This will hold higher precedence even if I attempt to use min or max. So I changed it to `min-width:40%` such that it should be at least 40% of the height for the parent container ( main purpose is for the mobile design) and if necessary, grow (for the desktop design)

### Continued development

I am satisfied with the project. I will need to continue understanding how to better structure my HTML and using flexbox more.

## Author

- Frontend Mentor - [@lysabrina](https://www.frontendmentor.io/profile/LySabrina)
- GitHub - [@lysabrina](https://github.com/LySabrina)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

Thanks to FrontendMentor for these projects. And me!.
