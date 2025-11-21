# Literary AI Shopify Theme

A custom Shopify theme combining sage (wisdom) and magician (mystery) archetypes for a literary AI analysis service. This theme showcases three main product offerings: AI-generated world maps, character family trees, and narrative timelines.

## 🎨 Design Philosophy

### Archetype Combination

**Sage Archetype - Wisdom & Knowledge**
- Represents deep understanding, scholarly wisdom, and analytical thinking
- Visual elements: Sage greens (#7A9B76, #9CAF88), classic serif typography
- Conveys authority, expertise, and trustworthiness

**Magician Archetype - Mystery & Transformation**
- Represents transformation, wonder, creative power, and possibility
- Visual elements: Deep purples (#6B4C9A, #9370DB), golden accents (#B8860B)
- Conveys enchantment, transformation, and making dreams reality

## 📁 Project Structure

```
abra-shopify-theme-main/
├── assets/
│   └── literary-sage-magician-theme.css.liquid  # Custom brand styling with Liquid variables
├── config/
│   └── settings_schema.json                     # Theme customization options
├── layout/
│   └── theme.liquid                             # Main theme layout
├── sections/
│   ├── literary-ai-hero.liquid                  # Homepage hero section with schema
│   └── literary-services.liquid                 # Services multicolumn section
├── snippets/
│   ├── literary-ai-nav.liquid                   # Custom navigation component
│   └── literary-ai-footer.liquid                # Branded footer component
├── templates/
│   └── index.json                               # Customized homepage template
├── docs/
│   └── style_guide.md                          # Design system documentation
├── THEME_DOCUMENTATION.md                       # Detailed theme documentation
└── README.md                                    # This file
```

## 🚀 Quick Start

### Prerequisites

- Shopify Partner Account ([partners.shopify.com](https://partners.shopify.com))
- Shopify CLI installed
- Git installed and configured
- Development store created

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd crispy-eureka
   ```

2. **Navigate to theme directory**
   ```bash
   cd abra-shopify-theme-main
   ```

3. **Connect to your Shopify store**
   ```bash
   shopify theme dev --store your-store-name.myshopify.com
   ```

4. **Push to store (creates unpublished theme)**
   ```bash
   shopify theme push --store your-store-name.myshopify.com --unpublished
   ```

## 🎨 Color Palette

| Color Type | Hex Code | CSS Variable | Usage |
|------------|----------|--------------|-------|
| Sage Primary | #7A9B76 | `--sage-primary` | Primary accent, borders, secondary buttons |
| Sage Light | #9CAF88 | `--sage-light` | Light backgrounds, hover states |
| Sage Deep | #4A5D23 | `--sage-deep` | Deep accents, headings |
| Magician Primary | #6B4C9A | `--magician-primary` | Primary headings, main brand color |
| Magician Light | #9370DB | `--magician-light` | Accents, hover effects |
| Magician Gold | #B8860B | `--magician-gold` | Prices, decorative elements |
| Parchment BG | #F5F3EE | `--parchment-bg` | Main background, scholarly feel |
| Text Primary | #2C2C2C | `--text-primary` | Body text |

## ⚙️ Theme Customization

### Through Shopify Admin

1. Navigate to **Online Store → Themes**
2. Click **Customize** on your theme
3. Go to **Theme Settings → Literary AI Branding**

Available settings:
- **Brand Identity**: Site title, subtitle, tagline
- **Colors**: All sage and magician palette colors
- **Typography**: Serif font toggle

### Theme Settings (Liquid Variables)

The theme uses Liquid settings that can be accessed in templates:

```liquid
{{ settings.site_title }}              <!-- Site Title -->
{{ settings.site_subtitle }}           <!-- Site Subtitle -->
{{ settings.brand_primary }}           <!-- Sage Primary Color -->
{{ settings.brand_accent }}            <!-- Magician Primary Color -->
{{ settings.brand_gold }}              <!-- Magician Gold Accent -->
{{ settings.brand_warm_white }}        <!-- Background Color -->
```

## 📄 Custom Sections

### Literary AI Hero Section

Location: `sections/literary-ai-hero.liquid`

Features:
- Background image support
- Configurable heading sizes
- Primary and secondary CTAs
- Responsive design
- Mystical gradient overlay

Schema Blocks:
- Heading (limit: 1)
- Subtitle (limit: 1)
- Description (limit: 1)
- Buttons (limit: 1)

### Literary Services Section

Location: `sections/literary-services.liquid`

Features:
- Customizable grid layout (1-4 columns)
- Font Awesome icon support
- Optional service images
- Hover effects with gradient borders
- Mobile-responsive

Service Blocks:
- Icon class (Font Awesome)
- Service title and description
- Optional image
- Call-to-action link

## 🧩 Custom Components

### Navigation (Snippet)

Location: `snippets/literary-ai-nav.liquid`

Features:
- Sticky navigation
- Logo or text branding
- Mobile hamburger menu
- Cart with item count
- Hover effects with gradient underlines

### Footer (Snippet)

Location: `snippets/literary-ai-footer.liquid`

Features:
- Four-column grid layout
- Social media links
- Newsletter signup form
- Quick links and support
- Sage-to-magician gradient background

## 🎯 Key Features

### Typography
- **Headings**: Baskerville, Georgia (serif) - conveys wisdom and authority
- **Body**: Georgia, Garamond (serif) - readable and scholarly
- **Letter Spacing**: Slightly increased for elegant, mystical feel

### Interactive Elements
- **Buttons**: Gradient backgrounds with mystical glow on hover
- **Cards**: Subtle lift animation with purple shadow on hover
- **Links**: Gradient underline animation
- **Mystical Effects**: Pulsing shadows and smooth transitions

### Responsive Design
- Mobile-first approach
- Breakpoints:
  - Mobile: < 749px
  - Tablet: 750px - 989px
  - Desktop: 990px+
- Adaptive typography and layouts

## 📱 Responsive Testing

Test the theme on:
- Desktop (1920x1080, 1440x900)
- Tablet (768x1024, landscape and portrait)
- Mobile (375x667, 414x896)

Use Chrome DevTools or Shopify's theme preview across devices.

## 🛠️ Development Workflow

### Local Development

```bash
# Start development server with live reload
shopify theme dev --store your-store-name.myshopify.com

# Access preview URL (usually http://127.0.0.1:9292)
```

### Making Changes

1. Edit files locally
2. Changes auto-reload in browser (with theme dev)
3. Test across devices
4. Commit changes to Git
5. Push to Shopify when ready

### Git Workflow

```bash
# Stage changes
git add .

# Commit with descriptive message
git commit -m "feat: Add new feature description"

# Push to remote
git push origin branch-name
```

## 📦 Deployment

### Push to Development Store

```bash
# Push as unpublished theme
shopify theme push --store your-store-name.myshopify.com --unpublished

# Push and publish immediately
shopify theme push --store your-store-name.myshopify.com --live
```

### Share Preview

```bash
# Get shareable preview link
shopify theme share --store your-store-name.myshopify.com --theme THEME_ID
```

## 🎓 Learning Resources

### Shopify Development
- [Shopify Theme Development](https://shopify.dev/docs/themes)
- [Liquid Template Language](https://shopify.dev/docs/api/liquid)
- [Theme Architecture](https://shopify.dev/docs/themes/architecture)

### This Project
- See `THEME_DOCUMENTATION.md` for detailed theme documentation
- See `docs/style_guide.md` for design system details
- Review section files for schema examples

## 🐛 Troubleshooting

### CSS Not Loading
- Ensure file has `.liquid` extension: `literary-sage-magician-theme.css.liquid`
- Check `theme.liquid` includes stylesheet: `{{ 'literary-sage-magician-theme.css' | asset_url | stylesheet_tag }}`

### Settings Not Appearing
- Verify `config/settings_schema.json` has proper JSON syntax
- Check settings are in correct section format
- Restart `shopify theme dev` if needed

### Liquid Errors
- Check Liquid syntax in `.liquid` files
- Ensure all tags are properly closed (`{% endfor %}`, `{% endif %}`, etc.)
- Review error messages in Shopify CLI output

## 🤝 Contributing

This is a student project for learning Shopify theme development. For questions or improvements:

1. Create an issue describing the problem/enhancement
2. Fork the repository
3. Make your changes
4. Submit a pull request

## 📝 License

This project is created for educational purposes.

## 🙏 Acknowledgments

- **Base Theme**: Shopify Dawn theme
- **Icons**: Font Awesome 6.0
- **Design Inspiration**: Everyday AI website archetype system
- **Typography**: Baskerville, Georgia (system fonts)

## 📞 Support

For Shopify-specific questions:
- [Shopify Help Center](https://help.shopify.com/)
- [Shopify Community Forums](https://community.shopify.com/)
- [Shopify Partners Slack](https://shopifypartners.slack.com/)

## 🗺️ Roadmap

Future enhancements:
- [ ] Product page customization with literary theme
- [ ] Blog template with scholarly styling
- [ ] Customer account page branding
- [ ] Advanced animations and parallax effects
- [ ] Accessibility improvements (WCAG 2.1 AA)
- [ ] Performance optimization (90+ Lighthouse score)

---

**Project Status**: ✅ Complete (Core Requirements)

**Last Updated**: November 2025

**Theme Version**: 1.0.0
