# Notes

## Editorconfig

Standardize configuration across any editor used by developers.
- Create file: `.editorconfig`
- Install plugin for editor: `ext install EditorConfig`

## Security

Node Security Platform:  `nsp check`
- Run it on npm install, manually, production build, pull request or npm start

## Sharing WIP

Available tools to make your work available:
- localtunnel: `lt --port 3000 --subdomain brent`
- ngrok
- surge
- now

## Automation

Automating tasks:
- Grunt
- Gulp
- npm Scripts (recommended)

## Transpiling (Source to Source compiler)

- Babel (recommended)
  - Modern, standards-based JS, today
  - Specify preset to determine what features need to be transpiled
- TypeScript
  - Superset of JavaScript
  - Adds type safety to JavaScript
- Elm

## Bundling

Reasons for bundling:
- CommonJS doesn't work in web browsers
- Package project into file(s)
- Improve Node performance

Pick a module format and then pick a bundler.

ES6 Modules (recommended)
- Standardized
- Statically analyzable
  - Imporved autocomplete
  - Intelligent refactoring
  - Fails fast
  - Tree shaking (dead code elimination)
- Easy to read
  - Named imports
  - Default exports

Select a bundler:
- Browserify
- Webpack (recommended)
  - Bundles more than just JS
  - Import CSS, images, etc like JS
  - Built in hot-reloading web server
- Rollup
  - Tree shaking
  - Faster loading production code
- JSPM

