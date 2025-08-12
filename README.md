# Add Custom SVG Icon to Home Text & Separator in Rank Math Breadcrumb

This project lets you customize **Rank Math breadcrumbs** by replacing the default "Home" text with a **custom SVG icon** and replacing the breadcrumb separator with another SVG icon.

📌 **Full Tutorial & Demo:** [https://wpoptimizelab.com/how-to-customize-rank-math-breadcrumb-style-add-custom-svg-icon-to-home-text-separator-in-rank-math-breadcrumb/](https://wpoptimizelab.com/how-to-customize-rank-math-breadcrumb-style-add-custom-svg-icon-to-home-text-separator-in-rank-math-breadcrumb/)

---

## ✨ Features

- 🏠 Replace "Home" text with an SEO-friendly SVG icon
- ➤ Replace default breadcrumb separator with a custom SVG arrow
- 🔧 Works with Rank Math breadcrumb output
- ♿ Accessibility attributes for screen readers
- 🪶 Lightweight, no extra plugin needed
- 🔄 Includes JavaScript fallback for caching compatibility
- 🎨 Custom CSS styling for icon alignment and hover effects

---

## 🚀 How to Use

### 1. Add the Code

Copy the PHP code from this repository into your **theme's `functions.php` file** or create a custom functionality plugin.

```php
add_action( 'wp_head', 'replace_rankmath_home_with_icon' );
add_action( 'wp_footer', 'rankmath_home_icon_js_fallback' );
add_action( 'wp_head', 'rankmath_home_icon_styles' );
```

### 2. Clear Cache

If you're using a caching plugin or CDN (like Cloudflare, LiteSpeed, etc.), clear the cache so the changes are visible.

### 3. Customize the SVG Icons

- **Home Icon** → Edit the `<svg>` code in the `$home_icon` variable
- **Separator Icon** → Edit the `<svg>` code in the `$separator_icon` variable

Both SVGs are inline for better performance and styling flexibility.

---

## ⚙️ How This Code Works

### PHP Filter Method
- Hooks into `rank_math/frontend/breadcrumb/html` filter
- Uses `preg_replace()` to find the "Home" link and replace the text with an SVG icon
- Replaces `<span class="separator">` content with a custom SVG separator

### JavaScript Fallback
- Runs after the page loads (`DOMContentLoaded`)
- Finds the first breadcrumb link and replaces its content with the home SVG icon
- Updates all separators with the custom SVG separator
- Ensures icons still display if the PHP filter fails due to output buffering or aggressive caching

### Custom CSS Styles
- Controls icon sizing, alignment, spacing, and hover color
- Uses `currentColor` so icons match text color automatically

---

## 📋 Requirements

- WordPress
- Rank Math SEO plugin with breadcrumbs enabled
- Basic knowledge of editing theme files

---

## 🎯 Example Output

**Before:**
```
Home » Category » Post
```

**After:**
```
🏠 Home ➤ Category ➤ Post
```
*(Where 🏠 and ➤ are replaced with actual SVG icons)*

---

## 🔍 SEO & Accessibility

- ✅ SVG `<title>` and `aria-label` tags for accessibility
- ✅ Minimal code footprint for faster loading  
- ✅ Breadcrumbs help Google understand site structure and improve SERP display
- ✅ Screen reader compatible with proper semantic markup
- ✅ Maintains breadcrumb schema markup for rich snippets

---

## 📁 File Structure

```
├── functions.php          # Main PHP code
├── README.md             # This file
└── demo/
    ├── before.png        # Screenshot before customization
    └── after.png         # Screenshot after customization
```

---

## 🛠️ Installation Options

### Option 1: Functions.php Method
1. Download the code from this repository
2. Copy the PHP code into your active theme's `functions.php` file
3. Save and clear any caching


---

## 🎨 Customization

You can easily customize the SVG icons by editing these variables in the code:

```php
// Change home icon
$home_icon = '<svg>...your custom SVG...</svg>Home';

// Change separator icon  
$separator_icon = '<svg>...your custom SVG...</svg>';
```

---

## 🐛 Troubleshooting

**Icons not showing?**
- Clear your cache (WordPress + CDN)
- Check if Rank Math breadcrumbs are enabled
- Verify the code was added correctly

**Icons showing as code?**
- The JavaScript fallback should fix this automatically
- Check browser console for any JavaScript errors

**Styling issues?**
- Adjust the CSS in the `rankmath_home_icon_styles()` function
- Use browser developer tools to inspect and modify styles

---

## 🤝 Contributing

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This code is released under the **MIT License**.  
You can freely use and modify it in personal or commercial projects.

---

## 👨‍💻 Author

**Developed by WP Optimize Lab**

📌 **Full Tutorial & Demo:** [https://wpoptimizelab.com/how-to-customize-rank-math-breadcrumb-style-add-custom-svg-icon-to-home-text-separator-in-rank-math-breadcrumb/](https://wpoptimizelab.com/how-to-customize-rank-math-breadcrumb-style-add-custom-svg-icon-to-home-text-separator-in-rank-math-breadcrumb/)

🌐 **Website:** [WP Optimize Lab](https://wpoptimizelab.com)  
📧 **Support:** [Contact Us](https://wpoptimizelab.com/contact)

---

## ⭐ Show Your Support

If this project helped you, please give it a ⭐ star on GitHub!

**Found a bug or have a suggestion?** [Open an issue](../../issues)

---

*Made with ❤️ for the WordPress community*
