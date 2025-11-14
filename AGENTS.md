# Agent Guidelines for Remnawave Reverse-Proxy Documentation

## Build Commands
- `npm run dev` - Start development server
- `npm run build` - Build for production  
- `npm run preview` - Preview production build
- `npm run astro` - Run Astro CLI commands

## Project Structure
This is an Astro Starlight documentation site with i18n support (English/Russian).
- Content: `src/content/docs/` (MDX files)
- Components: `src/components/` (Astro components)
- Assets: `src/assets/` (images, logos)
- Styles: `src/styles/custom.css`

## Code Style Guidelines

### Imports & Formatting
- Use ES6 imports with type imports: `import type { ComponentProps } from "astro/types"`
- Import Starlight components: `import { Steps, LinkButton } from '@astrojs/starlight/components'`
- Import images: `import { Image } from 'astro:assets'`
- Use consistent 2-space indentation

### MDX Content
- Frontmatter must include `title` and `description`
- Use Starlight components: `<Steps>`, `<LinkButton>`, tabs, alerts
- Use GitHub alert syntax: `:::danger[Warning]`, `:::note[Important]`
- Include image imports at top: `import darkBanner from '../../../assets/banner.webp'`
- Center images with flex containers: `<div style={{ display: 'flex', justifyContent: 'center' }}>`

### Astro Components
- Use TypeScript with proper type definitions
- Export Props type extending base component props
- Use `<style>` tags for component-specific CSS
- Follow Starlight component patterns

### CSS
- Use CSS custom properties for theming
- Support both light and dark modes with `:root[data-theme='light']`
- Use Starlight color variables: `var(--sl-color-accent)`

### File Naming
- Use kebab-case for all files and directories
- MDX files: `feature-name.mdx`
- Components: `ComponentName.astro`
- Assets: organize by language (`en/`, `ru/`)

### Images
- Use WebP format for better compression
- Provide both light/dark variants where needed
- Use descriptive alt text
- Center images with appropriate styling

### Internationalization
- All content must have English and Russian versions
- Use translations in sidebar configuration
- Follow the established directory structure: `content/docs/ru/`