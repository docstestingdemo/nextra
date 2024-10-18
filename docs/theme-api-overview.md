

  # Theme API Overview

The Nextra theme API provides a set of customizable options to configure the appearance and behavior of your documentation site. Here's an overview of the main components:

## Theme Configuration

The theme is configured through the `theme.config.jsx` file, which exports an object containing various options:

- `logo`: Customizes the logo displayed in the navbar
- `project`: Configures the project link in the navbar
- `docsRepositoryBase`: Sets the base URL for the documentation repository
- `footer`: Customizes the footer content
- `navbar`: Configures the navigation bar items
- `sidebar`: Customizes the sidebar behavior and appearance
- `toc`: Configures the table of contents
- `editLink`: Customizes the "Edit this page" link
- `feedback`: Configures the feedback link
- `search`: Customizes the search functionality
- `darkMode`: Enables or disables dark mode
- `primaryHue`: Sets the primary color hue
- `i18n`: Configures internationalization options

## Page Configuration

Individual pages can be configured using the `_meta.json` files in each directory:

- Customize page titles and ordering
- Hide pages from navigation
- Set page types (e.g., "page" or "menu")
- Configure nested pages and folders

## Built-in Components

Nextra provides several built-in components to enhance your documentation:

- `Callout`: Highlights important information
- `Tabs`: Creates tabbed content sections
- `Cards`: Displays content in card format
- `Steps`: Shows step-by-step instructions
- `FileTree`: Visualizes file and folder structures

## Customization

The theme can be further customized through:

- Custom CSS and Sass files
- Tailwind CSS integration
- Custom MDX components
- Syntax highlighting options

## Internationalization

Nextra supports multi-language documentation through:

- Locale-specific file naming conventions
- Language dropdown configuration in `theme.config.jsx`
- Middleware for language detection and routing

This overview covers the main aspects of the Nextra theme API, allowing you to create highly customized and feature-rich documentation sites.

  