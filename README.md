# DiferenciasEntre Landing Page - Maintenance Guide

This guide will help you maintain and customize the DiferenciasEntre landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Navigation Links](#managing-navigation-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- Call to Action
- Footer

### Updating Text Content

#### Hero Section
Located near the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-8">
    Diferencias Entre Conceptos y Términos Explicadas de Forma Clara
</h1>
```
To modify:
1. Locate this `<h1>` tag
2. Replace the text between the tags
3. Maintain the existing classes to preserve styling

#### Features Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Comparaciones Claras</h3>
    <p class="text-gray-600">Explicaciones detalladas y fáciles de entender...</p>
</div>
```
To modify:
1. Find the feature card you want to update
2. Change the text in the `<h3>` and `<p>` tags
3. Keep all class attributes unchanged

### Tailwind CSS Classes Explained

#### Responsive Design Classes
Example from the navigation:
```html
<div class="hidden md:flex space-x-8">
```
- `hidden`: Hides element by default
- `md:flex`: Shows element as flex container on medium screens and larger
- `space-x-8`: Adds horizontal spacing between child elements

#### Common Style Classes
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`
- Colors: `text-gray-600`, `text-blue-600`, `bg-white`
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Hover effects: `hover:text-blue-600`, `hover:bg-blue-700`

## Managing Navigation Links

### Internal Navigation Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#caracteristicas" class="text-gray-600 hover:text-blue-600">Características</a>
    <a href="#beneficios" class="text-gray-600 hover:text-blue-600">Beneficios</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="#contacto" class="text-gray-600 hover:text-blue-600">Contacto</a>
</div>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute
3. Update the link text between the `<a>` tags
4. Repeat in the mobile menu section below

### External Links
Example of external link:
```html
<a href="https://diferenciasentre.net/" class="inline-block bg-blue-600 text-white...">
```
To update:
1. Replace the URL in the `href` attribute
2. Ensure the URL includes `https://` or `http://`

## Adding Privacy and Terms Pages

### Footer Links Setup
Current footer link structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Términos de Uso</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Política de Privacidad</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Términos de Uso</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Navigation Links**
   - Verify that section IDs match the href attributes
   - Check for typos in IDs and href values
   - Ensure section IDs are unique

2. **Responsive Design Issues**
   - Test on different screen sizes using browser dev tools
   - Verify Tailwind breakpoint classes (sm:, md:, lg:) are correct
   - Check for conflicting responsive classes

3. **Style Inconsistencies**
   - Maintain consistent color classes (e.g., text-blue-600)
   - Keep spacing consistent using Tailwind's spacing utilities
   - Use the same hover effects across similar elements

### Need Help?
If you encounter issues:
1. Check the browser's developer console (F12) for errors
2. Verify all required files are properly linked
3. Ensure Tailwind CSS and Alpine.js CDN links are accessible
4. Test the page in multiple browsers

Remember to always backup your files before making significant changes, and test all modifications thoroughly before deploying to production.