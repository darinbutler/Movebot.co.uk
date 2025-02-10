# MoveBot Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the MoveBot landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Name/Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">MoveBot</a>
```
- Replace "MoveBot" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-[color]-[shade])

2. **Navigation Menu Items**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
```
- Update text between `>` and `</a>`
- Maintain the same class structure for consistent styling

### Hero Section
Located at the top of the page with main heading and buttons:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Cloud Migration & Backup For Google & Microsoft
</h1>
```
- Update heading text between the `<h1>` tags
- Responsive sizes:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-cloud-upload-alt text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Cloud Migration</h3>
    <p class="text-gray-600">Seamless transfer of your data between cloud platforms with zero downtime.</p>
</div>
```
To modify:
1. Change icon: Update `fa-cloud-upload-alt` with any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading: Modify text in `<h3>` tags
3. Update description: Change text in `<p>` tags

## Managing Links

### Navigation Links
Current links in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="http://www.movebot.co.uk">Get Started</a>
</div>
```

To update:
1. Internal links (starting with #): Point to section IDs on the page
2. External links: Replace full URL in `href`
3. Verify all links work by testing each one

### Call-to-Action (CTA) Links
Located in hero and CTA sections:
```html
<a href="http://www.movebot.co.uk" class="bg-blue-600 text-white px-8 py-4 rounded-full">
    Start Migration
</a>
```
- Update `href` with your application or signup URL
- Test the link thoroughly before deploying

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the footer section:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check for typos in `href` attributes
- Ensure file names match exactly
- Verify file locations are correct

2. **Styling Problems**
- Make sure Tailwind CSS CDN is loading:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check for missing classes
- Verify responsive classes (md:, lg:) are properly formatted

3. **Icons Not Showing**
- Confirm Font Awesome CDN is loading:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```
- Check icon class names against Font Awesome documentation

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check the [Font Awesome icon library](https://fontawesome.com/icons)
- Test all changes in multiple browsers
- Use browser developer tools (F12) to inspect elements

Remember to always backup your files before making changes and test thoroughly on a development environment before pushing to production.