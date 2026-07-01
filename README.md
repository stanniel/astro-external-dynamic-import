# Astro External Dynamic Import: Bug Minimal Reproducible Example

## Summary

External dynamic imports in <script> tags cause `ReferenceError: __VITE_PRELOAD__ is not defined` at runtime in Astro 7

## Steps to reproduce

1. clone the project
2. run `astro build`
3. inspect the build output `index.html` - `__VITE_PRELOAD__` appears unreplaced
4. run `astro preview` and open the site in a browser, the console should say `ReferenceError: __VITE_PRELOAD__ is not defined`

## Astro info

| Key             | Value         |
| --------------- | ------------- |
| Astro           | v7.0.5        |
| Vite            | v8.1.2        |
| Node            | v22.22.1      |
| System          | macOS (arm64) |
| Package Manager | pnpm          |
| Output          | static        |
| Adapter         | none          |
| Integrations    | none          |
