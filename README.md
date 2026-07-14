# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Overview

### The challenge
- Users should be able to: View the optimal layout for the site depending on their device's screen size.

### Links
- Solution URL: [Add solution URL here]
- Live Site URL: [Add live site URL here]

## My process

### Built with 
- Semantic HTML5 markup
- CSS custom properties (Variables)  
- Flexbox  
- CSS Grid  
- Mobile-first workflow  

### What I learned  
Working through this challenge was a huge step forward for my frontend fundamentals. I transitioned from just writing code that "looks right" to writing code that is semantic, structured, and genuinely responsive.  

Here are the major takeaways from my process:  

**1. Semantic HTML over Styling**
I initially used `<h1>` and `<h2>` tags simply to make the text bold for the names and titles. I learned that heading tags should be used for outlining document structure (Accessibility/SEO), not styling. I successfully refactored my code to use `<p>` tags with custom classes instead.

**2. Flexbox Container Rules**
I ran into an issue where the `gap` property wasn't working. I learned that `gap` only applies when the parent element is explicitly declared as a Flex container (`display: flex`) or Grid container.

```css
/* Realizing I needed to declare display: flex before using flex-direction and gap */
main {
    margin: 2.5rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
}
```
3. Mastering CSS Grid Placement
- Moving from the mobile-first layout to the desktop layout using Media Queries was challenging but rewarding. I learned how to count grid rows and columns, and how to make an element span across multiple areas.
```css
@media (min-width: 64em) {
    main {
        display: grid;
        grid-template-rows: repeat(2, 1fr);
        grid-template-columns: repeat(4, 1fr);
    }

    .card-daniel {
        grid-row: 1;
        grid-column: 1 / 3; /* Spanning across 2 columns */
    }
}
```
4. CSS Background Patterns
- I initially thought the large quotation mark was an `<img>` tag, but I learned how to layer background images over background colors directly in CSS, giving me much better control over positioning.

### Continued development
This project solidified my understanding of layout systems. Going forward, I want to practice more complex CSS Grid structures and continue focusing on responsive design best practices. My goal is to apply these exact layout skills to fully functional web applications and deploy them smoothly to hosting platforms like Render so they are accessible on the internet.

## Author
- Frontend Mentor - @CodyPhamQuynh
- Name - Pham Truc Quynh