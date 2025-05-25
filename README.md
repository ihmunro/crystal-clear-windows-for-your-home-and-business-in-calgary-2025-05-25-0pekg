# Crystal Clear Windows Landing Page - Maintenance Guide

This guide will help you maintain and customize the Crystal Clear Windows landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-teal-400 bg-clip-text text-transparent">
    Crystal Clear <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a> <!-- Update text here -->
    <a href="#benefits">Benefits</a> <!-- Update text here -->
    <a href="#faq">FAQ</a> <!-- Update text here -->
    <a href="#contact">Contact</a> <!-- Update text here -->
</div>
```

### Hero Section
To modify the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Crystal Clear Windows for Your Home and Business in Calgary
    <!-- Update this headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Reliable Window Services for a Crystal Clear View
    <!-- Update this subheading -->
</p>
```

### Tailwind CSS Class Guide
Common classes used in this template:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-100`, `text-gray-300`, `text-gray-400`
- Spacing: `px-6`, `py-4`, `mt-12`, `mb-8`
- Flex layout: `flex`, `items-center`, `justify-between`
- Responsive design: `md:text-xl`, `lg:text-6xl`

## Managing Links

### Internal Navigation Links
All section links use IDs. To update:

1. Locate the section ID:
```html
<section id="services" class="py-24 bg-gray-800">
```

2. Update corresponding navigation link:
```html
<a href="#services" class="text-gray-300 hover:text-white">Services</a>
```

### External Links
The main call-to-action buttons link to the business website:

```html
<!-- Update this URL for all CTA buttons -->
<a href="https://calgaryswindowcleaners.com" class="px-8 py-4 bg-gradient-to-r">
```

### Quick Link Checklist
- [ ] Navigation menu links
- [ ] CTA buttons (Get Quote, Get Started)
- [ ] Footer quick links
- [ ] Contact information
- [ ] Social media links (if added)

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all `href` attributes start with `#` for internal links
   - Verify external URLs include `https://`
   - Ensure section IDs match their corresponding links

2. **Responsive Design Issues**
   - Mobile menu is hidden by default (`hidden md:flex`)
   - Check responsive classes start with proper breakpoints (`md:`, `lg:`)
   - Test on different screen sizes using browser dev tools

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-blue-400 to-teal-400 bg-clip-text text-transparent
     ```

### Need Help?
- Double-check HTML syntax and closing tags
- Verify Tailwind CSS CDN link is working
- Test all links before deploying changes
- Use browser developer tools to inspect elements

Remember to always backup your files before making significant changes, and test your updates across different browsers and devices.