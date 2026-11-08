# Architectural Decisions

## ADR 001: ES Module Adoption and PostCSS Config Format

- **Context**: The project was configured with `"type": "module"` in `package.json`, causing PostCSS loading to fail because `postcss.config.js` was using CommonJS (`module.exports` and `require`).
- **Decision**: Converted `postcss.config.js` to ESM syntax using `import autoprefixer from 'autoprefixer'` and `export default { plugins: [ autoprefixer(...) ] }`.
- **Consequences**: Compatible with native Node ESM and Vite's PostCSS loader without needing `.cjs` workarounds.
