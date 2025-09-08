# Vercel Design System - Sass Library Demo

A comprehensive Sass library based on Vercel's Geist design system with automated GitHub Actions deployment.

## 🎨 Features

- **Complete Design System**: Colors, typography, spacing, and components based on Vercel's Geist design language
- **Modern Sass Architecture**: Well-organized SCSS files with mixins, utilities, and components
- **Responsive Design**: Mobile-first approach with flexible grid system
- **Dark Mode Support**: Built-in dark mode with CSS custom properties
- **GitHub Actions**: Automated Sass compilation and deployment to GitHub Pages
- **Performance Optimized**: Minimal CSS output with efficient component structure

## 🚀 Quick Start

### Local Development

1. Clone the repository:
```bash
git clone <your-repo-url>
cd github_actions
```

2. Install dependencies:
```bash
npm install
```

3. Compile Sass:
```bash
npm run build
```

4. For development with watch mode:
```bash
npm run build-dev
```

5. Serve locally:
```bash
npm run dev
```

### GitHub Actions Deployment

The project automatically deploys to GitHub Pages when you push to the main branch. The workflow:

1. **Checkout**: Gets the latest code
2. **Setup Node.js**: Installs Node.js and npm
3. **Install Dependencies**: Installs Sass compiler
4. **Compile Sass**: Converts SCSS to optimized CSS
5. **Deploy**: Publishes to GitHub Pages

## 📁 Project Structure

```
├── scss/
│   ├── base/
│   │   ├── _colors.scss      # Vercel color palette
│   │   ├── _typography.scss  # Font system and text styles
│   │   └── _spacing.scss     # Spacing scale and utilities
│   ├── components/
│   │   ├── _buttons.scss     # Button components
│   │   └── _cards.scss       # Card components
│   ├── utilities/
│   │   └── _layout.scss      # Layout utilities
│   └── vercel.scss           # Main entry point
├── .github/
│   └── workflows/
│       └── deploy.yml        # GitHub Actions workflow
├── index.html                # Sample landing page
├── style.scss                # Page-specific styles
└── package.json              # Dependencies and scripts
```

## 🎯 Design System Components

### Colors
Based on Vercel's Geist design system with comprehensive color scales:
- **Gray Scale**: 50-1000 with semantic naming
- **Blue Scale**: Primary brand colors
- **Semantic Colors**: Success, warning, error, info
- **Dark Mode**: Automatic dark mode support

### Typography
- **Font Families**: Geist Sans and Geist Mono
- **Type Scale**: From 12px to 128px with consistent ratios
- **Mixins**: Predefined heading and body text styles
- **Utilities**: Font weight, size, and spacing classes

### Components
- **Buttons**: Multiple variants, sizes, and states
- **Cards**: Interactive cards with hover effects
- **Layout**: Flexbox and grid utilities
- **Spacing**: Consistent spacing system

## 🛠️ Available Scripts

- `npm run build` - Compile Sass to compressed CSS
- `npm run build-dev` - Compile Sass with watch mode
- `npm run dev` - Development server with watch mode
- `npm run clean` - Remove compiled CSS files

## 🎨 Usage Examples

### Using the Design System

```scss
// Import the entire system
@import 'scss/vercel';

// Use design tokens
.my-component {
  background-color: var(--primary);
  padding: $spacing-4;
  border-radius: 8px;
}

// Use mixins
.my-heading {
  @include heading-2;
}

// Use utility classes in HTML
<button class="btn btn-primary btn-lg">Click me</button>
<div class="card card-interactive">
  <div class="card-body">
    <h3 class="card-title">Card Title</h3>
    <p class="card-text">Card content</p>
  </div>
</div>
```

### Component Classes

```html
<!-- Buttons -->
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary btn-sm">Small Secondary</button>
<button class="btn btn-ghost btn-lg">Large Ghost</button>

<!-- Cards -->
<div class="card card-interactive">
  <div class="card-header">
    <h4 class="card-title">Title</h4>
  </div>
  <div class="card-body">
    <p class="card-text">Content</p>
  </div>
</div>

<!-- Layout -->
<div class="container">
  <div class="grid grid-cols-3 gap-6">
    <div class="card">Item 1</div>
    <div class="card">Item 2</div>
    <div class="card">Item 3</div>
  </div>
</div>
```

## 🌙 Dark Mode

The design system automatically supports dark mode based on user preferences:

```css
/* Automatically switches based on prefers-color-scheme */
@media (prefers-color-scheme: dark) {
  :root {
    --text-primary: #f4f4f5;
    --background-1: #000000;
    /* ... other dark mode variables */
  }
}
```

## 📱 Responsive Design

Built with a mobile-first approach:

```scss
// Mobile first
.component {
  padding: $spacing-4;
  
  // Tablet and up
  @media (min-width: 768px) {
    padding: $spacing-6;
  }
  
  // Desktop and up
  @media (min-width: 1024px) {
    padding: $spacing-8;
  }
}
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test the build process
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🔗 Links

- [Vercel Design System](https://vercel.com/geist)
- [Sass Documentation](https://sass-lang.com/)
- [GitHub Actions](https://github.com/features/actions)

---

Built with ❤️ using Vercel's design principles and GitHub Actions automation.
