# NOLA Sprinter Van Rentals Directory Website

![NOLA Sprinter Van Rentals](assets/images/hero-banner.jpg)

> Compare 50+ Luxury Vans & Book Instantly

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Directory Structure](#directory-structure)
- [Customization Guide](#customization-guide)
- [Deployment](#deployment)
- [Custom Domain Setup](#custom-domain-setup)
- [Troubleshooting](#troubleshooting)
- [Support & Resources](#support--resources)

## Overview
NOLA Sprinter Van Rentals is a directory website showcasing luxury van rentals in New Orleans. The site features a responsive 3-column grid layout, search functionality, and instant booking capabilities.

## Features
- Responsive 3-column grid layout
- Advanced search and filtering
- Category-based navigation
- Instant booking integration
- Image gallery for each listing
- Mobile-optimized design
- SEO-friendly structure
- Contact forms
- Social media integration

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Git

### Installation
```bash
# Clone the repository
git clone https://github.com/your-username/nola-sprinter-rentals.git

# Navigate to project directory
cd nola-sprinter-rentals

# Install dependencies
npm install

# Start development server
npm run dev
```

## Directory Structure
```
nola-sprinter-rentals/
├── assets/
│   ├── images/
│   ├── css/
│   └── js/
├── components/
│   ├── Header/
│   ├── Footer/
│   └── DirectoryGrid/
├── data/
│   └── listings.json
├── pages/
└── config/
```

## Customization Guide

### Adding/Editing Directory Items
1. Navigate to `data/listings.json`
2. Add new listing using the following format:
```json
{
  "id": "van-001",
  "title": "Luxury Sprinter Van",
  "category": "Premium",
  "capacity": "12",
  "price": "299",
  "image": "van-001.jpg",
  "description": "Your description here"
}
```

### Modifying Category Labels
Edit the categories in `config/categories.js`:
```javascript
export const categories = [
  {
    id: 'premium',
    label: 'Premium Vans',
    icon: 'premium-icon.svg'
  },
  // Add more categories
];
```

### Updating Hero Section
1. Replace hero image in `assets/images/hero-banner.jpg`
2. Modify hero content in `components/Hero/Hero.js`:
```javascript
const heroContent = {
  title: "Your Title",
  subtitle: "Your Subtitle",
  cta: "Call to Action"
};
```

### Customizing Colors and Styling
1. Open `assets/css/variables.css`
2. Modify color variables:
```css
:root {
  --primary-color: #1a1a1a;
  --secondary-color: #4a90e2;
  --accent-color: #f5a623;
}
```

## Deployment

### Build for Production
```bash
# Create production build
npm run build

# Test production build locally
npm run preview
```

### Deploy to Hosting
```bash
# Deploy to Vercel
vercel deploy

# Deploy to Netlify
netlify deploy
```

## Custom Domain Setup

1. Purchase domain from preferred registrar
2. Add DNS records:
```
A     @     76.76.21.21
CNAME www   your-site.vercel.app
```
3. Configure domain in hosting dashboard
4. Wait for DNS propagation (24-48 hours)

## Troubleshooting

### Common Issues

#### Images Not Loading
- Verify image path in `listings.json`
- Check image format (supported: jpg, png, webp)
- Ensure images are in `assets/images/`

#### Search Not Working
- Clear browser cache
- Check console for JavaScript errors
- Verify search configuration in `config/search.js`

#### Styling Issues
- Run `npm run build:css` to rebuild styles
- Check browser console for CSS errors
- Verify media queries in `assets/css/responsive.css`

## Support & Resources

### Documentation
- [Component Documentation](docs/components.md)
- [API Reference](docs/api.md)
- [Styling Guide](docs/styling.md)

### Support Channels
- [GitHub Issues](https://github.com/your-username/nola-sprinter-rentals/issues)
- [Email Support](mailto:support@example.com)
- [Discord Community](https://discord.gg/example)

### Additional Resources
- [Contributing Guidelines](CONTRIBUTING.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [License Information](LICENSE.md)

---

© 2024 NOLA Sprinter Van Rentals. All rights reserved.