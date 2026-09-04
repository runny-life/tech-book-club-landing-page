# Frontend Mentor - Tech book club landing page solution

This is a solution to
the [Tech book club landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/tech-book-club-landing-page-fZQidjHU73).
Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![Tech Book Club Landing Page](./screenshot.jpg)

### Links

- Solution
  URL: [GitHub Repository]([https://github.com/yourusername/tech-book-club-landing-page](https://github.com/runny-life/tech-book-club-landing-page))
- Live Site URL: [Vercel Deployment](https://tech-book-club-landing-page.vercel.app)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [Tailwind CSS](https://tailwindcss.com/) - CSS framework
- [Vite](https://vitejs.dev/) - Build tool
- [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG) - Vector graphics for icons and decorations

### What I learned

This project was a great opportunity to practice building a modern, responsive landing page with Tailwind CSS. Here are
some key takeaways:

#### Responsive Design with Tailwind

I implemented a fully responsive layout using Tailwind's utility classes and custom breakpoints:

```html

<section class="relative grid gap-16 pb-20 lg:grid-cols-[35.625rem_1fr]">
  <!-- Content that adapts from mobile to desktop -->
</section>
```

#### Custom Utility Classes

I extended Tailwind with custom utilities for specific project needs:

```css
@utility container {
  max-width: 73.125rem;
  margin-inline: auto;
  padding-inline: 1rem;

  @media (min-width: 768px) {
    padding-inline: 2rem;
  }
}

@utility counter-reset {
  counter-reset: my-counter;
}

@utility counter-increment {
  counter-increment: my-counter;
}
```

#### CSS Counter for Step Indicators

One interesting technique I used was CSS counters to automatically number the "Your tech reading journey" steps:

```
.counter-reset {
  counter-reset: my-counter;
}

.counter-increment {
  counter-increment: my-counter;
}

/* Usage in HTML */
<li class="counter-increment before:content-[counter(my-counter)]"  >
Choose your membership tier
</li >
```

#### Gradient Text Effects

Creating gradient text with background clipping:

```css
.bg-gradient-text {
  background: linear-gradient(107.24deg, #fea36f 10.6%, #062630 58.45%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
```

#### Responsive Images with Picture Element

Using the `<picture>` element with multiple sources for optimal image loading:

```html

<picture>
  <source
    media="(min-width: 1024px)"
    srcset="./image-desktop.webp"
  />
  <source
    media="(min-width: 768px)"
    srcset="./image-tablet.webp"
  />
  <img
    src="./image-mobile.webp"
    alt=""
  />
</picture>
```

#### Interactive Button States

Implementing hover effects with pseudo-elements:

```css
.button-hover-effect {
  position: relative;
  overflow: hidden;
  transition: all 0.3s;
}

.button-hover-effect::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(90deg, #ffe2d1 0%, #fff5ef 100%);
  opacity: 0;
  transition: opacity 0.3s;
  z-index: 0;
}

.button-hover-effect:hover::before {
  opacity: 1;
}

.button-hover-effect > span {
  position: relative;
  z-index: 10;
}
```

### Continued development

In future projects, I want to focus on:

- **Performance optimization**: Implementing lazy loading for images and optimizing asset delivery
- **Accessibility**: Further improving ARIA attributes and keyboard navigation
- **Animation**: Adding subtle scroll-triggered animations for a more polished experience
- **Testing**: Adding unit and integration tests to ensure component reliability
- **CSS Variables**: Deeper exploration of CSS custom properties for theming

### Useful resources

- [Tailwind CSS Documentation](https://tailwindcss.com/docs) - The official documentation was invaluable for
  understanding utility classes and customization
- [CSS Gradient Generator](https://cssgradient.io/) - Helped me create the gradient effects for buttons and text
- [MDN Web Docs](https://developer.mozilla.org/) - Excellent resource for semantic HTML and CSS techniques
- [Frontend Mentor Community](https://www.frontendmentor.io/community) - Great for design inspiration and feedback

## Author

- Frontend Mentor - [@runny-life](https://www.frontendmentor.io/profile/runny-life)
- GitHub - [@runny-life](https://github.com/runny-life)

## Acknowledgments

Thank you to the Frontend Mentor team for creating this challenge and providing high-quality design assets. The
community feedback and solutions from other developers were also incredibly helpful in refining this project.

Special thanks to the Tailwind CSS team for creating such a powerful and flexible CSS framework that made responsive
development seamless.