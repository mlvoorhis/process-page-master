
<h1 align="center">Process Page | devChallenges</h1>

<div align="center">
   Solution for a challenge <a href="https://devchallenges.io/challenge/process-page" target="_blank">Process Page</a> from <a href="http://devchallenges.io" target="_blank">devChallenges.io</a>.
</div>

<div align="center">
  <h3>
    <a href="https://mlvoorhis.github.io/process-page-master/">
      Demo
    </a>
    <span> | </span>
    <a href="https://github.com/mlvoorhis/process-page-master">
      Solution
    </a>
    <span> | </span>
    <a href="https://devchallenges.io/challenge/process-page">
      Challenge
    </a>
  </h3>
</div>

<!-- TABLE OF CONTENTS -->

## Table of Contents

- [Overview](#overview)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Built with](#built-with)
- [Features](#features)
- [Contact](#contact)

<!-- OVERVIEW -->

## Overview

![screenshot](./thumbnail.jpg)
In this project, I created a responsive process page using HTML and CSS. The goal was to work with different breakpoints to ensure the page adapted to various screen sizes. I used the <code>::before</code> pseudo-element to add content before section headings, and incorporated dashed gray lines and purple markers for visual emphasis.



### What I learned
This project came fairly easy to me! My biggest challenge was aligning the dashed gray lines and making them responsive.

Initially, I tried applying the dashed lines to .main-content, thinking I needed the content to span the entire screen with padding instead of margins. This approach turned out to be ineffective and complicated the layout. The lines became harder to manage, and I was struggling with consistency.

Then, I realized the solution was right in front of me: I could use the ::before pseudo-elements, positioned relative to their respective elements. This made the lines consistent and tied them directly to their containers. To ensure the lines covered the full height, I used a large negative value, though I wonder if there’s a cleaner alternative to avoid using negative margins.

Here’s the updated code snippet:
```css
.four {
  position: relative;
}

.four::before {
    content: "";
    position: absolute;
    left: -21.5px;
    top: -99999px;
    bottom: 0;
    width: 1px;
    border-right: 1px dashed var(--light-purple-color);
    position: absolute;
    z-index: -1;
}
```
I made the purple markers similarly:
```css
.article-headline::before {
    position: absolute;
    content: "";
    top: 0;
    left: -21.5px;
    bottom: 0;
    border: 1px solid var(--purple-color);
}
```
### Useful resources
- [FreeCodeCamp](https://www.freecodecamp.org) - My HTML & CSS foundation.
- [DevChallenges](https://devchallenges.io) - Source of this challenge and great practice for aspiring web developers.

### Built with
- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid

## Features

<!-- List the features of your application or follow the template. Don't share the figma file here :) -->

This application/site was created as a submission to a [DevChallenges](https://devchallenges.io/challenges-dashboard) challenge.

## Contact

- GitHub [@mlvoorhis](https://github.com/mlvoorhis)
