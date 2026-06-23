# Lacfog Academy - Official Landing Page

## 📌 Project Overview
This is a lightweight, high-performance, single-page static website built for Lacfog Academy. It is designed to be fully responsive, visually engaging, and highly optimized for fast loading speeds across all devices. 

**Live Demo / Portal Integration:** The "Portal" links currently redirect to the Springdrill portal application (`https://springdrill-portal.vercel.app/login.html`).

## 🛠 Tech Stack
* **HTML5:** Semantic structuring.
* **Vanilla CSS3:** Custom styling, CSS Grid/Flexbox layouts, and keyframe animations.
* **Vanilla JavaScript (ES6):** DOM manipulation, Intersection Observers for scroll animations, and interval-based hero sliders.
* **Zero Dependencies:** No external frameworks (e.g., Bootstrap, Tailwind, jQuery) are required. 

## 📂 File Structure
Because this is a streamlined project, all code is contained within a single `index.html` file to minimize HTTP requests.
* `index.html` - Contains the HTML structure, `<style>` block (CSS), and `<script>` block (JS).
* `*.jpg` / `*.png` / `*.jpeg` - Local image assets referenced directly in the HTML.

## 🎨 Brand Identity & Styling (CSS)
All brand colors are centrally managed using CSS Custom Properties (Variables) at the very top of the `<style>` block inside `:root`. 

To update the primary colors, only change these variables:
* `--brand-dark: #8B001A;` (Deep Burgundy)
* `--brand-primary: #C8102E;` (Lacfog Crimson Red)
* `--brand-accent: #FACC15;` (Lacfog Uniform Yellow)

**Typography:** The project uses Google Fonts: *Fraunces* (Display/Headings) and *Inter* (Body).

## ⚙️ Key JavaScript Features
The JavaScript is located at the absolute bottom of the `<body>` tag and handles the following interactive elements:

1.  **Sticky Navigation:** Listens to the `window.scrollY` event to apply a drop-shadow and background blur when the user scrolls past 10px.
2.  **Mobile Hamburger Menu:** Toggles the `.open` class to reveal the mobile dropdown navigation.
3.  **Hero Background Fader:** An interval timer (`setInterval`) that loops every 5 seconds (5000ms), cycling the `.active` class through the `.hero-bg-slide` elements to create a smooth crossfade effect.
4.  **Scroll Animations (Intersection Observer):** Elements with the `data-animate` attribute start hidden and translate upwards. When the Intersection Observer detects they are in the viewport, the `.in-view` class is added to trigger the CSS transition.
5.  **Animated Number Counters:** Located in the "Stats" section. When scrolled into view, JS calculates an easing function to count up from 0 to the target number defined in the `data-stat` attribute.
6.  **Gallery Lightbox:** Clicking any `.gallery-item` extracts its inline `background-image` style and applies it to the `#lightboxContent` div, opening a modal.

## 🖼 Image Management
Images in the "Discover", "Features", and "Gallery" sections are applied as inline CSS `background-image` properties directly on the HTML `<div>` tags (e.g., `style="background-image: url('filename.png');"`). 

* To swap an image, replace the file in the root directory and update the specific inline style URL. Ensure new images are optimized/compressed for web to maintain performance.

## 🚀 How to Run Locally
No server setup is required. Simply open the `index.html` file in any modern web browser. If using VS Code, the "Live Server" extension is recommended for hot-reloading during development.