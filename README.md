# Frontend Mentor - Huddle landing page with alternating feature blocks solution

This is a solution to the [Huddle landing page with alternating feature blocks challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/huddle-landing-page-with-alternating-feature-blocks-5ca5f5981e82137ec91a5100). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Frontend Mentor - Huddle landing page with alternating feature blocks solution](#frontend-mentor---huddle-landing-page-with-alternating-feature-blocks-solution)
  - [Table of contents](#table-of-contents)
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

-   View the optimal layout for the site depending on their device's screen size
-   See hover states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

### Links

-   Solution URL: [https://github.com/chiroro-jr/huddle-landing-page](https://github.com/chiroro-jr/huddle-landing-page)
-   Live Site URL: [https://musing-leakey-26e892.netlify.app/](https://musing-leakey-26e892.netlify.app/)

## My process

### Built with

-   Semantic HTML5 markup
-   CSS and SCSS(using dart-sass) using a little bit of custom properties
-   Block Element Modifier(BEM) and the 7-1 pattern for architecture and folder structure
-   Flexbox
-   Grid
-   Desktop-first workflow
-   [Vite](https://vitejs.dev/) as a build tool and server
-   [Ionicons](https://ionic.io/ionicons)

### What I learned

-   **You can pick one** - As a beginner frontend developer, I learned CSS grid and flexbox for layout and responsive design. I am one of the many developers who were fortunate enough not to deal with float or table based layouts. Naturally I asked myself one of the most popular questions in CSS - *Should I use flexbox or grid?*I read quite a lot of blogposts and twitter threads around this question. The most common answer seems to be use both. You don't need to compare them. They compliment each other. I do agree with this to some extent, because well that's what I have been doing all along. But as I was working on this project I thought of something. If you are just starting out isn't it better to just pick one, stick to it and master it? Because in all honesty, flexbox can do almost everything grid can do and the same is true for grid (even more so). I feel this would take out a lot of decision fatigue when it comes to deciding between the two. If you are a grid guy, then you know you just use grid for everything. If you are a flexbox guy then you just use it for everything. Of course there are things flexbox can do better than grid and vice versa. In those instances, I think that's when you should pick one over the other. If you are going to pick one, I think grid is the better choice. Its more future proof, powerful and flexible (also [subgrid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Subgrid) is almost here). Those are just my thoughts.

-   **Use a preprocessor** - Including all the styles for your project in one CSS file can quickly get out of hand. Adopting a CSS preprocessor like SASS or LESS is a great idea and provides some nice advantages. Check out [this](https://raygun.com/blog/10-reasons-css-preprocessor/) article that talks about some of the reasons you would want to use a CSS preprocessor. In addition, CSS preprocessors allow you to adopt some kind or architecture and folder structure for arranging the CSS in your project. I used the **7-1 pattern** in this project. You can learn about it [here](https://bit.ly/32FbkM6).

-   **Take advantage of utility classes** - When working with pure HTML and CSS, without using any frameworks or libraries like React, TailwindCSS and so on, its useful to create component classes in your CSS. For example a `.btn` class for your button components or `.card` class for your card components.

    ```css
    .card {
        padding: 1em;
        border-radius: 0.7em;
        display: flex;
        box-shadow: 0 0 10px 1px rgb(0 0 0 / 7%);
    }
    ```

    The idea in doing this is to allow you to use these classes in your HTML to actually make the component look as you want in your UI. Note that these components need to be part of the layout of the UI, where other components exist. To separate one component from another component and introduces some whitespace you use techniques like `margin`, `position`, `gap` and etc. If you include a margin declaration on the component directly you may end up defeating the whole purpose of the component class. Instead you should use **utility classes**. What do I mean? Well lets take an example.

    ##### HTML

    ```html
    <div class="grid">
        <div class="card">
            <h1 class="card__title">...</h1>
            <p class="card__text">...</p>
        </div>
        <div class="card">
            <h1 class="card__title">...</h1>
            <p class="card__text">...</p>
        </div>
        <div class="card">
            <h1 class="card__title">...</h1>
            <p class="card__text">...</p>
        </div>
    </div>
    ```

    To add whitespace between these card you might think of adding a `margin-bottom` property on the `.card` class like this:

    ```css
    .card {
        padding: 1em;
        border-radius: 0.7em;
        display: flex;
        box-shadow: 0 0 10px 1px rgb(0 0 0 / 7%);
        margin-bottom: 1em;
    }
    ```

    But what if you want to use that component somewhere there needs to be a margin on the right for whitespace? Then what? A better idea is to create a utility class like `mb-1` that contains only that `margin-bottom` declaration such that you don't need to touch the code in your `.card` rule.

    ```css
    .mb-1 {
        margin-bottom: 1em;
    }
    ```

    > mb is a shorthand for **m**argin **b**ottom by the way. In case you were wondering.

    Now you can just add this class in your HTML markup as shown below.

    ```html
    <div class="grid">
        <div class="card mb-1">
            <h1 class="card__title">...</h1>
            <p class="card__text">...</p>
        </div>
        <div class="card mb-1">
            <h1 class="card__title">...</h1>
            <p class="card__text">...</p>
        </div>
        <div class="card">
            <h1 class="card__title">...</h1>
            <p class="card__text">...</p>
        </div>
    </div>
    ```

    > The last card doesn't have a `.mb-1` class like the others cards because it does not have a sibling after it. Therefore it doesn't need whitespace below it.

    If you want briefly learn more about the concept of utility classes in HTML and CSS, check out [this](https://designsystem.digital.gov/utilities/) short article. For a more detailed explanation of utility classes check out this blog from [Adam Wathan](https://adamwathan.me/), the creator of [TailwindCSS](https://tailwindcss.com/), a utility first CSS framework.

### Continued development

A big part of the modern web, particularly frontend web, is responsive design. This technique allows you to implement websites such that they adapt to whatever screen they are being viewed on. As I was developing this project I realized that responsive design is a major weak point on mine. Therefore my goal is to take some time improving my responsive design skills.

### Useful resources

-   [Advanced CSS and SASS course by Jonas Schmedtmann](https://www.udemy.com/course/advanced-css-and-sass/)

-   [The Responsive Design Bootcamp by Kevin Powel](https://scrimba.com/learn/responsive#)

-   [CSS in Depth book](https://www.manning.com/books/css-in-depth)

    **Note: I believe these 3 resources are enough to get you from beginner to pro css developer**

## Author

-   Frontend Mentor - [@chiroro-jr](https://www.frontendmentor.io/profile/chiroro-jr)
-   Twitter - [@chiroro_jr](https://www.twitter.com/chiroro_jr)

## Acknowledgments

If you would like to learn more about CSS architecture, how to arrange files and folders and the BEM methodology (and pretty much everything CSS) in detail you can check out **Jonas Schmedtmann**'s advanced CSS and Sass course [here](https://www.udemy.com/course/advanced-css-and-sass/). Most of what I know about CSS and Sass I learned in this course. I am sure it will help you too. I know I have already mentioned this course. That's how good I think it is.
