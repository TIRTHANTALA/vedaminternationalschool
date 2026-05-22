# Vedam International School Website

This is a modern, responsive, and animated single-page website for "Vedam International School", built using HTML5, Tailwind CSS, Vanilla CSS, and Vanilla JavaScript.

## Features Included

*   **Responsive Design:** Fully optimized for mobile, tablet, and desktop views.
*   **Animations:** Smooth scroll-triggered animations via AOS (Animate On Scroll).
*   **Notice Ticker:** Live animated ticker for urgent school notices at the top.
*   **Hero Section:** Engaging landing view with floating elements and CTA buttons.
*   **About Us:** Clean presentation of the school's mission, vision, and values.
*   **Virtual Campus Tour:** Embedded YouTube video section for a campus preview.
*   **Portals:** Quick access links for Students, Parents, Calendar, and Fees.
*   **Gallery (Lightbox):** Masonry-style grid layout. Clicking an image expands it in a beautiful lightbox modal.
*   **Dynamic FAQ:** Space-saving collapsible accordion for common queries.
*   **Contact Section:** Inquiry form alongside direct WhatsApp and Phone Call buttons.
*   **Premium Aesthetic:** Uses Google Fonts (Inter & Outfit), professional color palettes, and glassmorphism effects.

## File Structure

```text
/school
│
├── index.html   # Main HTML structure with Tailwind CSS (CDN)
├── style.css    # Custom CSS (Ticker animations, glassmorphism, etc.)
├── script.js    # Interactivity (Menu toggle, FAQ, Lightbox, AOS init)
└── README.md    # Instructions and Documentation
```

## How to Run

1.  Simply double-click `index.html` to open it in your default web browser.
2.  No build step or Node.js installation is required, as the project utilizes Tailwind CSS via a CDN for immediate rendering and simplicity.

## How to Configure WhatsApp and Phone Buttons

To make the WhatsApp and Phone call buttons functional for your specific school, follow these steps:

### 1. WhatsApp Button
Open `index.html` in a text editor. Locate the WhatsApp button inside the **Contact Section** (around line 348).
It looks like this:
```html
<a href="https://wa.me/1234567890?text=Hello,%20I%20would%20like%20to%20know%20more%20about%20admissions." target="_blank" ...>
```
*   Replace `1234567890` with the school's actual WhatsApp phone number. **Important:** Include the country code but remove any `+`, spaces, or dashes. (e.g., for India, use `919876543210`).
*   You can also customize the pre-filled message by changing the text after `?text=`. Ensure spaces are replaced with `%20`.

### 2. Phone Call Button
Locate the Phone Call button just below the WhatsApp button.
It looks like this:
```html
<a href="tel:+1234567890" class="...">
```
*   Replace `+1234567890` with the actual school phone number inside the `href="tel:..."` attribute. (e.g., `href="tel:+919876543210"`). You can leave the `+` here.

## How to Update the Virtual Tour Video

1. Go to your YouTube video, click **Share**, and then click **Embed**.
2. Copy the URL inside the `src="..."` attribute (it should look like `https://www.youtube.com/embed/YOUR_VIDEO_ID`).
3. Open `index.html` and locate the `<iframe ...>` tag in the **Virtual Campus Tour** section (around line 171).
4. Replace the existing `src` URL with your copied URL.

## Customization

*   **Colors:** You can change the primary (blue) and secondary (amber/yellow) colors in the `index.html` file within the `<script>` tag inside the `<head>` that configures Tailwind:
    ```javascript
    tailwind.config = {
        theme: {
            extend: {
                colors: {
                    primary: '#YOUR_HEX_CODE',
                    // ...
                }
            }
        }
    }
    ```
*   **Images:** Replace the placeholder Unsplash URLs in `index.html` with paths to your actual school photos (e.g., `images/hero.jpg`).

Enjoy building your school's digital presence!
