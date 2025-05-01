# Landing Page Maintenance Guide

This guide will help you maintain and customize your ParisWeb landing page. Follow these detailed instructions to make common updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Locate this line in the header:
```html
<a href="/" class="text-2xl font-bold text-gray-800">Paris<span class="text-blue-600">Web</span></a>
```
- Change "Paris" and "Web" to your desired text
- Keep the `<span>` tag to maintain the blue color on the second word

2. **Navigation Menu Items**: Find the navigation div:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `>` and `</a>` for each menu item
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Websites In Paris
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10 leading-relaxed">
    Custom Websites For Your Business
</p>
```
- Update heading and subheading text as needed
- Maintain the existing classes for responsive design:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Tailwind CSS Classes Explained
Common classes used throughout:
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `text-gray-600`: Sets text color
- `hover:text-blue-600`: Changes text color on hover
- `transition-colors`: Enables smooth color transitions
- `duration-300`: Sets transition duration to 300ms

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Locate the section you want to link to
2. Match the `href` value with the section's `id` attribute
3. Example: To link to the FAQ section, ensure it has `id="faq"`:
```html
<section id="faq" class="py-24 bg-white">
```

### Call-to-Action Links
Currently pointing to "https://sigmaseo.io":
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600...">
```
To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test the link to ensure it works
3. Keep all classes to maintain button styling

## Adding Privacy and Terms Pages

### Footer Link Setup
Current placeholder links in footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the `container` class on parent elements
- Maintain the existing responsive grid classes

3. **Style Changes Not Working**
- Verify Tailwind CDN link is present in `<head>`
- Check for typos in class names
- Ensure classes are space-separated

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all HTML tags are properly closed
3. Ensure all required classes remain intact
4. Test on multiple devices and browsers

Remember to always backup your files before making changes, and test thoroughly after each modification.