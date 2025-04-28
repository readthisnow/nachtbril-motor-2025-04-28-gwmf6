# Night Vision Glasses Landing Page - Maintenance Guide

This guide will help you maintain and customize the Night Vision Glasses landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">Nachtbril Motor</a>
```
- Replace "Nachtbril Motor" with your desired text
- The `text-2xl` class controls size (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
- `font-bold` controls text weight (options: font-normal, font-medium, font-semibold, font-bold)

### Hero Section
The main banner section contains your primary message:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8 leading-tight">
    Nachtbril Motor<br>
    <span class="text-blue-600">Tijdelijk 20% KORTING</span>
</h1>
```
- Update both lines of text while keeping the `<br>` and `<span>` tags
- The blue discount text is controlled by `text-blue-600` (change number 600 to 500-900 for different shades)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Verbeterd Nachtzicht</h3>
    <p class="text-gray-600">Nog maar 3 brillen beschikbaar...</p>
</div>
```
To add a new feature:
1. Copy the entire `<div>` block
2. Paste it within the `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8` container
3. Update the heading and paragraph text
4. Maintain the class structure for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag you want to change
2. Modify the `href` attribute:
   - For internal sections, use `#section-id`
   - For external pages, use the full URL (e.g., `https://example.com`)
3. Update the link text between the opening and closing tags

### Call-to-Action Buttons
There are two main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://nachtbril.com/shop" class="inline-block bg-blue-600 text-white text-lg px-8 py-4 rounded-full">
    Bestel Nu Met 20% Korting
</a>

<!-- Bottom section button -->
<a href="https://nachtbril.com/shop" class="inline-block bg-white text-blue-600 text-lg px-8 py-4 rounded-full">
    Profiteer Nu Van 20% Korting
</a>
```
- Update the `href` attributes to your actual shop URL
- Maintain the class structure for consistent styling

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the footer links section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

To link to policy pages:
1. Create your privacy.html and terms.html files in the same directory as index.html
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms & Conditions</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't work if the section ID is `id="features"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes

3. **Missing Styles**
   - Verify the Tailwind CSS CDN link is present in the head section
   - Check for typos in class names (Tailwind classes must be exact)

4. **Button Styling Problems**
   - Keep all classes on CTA buttons to maintain hover effects and transitions
   - The `transform` and `transition` classes work together for hover animations

### Need Help?
- Double-check all changes against the original code
- Use browser developer tools (F12) to inspect elements
- Maintain the existing class structure when making changes
- Test all changes on multiple screen sizes

Remember to backup your files before making significant changes!