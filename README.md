# FiberNet Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your FiberNet fiber optic internet landing page. This guide is designed for beginners with no prior coding experience.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Common Customizations](#common-customizations)
7. [Troubleshooting](#troubleshooting)

---

## Getting Started

### What You'll Need

- A text editor (we recommend VS Code, which is free: https://code.visualstudio.com/)
- Your `index.html` file
- Basic understanding of HTML tags like `<div>`, `<a>`, `<h1>`, etc.
- A web browser to preview your changes

### How to Edit Your File

1. **Open your HTML file in a text editor:**
   - Right-click on `index.html`
   - Select "Open with" → Choose your text editor
   - Or drag the file directly into your text editor

2. **Make changes to the code**

3. **Save your file:**
   - Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)
   - Or use File → Save

4. **View your changes:**
   - Open the `index.html` file in your web browser
   - Refresh the page (Press `F5` or `Ctrl+R`)

> **Tip:** Keep your file saved frequently while making edits. If something breaks, you can always undo with `Ctrl+Z`.

---

## Updating Text Content

### Understanding the Structure

Your landing page is divided into sections, each containing specific content. Here's how to find and update text:

### Section 1: Announcement Bar (Top of Page)

**Location:** Lines 224-228

**Current Text:**
```html
<span class="font-medium">Fast Nationwide Delivery • 5-Year Price Guarantee • No Hidden Fees</span>
```

**How to Update:**
1. Find the line above in your text editor
2. Replace the text between `<span class="font-medium">` and `</span>`
3. Keep the HTML tags (`<span>` and `</span>`) - only change the text

**Example - Change to:**
```html
<span class="font-medium">Limited Time Offer • Free Installation • Call Now!</span>
```

---

### Section 2: Navigation Menu (Header)

**Location:** Lines 237-243 (Desktop Menu)

**Current Text:**
```html
<a href="#home" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Home</a>
<a href="#features" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Features</a>
<a href="#benefits" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Benefits</a>
```

**How to Update Menu Items:**
1. Find the navigation section in the header
2. Change the text inside the `<a>` tags (between `>` and `</a>`)
3. Do NOT change the `href="#"` part - this controls where the link goes
4. Repeat for both desktop menu (lines 237-243) AND mobile menu (lines 259-265)

**Example - Add a new menu item:**
```html
<!-- Original -->
<a href="#contact" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Contact</a>

<!-- Updated with new item -->
<a href="#pricing" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Pricing</a>
<a href="#contact" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Contact</a>
```

> **Important:** If you add a new menu item, you MUST also add a matching section in the page with the same ID. For example, if you add `href="#pricing"`, you need a section with `id="pricing"`.

---

### Section 3: Hero Section (Main Banner)

**Location:** Lines 282-313

**Key Text Areas:**

**3a. Main Heading:**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold text-white mb-6 md:mb-8 leading-tight tracking-tight">
    100% Fiber Optic Internet, Nationwide Coverage, No Contracts
</h1>
```

**How to Update:**
1. Find this `<h1>` tag (it's the largest heading)
2. Replace the text between `<h1>` and `</h1>`
3. Keep all the class names - they control the size and styling

**Example - Change to:**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold text-white mb-6 md:mb-8 leading-tight tracking-tight">
    Lightning-Fast Fiber Internet with Zero Contracts
</h1>
```

**3b. Subheading:**
```html
<p class="text-xl md:text-2xl lg:text-3xl text-white mb-8 md:mb-12 font-light leading-relaxed max-w-3xl mx-auto">
    Get 1GB Fiber and receive a Nintendo Switch On Us!
</p>
```

**How to Update:**
1. Find this `<p>` tag (paragraph)
2. Replace the text between `<p...>` and `</p>`

**Example - Change to:**
```html
<p class="text-xl md:text-2xl lg:text-3xl text-white mb-8 md:mb-12 font-light leading-relaxed max-w-3xl mx-auto">
    Sign up today and get a free Nintendo Switch with your new service!
</p>
```

**3c. Call-to-Action Button Text:**
```html
<a href="tel:8883224944" class="cta-button text-white px-8 md:px-10 py-4 md:py-5 rounded-lg font-bold text-base md:text-lg btn-hover inline-flex items-center justify-center">
    <i class="fas fa-phone mr-3"></i>Call 888-322-4944
</a>
```

**How to Update:**
1. Find this button
2. You can change the text "Call 888-322-4944"
3. To change the phone number, update both the `href="tel:8883224944"` AND the button text
4. Keep the `<i class="fas fa-phone mr-3"></i>` part - it's the phone icon

**Example - Change to:**
```html
<a href="tel:8884445555" class="cta-button text-white px-8 md:px-10 py-4 md:py-5 rounded-lg font-bold text-base md:text-lg btn-hover inline-flex items-center justify-center">
    <i class="fas fa-phone mr-3"></i>Call 888-444-5555
</a>
```

**3d. Feature Checkmarks:**
```html
<div class="flex items-center">
    <i class="fas fa-check-circle mr-2"></i>
    <span>No Setup Fees</span>
</div>
```

**How to Update:**
1. Find the three checkmark items
2. Replace the text inside `<span>` tags
3. Keep the icon code `<i class="fas fa-check-circle mr-2"></i>`

---

### Section 4: Features Section ("Why Choose FiberNet?")

**Location:** Lines 327-400

**4a. Section Heading:**
```html
<h2 class="section-heading text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 inline-block">
    Why Choose FiberNet?
</h2>
```

**How to Update:**
1. Replace text between `<h2>` and `</h2>`
2. Keep the class names

**4b. Feature Cards (Three boxes):**

Each feature card follows this pattern:
```html
<h3 class="text-xl md:text-2xl font-bold text-gray-900 text-center mb-4">
    Nintendo Switch On Us
</h3>
<p class="text-gray-600 text-center text-sm md:text-base leading-relaxed mb-6">
    Get a brand new Nintendo Switch absolutely free with your new fiber internet service...
</p>
```

**How to Update:**
1. Find the three feature cards (starting around line 343)
2. Each card has an `<h3>` heading and a `<p>` description
3. Update the text between the tags
4. There are three cards total - one for Nintendo Switch, one for Price Guarantee, one for No Contracts

**Example - Update Feature 1:**
```html
<!-- Original -->
<h3 class="text-xl md:text-2xl font-bold text-gray-900 text-center mb-4">
    Nintendo Switch On Us
</h3>

<!-- Updated -->
<h3 class="text-xl md:text-2xl font-bold text-gray-900 text-center mb-4">
    Free Gaming Console
</h3>
```

---

### Section 5: Benefits Section

**Location:** Lines 405-550

This section contains three large benefit cards with images. Each has:
- An `<h3>` heading
- A `<p>` description with multiple bullet points

**How to Update Benefit Headings:**
```html
<h3 class="text-2xl md:text-3xl lg:text-4xl font-bold text-gray-900 mb-4 md:mb-6">
    100% Fiber Optic Technology
</h3>
```

**How to Update Benefit Descriptions:**
```html
<p class="text-gray-600 text-base md:text-lg leading-relaxed mb-6">
    Experience the fastest, most reliable internet technology available...
</p>
```

**How to Update Bullet Points:**
```html
<li class="flex items-start">
    <i class="fas fa-check-circle text-gray-900 mr-3 mt-1 flex-shrink-0"></i>
    <span class="text-gray-700 text-base">Ultra-fast download speeds up to 1GB/s</span>
</li>
```

1. Find the `<span>` tag
2. Replace the text between `<span class="text-gray-700 text-base">` and `</span>`
3. Keep the checkmark icon code

---

### Section 6: About Us Section

**Location:** Lines 555-610

**How to Update "Our Story":**
```html
<h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-4 md:mb-6">
    Our Story
</h3>
<p class="text-gray-600 text-base md:text-lg leading-relaxed mb-6">
    Founded in 2015, FiberNet was born from a simple vision...
</p>
```

1. Update the `<h3>` heading text
2. Update the `<p>` paragraph text
3. Repeat for "Our Mission" section

**How to Update Statistics:**
```html
<div class="text-4xl md:text-5xl font-bold text-gray-900 mb-2">
    500K+
</div>
<p class="text-gray-600 text-base md:text-lg font-medium">
    Satisfied Customers
</p>
```

1. Update the number in the `<div>` (500K+)
2. Update the label in the `<p>` below it

---

### Section 7: Testimonials Section

**Location:** Lines 615-730

Each testimonial card has:
- Customer name
- Location
- Star rating
- Testimonial text

**How to Update a Testimonial:**
```html
<h4 class="text-lg md:text-xl font-bold text-gray-900">
    Sarah Mitchell
</h4>
<p class="text-gray-600 text-sm md:text-base">
    Freelance Designer, Austin TX
</p>
<p class="text-gray-600 text-base leading-relaxed mb-4">
    "I switched from my old cable provider to FiberNet and immediately noticed the difference..."
</p>
```

1. Update the name in `<h4>`
2. Update the location/profession in the first `<p>`
3. Update the testimonial text in the second `<p>`
4. Do NOT change the star rating code

---

### Section 8: FAQ Section

**Location:** Lines 735-850

Each FAQ item has:
- A question (in the button)
- An answer (in the hidden content)

**How to Update an FAQ:**
```html
<button class="accordion-trigger w-full px-6 md:px-8 py-5 md:py-6 flex items-center justify-between hover:bg-gray-50 transition-smooth text-left">
    <span class="text-lg md:text-xl font-bold text-gray-900 pr-4">
        What speeds can I expect with FiberNet's 1GB fiber service?
    </span>
    <i class="fas fa-chevron-down text-gray-600 flex-shrink-0"></i>
</button>
<div class="accordion-content px-6 md:px-8 pb-0 md:pb-0">
    <p class="text-gray-600 text-base md:text-lg leading-relaxed pb-6 md:pb-6">
        With our 1GB fiber optic service, you can expect download speeds up to 1,000 Mbps...
    </p>
</div>
```

1. Update the question in the `<span>` inside the button
2. Update the answer in the `<p>` inside the accordion-content div
3. Keep all class names and the chevron icon

---

### Section 9: Call-to-Action Section

**Location:** Lines 855-880

**How to Update:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white mb-4 md:mb-6">
    Ready to Experience the FiberNet Difference?
</h2>
<p class="text-lg md:text-xl text-gray-100 mb-8 md:mb-12 max-w-2xl mx-auto leading-relaxed">
    Join hundreds of thousands of satisfied customers enjoying lightning-fast fiber optic internet...
</p>
```

1. Update the heading `<h2>`
2. Update the paragraph `<p>`

---

### Section 10: Footer

**Location:** Lines 885-1000

**10a. Company Description:**
```html
<p class="text-gray-400 text-sm md:text-base leading-relaxed mb-4">
    Delivering ultra-fast fiber optic internet to homes and businesses across the nation...
</p>
```

**10b. Footer Links and Labels:**
```html
<h4 class="text-white font-bold text-lg mb-4 md:mb-6">Quick Links</h4>
<li>
    <a href="#home" class="text-gray-400 hover:text-white transition-smooth text-sm md:text-base">
        Home
    </a>
</li>
```

**10c. Contact Information:**
```html
<a href="tel:8883224944" class="text-white hover:text-gray-300 transition-smooth text-sm md:text-base font-medium">
    888-322-4944
</a>
<a href="mailto:info@bestinternetandtv.com" class="text-white hover:text-gray-300 transition-smooth text-sm md:text-base font-medium">
    info@bestinternetandtv.com
</a>
```

---

## Modifying Tailwind CSS Classes

### What are Tailwind Classes?

Tailwind CSS is a system of pre-made style codes. Instead of writing traditional CSS, you add class names to HTML elements. These class names control how things look.

**Example:**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold text-white">
    Text Here
</h1>
```

Breaking this down:
- `text-4xl` = font size (extra large)
- `md:text-6xl` = font size on medium screens (larger)
- `lg:text-7xl` = font size on large screens (even larger)
- `font-bold` = makes text bold
- `text-white` = makes text white

### Common Tailwind Classes in Your Landing Page

#### Text Sizing
```
text-sm    = small text
text-base  = normal text
text-lg    = large text
text-xl    = extra large
text-2xl   = 2x large
text-3xl   = 3x large
text-4xl   = 4x large
text-5xl   = 5x large
text-6xl   = 6x large
text-7xl   = 7x large
```

#### Text Styling
```
font-bold      = bold text
font-semibold  = semi-bold text
font-medium    = medium weight
font-light     = light weight
text-center    = center align text
text-left      = left align text
text-white     = white color
text-gray-600  = gray color
text-gray-900  = dark gray/black
```

#### Spacing
```
mb-4   = margin-bottom (space below element)
mb-6   = more space below
mt-4   = margin-top (space above element)
px-4   = padding left and right
py-4   = padding top and bottom
p-8    = padding on all sides
```

#### Responsive Design (Mobile-First)
The landing page uses these prefixes:
```
(no prefix)  = mobile phones (default)
sm:          = small tablets and up
md:          = medium tablets and up
lg:          = large screens and up
```

**Example - Understanding Responsive Classes:**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl">Heading</h1>
```
- On phones: text size = `text-4xl` (large)
- On tablets (md): text size = `text-6xl` (larger)
- On desktops (lg): text size = `text-7xl` (largest)

### How to Modify Text Size

**Goal: Make all headings larger**

**Step 1: Find a heading**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold">
    Why Choose FiberNet?
</h2>
```

**Step 2: Identify the current sizes**
- Mobile: `text-3xl`
- Tablet: `md:text-4xl`
- Desktop: `lg:text-5xl`

**Step 3: Change to larger sizes**
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Why Choose FiberNet?
</h2>
```

Now it's one size larger on each device.

### How to Modify Colors

**Finding color classes:**
```html
<p class="text-gray-600">This is gray text</p>
<button class="bg-white">White background</button>
<div class="border-2 border-gray-100">Gray border</div>
```

**Color naming system:**
- `text-` = text color
- `bg-` = background color
- `border-` = border color

**Available colors in your page:**
```
white       = pure white
gray-100    = very light gray
gray-200    = light gray
gray-300    = medium-light gray
gray-400    = medium gray
gray-600    = medium-dark gray
gray-700    = dark gray
gray-800    = darker gray
gray-900    = very dark gray (almost black)
```

**Example - Change text color:**
```html
<!-- Original - gray text -->
<p class="text-gray-600">Some text</p>

<!-- Updated - darker gray text -->
<p class="text-gray-900">Some text</p>
```

### How to Modify Button Styling

**Finding buttons:**
```html
<a href="tel:8883224944" class="cta-button text-white px-8 md:px-10 py-4 md:py-5 rounded-lg font-bold text-base md:text-lg btn-hover inline-flex items-center justify-center">
    <i class="fas fa-phone mr-3"></i>Call 888-322-4944
</a>
```

**Breaking down the classes:**
- `cta-button` = custom button styling (defined in `<style>` section)
- `text-white` = white text
- `px-8 md:px-10` = horizontal padding (left/right)
- `py-4 md:py-5` = vertical padding (top/bottom)
- `rounded-lg` = rounded corners
- `font-bold` = bold text
- `text-base md:text-lg` = text size

**Example - Make button padding larger:**
```html
<!-- Original -->
<a class="cta-button text-white px-8 md:px-10 py-4 md:py-5 rounded-lg">

<!-- Updated - larger padding -->
<a class="cta-button text-white px-10 md:px-12 py-5 md:py-6 rounded-lg">
```

### How to Modify Card Styling

**Finding cards:**
```html
<div class="card-hover bg-white border-2 border-gray-100 rounded-xl p-8 md:p-10">
    <!-- Card content -->
</div>
```

**Breaking down the classes:**
- `card-hover` = hover effect styling
- `bg-white` = white background
- `border-2 border-gray-100` = 2px gray border
- `rounded-xl` = rounded corners
- `p-8 md:p-10` = padding

**Example - Change border color:**
```html
<!-- Original - light gray border -->
<div class="card-hover bg-white border-2 border-gray-100 rounded-xl p-8 md:p-10">

<!-- Updated - darker border -->
<div class="card-hover bg-white border-2 border-gray-300 rounded-xl p-8 md:p-10">
```

### How to Modify Spacing (Margins and Padding)

**Margin classes (space outside):**
```
mb-4   = margin-bottom: 1rem (16px)
mb-6   = margin-bottom: 1.5rem (24px)
mb-8   = margin-bottom: 2rem (32px)
mt-4   = margin-top: 1rem (16px)
mx-auto = center horizontally
```

**Padding classes (space inside):**
```
p-4    = padding all sides: 1rem
p-8    = padding all sides: 2rem
px-4   = padding left/right: 1rem
px-6   = padding left/right: 1.5rem
py-4   = padding top/bottom: 1rem
py-5   = padding top/bottom: 1.25rem
```

**Example - Increase spacing between sections:**
```html
<!-- Original -->
<section class="py-16 md:py-24">

<!-- Updated - more space -->
<section class="py-20 md:py-32">
```

### How to Modify Grid Layouts

**Finding grids:**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- Three columns on desktop, one on mobile -->
</div>
```

**Breaking down the classes:**
- `grid` = creates a grid layout
- `grid-cols-1` = 1 column on mobile
- `md:grid-cols-3` = 3 columns on tablets/desktops
- `gap-8` = space between items (2rem)

**Common grid setups in your page:**
```html
<!-- 3 columns on desktop, 1 on mobile -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">

<!-- 2 columns on desktop, 1 on mobile -->
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">

<!-- 4 columns on desktop -->
<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8">
```

**Example - Change from 3 columns to 2 columns:**
```html
<!-- Original - 3 columns -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- Content -->
</div>

<!-- Updated - 2 columns -->
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
    <!-- Content -->
</div>
```

### How to Modify Gap (Space Between Grid Items)

```html
<!-- Original -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">

<!-- Updated - more space between items -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
```

**Gap sizes:**
```
gap-4  = 1rem space
gap-6  = 1.5rem space
gap-8  = 2rem space
gap-12 = 3rem space
```

### How to Modify Border Radius (Rounded Corners)

```html
<!-- Slightly rounded -->
<div class="rounded">

<!-- More rounded -->
<div class="rounded-lg">

<!-- Very rounded (circle for squares) -->
<div class="rounded-xl">

<!-- Extremely rounded -->
<div class="rounded-full">
```

### How to Modify Shadow Effects

```html
<!-- No shadow -->
<div class="bg-white">

<!-- Light shadow -->
<div class="bg-white shadow">

<!-- Medium shadow -->
<div class="bg-white shadow-md">

<!-- Strong shadow -->
<div class="bg-white shadow-lg">
```

**Example - Add shadow to cards:**
```html
<!-- Original -->
<div class="card-hover bg-white border-2 border-gray-100 rounded-xl">

<!-- Updated - with shadow -->
<div class="card-hover bg-white border-2 border-gray-100 rounded-xl shadow-lg">
```

---

## Fixing and Managing Links

### Understanding Links in Your Page

A link in HTML looks like this:
```html
<a href="destination">Link Text</a>
```

**Parts of a link:**
- `<a>` = link tag (start)
- `href="destination"` = where the link goes
- `Link Text` = what users see and click
- `</a>` = link tag (end)

### Types of Links in Your Landing Page

#### 1. Internal Links (Links to sections on the same page)

**Example:**
```html
<a href="#features">Features</a>
```

**How it works:**
- `#features` = jumps to a section with `id="features"`
- Used in navigation menus
- Used in "Learn More" buttons

**Where they appear:**
- Navigation menu (lines 237-243)
- Mobile menu (lines 259-265)
- CTA buttons throughout the page

#### 2. External Links (Links to other websites)

**Example:**
```html
<a href="https://www.example.com">Visit Example</a>
```

**How it works:**
- Full URL starting with `https://`
- Opens in same window
- To open in new window, add: `target="_blank"`

#### 3. Phone Links (Click to call)

**Example:**
```html
<a href="tel:8883224944">Call 888-322-4944</a>
```

**How it works:**
- `tel:` prefix makes it clickable on phones
- Format: `tel:` + phone number (no spaces or dashes)

#### 4. Email Links (Click to email)

**Example:**
```html
<a href="mailto:info@bestinternetandtv.com">Email Us</a>
```

**How it works:**
- `mailto:` prefix opens email client
- Format: `mailto:` + email address

### Finding All Links in Your Page

**Here's a complete list of every link in your landing page:**

| Link Type | Location (Line) | Current URL | Purpose |
|-----------|-----------------|-------------|---------|
| Internal | 245 | `#home` | Home section |
| Internal | 246 | `#features` | Features section |
| Internal | 247 | `#benefits` | Benefits section |
| Internal | 248 | `#about` | About section |
| Internal | 249 | `#testimonials` | Testimonials section |
| Internal | 250 | `#faq` | FAQ section |
| Internal | 251 | `#contact` | Contact section |
| Phone | 254 | `tel:8883224944` | Call button |
| Internal | 263-269 | `#home`, `#features`, etc. | Mobile menu links |
| Phone | 270 | `tel:8883224944` | Mobile call button |
| Phone | 301 | `tel:8883224944` | Hero call button |
| Internal | 307 | `#features` | Learn More button |
| Phone | 398 | `tel:8883224944` | Feature section call button |
| Phone | 486 | `tel:8883224944` | Benefit section call button |
| Phone | 529 | `tel:8883224944` | Benefit section call button |
| Phone | 565 | `tel:8883224944` | Benefit section call button |
| Phone | 737 | `tel:8883224944` | Testimonial section call button |
| Phone | 873 | `tel:8883224944` | CTA section call button |
| Email | 877 | `mailto:info@bestinternetandtv.com` | Email button |
| Internal | 909 | `#home` | Footer link |
| Internal | 914 | `#features` | Footer link |
| Internal | 918 | `#benefits` | Footer link |
| Internal | 922 | `#about` | Footer link |
| Internal | 926 | `#testimonials` | Footer link |
| Internal | 931 | `#faq` | Footer link |
| External | 932 | `privacy.html` | Privacy Policy |
| External | 936 | `terms.html` | Terms of Service |
| External | 940 | `blog.html` | Blog |
| Internal | 944 | `#contact` | Contact link |
| Phone | 957 | `tel:8883224944` | Phone number |
| Email | 966 | `mailto:info@bestinternetandtv.com` | Email address |
| External | 1003 | `privacy.html` | Footer privacy |
| External | 1004 | `terms.html` | Footer terms |
| External | 1005 | `blog.html` | Footer blog |

### Step-by-Step: Update the Phone Number

**Goal: Change phone number from 888-322-4944 to 888-444-5555**

**Step 1: Understand what needs to change**
- The phone number appears in BOTH the `href` AND the visible text
- You must change it in BOTH places
- Example: `<a href="tel:8883224944">Call 888-322-4944</a>`

**Step 2: Find all occurrences**
1. Open your HTML file
2. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac) to open Find
3. Type: `8883224944`
4. This will highlight every occurrence

**Step 3: Replace each one**
1. Click "Replace All" (if your editor has it)
2. OR replace each one individually:
   - Find: `8883224944`
   - Replace with: `8884445555`

**Step 4: Also update the formatted version**
1. Find: `888-322-4944`
2. Replace with: `888-444-5555`

**Step 5: Save and test**
1. Save the file (`Ctrl+S`)
2. Open in browser and refresh
3. Click a phone link to verify it works

### Step-by-Step: Update the Email Address

**Goal: Change email from info@bestinternetandtv.com to support@fibernet.com**

**Step 1: Find all occurrences**
1. Press `Ctrl+F`
2. Type: `info@bestinternetandtv.com`

**Step 2: Replace each one**
1. Find: `info@bestinternetandtv.com`
2. Replace with: `support@fibernet.com`

**Step 3: Save and test**
1. Save the file
2. Click an email link to verify it opens your email client

### Step-by-Step: Fix Broken Internal Links

**Problem: A navigation link doesn't work**

**Example scenario:**
- You have a link: `<a href="#pricing">Pricing</a>`
- But there's no section with `id="pricing"`
- Clicking the link does nothing

**Solution:**

**Step 1: Find the broken link**
```html
<a href="#pricing">Pricing</a>
```

**Step 2: Create the matching section**
1. Find where you want to add the Pricing section
2. Add a new section with the matching ID:

```html
<section id="pricing" class="py-16 md:py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
            Pricing
        </h2>
        <!-- Add your pricing content here -->
    </div>
</section>
```

**Step 3: Verify**
1. Save the file
2. Click the link in your browser
3. It should now jump to the new section

### Step-by-Step: Add a New Navigation Link

**Goal: Add a "Services" link to the navigation menu**

**Step 1: Add to desktop navigation**
1. Find the desktop navigation (around line 237)
2. Find this line:
```html
<a href="#faq" class="nav-link text-gray-700 font-medium text-sm lg:text-base">FAQ</a>
<a href="#contact" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Contact</a>
```

3. Add your new link before Contact:
```html
<a href="#faq" class="nav-link text-gray-700 font-medium text-sm lg:text-base">FAQ</a>
<a href="#services" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Services</a>
<a href="#contact" class="nav-link text-gray-700 font-medium text-sm lg:text-base">Contact</a>
```

**Step 2: Add to mobile navigation**
1. Find the mobile menu (around line 259)
2. Add the same link:
```html
<a href="#faq" class="block py-2 px-4 text-gray-700 font-medium text-sm hover:bg-gray-100 transition-smooth">FAQ</a>
<a href="#services" class="block py-2 px-4 text-gray-700 font-medium text-sm hover:bg-gray-100 transition-smooth">Services</a>
<a href="#contact" class="block py-2 px-4 text-gray-700 font-medium text-sm hover:bg-gray-100 transition-smooth">Contact</a>
```

**Step 3: Create the Services section**
1. Find where you want to add it (after FAQ, before Contact)
2. Add a new section:
```html
<section id="services" class="py-16 md:py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
            Our Services
        </h2>
        <!-- Add your services content here -->
    </div>
</section>
```

**Step 4: Save and test**
1. Save the file
2. Verify the link appears in both desktop and mobile menus
3. Click it to verify it jumps to the Services section

### Troubleshooting Links

**Problem: Link doesn't work**

| Symptom | Cause | Solution |
|---------|-------|----------|
| Internal link doesn't jump | No matching `id=` on target section | Add `id="sectionname"` to the section |
| Phone link doesn't work on mobile | Wrong format | Use `href="tel:5551234567"` (no spaces/dashes) |
| Email link doesn't open email | Wrong format | Use `href="mailto:email@example.com"` |
| External link opens in same window | Want new window | Add `target="_blank"` |

**Example - Fix phone link format:**
```html
<!-- Wrong -->
<a href="tel:888-322-4944">Call</a>

<!-- Correct -->
<a href="tel:8883224944">Call</a>
```

**Example - Make external link open in new window:**
```html
<!-- Original -->
<a href="https://example.com">Visit</a>

<!-- Updated -->
<a href="https://example.com" target="_blank">Visit</a>
```

---

## Adding Privacy and Terms Pages

### Understanding the Structure

Your landing page currently has:
- `index.html` (the main landing page)

You need to create:
- `privacy.html` (Privacy Policy)
- `terms.html` (Terms of Service)

All three files should be in the same folder.

### Step 1: Create the Privacy Policy Page

**Step 1a: Create a new file**
1. Open your text editor
2. Click File → New File
3. Save it as `privacy.html` in the same folder as `index.html`

**Step 1b: Add the HTML structure**

Copy and paste this code into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - FiberNet">
    <title>Privacy Policy - FiberNet</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center space-x-2">
                    <i class="fas fa-wifi text-3xl text-gray-900"></i>
                    <span class="text-2xl font-bold text-gray-900 hidden sm:inline">FiberNet</span>
                </div>
                <div class="flex items-center space-x-4">
                    <a href="index.html" class="text-gray-700 font-medium hover:text-gray-900">Back to Home</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>
                    FiberNet ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p>We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the Site or when you choose to participate in various activities related to the Site.</li>
                    <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase, order, return, exchange, or request information about our services from the Site.</li>
                    <li>Data From Social Networks: User information from social networks, including your name, your social network username, location, gender, birth date, email address, profile picture, and public data for contacts.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Your Information</h2>
                <p>Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Create and manage your account</li>
                    <li>Process your transactions and send related information</li>
                    <li>Email regarding your account or order</li>
                    <li>Fulfill and manage purchases, orders, payments, and other transactions related to the Site</li>
                    <li>Generate a personal profile about you in order to better understand and serve you</li>
                    <li>Increase the efficiency and operation of the Site</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the Site</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p>We may share information we have collected about you in certain situations:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information about you is necessary to comply with the law, enforce our Site policies, or protect ours or others' rights, property, or safety.</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with parties that perform services for us, including payment processors, data analysis firms, email delivery services, hosting providers, and customer service representatives.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to help protect your personal information. While we have taken reasonable steps to secure the personal information you provide to us, please be aware that despite our efforts, no security measures are perfect or impenetrable.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p>
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <div class="bg-gray-50 p-6 rounded-lg mt-4">
                    <p><strong>FiberNet</strong></p>
                    <p>Email: <a href="mailto:info@bestinternetandtv.com" class="text-blue-600 hover:underline">info@bestinternetandtv.com</a></p>
                    <p>Phone: <a href="tel:8883224944" class="text-blue-600 hover:underline">888-322-4944</a></p>
                </div>
            </div>

            <div class="mt-12 pt-8 border-t border-gray-200">
                <p class="text-gray-600 text-sm">
                    Last Updated: <span id="lastUpdated"></span>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-sm md:text-base">
                &copy; <span id="year">2024</span> FiberNet. All rights reserved.
            </p>
            <div class="mt-4 space-x-4">
                <a href="index.html" class="text-gray-400 hover:text-white transition-smooth">Home</a>
                <a href="privacy.html" class="text-gray-400 hover:text-white transition-smooth">Privacy</a>
                <a href="terms.html" class="text-gray-400 hover:text-white transition-smooth">Terms</a>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
        document.getElementById('lastUpdated').textContent = new Date().toLocaleDateString();
    </script>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**Step 2a: Create a new file**
1. Open your text editor
2. Click File → New File
3. Save it as `terms.html` in the same folder as `index.html`

**Step 2b: Add the HTML structure**

Copy and paste this code into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - FiberNet">
    <title>Terms of Service - FiberNet</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center space-x-2">
                    <i class="fas fa-wifi text-3xl text-gray-900"></i>
                    <span class="text-2xl font-bold text-gray-900 hidden sm:inline">FiberNet</span>
                </div>
                <div class="flex items-center space-x-4">
                    <a href="index.html" class="text-gray-700 font-medium hover:text-gray-900">Back to Home</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>
                    These Terms of Service constitute a legally binding agreement made between you, whether personally or on behalf of an entity ("you") and FiberNet ("we," "us," "our," or "Company"), concerning your access to and use of the fibernet.com website as well as any other media form, media channel, mobile website, or mobile application relating, linked, or otherwise connected thereto (collectively, the "Site").
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Intellectual Property Rights</h2>
                <p>
                    Unless otherwise indicated, the Site is our proprietary property and all source code, databases, functionality, software, website designs, audio, video, text, photographs, and graphics on the Site (collectively, the "Content") and the trademarks, service marks, and logos contained therein (the "Marks") are owned or controlled by us or licensed to us.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. User Representations</h2>
                <p>By using the Site, you represent and warrant that:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>All information you submit is true, accurate, current, and complete</li>
                    <li>You will maintain the accuracy of such information and promptly update such information as necessary</li>
                    <li>You have the legal capacity and you agree to comply with these Terms of Service</li>
                    <li>You are not under the age of 18</li>
                    <li>You will not access the Site through automated or non-human means, whether through a bot, script or otherwise</li>
                    <li>You will not use the Site for any illegal or unauthorized purpose</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Prohibited Activities</h2>
                <p>You may not access or use the Site for any purpose other than that for which we make the Site available. The Site may not be used in connection with any commercial endeavors except those specifically endorsed or approved by us.</p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Limitation of Liability</h2>
                <p>
                    In no event shall FiberNet or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of or in connection with the use or inability to use the materials on the Site.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Service Terms</h2>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>No long-term contracts required</li>
                    <li>Service can be cancelled anytime without penalty</li>
                    <li>5-year price guarantee on base service rate</li>
                    <li>Promotional offers are subject to terms and conditions</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications and Amendments</h2>
                <p>
                    We reserve the right, in our sole discretion, to modify or replace these Terms at any time. If a revision is material, we will try to provide at least 30 days' notice prior to any new terms taking effect. Your continued use of the Site following the posting of revised Terms means that you accept and agree to the changes.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Contact Information</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <div class="bg-gray-50 p-6 rounded-lg mt-4">
                    <p><strong>FiberNet</strong></p>
                    <p>Email: <a href="mailto:info@bestinternetandtv.com" class="text-blue-600 hover:underline">info@bestinternetandtv.com</a></p>
                    <p>Phone: <a href="tel:8883224944" class="text-blue-600 hover:underline">888-322-4944</a></p>
                </div>
            </div>

            <div class="mt-12 pt-8 border-t border-gray-200">
                <p class="text-gray-600 text-sm">
                    Last Updated: <span id="lastUpdated"></span>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-sm md:text-base">
                &copy; <span id="year">2024</span> FiberNet. All rights reserved.
            </p>
            <div class="mt-4 space-x-4">
                <a href="index.html" class="text-gray-400 hover:text-white transition-smooth">Home</a>
                <a href="privacy.html" class="text-gray-400 hover:text-white transition-smooth">Privacy</a>
                <a href="terms.html" class="text-gray-400 hover:text-white transition-smooth">Terms</a>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
        document.getElementById('lastUpdated').textContent = new Date().toLocaleDateString();
    </script>
</body>
</html>
```

### Step 3: Verify the Links in index.html

Your `index.html` already has links to these pages. Let's verify they're correct:

**Check the footer links (around lines 932, 936, 940):**
```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-smooth text-sm md:text-base">
    Privacy Policy
</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-smooth text-sm md:text-base">
    Terms of Service
</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-smooth text-sm md:text-base">
    Blog
</a>
```

These links are already correct! They point to `privacy.html` and `terms.html`.

**Also check the bottom footer (around lines 1003-1005):**
```html
<a href="privacy.html" class="hover:text-white transition-smooth">Privacy Policy</a>
<a href="terms.html" class="hover:text-white transition-smooth">Terms of Service</a>
<a href="blog.html" class="hover:text-white transition-smooth">Blog</a>
```

These are also correct!

### Step 4: File Organization

Your file structure should look like this:

```
project-folder/
├── index.html          (your main landing page)
├── privacy.html        (new file you created)
├── terms.html          (new file you created)
└── blog.html           (optional - create if needed)
```

**Important:** All files must be in the SAME folder for the links to work.

### Step 5: Test the Links

1. **Save all files** (`Ctrl+S`)
2. **Open `index.html` in your browser**
3. **Scroll to the footer**
4. **Click "Privacy Policy"** - it should open `privacy.html`
5. **Click "Terms of Service"** - it should open `terms.html`
6. **Click "Back to Home"** on either page - it should return to `index.html`

### Step 6: Customize the Policy Pages

The policy pages include placeholder text. You should update them with your actual policies:

**In `privacy.html`, update:**
- Section 2 (Information We Collect) - describe what data you actually collect
- Section 3 (Use of Your Information) - explain how you use the data
- Contact information

**In `terms.html`, update:**
- Section 6 (Service Terms) - match your actual service terms
- Any other sections specific to your business

### Common Issues and Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| Links don't work | Files in different folders | Put all HTML files in the same folder |
| Page shows 404 error | Wrong filename | Make sure filename matches exactly (case-sensitive) |
| Links work but styling looks off | CSS not loading | Ensure `<script src="https://cdn.tailwindcss.com"></script>` is in the head |
| "Back to Home" doesn't work | Wrong path | Use `href="index.html"` not `href="../index.html"` |

---

## Common Customizations

### Customization 1: Change Company Name

**Goal: Change "FiberNet" to your actual company name**

**Step 1: Find all occurrences**
1. Press `Ctrl+F`
2. Type: `FiberNet`
3. You'll see it appears many times

**Step 2: Replace strategically**

**Important locations:**
- Logo/Header (line 235)
- Hero section heading (line 287)
- Feature section heading (line 327)
- About section (lines 568-590)
- Footer (lines 892, 928)

**Example - Update logo:**
```html
<!-- Original -->
<span class="text-2xl font-bold text-gray-900 hidden sm:inline">FiberNet</span>

<!-- Updated -->
<span class="text-2xl font-bold text-gray-900 hidden sm:inline">YourCompanyName</span>
```

**Step 3: Save and verify**

---

### Customization 2: Change Hero Background Image

**Goal: Use a different background image for the hero section**

**Step 1: Find the hero section**
```html
<section id="home" class="relative h-screen md:h-[600px] bg-cover bg-center flex items-center justify-center overflow-hidden" style="background-image: url('https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80');">
```

**Step 2: Get a new image URL**

You can get free images from:
- Unsplash: https://unsplash.com
- Pexels: https://pexels.com
- Pixabay: https://pixabay.com

**Step 3: Replace the URL**

1. Find an image related to internet/fiber optics
2. Copy the image URL
3. Replace the URL in the code:

```html
<!-- Original -->
style="background-image: url('https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80');"

<!-- Updated -->
style="background-image: url('YOUR_NEW_IMAGE_URL_HERE');"
```

**Example:**
```html
style="background-image: url('https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=1600&h=900&fit=crop&q=80');"
```

**Step 4: Save and refresh**

---

### Customization 3: Change Colors

**Goal: Change the accent color from dark gray to blue**

**Step 1: Understand the current colors**

Your page uses:
- Dark gray (`#1f2937` and `#111827`)
- Light gray (`#f3f4f6`, `#e5e7eb`)
- White (`#ffffff`)

**Step 2: Find color definitions**

In the `<style>` section (around lines 20-100):
```css
.gradient-accent {
    background: linear-gradient(135deg, #1f2937 0%, #111827 100%);
}
```

**Step 3: Replace with new color**

For example, to use blue:
```css
.gradient-accent {
    background: linear-gradient(135deg, #1e40af 0%, #1e3a8a 100%);
}
```

**Step 4: Update Tailwind classes**

Find all instances of `text-gray-900` and replace with `text-blue-900`:
1. Press `Ctrl+H` to open Find and Replace
2. Find: `text-gray-900`
3. Replace with: `text-blue-900`

**Step 5: Save and test**

---

### Customization 4: Add a New Feature Card

**Goal: Add a 4th feature card to the Features section**

**Step 1: Find the Features section**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-6 lg:gap-8">
    <!-- Three feature cards here -->
</div>
```

**Step 2: Change grid from 3 columns to 4**

Find this line (around 340):
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-6 lg:gap-8">
```

Change to:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 md:gap-6 lg:gap-8">
```

**Step 3: Add a new feature card**

Copy one of the existing feature cards and add it after the 3rd one:

```html
<!-- New Feature 4 -->
<div class="card-hover bg-white border-2 border-gray-100 rounded-xl p-8 md:p-10">
    <div class="mb-6 flex justify-center">
        <div class="bg-gradient-to-br from-gray-100 to-gray-200 rounded-full p-6 md:p-8">
            <i class="fas fa-headset feature-icon"></i>
        </div>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 text-center mb-4">
        24/7 Customer Support
    </h3>
    <p class="text-gray-600 text-center text-sm md:text-base leading-relaxed mb-6">
        Our dedicated support team is available round-the-clock to help with any questions or issues. Get fast, friendly service whenever you need it.
    </p>
    <div class="flex items-center justify-center text-gray-900 font-semibold text-sm md:text-base">
        <i class="fas fa-star mr-2 text-gray-700"></i>
        <span>Always Here For You</span>
    </div>
</div>
```

**Step 4: Save and verify**

---

### Customization 5: Change Button Colors

**Goal: Change CTA buttons from dark gray to green**

**Step 1: Find button styling in CSS**

In the `<style>` section:
```css
.cta-button {
    background: linear-gradient(135deg, #1f2937 0%, #111827 100%);
    transition: all 0.3s ease-in-out;
}

.cta-button:hover {
    transform: scale(1.05);
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.3);
}
```

**Step 2: Replace with green**

```css
.cta-button {
    background: linear-gradient(135deg, #059669 0%, #047857 100%);
    transition: all 0.3s ease-in-out;
}

.cta-button:hover {
    transform: scale(1.05);
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.3);
}
```

**Step 3: Save and test**

---

### Customization 6: Add Social Media Links

**Goal: Add Instagram and Facebook links to the footer**

**Step 1: Find the social media section**

In the footer (around line 895):
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-facebook"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-twitter"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-instagram"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-linkedin"></i>
    </a>
</div>
```

**Step 2: Replace # with actual URLs**

```html
<div class="flex space-x-4">
    <a href="https://www.facebook.com/yourpage" target="_blank" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-facebook"></i>
    </a>
    <a href="https://www.twitter.com/yourhandle" target="_blank" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-twitter"></i>
    </a>
    <a href="https://www.instagram.com/yourprofile" target="_blank" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-instagram"></i>
    </a>
    <a href="https://www.linkedin.com/company/yourcompany" target="_blank" class="text-gray-400 hover:text-white transition-smooth text-lg">
        <i class="fab fa-linkedin"></i>
    </a>
</div>
```

**Important:** 
- Add `target="_blank"` so links open in new windows
- Replace URLs with your actual social media profiles

**Step 3: Save and test**

---

## Troubleshooting

### Issue 1: Page Looks Broken After Editing

**Symptoms:**
- Text overlapping
- Buttons in wrong places
- Colors changed unexpectedly

**Solutions:**

1. **Check for missing closing tags**
   - Every `<div>` needs a `</div>`
   - Every `<a>` needs a `</a>`
   - Look for red squiggly lines in your editor

2. **Undo recent changes**
   - Press `Ctrl+Z` multiple times to undo
   - Or reload the original file

3. **Check for typos in class names**
   - Tailwind classes are case-sensitive
   - `md:text-6xl` ≠ `md:text-6XL`

---

### Issue 2: Links Don't Work

**Symptoms:**
- Clicking a link does nothing
- Page doesn't navigate

**Solutions:**

1. **Check the href attribute**
   ```html
   <!-- Wrong -->
   <a href="#feature">Link</a>
   
   <!-- Correct -->
   <a href="#features">Link</a>
   ```

2. **Verify section IDs match**
   ```html
   <!-- Navigation link -->
   <a href="#features">Features</a>
   
   <!-- Must have matching section -->
   <section id="features">...</section>
   ```

3. **For external links, use full URLs**
   ```html
   <!-- Wrong -->
   <a href="example.com">Link</a>
   
   <!-- Correct -->
   <a href="https://example.com">Link</a>
   ```

---

### Issue 3: Text Not Displaying Correctly

**Symptoms:**
- Text too small or too large
- Text color invisible
- Text cut off

**Solutions:**

1. **Check text color vs background**
   ```html
   <!-- Problem: white text on white background -->
   <div class="bg-white text-white">Can't read</div>
   
   <!-- Solution: dark text on white background -->
   <div class="bg-white text-gray-900">Can read</div>
   ```

2. **Check responsive classes**
   ```html
   <!-- Might be too small on mobile -->
   <h1 class="text-2xl">Heading</h1>
   
   <!-- Better: larger on all devices -->
   <h1 class="text-4xl md:text-6xl lg:text-7xl">Heading</h1>
   ```

3. **Check for truncated text**
   ```html
   <!-- If text is cut off, remove width limits or increase them -->
   <p class="w-32">This text might be cut off</p>
   <p class="max-w-4xl">This text wraps nicely</p>
   ```

---

### Issue 4: Mobile Menu Not Working

**Symptoms:**
- Menu button doesn't open
- Menu items don't appear on mobile

**Solutions:**

1. **Check JavaScript is enabled**
   - This page requires JavaScript to work
   - Make sure your browser has JavaScript enabled

2. **Verify mobile menu HTML is present**
   - Find the mobile menu section (around line 259)
   - Make sure it's not deleted

3. **Check for console errors**
   - Press `F12` to open Developer Tools
   - Look for red error messages
   - Take note of any errors

---

### Issue 5: Images Not Displaying

**Symptoms:**
- Broken image icons
- Blank spaces where images should be

**Solutions:**

1. **Check image URLs are valid**
   ```html
   <!-- Wrong: broken link -->
   <img src="https://example.com/image.jpg">
   
   <!-- Correct: valid link -->
   <img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80">
   ```

2. **Verify image URLs are complete**
   - URLs should start with `https://`
   - Not just `/path/to/image.jpg`

3. **Check image file exists**
   - If using local images, make sure file is in the same folder
   - Use relative paths: `<img src="image.jpg">`

---

### Issue 6: Styling Not Updating

**Symptoms:**
- Changes don't appear in browser
- Old styling still showing

**Solutions:**

1. **Clear browser cache**
   - Press `Ctrl+Shift+Delete`
   - Select "Cached images and files"
   - Click "Clear"

2. **Hard refresh the page**
   - Press `Ctrl+Shift+R` (Windows)
   - Press `Cmd+Shift+R` (Mac)

3. **Close and reopen browser**
   - Sometimes browser cache is stubborn
   - Closing completely and reopening helps

---

### Issue 7: Form Not Working

**Symptoms:**
- Can't enter text in forms
- Submit button doesn't work

**Current Status:**
- Your landing page doesn't have a form
- Contact is done via phone/email links

**If you add a form later:**
- You'll need a backend service (like Formspree, Netlify Forms)
- Just having HTML isn't enough to process submissions

---

## Quick Reference

### File Locations for Common Updates

| What to Update | File | Approximate Line |
|---|---|---|
| Company name | index.html | 235, 287, 892 |
| Phone number | index.html | 254, 270, 301, etc. (many places) |
| Email address | index.html | 877, 966 |
| Hero text | index.html | 287, 295 |
| Feature titles | index.html | 350, 368, 386 |
| Testimonials | index.html | 650-730 |
| FAQ items | index.html | 735-850 |
| Footer links | index.html | 900-945 |
| Button colors | index.html | 95-98 (CSS section) |
| Text sizes | index.html | Varies (Tailwind classes) |

### Keyboard Shortcuts

```
Ctrl+S          Save file
Ctrl+Z          Undo
Ctrl+Y          Redo
Ctrl+F          Find text
Ctrl+H          Find and Replace
Ctrl+A          Select all
Ctrl+C          Copy
Ctrl+V          Paste
F5              Refresh browser
Ctrl+Shift+R    Hard refresh browser (clear cache)
F12             Open Developer Tools
```

### Tailwind Class Cheat Sheet

**Text:**
```
text-white          white text
text-gray-900       dark gray text
text-sm/base/lg/xl  text sizes
font-bold           bold text
text-center         center align
```

**Spacing:**
```
mb-4                margin bottom
mt-4                margin top
p-8                 padding all sides
px-6                padding left/right
py-4                padding top/bottom
```

**Colors:**
```
bg-white            white background
bg-gray-50          light gray background
border-gray-100     light gray border
```

**Responsive:**
```
md:text-6xl         larger text on medium screens
lg:grid-cols-3      3 columns on large screens
hidden md:block     hidden on mobile, visible on tablet+
```

---

## Getting Help

### Resources

- **Tailwind CSS Docs:** https://tailwindcss.com/docs
- **HTML Reference:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **Font Awesome Icons:** https://fontawesome.com/icons
- **Unsplash Images:** https://unsplash.com
- **Color Picker:** https://htmlcolorcodes.com

### Common Questions

**Q: How do I change the font?**
A: The font is defined in the `<style>` section:
```css
body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', sans-serif;
}
```

**Q: How do I add a new section?**
A: Copy an existing section and modify the content. Remember to add an `id` if you want it in the navigation menu.

**Q: How do I change spacing between elements?**
A: Use margin (`m-`) and padding (`p-`) classes. Larger numbers = more space.

**Q: Can I use this on mobile?**
A: Yes! The page is fully responsive and works on all devices.

**Q: How do I deploy this online?**
A: You'll need web hosting. Popular options:
- Netlify (easy, free tier available)
- Vercel (great for developers)
- Bluehost (traditional hosting)
- GoDaddy (domain + hosting)

---

## Summary

You now have a complete guide for:

✅ **Updating Text Content** - Change any text on the page
✅ **Modifying Tailwind CSS** - Adjust colors, sizes, spacing
✅ **Managing Links** - Fix, update, and add new links
✅ **Adding Policy Pages** - Create Privacy and Terms pages
✅ **Common Customizations** - Make popular changes easily
✅ **Troubleshooting** - Fix common problems

**Next Steps:**

1. Start with small changes (text updates)
2. Test each change in your browser
3. Save frequently
4. Use Ctrl+Z if something breaks
5. Reference this guide as needed

Good luck with your FiberNet landing page! 🚀