![Netlify](https://img.shields.io/badge/-Netlify-00C7B7?logo=netlify&logoColor=white&style=for-the-badge)

# Redirect Configuration

This repository contains a simple redirect configuration using a `[[redirects]]` rule.

## Overview
The purpose of this configuration is to redirect all incoming requests (`/*`) to a specific HTML file (`HTML-FILE-NAME`) with a `200` status.

## Configuration
The `.toml` configuration file contains the following rule:

```
toml
[[redirects]]
from = "/*"
to = "/HTML-FILE-NAME"
status = 200
```

## Explanation

- `from = "/*"` → Captures all routes.
- `to = "/HTML-FILE-NAME"` → Redirects all requests to the specified HTML file.
- `status = 200` → Serves the file instead of a redirect (useful for single-page applications or static site hosting).

## Usage

This setup is commonly used in static site hosting solutions like **Netlify** to ensure all routes point to a single entry file, such as an `index.html` in SPA frameworks like React or Vue.

## Deployment

If using **Netlify**, place the configuration in a `netlify.toml` file at the root of your repository. Ensure your project structure looks like this:

```
repo-root/
├── netlify.toml
├── HTML-FILE-NAME.html
└── other-assets/
```
