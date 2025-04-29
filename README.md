# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Written for beginners, it provides step-by-step instructions for common updates and modifications.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text (TWD)**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Creating stunning, high-performance websites...</p>
```
- Update heading and paragraph text as needed
- `md:` and `lg:` prefixes control responsive sizing
- `mb-6` controls bottom margin (options: mb-2, mb-4, mb-8, etc.)

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg">
    <div class="w-16 h-16 bg-blue-100 rounded-full">
        <i class="fas fa-server text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```
To modify:
1. Change icon: Replace `fa-server` with any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading: Modify the h3 text
3. Update description: Change the paragraph text
4. Adjust colors: Modify `bg-blue-100` and `text-blue-600`

## Managing Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure section IDs match exactly
2. External links:
   - Replace `#` with full URL
   - Example: `href="https://example.com/features"`

### Call-to-Action Buttons
Located in hero and CTA sections:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```
- Replace `https://twd.com` with your actual URL
- Test links after updating

### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#faq">FAQ</a></li>
</ul>
```
- Update href attributes to match your navigation structure
- Ensure consistency with main navigation links

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:
```html
<!-- Original code -->
<li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>

<!-- Updated code -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match exactly
- Example: `href="#features"` must match `id="features"`
- IDs are case-sensitive

2. **Responsive Design Issues**
- Check mobile view using browser dev tools
- Ensure `md:` and `lg:` classes are properly set
- Common responsive prefixes:
  - `sm:` (640px and up)
  - `md:` (768px and up)
  - `lg:` (1024px and up)

3. **Icon Not Displaying**
- Verify Font Awesome CDN link in header
- Check icon class names against Font Awesome documentation
- Ensure proper class syntax: `fas fa-[icon-name]`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test responsiveness across different devices

Remember to always test your changes across different browsers and screen sizes before deploying to production.