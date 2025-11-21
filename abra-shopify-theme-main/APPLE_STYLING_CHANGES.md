# Apple-Inspired Styling Changes

This document outlines the comprehensive styling changes made to transform the Shopify theme to match Apple's brand aesthetic.

## Overview

The theme has been updated with three custom CSS files that override the default styling to create a clean, minimalist design inspired by Apple's website:

1. **apple-style.css** - Core Apple design system
2. **apple-header-enhancements.css** - Navigation and header styling
3. **apple-product-page.css** - Product page enhancements

## Key Design Elements

### Typography
- **Font Family**: Apple's system fonts (-apple-system, SF Pro Display, SF Pro Text)
- **Letter Spacing**: Tighter, Apple-style spacing (-0.022em to -0.05em)
- **Font Weights**: Clean hierarchy with 400, 600, and 700 weights
- **Font Smoothing**: Antialiased rendering for crisp text

### Color Palette
- **Apple White**: rgb(255, 255, 255)
- **Apple Black**: rgb(29, 29, 31)
- **Apple Gray**: rgb(134, 142, 150)
- **Apple Light Gray**: rgb(245, 245, 247)
- **Apple Dark Gray**: rgb(66, 66, 69)
- **Apple Blue**: rgb(0, 113, 227) - Primary action color

### Spacing System
- **Extra Small**: 0.5rem
- **Small**: 1rem
- **Medium**: 2rem
- **Large**: 4rem
- **Extra Large**: 6rem
- **2X Large**: 8rem

## Component Styling

### Header & Navigation
- **Sticky header** with blur effect (backdrop-filter)
- **Translucent background**: rgba(255, 255, 255, 0.72) with 20px blur
- **Clean navigation items** with hover effects
- **Minimalist icons** with subtle opacity transitions
- **Smooth underline animations** on menu items

### Buttons
- **Pill-shaped buttons** with 980px border-radius
- **Primary button**: Apple blue with white text
- **Hover effects**: Subtle scale (1.02) and shadow
- **Secondary buttons**: Outlined style with blue border

### Cards & Product Cards
- **Rounded corners**: 18px border-radius
- **Subtle shadows**: 0 2px 8px rgba(0, 0, 0, 0.06)
- **Hover effect**: translateY(-4px) with enhanced shadow
- **Clean borders**: 1px solid rgba(0, 0, 0, 0.06)

### Product Pages
- **Large, bold titles**: Up to 6rem on desktop
- **Clean variant selectors**: Pill-style with rounded edges
- **Minimalist quantity selector**: Integrated design in light gray
- **Prominent Add to Cart**: Full-width Apple blue button
- **Product images**: Rounded corners with subtle shadows

### Forms & Inputs
- **Background**: Light gray (245, 245, 247)
- **Border radius**: 8px-12px for smooth corners
- **Focus states**: Blue outline with glow effect
- **Placeholder text**: Muted gray

### Hero Sections
- **Large typography**: Up to 6rem headlines
- **Gradient overlays**: Subtle dark gradients for text readability
- **Backdrop blur**: 10px blur for depth

### Footer
- **Background**: Light gray (245, 245, 247)
- **Small caps headings**: 0.75rem with letter spacing
- **Clean links**: Dark gray with blue hover

## Technical Enhancements

### Performance
- **CSS Custom Properties**: For consistent theming
- **Optimized transitions**: cubic-bezier(0.4, 0, 0.2, 1)
- **Smooth scrolling**: Enabled for better UX

### Accessibility
- **Focus states**: 2px solid outline with offset
- **Contrast ratios**: Maintained for readability
- **Font rendering**: Optimized with text-rendering: optimizeLegibility

### Responsive Design
- **Mobile-first**: Scales appropriately on all devices
- **Breakpoints**: 750px (tablet), 990px (desktop)
- **Touch targets**: Adequate size for mobile interaction

## Files Modified

### Theme Files
- `layout/theme.liquid` - Added three new CSS file references

### New CSS Files
- `assets/apple-style.css` - 600+ lines of core styling
- `assets/apple-header-enhancements.css` - Navigation and header styles
- `assets/apple-product-page.css` - Product page specific styling

## Usage

The styles are automatically applied through the theme.liquid file. No additional configuration is needed. The CSS follows a cascade approach where Apple styles override base styles while maintaining theme functionality.

## Design Philosophy

The styling follows Apple's core design principles:

1. **Minimalism**: Clean, uncluttered interfaces
2. **White Space**: Generous spacing for breathing room
3. **Typography**: Clear hierarchy with system fonts
4. **Subtle Details**: Smooth transitions and hover effects
5. **User Focus**: Accessibility and usability first
6. **Performance**: Optimized CSS with minimal overhead

## Browser Support

- Modern browsers with CSS3 support
- Backdrop-filter support (Safari, Chrome, Edge)
- Graceful degradation for older browsers

## Notes

- The styling maintains compatibility with Shopify's theme structure
- Original base.css is preserved - new styles layer on top
- All custom properties use the `--apple-` prefix for clarity
- Responsive breakpoints align with Shopify standards
