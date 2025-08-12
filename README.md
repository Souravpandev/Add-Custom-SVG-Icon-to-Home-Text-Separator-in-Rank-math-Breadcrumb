
# Add-Custom-SVG-Icon-to-Home-Text-Separator-in-Rank-Math-Breadcrumb

This project allows you to **customize Rank Math breadcrumbs** by replacing the default "Home" text with a **custom SVG icon** and changing the breadcrumb separator into another SVG icon.  

📌 **Demo & Tutorial** → [View full tutorial here](https://wpoptimizelab.com/how-to-customize-rank-math-breadcrumb-style-add-custom-svg-icon-to-home-text-separator-in-rank-math-breadcrumb/)  

---

## Features
- Replace "Home" text with **SEO-friendly SVG icon**
- Replace default breadcrumb separator with a **custom SVG arrow**
- Works with Rank Math breadcrumb output
- Accessibility attributes for screen readers
- Lightweight, no extra plugin required
- Includes **JavaScript fallback** in case PHP filter fails due to caching
- Custom CSS styling for icon alignment and hover effect

---

## How to Use

### 1. Add the Code to Your Theme or Custom Plugin
- Copy the PHP code from `rankmath-breadcrumb-custom-icons.php`
- Paste it into your **theme’s `functions.php` file** or a custom plugin.

```php
// Example: Adding the main PHP function
add_action( 'wp_head', 'replace_rankmath_home_with_icon' );
add_action( 'wp_footer', 'rankmath_home_icon_js_fallback' );
add_action( 'wp_head', 'rankmath_home_icon_styles' );
