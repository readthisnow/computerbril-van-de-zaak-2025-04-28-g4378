# Landing Page Maintenance Guide

This guide will help you maintain and customize the ComputerBril landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## 1. Updating Text and Tailwind CSS Classes

### Hero Section Updates
The main hero section is located at the top of the page and contains the primary headline:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-gray-900 leading-tight mb-8">
    Computerbril Van De Zaak
    <span class="block text-blue-600 mt-2">Nu 20% Korting!</span>
</h1>
```

To modify:
1. Change the text between the `<h1>` tags to update the main headline
2. Modify the blue promotional text within the `<span>` element
3. The existing classes control:
   - `text-4xl`: Base text size
   - `sm:text-5xl`: Text size on small screens
   - `lg:text-6xl`: Text size on large screens
   - `font-extrabold`: Text weight
   - `text-gray-900`: Text color

### Feature Cards
Located in the "features" section, each card follows this structure:

```html
<div class="p-6 bg-white rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-2">Hoogwaardige Kwaliteit</h3>
    <p class="text-gray-600">Nog maar enkele exemplaren beschikbaar...</p>
</div>
```

To modify:
1. Locate the feature cards in the `features` section
2. Update the `<h3>` text for the feature title
3. Modify the `<p>` text for the feature description
4. Keep the existing classes to maintain consistent styling

### Important CSS Classes Reference
- Text colors:
  - `text-gray-900`: Dark text
  - `text-gray-600`: Secondary text
  - `text-blue-600`: Accent blue
  - `text-white`: White text
- Spacing:
  - `px-4`: Horizontal padding
  - `py-4`: Vertical padding
  - `mb-8`: Bottom margin
- Layout:
  - `container`: Centers content
  - `mx-auto`: Horizontal auto margins
  - `grid`: Grid layout
  - `flex`: Flexbox layout

## 2. Fixing Broken Links

### Navigation Menu Links
The navigation menu contains internal page links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#voordelen" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with the corresponding ID
3. Example: `href="#new-section-id"`
4. Ensure the target section has a matching `id` attribute

### Call-to-Action Links
The main CTA buttons currently point to:
```html
<a href="https://computerbril.org/winkel" class="inline-flex items-center px-8 py-4...">
```

To update:
1. Locate all instances of `https://computerbril.org/winkel`
2. Replace with your desired URL
3. Test the link after updating

## 3. Linking Privacy and Terms Pages

### Footer Link Updates
The footer contains placeholder privacy and terms links:

```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html pages
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting Tips

1. Broken Internal Links
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Remove any spaces in IDs

2. Responsive Design Issues
- Don't remove `sm:`, `md:`, or `lg:` prefixes from classes
- Keep the mobile-first approach intact
- Test all changes across different screen sizes

3. Style Inconsistencies
- Copy existing class combinations for new elements
- Maintain color scheme using provided color classes
- Keep spacing consistent using existing margin/padding classes

## Need Help?

If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all IDs and classes are spelled correctly
3. Ensure all HTML tags are properly closed
4. Test on multiple browsers and devices
5. Maintain backup copies before making significant changes

Remember to test all changes thoroughly before pushing to production, especially navigation links and contact information.