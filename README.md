# Landing Page Maintenance Guide

This guide will help you maintain and customize your WebAgency landing page. Follow these detailed instructions to make common updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-white">Web<span class="text-blue-500">Agency</span></a>
```
- Change "Web" and "Agency" to your brand name
- Keep the `<span>` tag to maintain the two-tone effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Maintain the class structure for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Best Web Agency In Sydney</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Grow your business with clicks</p>
```
- Update heading and subheading text
- Keep responsive classes (`md:`, `lg:`) for proper scaling

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-300`, `bg-blue-600`
- Spacing: `mb-6`, `py-24`, `px-6`
- Responsive: `md:text-4xl`, `lg:text-6xl`

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. For internal sections: Use `#section-id`
2. For external pages: Use full URL
   ```html
   <a href="https://yoursite.com/about">About</a>
   ```

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://fixrr.online" class="inline-block px-8 py-4 bg-blue-600">
```
Replace `https://fixrr.online` with your desired URL

### Footer Links
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Services</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Blog</a></li>
</ul>
```
Replace `#` with actual page URLs

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
In the footer section, locate:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
</ul>
```
Update to:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```

### Adding Terms of Service Link
Similarly, update:
```html
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Best Practices
1. Create matching `privacy.html` and `terms.html` files
2. Use relative paths for internal pages
3. Maintain consistent styling classes
4. Test links after updating

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - Verify proper hashtag (#) usage

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes
   - Keep the original responsive class structure
   - Test on multiple screen sizes

3. **Style Inconsistencies**
   - Copy existing Tailwind classes for new elements
   - Maintain color scheme (`blue-600`, `gray-900`, etc.)
   - Keep spacing consistent with surrounding elements

### Need Help?
- Check Tailwind CSS documentation for class references
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to back up your files before making significant changes, and always test your updates in a development environment first.