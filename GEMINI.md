# Project Overview: paaharu-github-io

This is a web project built with **Astro**, a modern web framework designed for content-driven websites. It is based on the [Astro Starter Kit: Basics](https://docs.astro.build/en/basics/project-structure/).

## Core Technologies
- **Astro**: Main web framework (version 6.1.6).
- **TypeScript**: Strict type-checking and modern JavaScript features.
- **Node.js**: Requires version `^22.12.0`.
- **Vanilla CSS**: Scoped styling within Astro components.

## Project Structure
- `src/pages/`: Contains the routes of the website.
- `src/components/`: Reusable Astro components.
- `src/layouts/`: Common layouts for multiple pages.
- `src/assets/`: Static assets such as images and fonts.
- `public/`: Public files like favicons.
- `astro.config.mjs`: Astro configuration file.
- `tsconfig.json`: TypeScript configuration, extending Astro's strict rules.

## Building and Running
All commands should be executed from the project root:

| Command | Action |
| :--- | :--- |
| `npm install` | Installs project dependencies. |
| `npm run dev` | Starts a local development server at `localhost:4321`. |
| `npm run build` | Compiles the production site into the `./dist/` folder. |
| `npm run preview` | Previews the production build locally. |
| `npm run astro ...` | Executes Astro CLI commands (e.g., `astro add`, `astro check`). |

## Development Conventions
- **Components**: Follow the [Astro component structure](https://docs.astro.build/en/basics/astro-components/) (Frontmatter for logic, HTML/JSX for structure, `<style>` for scoped CSS).
- **Styling**: Prefer vanilla CSS scoped to components unless global styles are needed.
- **Strict Mode**: The project uses `astro/tsconfigs/strict` for TypeScript, so ensure type safety and avoid using `any` when possible.
- **Asset Handling**: Images should be placed in `src/assets/` if they need optimization by Astro, or `public/` for static hosting.
