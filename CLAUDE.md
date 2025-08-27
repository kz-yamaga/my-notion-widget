# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a collection of minimal HTML widgets designed for embedding in Notion pages. Each widget is a self-contained HTML file optimized for iframe embedding.

## Development Commands

### Local Testing
Start local development server to test widgets before deployment:
```bash
python3 -m http.server 8000
```

Access widgets at:
- Main page: http://localhost:8000
- Widgets: http://localhost:8000/widgets/

Stop server with `Ctrl+C`.

### Deployment
Changes are automatically deployed via GitHub Actions on push to `main` branch. No build process required.

## Architecture

### Project Structure
- `index.html` - Landing page with widget directory
- `widgets/` - Individual widget HTML files
- `.github/workflows/deploy.yml` - GitHub Actions deployment

### Widget Design Patterns

Each widget follows these conventions:
- **Self-contained**: All CSS and JavaScript inline
- **Responsive layout**: Uses CSS variables and flexible sizing
- **Dark mode support**: `prefers-color-scheme: dark` media queries
- **Notion-optimized**: Minimal padding, clean borders, accessible colors
- **Accessibility**: Proper ARIA labels and semantic HTML

### CSS Variable System
Standard color scheme across widgets:
```css
:root {
  --bg: #ffffff;
  --text: #0e1a2b;
  --muted: #6b7280;
  --border: #e5e7eb;
  --input-bg: #ffffff;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg: #1a1a1a;
    --text: #e5e7eb;
    --muted: #9ca3af;
    --border: #262b36;
    --input-bg: #262b36;
  }
}
```

### Widget Layout Standards
- Container: `width: 90%; max-width: 800px; margin: 0 auto`
- Minimal padding for embedding contexts
- Auto-sizing components where appropriate

## Development Workflow

1. Create/modify widget files in `widgets/` directory
2. Test locally using Python HTTP server
3. Verify both light and dark mode appearance
4. Test responsive behavior at different screen sizes
5. Commit and push - deployment is automatic via GitHub Actions

When adding new widgets:
- Add entry to `index.html` widget list
- Follow existing naming conventions
- Include Japanese language support where applicable
- Ensure iframe embedding compatibility