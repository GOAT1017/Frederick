# Copilot Instructions for Griffin's Rise Trading Journal

## Project Overview

This repository contains **Griffin's Rise: Advanced Trading Journal — Pro Edition**, a comprehensive single-file HTML application designed for trading education and journal management. The application is self-contained with embedded CSS, JavaScript, and all functionality within a single `Dashboard` file.

## Architecture & Tech Stack

- **Frontend**: Pure HTML5, CSS3, and vanilla JavaScript
- **Charts**: Chart.js library (via CDN)
- **Storage**: Browser localStorage for persistence
- **Styling**: Custom CSS with utility classes (similar to Tailwind approach)
- **Structure**: Single-page application with tab-based navigation

## Key Features & Components

### Core Functionality
1. **Onboarding System**: Step-by-step user introduction
2. **Training Modules**: 7 educational modules with quizzes
3. **Trading Journal**: Trade entry, management, and analysis
4. **Dashboard**: Performance metrics and charts
5. **Syllabus**: Structured learning phases

### Main Sections
- **Onboarding Tab**: Welcome flow and initial setup
- **Syllabus Tab**: Learning phases with progress tracking
- **Training Tab**: Interactive modules and assessments
- **Journal Tab**: Trade logging and management
- **Dashboard Tab**: Analytics and performance visualization

## Development Guidelines

### Code Style & Structure
- Use existing utility class patterns for styling
- Maintain the current modular JavaScript function structure
- Follow the established naming conventions (camelCase for functions, kebab-case for IDs)
- Keep all code within the single HTML file unless absolutely necessary

### JavaScript Patterns
- Functions are organized by feature area with clear comment sections
- State management through `appState` object and localStorage
- Event-driven architecture with proper event listeners
- Consistent error handling and user notifications

### CSS Organization
- Utility-first approach with custom CSS classes
- Responsive design using media queries
- Consistent color scheme (dark theme with slate/blue palette)
- Shadow and rounded corner styling for modern UI

### Data Management
- All data persists to localStorage with JSON serialization
- State management through global `appState` object
- Trade data includes comprehensive metrics (entry/exit, P&L, analysis)
- Progress tracking for onboarding and training modules

## Common Tasks & How to Handle Them

### Adding New Features
1. **New UI Sections**: Add HTML structure, implement show/hide functionality
2. **New JavaScript Functions**: Follow existing organization patterns with clear comments
3. **New Styling**: Use existing utility classes or extend the pattern
4. **Data Storage**: Extend `appState` object and ensure localStorage persistence

### Modifying Existing Features
1. **UI Changes**: Update HTML structure and corresponding CSS
2. **Functionality Updates**: Modify existing functions while maintaining backward compatibility
3. **Data Structure Changes**: Consider migration strategy for existing localStorage data

### Testing & Validation
- Test localStorage functionality across browser sessions
- Verify responsive design on different screen sizes
- Ensure all interactive elements (buttons, forms, charts) work correctly
- Validate trade calculations and data persistence

## Important Considerations

### Single-File Architecture
- All code must remain in the `Dashboard` file
- External dependencies should use CDN links only
- Minimize external resource dependencies

### User Experience
- Maintain the current professional dark theme
- Ensure smooth transitions between tabs and modals
- Preserve existing keyboard navigation (Alt + number shortcuts)
- Keep the responsive design working across devices

### Data Integrity
- Always validate user input before storage
- Provide clear error messages and success notifications
- Maintain data consistency across different sections
- Handle edge cases in calculations and data display

## File Structure Context

```
Frederick/
├── Dashboard          # Main HTML application file (contains everything)
├── .git/             # Git repository
└── .copilot/         # Copilot configuration (this directory)
    └── instructions.md
```

## Security & Best Practices

- No server-side code or external API calls
- All data remains client-side in browser storage
- Input validation for all user-entered data
- Secure handling of financial calculations

## When Making Changes

1. **Always test thoroughly** - The application is complex with many interconnected features
2. **Maintain backward compatibility** - Users may have existing data in localStorage
3. **Follow existing patterns** - The codebase has established conventions for consistency
4. **Consider performance** - Keep the single-file architecture efficient
5. **Document complex logic** - Add comments for any non-obvious implementations

## Common Patterns to Follow

- Tab navigation: `showTab(tabName)` function pattern
- Modal management: `open/close` function pairs
- Data persistence: Update `appState` then call `saveState()`
- UI updates: Separate DOM manipulation from business logic
- Form handling: Validate input, update state, provide user feedback