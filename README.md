# DharaMitra Landing Page - Maintenance Guide

This guide will help you maintain and customize the DharaMitra landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Key Sections for Text Updates

#### 1. Announcement Bar
```html
<div class="bg-green-600 text-white text-center py-2 text-sm">
    <p>Fast Worldwide Shipping (5 days delivery) 🚚</p>
</div>
```
To modify the announcement:
- Locate this section at the top of the body
- Change the text between the `<p>` tags
- Keep the message brief and include emojis if desired

#### 2. Hero Section
```html
<div class="max-w-4xl mx-auto text-center text-white">
    <h1 class="text-4xl md:text-6xl font-bold mb-6">DharaMitra(Trichoderma viride) is a biocontrol fungus that protects crops</h1>
    <p class="text-xl md:text-2xl mb-8">Biocontrol Fungus Containing Trichoderma Viride</p>
</div>
```
To update the hero section:
- Change the main heading between the `<h1>` tags
- Modify the subheading in the `<p>` tags
- Maintain the existing class structure for responsive design

### Understanding Tailwind Classes

Key class patterns used throughout the page:

1. Spacing Classes:
   - `px-4`: Horizontal padding
   - `py-24`: Vertical padding
   - `mb-6`: Margin bottom
   - `space-x-6`: Horizontal spacing between elements

2. Typography Classes:
   - `text-sm`: Small text
   - `text-xl`: Extra large text
   - `font-bold`: Bold text
   - `text-center`: Centered text

3. Color Classes:
   - `bg-green-600`: Green background
   - `text-white`: White text
   - `hover:text-green-500`: Green text on hover

To modify styling:
```html
<!-- Original -->
<div class="bg-green-600 text-white px-6 py-2">

<!-- To change colors -->
<div class="bg-blue-600 text-white px-6 py-2">

<!-- To adjust spacing -->
<div class="bg-green-600 text-white px-8 py-4">
```

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-6">
    <a href="#features" class="hover:text-green-600 transition-colors">Features</a>
    <a href="#benefits" class="hover:text-green-600 transition-colors">Benefits</a>
    <a href="#faq" class="hover:text-green-600 transition-colors">FAQ</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. Ensure it matches the corresponding section ID
3. Section IDs are prefixed with `#`

### WhatsApp Button Links
```html
<a href="https://wa.me/917032666266?text=Dharamitra" class="bg-green-600 text-white px-6 py-2 rounded-full">
    Buy Now
</a>
```

To update WhatsApp links:
1. Replace the phone number in the URL
2. Modify the default message in the `text=` parameter
3. Test the link on mobile devices

## Adding Policy Pages

### Footer Policy Links
```html
<div>
    <h4 class="text-xl font-bold mb-4">Policies</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-green-500">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-green-500">Terms of Service</a></li>
        <li><a href="#" class="hover:text-green-500">Shipping Policy</a></li>
    </ul>
</div>
```

To link policy pages:
1. Create your policy HTML files (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-green-500">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-green-500">Terms of Service</a></li>
```

### Creating Matching Policy Pages
Create new HTML files with consistent styling:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - DharaMitra</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="font-sans antialiased">
    <!-- Copy the header from index.html -->
    
    <!-- Add your policy content here -->
    <div class="container mx-auto px-4 py-24">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add policy content -->
    </div>

    <!-- Copy the footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues and Solutions:

1. Broken Internal Links
   - Verify that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. Responsive Design Issues
   - Check mobile-specific classes (prefixed with `md:`)
   - Test different screen sizes using browser developer tools
   - Maintain the responsive class structure when making changes

3. Social Media Links
   - Update all placeholder `#` links in the footer
   - Ensure icons display correctly by checking Font Awesome classes
   - Test all social media links before deploying

Remember to:
- Always backup your files before making changes
- Test all modifications in multiple browsers
- Validate your HTML using W3C Validator
- Check mobile responsiveness on real devices when possible