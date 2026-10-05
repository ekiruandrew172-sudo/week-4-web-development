# SpendWise Dashboard Shell

## Project Overview

SpendWise is a modern personal finance dashboard designed to help users monitor their budget and spending categories.

This project focuses on creating the **visual dashboard shell** using HTML and modern CSS layout techniques. The current version uses static financial information and does not include JavaScript functionality.

## Features

The dashboard includes:

* Sidebar navigation menu
* Dashboard header
* User profile section
* Budget summary cards
* Six spending category cards
* Responsive mobile layout
* Hover and keyboard focus micro-interactions
* CSS custom properties for theming
* Optional dark theme

## Spending Categories

The dashboard displays the following categories:

1. Food
2. Transport
3. Rent
4. Entertainment
5. Savings
6. Utilities

Each category contains realistic static financial information, including spending amounts, budgets or savings goals, and progress indicators.

## Technologies Used

* HTML5
* CSS3
* CSS Grid
* CSS Flexbox
* CSS Custom Properties
* CSS Media Queries

## Project Structure

```text
SpendWise/
│
├── index.html
└── style.css
```

### `index.html`

Contains the structure of the SpendWise dashboard, including:

* Sidebar
* Navigation menu
* Header
* User information
* Summary section
* Spending category cards

### `style.css`

Contains all the styling for the dashboard, including:

* Color theme
* Grid layout
* Flexbox layouts
* Card styling
* Progress bars
* Responsive design
* Hover and focus effects
* Dark theme

## CSS Grid and Flexbox

CSS Grid is used for the main dashboard layout and category card layout.

The main dashboard uses:

```css
.dashboard {
    display: grid;
    grid-template-columns: 240px 1fr;
}
```

The category cards use:

```css
.card-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}
```

Flexbox is used inside the header, sidebar navigation, summary boxes, and individual dashboard cards.

## Theme Variables

The project uses CSS custom properties to maintain a consistent color theme.

Example:

```css
:root {
    --brand-color: #2563eb;
    --accent-color: #10b981;
    --surface-color: #ffffff;
    --background-color: #f3f6fa;
    --primary-text: #1f2937;
    --secondary-text: #6b7280;
}
```

Using variables makes it easier to change the application's color scheme without editing every individual element.

## Responsive Design

The dashboard becomes a single-column layout on screens below **768px**.

The responsive layout is created using:

```css
@media (max-width: 768px) {
    .dashboard {
        grid-template-columns: 1fr;
    }

    .card-grid {
        grid-template-columns: 1fr;
    }
}
```

The design was tested using the **Chrome DevTools Device Toolbar** to verify how the dashboard behaves on smaller screens.

## Card Micro-interactions

The category cards include subtle hover and keyboard focus effects.

```css
.category-card:hover,
.category-card:focus {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12);
}
```

The transition lasts **200ms**, which is below the required 250ms maximum.

The cards also use `tabindex="0"` to make them keyboard focusable.

## Dark Theme

As a stretch goal, the dashboard supports the user's system dark-mode preference.

```css
@media (prefers-color-scheme: dark) {
    :root {
        --brand-color: #60a5fa;
        --accent-color: #34d399;
        --surface-color: #1f2937;
        --background-color: #111827;
        --primary-text: #f9fafb;
        --secondary-text: #9ca3af;
    }
}
```

Only the CSS custom property values are overridden for the dark theme.

## How to Run

1. Download or clone the project.
2. Open the `SpendWise` folder.
3. Open `index.html` in a web browser.
4. Use Chrome DevTools to test the responsive layout.

No server or additional installation is required.

## Future Improvements

Future versions of SpendWise could include:

* Add and edit expenses
* Income tracking
* Budget creation
* Expense filtering
* Interactive charts
* Local storage or database integration
* User authentication
* Monthly financial reports
* JavaScript functionality

## Conclusion

The SpendWise Dashboard Shell provides a responsive foundation for a personal finance application. It demonstrates the use of **CSS Grid, Flexbox, CSS custom properties, media queries, and accessible micro-interactions** to create a clean and modern dashboard interface.
