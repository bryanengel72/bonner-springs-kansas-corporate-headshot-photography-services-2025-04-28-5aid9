# 101Headshots Landing Page Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections for Text Updates

#### Header Logo
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">101Headshots</a>
```
To update the logo text, simply replace "101Headshots" with your desired text.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Bonner Springs, Kansas Corporate Headshot Photography Services
</h1>
```
- Replace the heading text while maintaining the HTML structure
- The text scales responsively due to the `text-4xl md:text-5xl lg:text-6xl` classes
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

#### Features Cards
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:scale-105 transition-transform duration-300 shadow-xl">
    <h3 class="text-xl font-semibold mb-4">Skill Shots</h3>
    <p class="text-gray-400">Capture your professional expertise...</p>
</div>
```
To update:
1. Locate the feature card you want to modify
2. Change the `<h3>` title text
3. Update the description in the `<p>` tag

### Understanding Key Tailwind Classes

#### Responsive Design Classes
- `container mx-auto`: Centers content and sets max-width
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `md:grid-cols-3`: Creates 3 columns on medium screens
- `space-x-8`: Adds horizontal spacing between elements

#### Color and Style Classes
- `bg-gray-900`: Dark background
- `text-gray-100`: Light text
- `hover:scale-105`: Enlarges element on hover
- `rounded-2xl`: Rounds corners
- `shadow-xl`: Adds shadow effect

## Fixing Broken Links

### Current Navigation Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="px-6 py-2 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full">Contact Us</a>
</div>
```

To update navigation links:
1. Locate the `href` attribute
2. Replace the value with:
   - `#section-id` for same-page links
   - `./page.html` for internal pages
   - `https://website.com` for external links

### Book Session Link
```html
<a href="https://www.101headshots.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full">
    Book Your Session
</a>
```
Replace the placeholder URL with your actual booking page URL.

## Linking Privacy and Terms Pages

### Current Footer Links Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the footer links:
```html
<li><a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Gradients**
   - Ensure all gradient classes include both `from-` and `to-` values
   - Example: `bg-gradient-to-r from-purple-500 to-pink-500`

2. **Responsive Issues**
   - Check mobile preview in browser dev tools
   - Verify media query classes (md:, lg:) are properly set
   - Test different screen sizes

3. **Missing Styles**
   - Confirm Tailwind CDN is properly loaded
   - Check for typos in class names
   - Ensure classes are space-separated

4. **Link Issues**
   - Verify file paths are correct
   - Use `./` for same-directory files
   - Include `https://` for external links

Remember to:
- Test all changes in multiple browsers
- Validate links after updates
- Keep backup copies of working code
- Maintain consistent styling across pages