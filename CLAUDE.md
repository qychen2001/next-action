# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a WebExtension starter template powered by Vite, Vue 3, and TypeScript. It provides a modern development environment for building browser extensions that work across Chrome, Firefox, and other browsers.

## Architecture

- **Framework**: Vue 3 with Composition API and `<script setup>` syntax
- **Build System**: Vite with multiple configurations for different extension contexts
- **Extension Structure**:
  - Popup UI (src/popup)
  - Options page (src/options)
  - Side panel (src/sidepanel)
  - Background scripts (src/background)
  - Content scripts (src/contentScripts)
- **Styling**: UnoCSS (Atomic CSS engine)
- **Communication**: webext-bridge for context communication
- **Icons**: Unplugin-icons with Iconify
- **Auto-importing**: Vue components and APIs via unplugin-vue-components and unplugin-auto-import

## Key Commands

### Development
- `pnpm dev` - Start development server with HMR
- `pnpm dev-firefox` - Start development for Firefox

### Building
- `pnpm build` - Build the extension for production
- `pnpm pack` - Package extension (zip, crx, xpi)

### Testing
- `pnpm test` - Run unit tests with Vitest
- `pnpm test:e2e` - Run end-to-end tests with Playwright

### Code Quality
- `pnpm lint` - Run ESLint
- `pnpm typecheck` - Run TypeScript type checking

## Development Workflow

1. Run `pnpm dev` to start development
2. Load the extension from the `extension/` folder in your browser
3. Changes will be hot-reloaded automatically
4. Run tests with `pnpm test`
5. Build for production with `pnpm build`

## Project Structure

- `src/` - Main source code
  - `manifest.ts` - Dynamic manifest generation
  - `popup/` - Extension popup UI
  - `options/` - Extension options page
  - `sidepanel/` - Extension side panel
  - `background/` - Background scripts
  - `contentScripts/` - Content scripts injected into pages
  - `components/` - Shared Vue components
- `extension/` - Built extension files
- `scripts/` - Development helper scripts
- `vite.config.*.mts` - Vite configuration files for different contexts

## Key Technologies

- TypeScript for type safety
- Vue 3 Composition API
- Vite for fast development
- UnoCSS for styling
- webext-bridge for cross-context communication
- Playwright for E2E testing
- Vitest for unit testing
