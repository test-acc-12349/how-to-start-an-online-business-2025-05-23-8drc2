# BusinessNinja Landing Page Maintenance Guide

This guide will help you maintain and customize the BusinessNinja landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">BusinessNinja</a>
```
Simply replace "BusinessNinja" with your desired brand name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
The main headline and subheading can be modified here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 text-gray-900">
    How To Start An Online Business
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Generate your complete business plan in just 3 simple steps
</p>
```

### Tailwind CSS Class Guide
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color

Example of modifying styles:
```html
<!-- Original -->
<div class="bg-white rounded-xl p-8 shadow-lg">

<!-- Modified for darker background and larger padding -->
<div class="bg-gray-100 rounded-xl p-10 shadow-lg">
```

## Fixing Broken Links

### Current Link Structure
1. **Navigation Menu Links:**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://ninja200.online">Get Started</a>
```

To update external links:
1. Locate the `href` attribute
2. Replace `https://ninja200.online` with your desired URL
```html
<!-- Example -->
<a href="https://your-domain.com">Get Started</a>
```

### Internal Links
Internal links use hashtags (#) to navigate to sections:
```html
<!-- Section ID -->
<section id="features">

<!-- Link to section -->
<a href="#features">Features</a>
```

Ensure each section ID matches its corresponding link.

## Linking Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- IDs are case-sensitive
```html
<!-- Correct -->
<section id="features">
<a href="#features">

<!-- Wrong -->
<section id="Features">
<a href="#features">
```

2. **Responsive Design Issues**
- Ensure you maintain the responsive classes:
  - `md:` prefix for medium screens
  - `lg:` prefix for large screens
```html
<!-- Example of responsive classes -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```

3. **Social Media Icons Not Showing**
- Verify the Boxicons CSS is properly loaded:
```html
<link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
```
- Check icon class names match exactly:
```html
<i class='bx bxl-twitter'></i>
```

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation for class references
2. Verify all external resources are loading properly
3. Use browser developer tools (F12) to inspect elements
4. Ensure all changes maintain the responsive design structure

Remember to test your changes across different screen sizes to maintain the responsive design.