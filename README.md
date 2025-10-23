# Rooing the Day Static Site

A simple static website built with Primer design system, featuring a clean, accessible interface.

## Project Structure

```
rooingtheday-static
├── public
│   ├── index.html        # Main landing page
│   ├── about.html        # About page
│   ├── contact.html      # Contact page
│   ├── css
│   │   └── styles.css    # Custom CSS styles
│   ├── js
│   │   └── includes.js   # Client-side partial includes
│   ├── includes
│   │   ├── header.html   # Navigation header
│   │   └── footer.html   # Site footer
│   └── assets
│       └── fonts         # Font files directory
├── .gitignore            # Files to ignore in version control
├── package.json          # npm configuration
└── README.md             # This file
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

### Using Primer Design System

This project uses Primer CSS via CDN for styling. The design system provides:

- Responsive grid system
- Typography utilities
- Form components
- Button styles
- Layout utilities

### Client-side partials (includes)

To avoid repeated markup, the site uses simple client-side includes. Partials live under `public/includes/` and are injected into pages at runtime by `public/js/includes.js`.

How it works:

- Add a placeholder in an HTML page where you want the partial inserted:

```html
<div data-include="/includes/header.html"></div>
```

- The `public/js/includes.js` script fetches the URL and inserts the HTML into the placeholder.

Notes:

- Client-side includes require the site be served over HTTP (e.g., `npm start` with `live-server`) to avoid CORS/file:// fetch issues.
- If you open files via `file://` in the browser, the fetch will fail.

## Usage

- The `index.html` file serves as the main entry point.
- The `about.html` file provides information about the site.
- The `contact.html` file includes a contact form.
- CSS styles are defined in `public/css/styles.css`.
- JavaScript functionality is in `public/js/includes.js`.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any suggestions or improvements.

## License

This project is licensed under the MIT License.