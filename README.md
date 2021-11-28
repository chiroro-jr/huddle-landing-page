# Frontend Mentor - Huddle landing page with alternating feature blocks solution

This is a solution to the [Huddle landing page with alternating feature blocks challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/huddle-landing-page-with-alternating-feature-blocks-5ca5f5981e82137ec91a5100). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [https://github.com/chiroro-jr/huddle-landing-page](https://github.com/chiroro-jr/huddle-landing-page)
- Live Site URL: [https://musing-leakey-26e892.netlify.app/](https://musing-leakey-26e892.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS and SCSS(using dart-sass) using a little bit of custom properties
- Block Element Modifier(BEM) and the 7-1 pattern for architecture and folder structure
- Flexbox
- Grid
- Desktop-first workflow
- [Vite](https://vitejs.dev/) as a build tool and server
- [Ionicons](https://ionic.io/ionicons)

### What I learned

- you can just pick one or the other, either grid or flex. You dont have to use both.
- use sass or any css preprocessor you are comfortable with to make it easier to arrange the files and folders in your project. I used the 7-1 pattern which I leaned in this course. (an aside on using @use and @forward instead of @import in sass).
- make use of utility classes to prevent high coupling between your components and the layout. Example of a grid ad card. You dont want to change the component's course just because the layout changed.
- the owl selector ( * + * {}) 

### Continued development

A big part of the modern web, particularly frontend web, is responsive design. This technique allows you to implement websites such that they adapt to whatever screen they are being viewed on. As I was developing this project I realized that responsive design is a major weak point on mine. Therefore my goal is to take some time improving my responsive design skills. 

### Useful resources

- [Advanced CSS and SASS course by Jonas Schmedtmann](https://www.udemy.com/course/advanced-css-and-sass/)

- [The Responsive Design Bootcamp by Kevin Powel](https://scrimba.com/learn/responsive#)

- [CSS in Depth book](https://www.manning.com/books/css-in-depth)

  **Note: I believe these 3 resources are enough to get you from beginner to pro css developer**

## Author

- Frontend Mentor - [@chiroro-jr](https://www.frontendmentor.io/profile/chiroro-jr)
- Twitter - [@chiroro_jr](https://www.twitter.com/chiroro_jr)

## Acknowledgments

If you would like to learn more about CSS architecture, how to arrange files and folders and the BEM methodology (and pretty much everything CSS) in detail you can check out  **Jonas Schmedtmann**'s advanced CSS and Sass course [here](https://www.udemy.com/course/advanced-css-and-sass/). Most of what I know about CSS and Sass I learned in this course. I am sure it will help you too. I know I have already mentioned this course. That's how good I think it is.
