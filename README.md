# Customer Testimonials Grid

A modern, responsive customer testimonials section built with semantic HTML5 and CSS3. This project demonstrates how to create a polished collection of customer review cards using Flexbox, reusable CSS components, responsive design principles, and accessible markup.

The layout features customer avatars, star ratings, professional details, quotation text, and a highlighted testimonial card.

## Overview

The **Customer Testimonials Grid** is a front-end development project focused on presenting customer feedback in a clean, visually engaging, and responsive layout.

The interface uses a flexible card layout to accommodate testimonials of different lengths while maintaining consistent spacing and a clear visual hierarchy.

The project is built using HTML5 and CSS3 without JavaScript or external CSS frameworks.

## Features

- **Responsive Layout:** Adapts to desktop, tablet, and mobile screen sizes.
- **Flexbox Layout:** Arranges testimonial cards and their internal content.
- **Flexible Card Sizing:** Uses `flex-basis`, `flex-grow`, and `flex-shrink` to manage card dimensions.
- **Featured Testimonial:** Highlights one review with a contrasting visual design.
- **Customer Avatars:** Displays customer profile images alongside their details.
- **Star Ratings:** Presents review ratings with accessible labels.
- **Customer Information:** Shows customer names and professional roles.
- **Quotation Styling:** Uses decorative quotation marks to establish visual hierarchy.
- **Consistent Spacing:** Uses Flexbox `gap` and reusable spacing rules.
- **Reusable CSS Components:** Applies shared styles across testimonial cards.
- **CSS Custom Properties:** Centralizes colors, shadows, borders, and transitions.
- **Interactive Hover Effects:** Adds subtle visual feedback when users hover over cards.
- **Semantic HTML5:** Uses meaningful structural elements.
- **Accessibility Considerations:** Includes alternative text, descriptive rating labels, and reduced-motion support.
- **Clean Code Organization:** Separates HTML content from CSS presentation.

## Preview

The interface includes:

- A branded header.
- A centered introductory heading.
- A collection of five testimonial cards.
- A featured review with a contrasting background.
- Customer avatars, ratings, and review text.
- A closing message and footer.

The design uses a light background, dark navy accents, warm highlights, rounded cards, and subtle shadows.

## Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Structures the testimonial content. |
| CSS3 | Defines the appearance and layout of the interface. |
| CSS Flexbox | Controls alignment, spacing, wrapping, and card sizing. |
| CSS Media Queries | Adjusts the layout for smaller screens. |
| CSS Custom Properties | Provides reusable design variables. |
| CSS Pseudo-classes | Creates hover effects and interactive visual states. |
| Git | Tracks changes to the project. |
| GitHub | Hosts the source code and documentation. |
| Visual Studio Code | Provides the development environment. |

## Project Structure

```text
Customer-Testimonials-Grid/
│
├── index.html
├── styles.css
├── README.md
└── .gitignore
```

### File Descriptions

- `index.html` — Contains the page structure, testimonial cards, customer details, ratings, and review content.
- `styles.css` — Defines the card layout, Flexbox rules, typography, colors, responsive behavior, and visual effects.
- `README.md` — Documents the project and explains its implementation.
- `.gitignore` — Excludes selected local development and temporary files from version control.

## Getting Started

Follow these steps to run the project locally.

### Prerequisites

You will need:

- A modern web browser.
- Visual Studio Code or another code editor.
- Git installed if you intend to use Git for version control.

### 1. Clone the Repository

```bash
git clone https://github.com/Regalson001/Customer-Testimonials-Grid.git
```

### 2. Navigate to the Project Directory

```bash
cd Customer-Testimonials-Grid
```

### 3. Open the Project in Visual Studio Code

```bash
code .
```

Alternatively, open Visual Studio Code, select **File → Open Folder**, and choose the project directory.

### 4. Run the Project

Open `index.html` in your browser.

You can also use the Live Server extension in Visual Studio Code to preview changes while developing.

**Note:** The customer avatars are loaded from an external image service. An internet connection is required to display them.

## Implementation Details

### 1. Semantic HTML Structure

The project uses semantic elements to organize its content.

- `<header>` contains the brand and page label.
- `<main>` contains the primary page content.
- `<section>` groups the testimonials.
- `<article>` represents an individual testimonial.
- `<blockquote>` identifies the quoted review.
- `<footer>` contains testimonial attribution details and the page footer.

This structure improves code readability and communicates the role of each section.

### 2. Flexbox Container

The testimonials are arranged using Flexbox.

```css
.testimonials-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: stretch;
  gap: 24px;
}
```

The container allows cards to wrap onto additional rows when the available width is insufficient.

The `gap` property provides consistent spacing between cards without requiring individual margins.

### 3. Flexible Card Sizing

The standard cards use:

```css
.testimonial-card {
  flex: 1 1 280px;
}
```

This allows cards to grow or shrink according to the available space, starting from a preferred basis of `280px`.

The featured card uses:

```css
.testimonial-card--featured {
  flex-grow: 2;
  flex-basis: 420px;
}
```

This gives the featured card a larger starting basis and a greater share of positive free space under comparable sizing conditions.

### 4. Internal Flexbox Layout

Each testimonial card uses a vertical layout.

```css
.testimonial-card {
  display: flex;
  flex-direction: column;
}
```

The customer profile uses a horizontal layout:

```css
.customer-profile {
  display: flex;
  align-items: center;
  gap: 14px;
}
```

These nested layouts allow the avatar, customer information, rating, testimonial text, and footer to be arranged independently.

### 5. Footer Alignment

The testimonial footer uses:

```css
.testimonial-footer {
  margin-top: auto;
}
```

This pushes the footer toward the bottom of the available vertical space in a column-oriented flex container.

The result is useful when cards have different amounts of testimonial text.

### 6. Responsive Design

Media queries adjust the layout for tablets and mobile devices.

```css
@media (max-width: 480px) {
  .testimonials-grid {
    flex-direction: column;
    align-items: stretch;
    gap: 18px;
  }

  .testimonial-card {
    width: 100%;
    max-width: none;
  }
}
```

On narrow screens, the cards stack vertically and use the available width.

### 7. CSS Custom Properties

The project uses custom properties to centralize shared design values.

```css
:root {
  --color-primary: #172554;
  --color-accent: #e8a23a;
  --color-text: #273449;
  --color-muted: #718096;
}
```

This makes the visual theme easier to maintain and update.

### 8. Accessibility

Accessibility considerations include:

- Semantic HTML elements.
- Alternative text for customer avatar images.
- Descriptive labels for star ratings.
- Decorative quotation marks hidden from assistive technology.
- Responsive text and layouts.
- Reduced-motion support.

The project has been designed with accessibility in mind, but it has not been formally audited against WCAG requirements.

## Learning Objectives

This project provides practical experience with:

- Building a testimonial interface using semantic HTML5.
- Creating reusable components with CSS classes.
- Using `display: flex` to create flexible layouts.
- Applying `flex-direction: column` to stack content vertically.
- Using `flex-wrap` to allow cards to flow onto multiple rows.
- Controlling card sizing with `flex-basis`, `flex-grow`, and `flex-shrink`.
- Aligning content with `justify-content` and `align-items`.
- Using `gap` for consistent spacing.
- Positioning card footers with `margin-top: auto`.
- Nesting Flexbox layouts for customer profiles and card content.
- Creating responsive layouts with media queries.
- Applying CSS custom properties for maintainable styling.
- Improving accessibility with semantic markup and descriptive labels.
- Managing a front-end project with Git and GitHub.

## Current Limitations

This is a static front-end demonstration.

- Customer names and testimonials are fictional sample content.
- Star ratings are illustrative and are not connected to a review platform.
- Customer avatars are loaded from an external service.
- Testimonials are not retrieved from a database or API.
- There is no customer review submission form or content management system.

These limitations are intentional because the project focuses on HTML and CSS layout skills.

## Future Improvements

Potential enhancements include:

- Adding more testimonial cards.
- Creating a version using CSS Grid.
- Adding a responsive company logo section.
- Introducing a dark-mode theme.
- Loading testimonials from an API.
- Building a customer review submission form.
- Adding automated accessibility checks.
- Testing the layout across a wider range of screen sizes.

## Author

**Stephen Oyugi**

Front-End Developer in Training

Focused on building clean, responsive, accessible, and user-friendly interfaces using HTML5 and CSS3.

- **GitHub:** [@Regalson001](https://github.com/Regalson001)
- **Repository:** [Customer-Testimonials-Grid](https://github.com/Regalson001/Customer-Testimonials-Grid)

## License

This project is intended for educational and portfolio purposes.

A license has not been specified. If you want others to reuse or distribute your code under explicit terms, consider adding a suitable license file.

---

*Building better web experiences, one project at a time.*
