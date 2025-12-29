# Testimonials Grid Section

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Built with

- Semantic HTML5 markup
- CSS Custom Properties
- CSS Contextual Variables
- Flexbox
- CSS Grid
- Mobile-first workflow

## The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

## What I learned

During this refactoring exercise, I implemented a powerful architecture pattern using **contextual CSS custom properties**. This approach creates self-contained, themeable components that automatically adapt their styling based on their context.

**Key Concepts Implemented:**

1. **Contextual Theming System**
   I defined CSS variables at the **card level** that propagate down to all children:

```css
.card-featured {
  background-color: var(--clr-primary-500);

  --avatar-border-color: var(--clr-primary-300);
  --text-primary-color: var(--clr-white);
  --text-secondary-color: var(--clr-grey-200);
}
```

2. **Component-Based Consumption**
   Child components consume these contextual variables without knowing about their parent:

```css
.avatar {
  border: 2px solid var(--avatar-border-color, transparent);
}

.heading-sm {
  color: var(--text-primary-color, currentColor);
}
```

3. **Automatic Theme Propagation**
   Component automatically adapt based on their container's theme variables. No need for multiple modifier classes.

```html
  <article class="card  card-featured">

    <img class="avatar"/>
    <h3 class="heading-sm">
    <p class="text-subdued">

  </article>
```

**Benefits discovered**

- Cleaner HTML
- Easier Maintenance
- Scalability

**Technical Implementation**

1. Root Variables: Define color palette at :root
2. Contextual Variables: Define theme variables at component level
3. Fallback Values: Use `var(--variable, fallback) for safety
4. Cascading Inheritance: Variables cascade naturally through the DOM

**Conclusion**

The pattern works particularly well for card-based interfaces where multiple visual variations share the same structural markup, allowing for rapid theme creation and consistent styling across an entire application.

## Screenshot

![Destop screenshot](./screenshots/desktop-screenshot.png)

## Links

- Solution URL: [https://www.frontendmentor.io/solutions/responsive-testimonials-grid-with-css-customized-cards-l5T4woOxaK](https://www.frontendmentor.io/solutions/responsive-testimonials-grid-with-css-customized-cards-l5T4woOxaK)
- Live Site URL:
  [https://codereme.github.io/frontend-mentor-solutions/testimonials-grid-section/index.html](https://codereme.github.io/frontend-mentor-solutions/testimonials-grid-section/index.html)

## Author

- Frontend Mentor - [@codereme](https://www.frontendmentor.io/profile/codereme)
- Github - [@codereme](https://github.com/codereme)
