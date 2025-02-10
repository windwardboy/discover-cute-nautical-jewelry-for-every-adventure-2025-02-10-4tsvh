# Project Nautica Landing Page - Maintenance Guide

This guide will help you maintain and customize the Project Nautica landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To modify:

1. **Brand Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-blue-900">Project Nautica</a>
```
Simply replace "Project Nautica" with your desired text.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600 hover:text-blue-900 transition duration-300">Shop</a>
    <a href="#" class="text-gray-600 hover:text-blue-900 transition duration-300">About</a>
    <a href="#" class="text-gray-600 hover:text-blue-900 transition duration-300">Contact</a>
</div>
```
Replace "Shop", "About", and "Contact" with your desired menu items.

### Hero Section
The main banner section contains:

1. **Main Heading**
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Discover Cute Nautical Jewelry for Every Adventure
</h1>
```
Update the text between the `<h1>` tags.

2. **Subheading**
```html
<p class="text-xl md:text-2xl mb-8">
    Project Nautica: Where seaside dreams meet timeless style.
</p>
```

### Tailwind CSS Tips
- `md:` prefix means the style applies only on medium screens and larger
- Font sizes use patterns like `text-xl`, `text-2xl`, etc.
- Colors use patterns like `text-blue-900` (darker blue) or `text-blue-100` (lighter blue)
- Spacing uses patterns like `mb-6` (margin-bottom) or `py-4` (padding-top and bottom)

## Managing Links

### Navigation Links
1. Locate the navigation section:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600 hover:text-blue-900 transition duration-300">Shop</a>
```

2. Replace `#` with your actual URL:
```html
<a href="https://yoursite.com/shop" class="text-gray-600 hover:text-blue-900 transition duration-300">Shop</a>
```

### Call-to-Action Buttons
1. Hero section button:
```html
<a href="https://projectnautica.com" 
   class="inline-block bg-white text-blue-900 px-8 py-4 rounded-full">
    Explore Collection
</a>
```
Replace `https://projectnautica.com` with your desired URL.

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-blue-100 hover:text-white transition duration-300">
        <!-- Facebook icon -->
    </a>
```
Replace `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the Quick Links section in the footer:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="text-blue-100 hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-blue-100 hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Add your policy content between them

Example structure:
```html
<!-- privacy.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header from index.html -->
    
    <div class="container mx-auto px-4 py-12">
        <h1 class="text-3xl font-bold mb-6">Privacy Policy</h1>
        <!-- Add your privacy policy content here -->
    </div>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout on Mobile**
   - Check for `md:` prefixes in classes
   - Ensure the viewport meta tag is present:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

2. **Images Not Loading**
   - Verify image URLs are correct
   - Check file paths relative to your HTML file
   - Ensure images are uploaded to your server

3. **Links Not Working**
   - Confirm URLs are correct and complete
   - Check for typos in `href` attributes
   - Test links in different browsers

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Check for console errors in developer tools

Remember to always test your changes across different devices and browsers before pushing to production.