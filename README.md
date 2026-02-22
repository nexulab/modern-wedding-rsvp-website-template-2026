# 💍 Modern Wedding RSVP Website Template 2026

An elegant, high-performance, and fully responsive single-page wedding website template. Designed with modern UI/UX principles, this template provides everything a couple needs to share their special day with loved ones, from event details to a fully interactive RSVP form.

(Placeholder for your actual screenshot)

## ✨ Features

- **Modern Design**: Clean, minimalist aesthetic utilizing glassmorphism, elegant typography (Playfair Display & Inter), and subtle scroll animations.

- **Fully Responsive**: Looks perfect on mobile devices, tablets, and large desktop screens.

- **Smart RSVP Form**: Includes custom radio buttons, interactive loading states, and a delightful Canvas Confetti celebration upon successful submission.

- **Live Countdown Timer**: Automatically calculates the days, hours, minutes, and seconds until the big day.

- **Dynamic "Add to Calendar"**: Generates an .ics file directly in the browser using vanilla JavaScript so guests can easily save the date.

- **SEO & AI Search Ready**: Pre-configured with Schema.org JSON-LD structured data (Event and FAQPage schemas) for rich Google snippets.

- **Zero Dependencies**: Built with a single HTML file using Tailwind CSS via CDN. No Node.js, Webpack, or complex build tools required.

## 🚀 Quick Start

1. Clone or Download this repository.
2. Open the `index.html` file in your favorite code editor.
3. Open `index.html` in your browser to view the template live!

## 🛠️ Customization Guide

This template is designed to be highly customizable right out of the box.

### 1. Changing the Wedding Date

To update the countdown timer and the dynamic calendar event, scroll to the bottom of the `index.html` file and update these JavaScript variables:

```javascript
// Change the countdown target date
const weddingDate = new Date("September 12, 2026 16:00:00").getTime();

// Change the calendar event details
const eventTitle = "Your Name & Partner's Name Wedding";
const location = "Your Venue, City, State ZIP";
const startTime = "20260912T230000Z"; // Adjust to your time in UTC
const endTime = "20260913T063000Z";   // Adjust to your time in UTC
```

### 2. Customizing Colors & Fonts

The color palette is controlled via the Tailwind configuration block in the <head> of the document. You can easily swap the "Sage" theme for your wedding colors:

```javascript
<script>
    tailwind.config = {
        theme: {
            extend: {
                colors: {
                    sage: { 100: '#...', 500: '#...', 800: '#...' }, // Replace with your primary color
                    cream: '#FDFBF7',
                    charcoal: '#2D2D2D',
                }
            }
        }
    }
</script>
```

### 3. Activating the RSVP Form

Currently, the RSVP form uses a mock front-end submission to demonstrate the loading spinner and confetti animation. To collect real RSVPs, change the <form> tag to point to a backend service like Formspree, Netlify Forms, or your own server:

```html
<!-- Example using Formspree -->
<form id="rsvp-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

## 💻 Tech Stack

- **HTML5**: Semantic structure and accessibility.
- **Tailwind CSS (CDN)**: Utility-first styling for rapid UI development.
- **Vanilla JavaScript**: For the countdown, mobile menu, scroll animations (IntersectionObserver), calendar generation, and form interactions.
- **Canvas Confetti**: For the celebration animation.

## 📄 License

This project is licensed under the Creative Commons Zero v1.0 Universal (CC0 1.0) license.

You can copy, modify, distribute, and perform the work, even for commercial purposes, all without asking permission. See the LICENSE file for more details.

(Attribution is appreciated but never required!)