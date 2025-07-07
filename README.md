# XStreamFlex Landing Page Maintenance Guide

This guide will help you maintain and customize the XStreamFlex landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-xl font-bold tracking-tighter">XStreamFlex</a>
```
Simply replace "XStreamFlex" with your brand name.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tighter mb-8">
    The Ultimate Idea Launch Pad
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Launch your business in 3 days or less
</p>
```

To modify:
1. Replace the h1 text for your main headline
2. Update the paragraph text for your subheading
3. The responsive text sizes are controlled by:
   - `text-4xl`: Mobile size
   - `md:text-5xl`: Tablet size
   - `lg:text-6xl`: Desktop size

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 p-8 rounded-xl hover:shadow-2xl transition-all duration-300">
    <div class="text-indigo-500 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description</p>
</div>
```

To update:
1. Change the feature title in the `<h3>` tag
2. Modify the description in the `<p>` tag
3. Key styling classes:
   - `bg-gray-900`: Background color
   - `p-8`: Padding
   - `rounded-xl`: Border radius
   - `hover:shadow-2xl`: Hover effect

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://join.xstreamflex.com">Get Started</a>
```

To update:
1. Internal links (starting with #) point to section IDs
2. External links (starting with https://) point to other websites
3. Replace `https://join.xstreamflex.com` with your actual signup URL

### Call-to-Action Buttons
Located in hero and final sections:
```html
<a href="https://join.xstreamflex.com" class="inline-block px-8 py-4 text-lg font-semibold bg-indigo-600 hover:bg-indigo-700 rounded-lg">
    Start Your Journey
</a>
```

Update the `href` attribute with your desired URL.

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to policy pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query classes (md: and lg: prefixes)
   - Test all screen sizes

3. **Style Conflicts**
   - Tailwind classes should be in the correct order
   - More specific classes should come later
   - Check for duplicate classes

### Need Help?
If you encounter issues:
1. Verify all changes against the original code
2. Test in multiple browsers
3. Contact support at support@xstreamflex.com

Remember to always backup your files before making changes, and test all modifications in a development environment first.