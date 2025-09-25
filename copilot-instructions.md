# Griffin's Rise Trading Journal - Development Guide

## Quick Start for Developers

This is a **single-file HTML application** for trading education and journal management. Everything is contained in the `Dashboard` file.

### Key Points for Code Changes

1. **Single File Architecture**: All HTML, CSS, and JavaScript is in the `Dashboard` file
2. **No Build Process**: Direct HTML file that opens in any modern browser
3. **Local Storage**: All user data persists in browser localStorage
4. **Self-Contained**: Uses CDN for Chart.js, no other external dependencies

### Main Application Structure

The app has 5 main tabs:
- **Onboarding**: User introduction and setup
- **Syllabus**: Learning phases with quizzes  
- **Training**: 7 educational modules
- **Journal**: Trade entry and management
- **Dashboard**: Performance analytics with charts

### Making Changes

**Before modifying code:**
- Understand the existing utility class system (similar to Tailwind)
- Review the JavaScript function organization (clearly commented sections)
- Test changes by opening the HTML file in a browser

**Common modification patterns:**
- New UI elements: Add HTML + CSS utilities + JavaScript event handlers
- Data changes: Update `appState` object structure + localStorage persistence
- Styling: Use existing utility classes or extend the pattern

### Testing Your Changes

Simply open the `Dashboard` file in a web browser:
```bash
# Open in default browser (macOS)
open Dashboard

# Open in default browser (Linux)
xdg-open Dashboard

# Or just double-click the file
```

### Code Organization

The JavaScript is organized into clear sections:
- State Management & Storage
- UI Management Functions  
- Tab Navigation
- Journal Functionality
- Training & Quiz System
- Dashboard Analytics
- Initialization

Look for the comment headers like `// ===== SECTION NAME =====` to navigate the code.