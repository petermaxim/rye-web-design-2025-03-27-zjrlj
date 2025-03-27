# Rye Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Rye Web Design landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu:

```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
    <a href="/" class="text-2xl font-bold text-blue-600">Rye Web Design</a>
</header>
```

To update:
1. Change company name: Replace "Rye Web Design" with your business name
2. Modify color: Change `text-blue-600` to other colors (e.g., `text-red-600`, `text-green-600`)

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Small Business Service Websites in Rye
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8 max-w-3xl mx-auto">
    Professional web design services tailored for local businesses
</p>
```

To update:
1. Change heading: Replace text between `<h1>` tags
2. Update subheading: Modify text in the `<p>` tag
3. Adjust text size:
   - `text-4xl`: Default size
   - `md:text-5xl`: Medium screen size
   - `lg:text-6xl`: Large screen size

### Features Section
Four feature cards with icons and descriptions:

```html
<div class="p-6 bg-white rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-2">Custom Design</h3>
    <p class="text-gray-600">Unique, professional designs tailored to your brand identity</p>
</div>
```

To update:
1. Change feature title: Modify text in `<h3>` tags
2. Update description: Change text in `<p>` tags
3. Modify styling:
   - `shadow-lg`: Box shadow intensity
   - `rounded-xl`: Corner roundness
   - `p-6`: Padding size

## Managing Links

### Navigation Menu Links
Located in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
</div>
```

To update:
1. Internal links: Keep `#` followed by section ID (e.g., `#features`)
2. External links: Replace with full URL (e.g., `https://example.com`)
3. Update text: Change link text between `<a>` tags

### Call-to-Action Links
Currently pointing to `get.zippsites.com`:

```html
<a href="get.zippsites.com" class="inline-flex items-center px-8 py-4 border border-transparent">
    Start Your Project
</a>
```

To update:
1. Replace `get.zippsites.com` with your signup/contact page URL
2. Add `https://` for external links
3. Use relative paths (`/contact`) for internal pages

## Adding Privacy and Terms Pages

### Footer Links Setup
Located in the footer section:

```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update links in footer:
   ```html
   <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for missing `https://` in external URLs
   - Verify internal link IDs match section IDs
   - Ensure file paths are correct for internal pages

2. **Styling Problems**
   - Tailwind classes must be exact matches
   - Check for missing responsive prefixes (`md:`, `lg:`)
   - Verify all closing tags are present

3. **Layout Issues**
   - Maintain grid structure in features section
   - Keep responsive classes for proper mobile display
   - Don't remove container classes (`max-w-7xl mx-auto`)

### Need Help?
- Double-check HTML structure
- Verify all changes against original code
- Test on multiple screen sizes
- Keep backup copies before making changes

Remember to test all changes in a development environment before pushing to production.