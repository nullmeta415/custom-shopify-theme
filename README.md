# Custom Featured Products - Shopify Section

A fully customizable, responsive Shopify section for showcasing featured products with dynamic grid layouts and merchant-friendly controls.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Shopify](https://img.shields.io/badge/Shopify-Compatible-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Customization Options](#customization-options)
- [Technical Details](#technical-details)
- [Browser Support](#browser-support)
- [Troubleshooting](#troubleshooting)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🎯 Overview

**Custom Featured Products** is a professional-grade Shopify section that allows merchants to showcase selected products in a beautiful, responsive grid layout. Built with modern web standards and Shopify best practices, this section provides extensive customization options without requiring any coding knowledge.

### Why This Section?

- **Zero Dependencies**: Self-contained with inline CSS, no external files needed
- **Merchant-Friendly**: Intuitive controls in the Shopify theme editor
- **Performance Optimized**: Lazy loading, optimized images, efficient CSS Grid
- **Fully Responsive**: Perfect display on desktop, tablet, and mobile devices
- **Production Ready**: Handles edge cases, includes fallbacks, error-free

---

## ✨ Features

### Core Functionality
- ✅ **Product Selection**: Choose up to 12 products via intuitive picker
- ✅ **Dynamic Grid Layouts**: 2, 3, or 4 columns on desktop
- ✅ **Mobile Responsive**: Automatically adapts to single column on mobile
- ✅ **Display Limit Control**: Show 2-12 products (even if more are selected)
- ✅ **Sale Price Display**: Automatically shows compare-at prices with strikethrough
- ✅ **Image Optimization**: Automatic resizing and lazy loading
- ✅ **Placeholder Handling**: Graceful fallback for products without images

### Customization Options
- 🎨 **Custom Section Title**: Add/remove section heading
- 🎨 **Color Controls**: Background, title, button background, and button text colors
- 🎨 **View All Button**: Optional CTA with custom text and link
- 🎨 **Hover Effects**: Smooth transitions and interactive animations
- 🎨 **Flexible Layout**: Adjustable grid columns for different use cases

### User Experience
- 🚀 **Fast Loading**: Optimized images and lazy loading
- 🚀 **Smooth Animations**: Card hover effects and button interactions
- 🚀 **Empty State Guidance**: Clear instructions when no products selected
- 🚀 **Accessibility Ready**: Semantic HTML and proper alt tags
- 🚀 **SEO Friendly**: Proper heading hierarchy and structured markup

---

## 🖼️ Demo

### Desktop View (3 Columns)
```
┌─────────────────────────────────────────────────┐
│           Featured Products                      │
├────────────┬────────────┬─────────────┐
│  Product 1 │ Product 2  │  Product 3  │
│  $29.99    │ $39.99     │  $49.99     │
├────────────┼────────────┼─────────────┤
│  Product 4 │ Product 5  │  Product 6  │
│  $19.99    │ $59.99     │  $34.99     │
└────────────┴────────────┴─────────────┘
         [View All Products]
```

### Mobile View (1 Column)
```
┌──────────────────┐
│ Featured Products│
├──────────────────┤
│   Product 1      │
│   $29.99         │
├──────────────────┤
│   Product 2      │
│   $39.99         │
├──────────────────┤
│   Product 3      │
│   $49.99         │
└──────────────────┘
  [View All Products]
```

---

## 🚀 Installation

### Prerequisites
- Shopify store with theme development access
- Shopify CLI installed ([Installation Guide](https://shopify.dev/docs/themes/tools/cli/install))
- Code editor (VS Code, Sublime Text, etc.)
- Basic understanding of Shopify themes

### Step-by-Step Installation

#### 1. Clone or Download Theme
```bash
# Authenticate with Shopify
shopify login

# Pull your current theme
shopify theme pull
```

#### 2. Create Section File
Create a new file at: `sections/custom-featured-products.liquid`

#### 3. Add the Code
Copy the complete section code into the file (available in the project repository).

#### 4. Push to Shopify
```bash
# Push changes to your store
shopify theme push
```

#### 5. Verify Installation
- Go to **Online Store → Themes → Customize**
- Click **Add Section**
- Look for **"Custom Featured Products"** in the section list

---

## 📖 Usage

### Adding the Section

1. **Open Theme Editor**
   - Navigate to **Online Store → Themes**
   - Click **Customize** on your active theme

2. **Add the Section**
   - Choose a page/template (Homepage, Product page, etc.)
   - Click **Add Section**
   - Select **Custom Featured Products**

3. **Configure Settings**
   - Select products to feature
   - Customize title, layout, and colors
   - Enable/disable View All button
   - Save changes

### Basic Configuration Example

```plaintext
Section Title: "Best Sellers"
Products Selected: 6 products
Products to Show: 6
Products per Row: 3
Background Color: #ffffff
Title Color: #000000
Show View All: Yes
Button Text: "Shop All Best Sellers"
Button Link: /collections/best-sellers
```

---

## ⚙️ Customization Options

### Section Settings

| Setting | Type | Default | Description |
|---------|------|---------|-------------|
| **Section Title** | Text | "Featured Products" | Main heading (leave blank to hide) |
| **Products** | Product List | Empty | Select up to 12 products |
| **Products to Show** | Range (2-12) | 6 | Limit displayed products |
| **Products per Row** | Range (2-4) | 3 | Desktop column count |
| **Show View All Button** | Checkbox | Yes | Toggle button visibility |
| **Button Text** | Text | "View All Products" | CTA button label |
| **Button Link** | URL | Empty | Link destination |
| **Background Color** | Color | #ffffff | Section background |
| **Title Color** | Color | #000000 | Heading text color |
| **Button Color** | Color | #000000 | Button background |
| **Button Text Color** | Color | #ffffff | Button text color |

### Layout Options

#### 2 Columns (Wide Cards)
Best for: Detailed product views, fewer products
```css
Grid: 2 equal columns on desktop
Mobile: 1 column
```

#### 3 Columns (Balanced)
Best for: Most use cases, balanced layout
```css
Grid: 3 equal columns on desktop
Mobile: 1 column
```

#### 4 Columns (Compact)
Best for: Showing many products, compact displays
```css
Grid: 4 equal columns on desktop
Mobile: 1 column
```

---

## 🛠️ Technical Details

### File Structure
```
sections/
└── custom-featured-products.liquid
    ├── Liquid Code (HTML structure)
    ├── {% style %} (Inline CSS)
    └── {% schema %} (Settings configuration)
```

### Key Technologies
- **Liquid**: Shopify templating language
- **CSS Grid**: Modern responsive layouts
- **Lazy Loading**: Native browser image optimization
- **Shopify Filters**: Money formatting, image URLs, color manipulation

### Code Architecture

#### 1. Liquid Logic Flow
```liquid
1. Check if section title exists → Display or hide
2. Check if products selected → Show grid or empty state
3. Loop through products → Generate product cards
4. Check for sale prices → Display pricing logic
5. Check button setting → Show or hide CTA
```

#### 2. Responsive CSS Strategy
```css
/* Mobile-first approach */
Base: Single column, flexible width
Breakpoint (768px+): Multi-column grid based on settings
```

#### 3. Schema Structure
```json
{
  "name": "Display name in editor",
  "settings": [
    {/* Content settings */},
    {/* Layout settings */},
    {/* Color settings */}
  ],
  "presets": [{/* Default configuration */}]
}
```

### Performance Optimizations

- **Image Optimization**: Dynamic resizing to 600px width
- **Lazy Loading**: Images load only when scrolling into view
- **CSS Efficiency**: Single inline stylesheet, no external requests
- **Minimal JavaScript**: Zero JS dependencies
- **Grid System**: Hardware-accelerated CSS Grid

---

## 🐛 Troubleshooting

### Common Issues & Solutions

#### Section Not Appearing in Editor
**Problem**: Can't find "Custom Featured Products" when adding section

**Solutions**:
- ✅ Verify file is in `sections/` folder
- ✅ Check filename: `custom-featured-products.liquid`
- ✅ Run `shopify theme push` again
- ✅ Validate schema JSON syntax
- ✅ Clear browser cache (Cmd/Ctrl + Shift + R)

#### Products Not Displaying
**Problem**: Section shows but no products appear

**Solutions**:
- ✅ Verify products are selected in settings
- ✅ Check products are published (not drafts)
- ✅ Increase "Products to Show" slider
- ✅ Check browser console for Liquid errors

#### Grid Layout Issues
**Problem**: All products in single column on desktop

**Solutions**:
- ✅ Check browser supports CSS Grid (not IE11)
- ✅ Inspect element to verify grid classes applied
- ✅ Check viewport width is 768px+ for multi-column
- ✅ Look for CSS conflicts from theme

#### Schema/JSON Errors
**Problem**: Settings don't appear or can't save

**Solutions**:
- ✅ Validate JSON at [jsonlint.com](https://jsonlint.com)
- ✅ Remove trailing commas in arrays
- ✅ Use double quotes, not single quotes
- ✅ Match all opening/closing brackets

---

## 🚀 Future Enhancements

### Planned Features
- [ ] Quick view modal on product click
- [ ] Add to cart buttons on cards
- [ ] Product filtering by tag/collection
- [ ] Carousel/slider view option
- [ ] Product badge support ("New", "Sale", etc.)
- [ ] Video support for products
- [ ] Variant selector on cards
- [ ] Wishlist integration
- [ ] Comparison feature
- [ ] Advanced animations (AOS, GSAP)

### Advanced Customizations
- [ ] Custom card templates
- [ ] Integration with review apps
- [ ] Stock level indicators
- [ ] Countdown timers for sales
- [ ] Social proof badges
- [ ] Related products suggestions

---

## 🔗 Useful Links

- [Shopify Liquid Documentation](https://shopify.dev/docs/api/liquid)
- [Theme Development Guide](https://shopify.dev/docs/themes)
- [Shopify CLI Reference](https://shopify.dev/docs/themes/tools/cli)
- [CSS Grid Complete Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Shopify Partners](https://partners.shopify.com/)
