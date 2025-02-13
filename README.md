# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line:
```html
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
Simply replace "TWD" with your desired text.

2. **Navigation Links**: Locate the navigation section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other navigation items -->
</div>
```
To modify link text, change the text between `<a>` tags.

### Hero Section
Find the hero section starting with:
```html
<section class="pt-32 pb-24 bg-gradient-to-r from-blue-50 to-indigo-50">
```

To update:
1. Main heading: Replace "Texas Web Design"
2. Subheading: Replace "Best Websites In Texas"
3. Button text: Modify "Get Started" or "Learn More"

### Tailwind CSS Class Guide
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `bg-[color]`: Sets background color (e.g., `bg-blue-600`)
- `text-[color]`: Sets text color (e.g., `text-gray-600`)
- `p-[size]`: Sets padding (e.g., `p-8`)
- `m-[size]`: Sets margin (e.g., `mb-4`)

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="...">Get Started</a>
```

3. Social Media Links (in footer):
```html
<a href="#" class="..."><i class="fab fa-twitter text-xl"></i></a>
```

### Updating Links
1. To update internal links (sections on the same page):
   - Keep the `#` symbol
   - Match the ID of the section you're linking to
   - Example: `href="#features"` links to `<section id="features">`

2. To update external links:
   - Replace placeholder URLs
   - Example: Change `https://twd.com` to your actual website URL
   - For social media, replace `#` with actual profile URLs

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Privacy and Terms Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section IDs match href attributes
   - Check for typos in IDs
   - Ensure IDs are unique

2. **Responsive Design Issues**
   - Check mobile display using browser dev tools
   - Verify `md:` breakpoint classes are correct
   - Test different screen sizes

3. **Icon Display Problems**
   - Confirm Font Awesome CSS is properly loaded
   - Check icon class names against Font Awesome documentation
   - Verify internet connection for CDN access

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all CDN links are accessible
3. Test the page in multiple browsers
4. Ensure all HTML tags are properly closed

Remember to always backup your files before making changes!