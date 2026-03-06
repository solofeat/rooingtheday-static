# Rooing the Day Static Site

A static website built with Primer design system, featuring a clean, accessible interface with custom color scheme.

## Custom Color Palette

The site uses a custom color palette:
- **French Blue**: #0069AA
- **Vivid Tangerine**: #FF6B35
- **Dark Emerald**: #0D5E36
- **Bright Snow**: #FBFBFB
- **Gunmetal**: #343A40

These colors are defined in [`public/css/styles.css`](public/css/styles.css) as CSS custom properties and used throughout the site for buttons, headers, backgrounds, and accents.

## Project Structure

```
rooingtheday-static
├── public
│   ├── index.html        # Main landing page
│   ├── about.html        # About page
│   ├── contact.html     # Contact page
│   ├── rentals.html     # Equipment rentals page
│   ├── css
│   │   └── styles.css   # Custom CSS styles with color palette
│   ├── js
│   │   └── includes.js  # Legacy client-side partial includes (not currently used)
│   ├── includes
│   │   ├── header.html  # Navigation header (reference only)
│   │   └── footer.html # Site footer (reference only)
│   └── _headers        # Cloudflare Pages configuration
├── .gitignore           # Files to ignore in version control
├── package.json         # npm configuration
└── README.md            # This file
```

## Getting Started

1. **Navigate to the project directory**:
   ```
   cd rooingtheday-static
   ```

2. **Install dependencies**:
   ```
   npm install
   ```

3. **Start the development server**:
   ```
   npm start
   ```

   This will open your browser to `http://localhost:8080` with live reloading.

## Building for Production

The project is configured for Cloudflare Pages deployment. To build:

```
npm run build
```

This will verify the CSS files exist (required for Cloudflare Pages).

## Deployment to Cloudflare Pages

1. Connect your GitHub repository to Cloudflare Pages
2. Set the following configuration:
   - **Build command**: `npm run build`
   - **Build output directory**: `public`
3. Deploy

The site is deployed at [rooingtheday.com](https://rooingtheday.com)

### Using Primer Design System

This project uses Primer CSS via CDN for styling. The design system provides:

- Responsive grid system
- Typography utilities
- Form components
- Button styles
- Layout utilities

The Primer CSS is pinned to version 21.3.2 for stability.

## Usage

- The `index.html` file serves as the main entry point.
- The `about.html` file provides information about the channel.
- The `rentals.html` page lists equipment available for rent.
- The `contact.html` file includes contact information.
- Custom CSS styles are defined in `public/css/styles.css`.

## Technical Notes

### Inlined Layout Components

The header and footer are inlined directly in each HTML file rather than loaded dynamically. This ensures:
- Faster page loads (no additional HTTP requests)
- Better SEO (content is present in initial HTML)
- Works reliably on all hosting platforms including Cloudflare Pages

### Cloudflare Pages Configuration

The project includes a `_headers` file for configuring caching behavior on Cloudflare Pages.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any suggestions or improvements.

## License

This project is licensed under the MIT License.
