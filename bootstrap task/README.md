<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/b/b2/Bootstrap_logo.svg" alt="Bootstrap Logo" width="80" height="80">
</p>

<h1 align="center">☕ The Daily Grind — Campus Cafe</h1>

<p align="center">
  <em>A single-page, fully responsive and modern website for a fictional campus cafe, built entirely utilizing <strong>Bootstrap 5.3</strong> components, grid system, and utilities.</em>
</p>

<p align="center">
  <a href="#about-the-project"><strong>Explore the docs »</strong></a>
  <br />
  <br />
  <a href="index.html">View Project</a>
  ·
  <a href="#how-to-run">How to Run</a>
  ·
  <a href="#task-requirements--implementation-details">Implementation Details</a>
</p>

---

## 📖 About The Project

**"The Daily Grind"** is an interactive, mobile-first web page designed to demonstrate a comprehensive understanding of the Bootstrap 5.3 HTML/CSS framework. It features everything from auto-playing carousels and interactive modals to custom form validation and responsive grid layouts, completely loaded via CDN without requiring any build tools.

### 📁 Project Structure

| File         | Purpose                                                                                                                                                                                       |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `index.html` | The main webpage containing all the structural HTML and Bootstrap 5.3 components.                                                                                                             |
| `style.css`  | A minimal custom stylesheet (under 100 lines) handling specifics that Bootstrap doesn't provide out-of-the-box (like fixed image heights, hover lift effects, and custom scrolling behavior). |

---

## 🚀 How to Run

1. **Clone or Download** this repository/folder to your local machine.
2. **Open `index.html`** in any modern web browser (Chrome, Firefox, Safari, Edge).
3. _That's it!_ No Node.js, Webpack, or local servers are required. All styling and scripts are fetched directly via Bootstrap CDNs.

---

## ✅ Task Requirements & Implementation Details

Below is a detailed breakdown mapping our specific task requirements to exactly how they were implemented using Bootstrap 5.3 features.

### 1. Carousel with at least 3 slides and custom captions

> **Location:** Hero area at the top of the page (`#home`)

Implemented a full-width auto-playing carousel featuring **4 unique slides**. Each slide includes an engaging image, a custom heading, descriptive text, and calls to action.

- **Core Components:** `.carousel`, `.carousel-inner`, `.carousel-item`, `.carousel-indicators`
- **Text & Controls:** `.carousel-caption`, `.carousel-control-prev`, `.carousel-control-next`
- **Attributes:** `data-bs-ride="carousel"` (auto-play), `data-bs-target`, `data-bs-slide-to`
- **Utilities:** `.d-block`, `.w-100` ensuring images fill the container accurately.

### 2. Pricing table using Bootstrap cards and grid system

> **Location:** Monthly Coffee Plans (`#pricing`)

Built a responsive 3-column layout featuring different pricing tiers (Starter, Popular, Unlimited). The "Popular" tier uses primary border utilities and a badge to stand out. Below the cards, a dark-themed `.table` provides side-by-side plan comparisons.

- **Card Anatomy:** `.card`, `.card-header`, `.card-body`, `.card-title`
- **Grid Layout:** `.row`, `.row-cols-1`, `.row-cols-md-3`, `.col`, `.g-4` (gutters)
- **Styling Utilities:** `.h-100` (equal height), `.shadow-sm`, `.border-primary`, `.mt-auto` (pushes buttons to bottom)
- **Comparison Table:** `.table`, `.table-dark`, `.table-responsive` (for mobile-friendly horizontal scrolling).

### 3. Sticky footer layout using utilities

> **Location:** Footer at the absolute bottom of the document

Used Bootstrap's flexbox utilities on the `<body>` element to ensure the footer always sticks perfectly to the bottom of the viewport, even on ultra-wide screens or pages with very minimal content.

- **Flexbox Setup:** `.d-flex`, `.flex-column`, `.h-100` on the `<body>` and `<html>`
- **Content Restraints:** `.flex-shrink-0` on the `<main>` area so it doesn't collapse
- **Footer Positioning:** `.mt-auto` on the `<footer>` tags to dynamically push it downward.

### 4. Responsive navbar with dropdown menus and a search bar

> **Location:** Top navigation bar

A dark-themed, sleek navigation bar that sticks to the top of the screen as the user scrolls. It seamlessly collapses into a mobile hamburger menu on smaller screens and includes multi-tier dropdown menus and an inline search form.

- **Base Navbar:** `.navbar`, `.navbar-expand-lg`, `.navbar-dark`, `.bg-dark`, `.sticky-top`
- **Responsiveness:** `.navbar-toggler`, `.collapse`, `.navbar-collapse`
- **Dropdowns:** `.dropdown`, `.dropdown-toggle`, `.dropdown-menu`, `.dropdown-item`
- **Search Form:** Implemented using `.d-flex`, `.form-control`, and `.btn-outline-light`.

### 5. Modals for displaying additional content on button click

> **Location:** "Today's Specials" pop-up (`#specialsModal`)

A vertically centered dialogue box that appears over the page content when triggered. It presents a cleanly styled `list-group` of special menu items accompanied by price badges.

- **Modal Structure:** `.modal`, `.modal-dialog`, `.modal-dialog-centered`, `.modal-content`
- **Sub-sections:** `.modal-header`, `.modal-body`, `.modal-footer`
- **Interactive Elements:** `data-bs-toggle="modal"`, `data-bs-target`, `.btn-close`
- **Interior Content:** Flushed lists via `.list-group` and `.list-group-flush`.

### 6. Forms with validation

> **Location:** Reservation / Feedback Form (`#contact`)

A comprehensive, client-side validated form collecting user information, visit purpose (radios), interests (checkboxes), and a message text area.

- **Input Styling:** `.form-control`, `.form-label`
- **Checkboxes/Radios:** `.form-check`, `.form-check-input`, `.form-check-label`
- **Validation:** Used `.needs-validation` coupled with the `.invalid-feedback` classes.
- **JavaScript Hook:** Triggered Bootstrap's custom pseudo-class validation script appended via `.was-validated` upon submission attempt.

### 7. Grid-based gallery that adjusts for different screen sizes

> **Location:** Our Cafe Gallery (`#gallery`)

A visually dynamic masonry-like responsive image gallery ranging from 2 columns on mobile devices up to 4 columns on large desktop screens, giving a stunning scrapbook feel.

- **Grid Classes:** `.row`, `.col-6` (mobile), `.col-md-3`, `.col-md-4`, `.col-md-6` (medium+ breakpoints)
- **Image Aesthetics:** `.img-fluid` (scales down automatically), `.rounded`, `.shadow-sm`
- **Spacing:** Handled completely via grid gutters (`.g-3`).

### 8. Alerts for different message types

> **Location:** Announcements section (below Hero Carousel)

Four distinct alert components demonstrating Bootstrap's contextual color palette to deliver notifications effectively to users.

- **Contextual Alerts:** `.alert-success`, `.alert-warning`, `.alert-info`, `.alert-danger`
- **Interactivity:** `.alert-dismissible`, coupled with `.fade` and `.show` for smooth disappearing animations when the `.btn-close` is clicked.

### 9. Badges and buttons with various colors and sizes

> **Location:** Our Popular Picks (`#menu`)

Showcases the power of Bootstrap's component variants, providing differently sized and colored interactive elements for menu classifications and actions.

- **Buttons:** `.btn-primary`, `.btn-success`, `.btn-danger`, `.btn-outline-dark`, `.btn-lg`, `.btn-sm`
- **Badges:** `.bg-primary`, `.bg-warning text-dark`, `.rounded-pill`, etc. Used heavily in the pricing section ("Best Value") and the menu items lists.

### 10. Bootstrap utilities (Spacing, Alignment, Colors, Shadows)

> **Location:** Used ubiquitously across the entire application

Relied heavily on Bootstrap's utility API to handle margin, padding, typography, element alignment, and aesthetic touches without writing arbitrary CSS.

- **Spacing:** `.m-1`, `.mt-5`, `.mb-4`, `.py-5`, `.px-3`, `.gap-2`
- **Text Formatting:** `.text-center`, `.text-muted`, `.fw-bold`, `.fs-4`, `.text-md-start`
- **Backgrounds & Shadows:** `.bg-light`, `.bg-dark`, `.shadow`, `.shadow-sm`
- **Flexbox:** `.d-flex`, `.justify-content-between`, `.align-items-center`

### 11. Offcanvas sidebar for navigation

> **Location:** Left-side pull-out menu on mobile devices

Provides an engaging navigational experience on constrained viewing spaces. Clicking the hamburger icon on mobile triggers a smooth, sliding side-panel menu.

- **Offcanvas Anatomy:** `.offcanvas`, `.offcanvas-start`, `.offcanvas-header`, `.offcanvas-body`
- **Triggers:** `data-bs-toggle="offcanvas"`, `data-bs-target="#sidebar"`
- **Styling:** Features dark mode header `.bg-dark text-white` and a `.btn-close-white`.

### 12. Tooltips and popovers for extra information

> **Location:** Menu item buttons (`#menu`)

Improves UI cleanliness by hiding secondary information (like drink descriptions or detailed prices/ingredients) until the user requests it via hover or click.

- **Tooltips:** `data-bs-toggle="tooltip"` triggering native Bootstrap floating titles on hover.
- **Popovers:** `data-bs-toggle="popover"`, `data-bs-trigger="focus"` showing expanded contextual blocks on button click.
- **Initialization:** A small custom JavaScript snippet natively initializes these elements, as Bootstrap requires manual opt-in.

---

## 🎨 External Resources List

| Resource              | Version  | Delivery Method | Link                                                                                     |
| --------------------- | -------- | --------------- | ---------------------------------------------------------------------------------------- |
| **Bootstrap CSS**     | `5.3.3`  | jsDelivr CDN    | [Link](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css)          |
| **Bootstrap JS**      | `5.3.3`  | jsDelivr CDN    | [Link](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js)     |
| **Bootstrap Icons**   | `1.11.3` | jsDelivr CDN    | [Link](https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css) |
| **Stock Photography** | N/A      | Unsplash        | [Unsplash.com](https://unsplash.com)                                                     |

<br>
<p align="center">
  <i>Crafted with ❤️ and ☕  by Aaryan K.</i>
</p>
