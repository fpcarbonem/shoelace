# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

### Core Development
- `npm start` - Start dev server with live reloading
- `npm run build` - Build production distribution
- `npm run verify` - Run full verification (prettier, lint, build, test)

### Testing
- `npm run test` - Run all tests
- `npm run test:component` - Run tests for specific component (e.g., `npm run test -- --group button`)
- `npm run test:watch` - Run tests in watch mode

### Code Quality
- `npm run lint` - Run ESLint
- `npm run lint:fix` - Run ESLint with auto-fix
- `npm run prettier` - Format code with Prettier
- `npm run prettier:check` - Check code formatting

### Component Generation
- `npm run create sl-tag-name` - Scaffold a new component with all necessary files

## Architecture Overview

### Component Structure
Each component follows a consistent structure in `src/components/[component-name]/`:
- `[component].component.ts` - Main component implementation extending ShoelaceElement
- `[component].styles.ts` - Component-specific styles using Lit's CSS
- `[component].test.ts` - Web Test Runner tests
- `[component].ts` - Export file that registers the component

### Core Technologies
- **LitElement**: Base class for all web components
- **TypeScript**: Strongly typed development
- **Web Components**: Standards-based custom elements
- **ESBuild**: Fast bundling and compilation
- **Web Test Runner**: Component testing with Playwright

### Key Base Classes
- `ShoelaceElement` (`src/internal/shoelace-element.ts`) - Base class extending LitElement with Shoelace-specific functionality
- Form controls implement `ShoelaceFormControl` interface for consistent form integration

### Styling System
- Component styles use Lit's `css` tagged template literals
- Design tokens defined in `src/themes/` (light.css, dark.css, harmony-light.css, harmony-dark.css)
- Component-specific styles in individual `.styles.ts` files

### Build System
- Custom build script (`scripts/build.js`) handles:
  - TypeScript compilation
  - Component bundling
  - Theme generation
  - Documentation building
  - React wrapper generation

### Testing Setup
- Web Test Runner with Playwright browsers (Chromium, WebKit)
- Tests run against built components in production mode
- Named test groups allow running individual component tests
- Timeout: 3000ms with 1 retry

### Internationalization
- Localization system in `src/utilities/localize.ts`
- Translation files in `src/translations/`
- Components use `LocalizeController` for reactive translations

### Event System
- Custom events defined in `src/events/`
- Type-safe event emission through ShoelaceElement base class
- Consistent event naming with `sl-` prefix