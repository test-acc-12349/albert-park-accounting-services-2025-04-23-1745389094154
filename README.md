# Albert Park Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:

```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park
</div>
```

To update:
1. Change "Albert Park" to your company name
2. Modify gradient colors by changing `from-purple-500` and `to-pink-500` to different colors (e.g., `from-blue-500` to `to-green-500`)

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park accounting services
</h1>
<p class="text-xl md:text-2xl lg:text-3xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Your financial success is our bottom line
</p>
```

To update:
1. Replace headline text between `<h1>` tags
2. Update subheading text between `<p>` tags
3. Text sizes use responsive classes:
   - `text-4xl`: Default size
   - `md:text-5xl`: Medium screens
   - `lg:text-7xl`: Large screens

### Services Section
Each service card follows this structure:

```html
<div class="bg-gray-800 rounded-2xl p-8 hover:scale-105 transform transition duration-300 shadow-xl hover:shadow-purple-500/20">
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-xl mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Tax Optimization</h3>
    <p class="text-gray-400">Strategic tax planning and optimization...</p>
</div>
```

To update:
1. Change service title between `<h3>` tags
2. Update description between `<p>` tags
3. Modify hover effect by changing `hover:scale-105` value
4. Adjust padding with `p-8` class (e.g., `p-6` for less padding)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Keep the `#` prefix
   - Match the `id` of the target section
   - Example: `href="#services"` jumps to `<section id="services">`

2. External links:
   - Replace `href="#"` with full URL
   - Example: `href="https://your-website.com/about"`

### Call-to-Action Buttons
Current CTA link:

```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 text-lg font-semibold bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
    Get Started Today
</a>
```

To update:
1. Replace `https://theaccountants.com` with your actual URL
2. Update button text between `<a>` tags
3. Maintain the classes for consistent styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To update:
1. Replace `href="#"` with actual page links:
   ```html
   <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

2. Ensure privacy.html and terms.html exist in the same directory
3. Maintain the hover effect classes for consistent styling

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Verify that section `id` attributes match href values
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check media query classes (md:, lg:)
   - Test on different screen sizes
   - Common classes:
     - `md:`: 768px and up
     - `lg:`: 1024px and up

3. **Gradient Colors Not Showing**
   - Ensure both `from-` and `to-` colors are specified
   - Verify `bg-gradient-to-r` or `bg-gradient-to-br` is present
   - Check that `bg-clip-text` and `text-transparent` are used together for text gradients

Remember to:
- Always backup before making changes
- Test all links after updating
- View changes on multiple devices
- Validate HTML code after modifications

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).