# Blog Preview Card

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Built with

- Semantic HTML5 markup
- Accessible markup
- CSS custom properties
- Utility classes
- Flexbox
- Mobile-first workflow

## Screenshot

![Desktop screenshot](./assets/screenshots/desktop-screenshot.png)

## Links

- Solution URL: [https://www.frontendmentor.io/solutions/responsive-blog-preview-card-PSsvCYF15u](https://www.frontendmentor.io/solutions/responsive-blog-preview-card-PSsvCYF15u)

- Live Site URL: [https://codereme.github.io/frontend-mentor-solutions/blog-preview-card/index.html](https://codereme.github.io/frontend-mentor-solutions/blog-preview-card/index.html)

## What I learned

- Adaptive image cropping: Using image container `height` and blog image `object=fit: cover` to show different image sections - a cropped portion on mobile vs. the complete image on desktop.

```css
.card__header {
  inline-size: 100%;
  block-size: 12.5rem;
}
.blog-img {
  inline-size: 100%;
  block-size: 100%;
  object-fit: cover;
}
```

- How to apply stylish borders to the card using `border` and `box-shadow`

```css
.card {
  border: 1px solid var(--gray-950);
  box-shadow: 8px 8px 0px 0px #000000;
}
```

## Author

- Frontend Mentor - [@codereme](https://www.frontendmentor.io/profile/codereme)
- Github - [@codereme](https://github.com/codereme)
