# PolicyPals Landing Page Maintenance Guide

This guide will help you maintain and customize the PolicyPals landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header and Navigation
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-purple-400">PolicyPals</a>
```
To change the logo text, simply replace "PolicyPals" with your desired text.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Discover Your Ideal Policy with PolicyPals.co.uk
</p>
```
Update these text elements to change your main headline and subheading.

#### Features Section
Each feature card follows this structure:
```html
<h3 class="text-xl font-semibold mb-4">Personalised Policy Matching</h3>
<p class="text-gray-400 leading-relaxed">
    Advanced algorithms match you with tailored insurance policies...
</p>
```
Modify the `<h3>` and `<p>` content to update feature descriptions.

### Tailwind CSS Classes

#### Understanding Responsive Classes
- `md:` prefix applies styles on medium screens and up
- `lg:` prefix applies styles on large screens and up
Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Medium screens: text-5xl (3rem)
- Large screens: text-6xl (3.75rem)

#### Common Class Modifications

**Colors:**
```html
<!-- Current purple button -->
<button class="bg-purple-500 hover:bg-purple-600 text-white">
```
To change colors, replace:
- `bg-purple-500` with other colors like `bg-blue-500`
- `hover:bg-purple-600` with matching hover state

**Spacing:**
```html
<div class="px-6 py-4"> <!-- padding: x-axis 1.5rem, y-axis 1rem -->
<div class="mb-8">      <!-- margin-bottom: 2rem -->
```

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

To update internal links:
1. Locate the section ID you want to link to (e.g., `id="features"`)
2. Use `#section-id` in the href attribute
3. Example: `<a href="#features">Features</a>`

For external links:
```html
<!-- Example of adding an external link -->
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
    External Link
</a>
```

### Checking All Links
Current link locations:
1. Navigation menu (header)
2. Mobile menu
3. Footer quick links
4. Footer legal links
5. Contact email link

## 3. Linking Privacy and Terms Pages

### Footer Legal Links Section
Current structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-purple-400">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-purple-400">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-purple-400">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating new pages, copy these classes for consistent link styling:
```html
class="hover:text-purple-400 transition-colors duration-300"
```

## Troubleshooting Tips

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Test at different screen sizes using browser dev tools
   - Verify `md:` and `lg:` prefixed classes are working
   - Check mobile menu functionality

3. **Color Inconsistencies**
   - Maintain the purple theme using these color classes:
     - Primary: `text-purple-400`
     - Hover: `hover:text-purple-400`
     - Buttons: `bg-purple-500`

4. **Layout Problems**
   - Ensure container classes remain intact:
     ```html
     <div class="container mx-auto px-6">
     ```
   - Maintain the grid structure in features section:
     ```html
     <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
     ```

Remember to test all changes across different devices and browsers before deploying to production.