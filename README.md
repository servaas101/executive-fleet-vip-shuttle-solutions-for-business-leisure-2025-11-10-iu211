# Pogiso Tours Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the Pogiso Tours executive transportation landing page. Whether you're updating content, fixing links, or adding new pages, we'll walk you through each step with clear instructions and examples.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Working with Tailwind CSS Classes](#working-with-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Mobile Responsiveness](#mobile-responsiveness)
8. [Common Customizations](#common-customizations)
9. [Troubleshooting](#troubleshooting)

---

## Getting Started

### What You'll Need

- **A text editor**: We recommend free options like:
  - [Visual Studio Code](https://code.visualstudio.com/) (recommended)
  - [Notepad++](https://notepad-plus-plus.org/)
  - [Sublime Text](https://www.sublimetext.com/)

- **Basic file management**: Know how to save `.html` files on your computer

- **A web browser**: Chrome, Firefox, Safari, or Edge to preview changes

### How to Open and Edit Files

1. **Open your text editor**
2. **Go to File → Open** and select your `index.html` file
3. **Make your changes** (we'll show you exactly where!)
4. **Save the file** (Ctrl+S or Cmd+S)
5. **Refresh your browser** to see the changes

---

## Understanding the Page Structure

Your landing page is organized into clear sections. Here's what each section contains:

### Page Sections Overview

```
┌─────────────────────────────────────────┐
│ HEADER / NAVIGATION                     │  (Sticky at top)
├─────────────────────────────────────────┤
│ HERO SECTION                            │  (Main banner with headline)
├─────────────────────────────────────────┤
│ FEATURES SECTION                        │  (3 feature cards)
├─────────────────────────────────────────┤
│ BENEFITS SECTION                        │  (3 benefit cards)
├─────────────────────────────────────────┤
│ ABOUT US SECTION                        │  (Company information)
├─────────────────────────────────────────┤
│ TESTIMONIALS SECTION                    │  (4 client reviews)
├─────────────────────────────────────────┤
│ FAQ SECTION                             │  (Expandable questions)
├─────────────────────────────────────────┤
│ CALL-TO-ACTION SECTION                  │  (Final push to book)
├─────────────────────────────────────────┤
│ CONTACT FORM SECTION                    │  (Newsletter signup)
├─────────────────────────────────────────┤
│ FOOTER                                  │  (Links & copyright)
└─────────────────────────────────────────┘
```

---

## Updating Text Content

### 1. Changing the Page Title and Meta Description

The page title appears in browser tabs and search results. Meta descriptions help with SEO.

**Location**: Top of the file, inside the `<head>` section

**Find this code**:
```html
<meta name="description" content="Executive Fleet & VIP Shuttle Solutions for Business & Leisure - Premium corporate transportation and luxury rides.">
<meta name="keywords" content="executive shuttle, VIP transport, corporate fleet, luxury rides, business travel">
<title>Executive Fleet & VIP Shuttle Solutions | Pogiso Tours</title>
```

**How to update**:
- **Description**: Replace the text after `content="` with your new description (keep it under 160 characters)
- **Keywords**: Update the keywords relevant to your business
- **Title**: Change the title that appears in browser tabs

**Example**:
```html
<meta name="description" content="Premium luxury transportation in Johannesburg - Book executive cars and VIP shuttles now.">
<meta name="keywords" content="luxury cars johannesburg, executive transport, VIP shuttle service">
<title>Luxury Transportation & Executive Cars | Your Company Name</title>
```

---

### 2. Updating the Header/Logo Text

**Location**: Top navigation bar

**Find this code**:
```html
<span class="text-xl font-bold text-black hidden sm:inline" style="font-family: 'Space Grotesk', sans-serif;">Pogiso Tours</span>
```

**How to update**:
Simply replace `Pogiso Tours` with your company name.

**Example**:
```html
<span class="text-xl font-bold text-black hidden sm:inline" style="font-family: 'Space Grotesk', sans-serif;">Elite Transport Co</span>
```

> **Note**: The `hidden sm:inline` classes mean the logo text is hidden on mobile phones but shows on larger screens. This saves space on mobile devices.

---

### 3. Updating the Hero Section Headline

**Location**: Main banner section (the first big section after the header)

**Find this code**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-black mb-6 leading-tight tracking-tight" style="font-family: 'Space Grotesk', sans-serif;">Executive Fleet & VIP Shuttle Solutions for Business & Leisure</h1>
```

**How to update**:
Replace the text between `>` and `</h1>` with your headline.

**Example**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-black mb-6 leading-tight tracking-tight" style="font-family: 'Space Grotesk', sans-serif;">Premium Transportation for Corporate Excellence</h1>
```

---

### 4. Updating the Hero Subheading and Description

**Location**: Just below the hero headline

**Find these codes**:
```html
<p class="text-lg md:text-xl text-gray-700 font-light mb-8 leading-relaxed">Seamless Transfers. Premium Rides. Lasting Impressions.</p>

<p class="text-base md:text-lg text-gray-600 font-light mb-8 leading-relaxed">Experience unparalleled luxury and professionalism with our premium fleet management solutions. Whether you're coordinating executive transportation or planning VIP shuttles for special events, we deliver excellence at every mile.</p>
```

**How to update**:
- **First paragraph**: Your tagline/subheading
- **Second paragraph**: Your main value proposition

**Example**:
```html
<p class="text-lg md:text-xl text-gray-700 font-light mb-8 leading-relaxed">On-Time. Professional. Luxury.</p>

<p class="text-base md:text-lg text-gray-600 font-light mb-8 leading-relaxed">We specialize in providing reliable executive transportation for busy professionals. Our fleet of premium vehicles and experienced drivers ensure you arrive refreshed and ready for success.</p>
```

---

### 5. Updating Feature Cards

**Location**: "Premium Service Features" section (grey background area)

Each feature card has three parts: **icon**, **title**, and **description**.

**Find this structure** (repeated 3 times):
```html
<div class="card-hover bg-white p-8 rounded-lg shadow-md border border-gray-200">
    <div class="w-14 h-14 bg-gradient-to-r from-black to-blue-500 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-clock text-white text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-black mb-3 tracking-tight" style="font-family: 'Space Grotesk', sans-serif;">24/7 Corporate Service</h3>
    <p class="text-gray-700 font-light leading-relaxed">Round-the-clock availability ensures your executive transportation needs are always met...</p>
</div>
```

**How to update**:

1. **Change the icon** (optional):
   - Find the `<i class="fas fa-clock"></i>` line
   - Replace `fa-clock` with another [Font Awesome icon](https://fontawesome.com/icons)
   - Examples: `fa-star`, `fa-car`, `fa-shield-alt`, `fa-headset`

2. **Change the title**:
   - Replace `24/7 Corporate Service` with your feature title

3. **Change the description**:
   - Replace the paragraph text with your feature description

**Complete Example**:
```html
<div class="card-hover bg-white p-8 rounded-lg shadow-md border border-gray-200">
    <div class="w-14 h-14 bg-gradient-to-r from-black to-blue-500 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-car text-white text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-black mb-3 tracking-tight" style="font-family: 'Space Grotesk', sans-serif;">Modern Fleet</h3>
    <p class="text-gray-700 font-light leading-relaxed">Our vehicles are regularly maintained and updated with the latest technology and luxury amenities.</p>
</div>
```

---

### 6. Updating Benefits Section

**Location**: "Why Choose Our Executive Solutions" section (white background)

Similar to features, but with different styling. Find sections like:

```html
<h3 class="text-2xl font-bold text-black mb-4 tracking-tight" style="font-family: 'Space Grotesk', sans-serif;">Elevate Your Brand</h3>
<p class="text-gray-700 font-light leading-relaxed">First impressions matter. Our premium fleet and professional drivers project success and sophistication...</p>
```

**How to update**:
- Change the benefit title
- Change the benefit description
- Optionally change the icon by updating `fa-star` to another icon name

---

### 7. Updating About Us Section

**Location**: "About Pogiso Tours" section (grey background)

**Find this code**:
```html
<p class="text-lg text-gray-700 font-light leading-relaxed text-justify">
    Founded with a vision to revolutionize executive transportation, Pogiso Tours emerged from a deep understanding of the corporate travel landscape...
</p>
```

**How to update**:
Replace the entire paragraph with your company's story. You can have multiple paragraphs by adding more `<p>` tags.

**Example**:
```html
<p class="text-lg text-gray-700 font-light leading-relaxed text-justify">
    Since 2015, we've been the trusted partner for executive transportation across the region. Our commitment to excellence has made us the preferred choice for Fortune 500 companies and government agencies.
</p>

<p class="text-lg text-gray-700 font-light leading-relaxed text-justify">
    We believe that transportation is more than just moving people from point A to point B. It's about creating an experience that reflects your professionalism and values.
</p>
```

---

### 8. Updating Testimonials

**Location**: "What Our Clients Say" section

Each testimonial has: **star rating**, **quote**, **client name**, and **client title**.

**Find this structure** (repeated 4 times):
```html
<div class="card-hover bg-white p-6 md:p-8 rounded-lg shadow-md border border-gray-200">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 font-light leading-relaxed mb-6">"Pogiso Tours has transformed how we manage executive transportation..."</p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-black" style="font-family: 'Space Grotesk', sans-serif;">James Mthembu</p>
        <p class="text-sm text-gray-600 font-light">CEO, Corporate Solutions Ltd</p>
    </div>
</div>
```

**How to update**:

1. **Change the star rating** (optional):
   - To show 4 stars instead of 5, change one line from:
     ```html
     <i class="fas fa-star text-yellow-400"></i>
     ```
     to:
     ```html
     <i class="fas fa-star-half-alt text-yellow-400"></i>
     ```

2. **Change the quote**:
   - Replace the text between the quotation marks

3. **Change the client name**:
   - Replace `James Mthembu`

4. **Change the client title**:
   - Replace `CEO, Corporate Solutions Ltd`

**Complete Example**:
```html
<p class="text-gray-700 font-light leading-relaxed mb-6">"Working with this team has been a game-changer for our company. Reliable, professional, and always on time."</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-semibold text-black" style="font-family: 'Space Grotesk', sans-serif;">Sarah Johnson</p>
    <p class="text-sm text-gray-600 font-light">Operations Director, Tech Innovations Inc</p>
</div>
```

---

### 9. Updating FAQ Questions and Answers

**Location**: "Frequently Asked Questions" section

**Find this structure** (repeated 5 times):
```html
<div class="faq-item bg-white rounded-lg shadow-md border border-gray-200 overflow-hidden">
    <button class="faq-question w-full px-6 md:px-8 py-5 md:py-6 text-left flex items-center justify-between cursor-pointer hover:bg-gray-50 smooth-transition">
        <span class="text-lg font-semibold text-black" style="font-family: 'Space Grotesk', sans-serif;">What is included in your corporate transportation packages?</span>
        <i class="faq-icon fas fa-chevron-down text-blue-500 text-lg transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-6 md:px-8 py-6 md:py-8 border-t border-gray-200 bg-gray-50">
        <p class="text-gray-700 font-light leading-relaxed mb-4">Our comprehensive corporate transportation packages include...</p>
    </div>
</div>
```

**How to update**:

1. **Change the question**:
   - Replace the text in the `<span>` tag

2. **Change the answer**:
   - Replace the text in the `<p>` tag inside the `faq-answer` div

**Example**:
```html
<span class="text-lg font-semibold text-black" style="font-family: 'Space Grotesk', sans-serif;">Do you offer airport transfers?</span>

<!-- And in the answer section: -->
<p class="text-gray-700 font-light leading-relaxed mb-4">Yes! We specialize in airport transfers with real-time flight tracking and flexible wait times.</p>
```

---

### 10. Updating Footer Company Information

**Location**: Bottom of the page

**Find these sections**:

**Logo and description**:
```html
<div class="w-10 h-10 bg-gradient-to-r from-white to-blue-500 rounded-lg flex items-center justify-center">
    <i class="fas fa-shuttle-van text-black text-lg"></i>
</div>
<span class="text-lg font-bold" style="font-family: 'Space Grotesk', sans-serif;">Pogiso Tours</span>
<p class="text-gray-400 font-light text-sm leading-relaxed">Premium executive transportation and VIP shuttle solutions for business and leisure.</p>
```

**Contact information**:
```html
<li class="flex items-center gap-2">
    <i class="fas fa-envelope text-blue-500"></i>
    <a href="mailto:info@pogisostours.co.za" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">info@pogisostours.co.za</a>
</li>
```

**How to update**:
- Change company name in the `<span>` tag
- Change description in the `<p>` tag
- Update email address in the `href="mailto:..."` attribute

---

## Working with Tailwind CSS Classes

Tailwind CSS is a utility-first framework that uses pre-built classes to style elements. Don't worry—you don't need to write CSS code!

### Understanding Common Tailwind Classes in This Page

Here are the most important classes used in your landing page:

#### Text and Font Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-xl` | Makes text larger | `<h1 class="text-xl">` |
| `text-black` | Makes text black | `<p class="text-black">` |
| `text-white` | Makes text white | `<p class="text-white">` |
| `text-gray-700` | Makes text dark grey | `<p class="text-gray-700">` |
| `font-bold` | Makes text bold | `<h1 class="font-bold">` |
| `font-light` | Makes text thin/light | `<p class="font-light">` |
| `text-center` | Centers text | `<p class="text-center">` |

#### Size and Spacing Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `px-4` | Adds left and right padding | `<div class="px-4">` |
| `py-6` | Adds top and bottom padding | `<div class="py-6">` |
| `mb-6` | Adds margin (space) below | `<h1 class="mb-6">` |
| `gap-4` | Adds space between items | `<div class="gap-4">` |
| `w-10` | Sets width (40px) | `<div class="w-10">` |
| `h-10` | Sets height (40px) | `<div class="h-10">` |

#### Background and Color Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `bg-white` | White background | `<div class="bg-white">` |
| `bg-gray-50` | Light grey background | `<section class="bg-gray-50">` |
| `bg-black` | Black background | `<div class="bg-black">` |
| `bg-blue-500` | Blue background | `<button class="bg-blue-500">` |
| `border` | Adds a border | `<div class="border">` |
| `border-gray-200` | Light grey border | `<div class="border-gray-200">` |

#### Responsive Classes

Tailwind uses prefixes to make things responsive:

| Prefix | Screen Size | Example |
|--------|------------|---------|
| (none) | Mobile (small) | `text-4xl` |
| `md:` | Tablet/Medium | `md:text-5xl` |
| `lg:` | Desktop/Large | `lg:text-6xl` |

**Example**: `text-4xl md:text-5xl lg:text-6xl` means:
- On phones: text size 4xl
- On tablets: text size 5xl
- On desktop: text size 6xl

---

### How to Modify Tailwind Classes While Keeping Design Consistent

#### Example 1: Making a Button Larger

**Original**:
```html
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-6 py-3 rounded">Book Now</a>
```

**To make it larger**:
```html
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-8 py-4 rounded">Book Now</a>
```

What changed:
- `px-6` → `px-8` (wider padding on sides)
- `py-3` → `py-4` (taller padding on top/bottom)

#### Example 2: Changing Text Color

**Original**:
```html
<p class="text-gray-700 font-light">Description text</p>
```

**To make it darker**:
```html
<p class="text-gray-900 font-light">Description text</p>
```

The numbers go from 50 (lightest) to 900 (darkest): `50, 100, 200, 300, 400, 500, 600, 700, 800, 900`

#### Example 3: Changing Background Color

**Original**:
```html
<section class="bg-gray-50">
```

**To make it white**:
```html
<section class="bg-white">
```

**To make it light blue**:
```html
<section class="bg-blue-50">
```

---

### Maintaining Responsive Design

**IMPORTANT**: When you modify Tailwind classes, always include the responsive prefixes:

**Good** (will work on all devices):
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">Headline</h1>
```

**Bad** (will only show the desktop size everywhere):
```html
<h1 class="text-6xl">Headline</h1>
```

**When modifying, keep this pattern**:
- `text-[mobile]` - How it looks on phones
- `md:text-[tablet]` - How it looks on tablets
- `lg:text-[desktop]` - How it looks on large screens

---

### Common Tailwind Modifications for This Page

#### Changing Section Background Colors

Find sections and change the `bg-` class:

```html
<!-- Current (light grey) -->
<section class="py-12 md:py-16 px-4 md:px-8 bg-gray-50">

<!-- Change to white -->
<section class="py-12 md:py-16 px-4 md:px-8 bg-white">

<!-- Change to light blue -->
<section class="py-12 md:py-16 px-4 md:px-8 bg-blue-50">
```

#### Changing Button Colors

The page uses a `gradient-button` class, but you can add regular Tailwind classes:

```html
<!-- Original gradient button -->
<a href="#" class="gradient-button text-white px-8 py-4 rounded">Book Now</a>

<!-- Solid blue button (if you prefer) -->
<a href="#" class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded">Book Now</a>

<!-- Solid black button -->
<a href="#" class="bg-black hover:bg-gray-900 text-white px-8 py-4 rounded">Book Now</a>
```

#### Changing Spacing (Padding and Margins)

```html
<!-- Increase padding inside cards -->
<!-- Original -->
<div class="card-hover bg-white p-8 rounded-lg">

<!-- More padding -->
<div class="card-hover bg-white p-12 rounded-lg">

<!-- Less padding -->
<div class="card-hover bg-white p-6 rounded-lg">
```

---

## Fixing and Managing Links

Your landing page contains many links that direct users to different pages and external websites. Let's learn how to find and update them.

### Understanding Links in HTML

A link looks like this:
```html
<a href="https://example.com">Click Here</a>
```

Breaking it down:
- `<a>` = the link tag (anchor)
- `href="..."` = where the link goes
- `Click Here` = what the user sees and clicks
- `</a>` = closes the link

### All Links in Your Landing Page

Here's a complete list of every link on your page and where to find it:

#### 1. Navigation Menu Links (Header)

**Location**: Inside `<header>` at the top of the page

```html
<a href="#features" class="text-black hover:text-blue-500 font-light smooth-transition">Features</a>
<a href="#benefits" class="text-black hover:text-blue-500 font-light smooth-transition">Benefits</a>
<a href="#testimonials" class="text-black hover:text-blue-500 font-light smooth-transition">Testimonials</a>
<a href="#faq" class="text-black hover:text-blue-500 font-light smooth-transition">FAQ</a>
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-6 py-3 rounded">Book Now</a>
```

**What these do**:
- `#features` = jumps to the Features section on the same page
- `#benefits` = jumps to the Benefits section
- `#testimonials` = jumps to the Testimonials section
- `#faq` = jumps to the FAQ section
- `https://pogisostours.co.za/booking` = goes to the booking website

**How to update**:
- If you have your own booking page, replace `https://pogisostours.co.za/booking` with your URL
- The anchor links (`#features`, `#benefits`, etc.) work automatically if the sections have matching `id` attributes (they already do in this page)

#### 2. Hero Section Call-to-Action Links

**Location**: In the hero section (the first big banner)

```html
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-8 py-4 rounded font-medium text-center inline-flex items-center justify-center gap-2 hover:shadow-lg">
    <i class="fas fa-calendar-check"></i>
    Book Your Ride
</a>

<a href="#features" class="border-2 border-black text-black px-8 py-4 rounded font-medium text-center inline-flex items-center justify-center gap-2 hover:bg-black hover:text-white smooth-transition">
    <i class="fas fa-arrow-right"></i>
    Learn More
</a>
```

**How to update**:
- "Book Your Ride" button: Update `https://pogisostours.co.za/booking` to your booking page
- "Learn More" button: This already links to `#features` (correct)

#### 3. CTA Section Links

**Location**: The large banner section near the bottom (before footer)

```html
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-8 py-4 rounded font-medium inline-flex items-center justify-center gap-2 hover:shadow-lg text-center">
    <i class="fas fa-check-circle"></i>
    Book Your First Ride
</a>

<a href="mailto:info@pogisostours.co.za" class="bg-white text-black px-8 py-4 rounded font-medium inline-flex items-center justify-center gap-2 hover:bg-gray-100 smooth-transition text-center">
    <i class="fas fa-envelope"></i>
    Contact Sales
</a>
```

**How to update**:
- "Book Your First Ride": Update to your booking page URL
- "Contact Sales": Update `info@pogisostours.co.za` to your email address

**Important**: The `mailto:` prefix is special—it opens the user's email client. Always keep `mailto:` before the email address.

#### 4. Footer Links - Services Column

**Location**: Footer section at the bottom, left side

```html
<li><a href="#features" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Executive Transport</a></li>
<li><a href="#features" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">VIP Shuttles</a></li>
<li><a href="#features" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Corporate Packages</a></li>
<li><a href="#features" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Event Transportation</a></li>
```

**Current behavior**: All these links jump to the Features section

**How to update** (if you have separate service pages):
```html
<li><a href="services/executive-transport.html" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Executive Transport</a></li>
<li><a href="services/vip-shuttles.html" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">VIP Shuttles</a></li>
<li><a href="services/corporate-packages.html" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Corporate Packages</a></li>
<li><a href="services/event-transportation.html" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Event Transportation</a></li>
```

#### 5. Footer Links - Company Column

**Location**: Footer, second column

```html
<li><a href="#" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">About Us</a></li>
<li><a href="#testimonials" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Testimonials</a></li>
<li><a href="#faq" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">FAQ</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">Blog</a></li>
```

**Current issues**:
- "About Us" has `href="#"` which doesn't go anywhere
- "Testimonials" correctly links to `#testimonials`
- "FAQ" correctly links to `#faq`
- "Blog" links to `blog.html`

**How to fix**:
```html
<!-- Fix About Us -->
<li><a href="#" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">About Us</a></li>
<!-- Change to: -->
<li><a href="#about" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">About Us</a></li>

<!-- If you have a separate about page: -->
<li><a href="about.html" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">About Us</a></li>
```

#### 6. Footer Links - Contact Column

**Location**: Footer, third column

```html
<li class="flex items-center gap-2">
    <i class="fas fa-envelope text-blue-500"></i>
    <a href="mailto:info@pogisostours.co.za" class="text-gray-400 hover:text-blue-500 font-light smooth-transition">info@pogisostours.co.za</a>
</li>
```

**How to update**:
Replace `info@pogisostours.co.za` with your email address (in both places—the `href` and the visible text).

#### 7. Footer Legal Links

**Location**: Bottom of footer

```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-500 font-light text-sm smooth-transition flex items-center gap-2">
    <i class="fas fa-shield-alt"></i>
    Privacy Policy
</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-500 font-light text-sm smooth-transition flex items-center gap-2">
    <i class="fas fa-file-contract"></i>
    Terms of Service
</a>
<a href="blog.html" class="text-gray-400 hover:text-blue-500 font-light text-sm smooth-transition flex items-center gap-2">
    <i class="fas fa-newspaper"></i>
    Blog
</a>
```

**Current status**:
- `privacy.html` ✓ Correct (we'll create this)
- `terms.html` ✓ Correct (we'll create this)
- `blog.html` ✓ Correct (you'll create this)

#### 8. Footer Social Media Links

**Location**: Bottom right of footer

```html
<a href="#" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="Facebook">
    <i class="fab fa-facebook"></i>
</a>
<a href="#" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="Twitter">
    <i class="fab fa-twitter"></i>
</a>
<a href="#" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="LinkedIn">
    <i class="fab fa-linkedin"></i>
</a>
<a href="#" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="Instagram">
    <i class="fab fa-instagram"></i>
</a>
```

**Current issue**: All links have `href="#"` which doesn't go anywhere

**How to fix**:
```html
<!-- Replace with your actual social media URLs -->
<a href="https://www.facebook.com/pogisotours" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="Facebook">
    <i class="fab fa-facebook"></i>
</a>
<a href="https://www.twitter.com/pogisotours" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="Twitter">
    <i class="fab fa-twitter"></i>
</a>
<a href="https://www.linkedin.com/company/pogiso-tours" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="LinkedIn">
    <i class="fab fa-linkedin"></i>
</a>
<a href="https://www.instagram.com/pogisotours" class="text-gray-400 hover:text-blue-500 smooth-transition text-lg" aria-label="Instagram">
    <i class="fab fa-instagram"></i>
</a>
```

---

### Step-by-Step: How to Update All Links

**Step 1**: Open `index.html` in your text editor

**Step 2**: Use Find & Replace to update booking URLs
- Press `Ctrl+H` (or `Cmd+H` on Mac) to open Find & Replace
- Find: `https://pogisostours.co.za/booking`
- Replace with: Your booking page URL
- Click "Replace All"

**Step 3**: Update email addresses
- Find: `info@pogisostours.co.za`
- Replace with: Your email address
- Click "Replace All"

**Step 4**: Update social media links manually (one at a time):
- Find each `href="#"` in the social media section
- Replace with the actual URL

**Step 5**: Save the file (`Ctrl+S` or `Cmd+S`)

**Step 6**: Open `index.html` in your browser and test all links

---

### Testing Links

After updating, test each link:

1. **Navigation links** - Should jump to the right section
2. **Booking buttons** - Should go to your booking page
3. **Email links** - Should open your default email client
4. **Social media** - Should open your social profiles
5. **Footer links** - Should go to the right pages

---

## Adding Privacy and Terms Pages

Your landing page already has links to `privacy.html` and `terms.html` in the footer, but these files don't exist yet. Let's create them!

### Step 1: Create the Privacy Policy Page

**What you'll do**: Create a new file called `privacy.html`

**Step-by-step**:

1. **Open your text editor**
2. **Create a new file** (File → New)
3. **Paste this code**:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Pogiso Tours Executive Transportation">
    <title>Privacy Policy | Pogiso Tours</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header / Navigation -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200">
        <nav class="max-w-7xl mx-auto px-4 md:px-8 py-4 md:py-6 flex items-center justify-between">
            <!-- Logo -->
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-gradient-to-r from-black to-blue-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-shuttle-van text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-black hidden sm:inline" style="font-family: 'Space Grotesk', sans-serif;">Pogiso Tours</a>
            </div>
            
            <!-- Back to Home -->
            <a href="index.html" class="text-black hover:text-blue-500 font-light transition">← Back to Home</a>
        </nav>
    </header>

    <!-- Content -->
    <section class="py-12 md:py-16 px-4 md:px-8">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-black mb-8" style="font-family: 'Space Grotesk', sans-serif;">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 font-light space-y-6">
                <p><strong>Last Updated:</strong> January 2025</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">1. Introduction</h2>
                <p>Pogiso Tours ("we," "us," "our," or "Company") operates the landing page. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our service and the choices you have associated with that data.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">2. Information Collection and Use</h2>
                <p>We collect several different types of information for various purposes to provide and improve our service to you.</p>
                
                <h3 class="text-xl font-bold text-black mt-6 mb-3" style="font-family: 'Space Grotesk', sans-serif;">Types of Data Collected:</h3>
                <ul class="list-disc list-inside space-y-2">
                    <li><strong>Personal Data:</strong> While using our service, we may ask you to provide us with certain personally identifiable information that can be used to contact or identify you ("Personal Data"). This may include, but is not limited to:
                        <ul class="list-disc list-inside ml-4 mt-2 space-y-1">
                            <li>Email address</li>
                            <li>First name and last name</li>
                            <li>Phone number</li>
                            <li>Address, State, Province, ZIP/Postal code, City</li>
                            <li>Cookies and Usage Data</li>
                        </ul>
                    </li>
                    <li><strong>Usage Data:</strong> We may also collect information on how the service is accessed and used ("Usage Data"). This may include information such as your computer's Internet Protocol address (e.g., IP address), browser type, browser version, the pages you visit, the time and date of your visit, and other diagnostic data.</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">3. Use of Data</h2>
                <p>Pogiso Tours uses the collected data for various purposes:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>To provide and maintain our service</li>
                    <li>To notify you about changes to our service</li>
                    <li>To allow you to participate in interactive features of our service when you choose to do so</li>
                    <li>To provide customer care and support</li>
                    <li>To gather analysis or valuable information so that we can improve our service</li>
                    <li>To monitor the usage of our service</li>
                    <li>To detect, prevent and address technical issues</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">4. Security of Data</h2>
                <p>The security of your data is important to us, but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">5. Changes to This Privacy Policy</h2>
                <p>We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "Last Updated" date at the top of this Privacy Policy.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">6. Contact Us</h2>
                <p>If you have any questions about this Privacy Policy, please contact us at:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Email: <a href="mailto:info@pogisostours.co.za" class="text-blue-500 hover:underline">info@pogisostours.co.za</a></li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black text-white py-12 px-4 md:px-8 mt-16">
        <div class="max-w-7xl mx-auto text-center">
            <p class="text-gray-400 font-light">&copy; 2025 Pogiso Tours. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

4. **Save the file**:
   - Click File → Save As
   - Name it: `privacy.html`
   - Save it in the **same folder** as your `index.html`

---

### Step 2: Create the Terms of Service Page

**What you'll do**: Create a new file called `terms.html`

**Step-by-step**:

1. **Open your text editor** and create a new file
2. **Paste this code**:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Pogiso Tours Executive Transportation">
    <title>Terms of Service | Pogiso Tours</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header / Navigation -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200">
        <nav class="max-w-7xl mx-auto px-4 md:px-8 py-4 md:py-6 flex items-center justify-between">
            <!-- Logo -->
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-gradient-to-r from-black to-blue-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-shuttle-van text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-black hidden sm:inline" style="font-family: 'Space Grotesk', sans-serif;">Pogiso Tours</a>
            </div>
            
            <!-- Back to Home -->
            <a href="index.html" class="text-black hover:text-blue-500 font-light transition">← Back to Home</a>
        </nav>
    </header>

    <!-- Content -->
    <section class="py-12 md:py-16 px-4 md:px-8">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-black mb-8" style="font-family: 'Space Grotesk', sans-serif;">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 font-light space-y-6">
                <p><strong>Last Updated:</strong> January 2025</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">1. Agreement to Terms</h2>
                <p>By accessing and using the Pogiso Tours website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">2. Use License</h2>
                <p>Permission is granted to temporarily download one copy of the materials (information or software) on Pogiso Tours' website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">3. Disclaimer</h2>
                <p>The materials on Pogiso Tours' website are provided on an 'as is' basis. Pogiso Tours makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">4. Limitations</h2>
                <p>In no event shall Pogiso Tours or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the Pogiso Tours website, even if Pogiso Tours or a Pogiso Tours authorized representative has been notified orally or in writing of the possibility of such damage.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">5. Accuracy of Materials</h2>
                <p>The materials appearing on Pogiso Tours' website could include technical, typographical, or photographic errors. Pogiso Tours does not warrant that any of the materials on its website are accurate, complete, or current. Pogiso Tours may make changes to the materials contained on its website at any time without notice.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">6. Links</h2>
                <p>Pogiso Tours has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Pogiso Tours of the site. Use of any such linked website is at the user's own risk.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">7. Modifications</h2>
                <p>Pogiso Tours may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">8. Governing Law</h2>
                <p>These terms and conditions are governed by and construed in accordance with the laws of South Africa, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.</p>
                
                <h2 class="text-2xl font-bold text-black mt-8 mb-4" style="font-family: 'Space Grotesk', sans-serif;">9. Contact Us</h2>
                <p>If you have any questions about these Terms of Service, please contact us at:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Email: <a href="mailto:info@pogisostours.co.za" class="text-blue-500 hover:underline">info@pogisostours.co.za</a></li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black text-white py-12 px-4 md:px-8 mt-16">
        <div class="max-w-7xl mx-auto text-center">
            <p class="text-gray-400 font-light">&copy; 2025 Pogiso Tours. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

3. **Save the file**:
   - Click File → Save As
   - Name it: `terms.html`
   - Save it in the **same folder** as your `index.html`

---

### Step 3: Verify the Links Work

1. **Open `index.html` in your browser**
2. **Scroll to the footer** (bottom of the page)
3. **Click on "Privacy Policy"** - should open `privacy.html`
4. **Click on "Terms of Service"** - should open `terms.html`
5. **Click "← Back to Home"** on either page - should return to `index.html`

---

### Step 4: Customize the Privacy and Terms Pages

The pages we created are templates. You should customize them with your actual policies:

**For Privacy Policy**:
- Update the email address
- Add your specific data collection practices
- Add any additional sections relevant to your business

**For Terms of Service**:
- Update the email address
- Add your cancellation/refund policies
- Add your payment terms
- Add any liability limitations specific to your business

---

### File Structure

After creating these files, your folder should look like:

```
your-project-folder/
├── index.html          (main landing page)
├── privacy.html        (privacy policy)
├── terms.html          (terms of service)
└── blog.html           (optional - blog page you'll create later)
```

---

## Mobile Responsiveness

Your landing page uses Tailwind CSS's responsive design system. Here's how it works:

### Understanding Responsive Breakpoints

Tailwind uses these screen sizes:

| Prefix | Screen Width | Device |
|--------|-------------|--------|
| (none) | < 768px | Mobile phones |
| `sm:` | ≥ 640px | Large phones |
| `md:` | ≥ 768px | Tablets |
| `lg:` | ≥ 1024px | Desktops |
| `xl:` | ≥ 1280px | Large desktops |

### Examples from Your Page

**Text sizing** (gets bigger on larger screens):
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
- Mobile: 36px
- Tablet: 48px
- Desktop: 60px

**Hiding elements on mobile**:
```html
<img class="hidden lg:block">
```
This image is hidden on mobile and tablet, only shows on desktop.

**Showing elements only on mobile**:
```html
<button class="md:hidden">
```
This button only shows on mobile, hidden on tablet and desktop.

**Spacing adjustments**:
```html
<section class="py-12 md:py-16">
```
- Mobile: 48px padding top/bottom
- Tablet+: 64px padding top/bottom

---

### Testing Responsiveness

1. **Open your page in a browser**
2. **Press F12** to open Developer Tools
3. **Click the device icon** (looks like a phone/tablet)
4. **Test different screen sizes**:
   - iPhone SE (375px)
   - iPad (768px)
   - Desktop (1024px+)

---

### When to Use Responsive Classes

**Always include mobile-first design**:
- Base classes (no prefix) = mobile
- Add `md:` for tablets
- Add `lg:` for desktops

**Good**:
```html
<div class="text-4xl md:text-5xl lg:text-6xl">
```

**Bad** (only works on desktop):
```html
<div class="lg:text-6xl">
```

---

## Common Customizations

### 1. Changing the Brand Color Scheme

The page uses black and blue (`#000000` and `#4A90E2`). To change these:

**Find the gradient button style**:
```html
.gradient-button {
    background: linear-gradient(to right, #000000, #4A90E2);
}
```

**Change to your colors**:
```html
.gradient-button {
    background: linear-gradient(to right, #1a1a2e, #16c784);
}
```

Then update all `bg-blue-500` classes to your new color:

**Find**:
```html
<div class="bg-gradient-to-r from-black to-blue-500">
```

**Change to**:
```html
<div class="bg-gradient-to-r from-black to-green-500">
```

---

### 2. Adding a New Feature Card

**Find the Features section** and copy this entire block:

```html
<div class="card-hover bg-white p-8 rounded-lg shadow-md border border-gray-200">
    <div class="w-14 h-14 bg-gradient-to-r from-black to-blue-500 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-clock text-white text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-black mb-3 tracking-tight" style="font-family: 'Space Grotesk', sans-serif;">24/7 Corporate Service</h3>
    <p class="text-gray-700 font-light leading-relaxed">Round-the-clock availability ensures...</p>
</div>
```

**Paste it after the last feature card**, and update:
- The icon (change `fa-clock`)
- The title
- The description

---

### 3. Changing the Hero Image

**Find this code**:
```html
<img src="https://images.unsplash.com/photo-1449824913935-59a10b8d2000?w=600&h=400&fit=crop" alt="Premium luxury vehicle" class="rounded-lg shadow-lg w-full object-cover">
```

**To use your own image**:
1. Upload your image to a service like [Unsplash](https://unsplash.com) or [Imgur](https://imgur.com)
2. Copy the image URL
3. Replace the `src` value with your URL

**Example**:
```html
<img src="https://your-image-url.com/car.jpg" alt="Premium luxury vehicle" class="rounded-lg shadow-lg w-full object-cover">
```

---

### 4. Adding a New Testimonial

**Find the Testimonials section** and copy this block:

```html
<div class="card-hover bg-white p-6 md:p-8 rounded-lg shadow-md border border-gray-200">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 font-light leading-relaxed mb-6">"Quote text here..."</p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-black" style="font-family: 'Space Grotesk', sans-serif;">Name</p>
        <p class="text-sm text-gray-600 font-light">Title, Company</p>
    </div>
</div>
```

**Paste it after the last testimonial** and update the quote, name, and title.

---

### 5. Changing Button Text

**Find the button**:
```html
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-8 py-4 rounded font-medium text-center inline-flex items-center justify-center gap-2 hover:shadow-lg">
    <i class="fas fa-calendar-check"></i>
    Book Your Ride
</a>
```

**Change the text**:
```html
<a href="https://pogisostours.co.za/booking" class="gradient-button text-white px-8 py-4 rounded font-medium text-center inline-flex items-center justify-center gap-2 hover:shadow-lg">
    <i class="fas fa-calendar-check"></i>
    Schedule Now
</a>
```

---

### 6. Changing Section Background Colors

**Find a section**:
```html
<section class="py-12 md:py-16 px-4 md:px-8 bg-gray-50">
```

**Change the background**:
```html
<!-- To white -->
<section class="py-12 md:py-16 px-4 md:px-8 bg-white">

<!-- To light blue -->
<section class="py-12 md:py-16 px-4 md:px-8 bg-blue-50">

<!-- To light green -->
<section class="py-12 md:py-16 px-4 md:px-8 bg-green-50">
```

---

### 7. Adding a New FAQ Item

**Find the FAQ section** and copy this block:

```html
<div class="faq-item bg-white rounded-lg shadow-md border border-gray-200 overflow-hidden">
    <button class="faq-question w-full px-6 md:px-8 py-5 md:py-6 text-left flex items-center justify-between cursor-pointer hover:bg-gray-50 smooth-transition">
        <span class="text-lg font-semibold text-black" style="font-family: 'Space Grotesk', sans-serif;">Question here?</span>
        <i class="faq-icon fas fa-chevron-down text-blue-500 text-lg transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-6 md:px-8 py-6 md:py-8 border-t border-gray-200 bg-gray-50">
        <p class="text-gray-700 font-light leading-relaxed mb-4">Answer text here.</p>
    </div>
</div>
```

**Paste it after the last FAQ item** and update the question and answer.

---

## Troubleshooting

### Problem: Links Don't Work

**Symptoms**: Clicking a link does nothing

**Solutions**:
1. Check the `href` value is correct
2. For email links, make sure it starts with `mailto:`
3. For internal links, make sure the file exists in the same folder
4. Check for typos in the URL

**Example of correct link**:
```html
<a href="https://example.com">Link</a>
```

**Example of incorrect link**:
```html
<a href="htp://example.com">Link</a>  <!-- Typo: "htp" -->
```

---

### Problem: Page Looks Different on Mobile

**Symptoms**: Layout breaks on mobile phones

**Solutions**:
1. Check that you're using responsive classes (`md:`, `lg:`)
2. Test in browser's mobile view (F12 → Device mode)
3. Make sure you didn't remove the viewport meta tag:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

---

### Problem: Styling Looks Wrong

**Symptoms**: Colors, fonts, or spacing look incorrect

**Solutions**:
1. **Check Tailwind classes** - make sure you didn't accidentally delete or modify them
2. **Clear browser cache** - Press Ctrl+Shift+Delete and clear cached files
3. **Hard refresh** - Press Ctrl+Shift+R (or Cmd+Shift+R on Mac)
4. **Check for typos** - Tailwind classes are case-sensitive

**Common mistakes**:
```html
<!-- Wrong -->
<div class="text-Blue-500">  <!-- Capital B -->

<!-- Correct -->
<div class="text-blue-500">  <!-- lowercase b -->
```

---

### Problem: Form Doesn't Submit

**Symptoms**: Contact form doesn't send messages

**Solutions**:
1. Check that the form has the correct action URL:
   ```html
   <form action="https://api.web3forms.com/submit" method="POST">
   ```
2. Verify the access key is present:
   ```html
   <input type="hidden" name="access_key" value="3bb39263-2490-491b-89f8-213fa513edae">
   ```
3. Make sure all required fields are filled
4. Check browser console for errors (F12 → Console tab)

---

### Problem: Images Don't Load

**Symptoms**: Broken image icons instead of pictures

**Solutions**:
1. Check the image URL is correct and accessible
2. Try a different image URL
3. Verify the image format is supported (JPG, PNG, WebP, GIF)
4. Check for typos in the URL

**Example**:
```html
<!-- Correct -->
<img src="https://images.unsplash.com/photo-1449824913935-59a10b8d2000?w=600&h=400&fit=crop" alt="Car">

<!-- Incorrect (broken URL) -->
<img src="https://images.unsplash.com/photo-invalid-url" alt="Car">
```

---

### Problem: Text Formatting Looks Wrong

**Symptoms**: Text is too small, too large, wrong color, etc.

**Solutions**:
1. Check the Tailwind classes:
   - `text-xl` = size
   - `text-black` = color
   - `font-bold` = weight
2. Check for conflicting classes
3. Verify you're editing the right text element

**Example of checking text styling**:
```html
<!-- This text will be: Large (text-2xl), Black (text-black), Bold (font-bold) -->
<h2 class="text-2xl text-black font-bold">Heading</h2>
```

---

### Problem: Footer Links Don't Go to the Right Place

**Symptoms**: Footer links go to wrong pages

**Solutions**:
1. Check the `href` values in footer links
2. Verify file names match exactly (case-sensitive)
3. Make sure files exist in the same folder

**Correct footer link structure**:
```html
<a href="privacy.html">Privacy Policy</a>  <!-- Goes to privacy.html -->
<a href="index.html">Home</a>               <!-- Goes to index.html -->
<a href="https://example.com">External</a>  <!-- Goes to external site -->
```

---

### Problem: Mobile Menu Doesn't Open

**Symptoms**: Hamburger menu button doesn't work on mobile

**Solutions**:
1. Check that JavaScript isn't disabled in your browser
2. Open browser console (F12 → Console) to check for errors
3. Verify the mobile menu HTML is present:
   ```html
   <div class="mobile-menu hidden">
   ```
4. Test on an actual mobile device or mobile view (F12 → Device mode)

---

## Best Practices for Maintenance

### 1. Regular Backups
- Keep a backup copy of your HTML files
- Use version control (Git) if possible
- Save before making major changes

### 2. Testing Changes
- Always test changes in a browser before publishing
- Test on mobile and desktop
- Test all links after updating them

### 3. Keeping Content Fresh
- Update testimonials regularly
- Keep FAQ current
- Update pricing and services as needed

### 4. SEO Optimization
- Update meta descriptions when you change content
- Use descriptive alt text for images
- Keep headings (H1, H2, H3) properly structured

### 5. Security
- Keep your email address private
- Use HTTPS for external links
- Validate form submissions
- Keep software and tools updated

---

## Summary Checklist

Use this checklist when maintaining your landing page:

- [ ] Updated company name and branding
- [ ] Changed all booking URLs to your website
- [ ] Updated email addresses
- [ ] Created privacy.html and terms.html
- [ ] Tested all links on desktop and mobile
- [ ] Updated hero image with your own
- [ ] Customized features and benefits sections
- [ ] Added or updated testimonials
- [ ] Updated FAQ with your questions
- [ ] Tested contact form
- [ ] Verified responsive design on mobile
- [ ] Updated social media links
- [ ] Checked for broken images
- [ ] Tested on different browsers (Chrome, Firefox, Safari, Edge)

---

## Additional Resources

- **Tailwind CSS Documentation**: https://tailwindcss.com/docs
- **Font Awesome Icons**: https://fontawesome.com/icons
- **Unsplash Images**: https://unsplash.com
- **Web3Forms**: https://web3forms.com
- **Google Fonts**: https://fonts.google.com

---

## Support

If you encounter issues not covered in this guide:

1. Check the troubleshooting section above
2. Review the code comments in your HTML file
3. Search for solutions online using specific error messages
4. Consider consulting with a web developer for complex customizations

---

**Last Updated**: January 2025

Happy maintaining! Your Pogiso Tours landing page is now fully documented and ready for customization. 🚗