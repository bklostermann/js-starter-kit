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

## Source Maps

Source maps allow you to debug transpiled and minimified code.
- Only downloaded when developer tools are opened.
- Specified in the webpack.config.dev.js file: `devtool: 'inline-source-map'`.  
- There are other options than just `inline-source-map`.

Tip:
- Write `debugger` in the line of code you want the browser to pause at.

## Linting

Popular linting `ESLint`.

Decisions:
- Config format: separate file or inside `package.json`
- Which built-in rules?
- Warnings or errors?
- Which plugins?
  - Include plugin for React
- Use preset instead?
  - Instead of the above decisions choose a preset (recommended options)

ESLint runs automatically with `watch`.

## Testing and continous Integration

Testing framework:
- Mocha (Recommended)
- Jasmine (builtin assertion library)
- Tape
- QUnit
- AVA
- Jest (wrapper around Jasmine)

Assertion library:
- Chai (Recommeded)
- Should
- Expect

Helper library:
- JSDOM:
  - Simulate the browser's DOM
- Cherrio
  - jQuery for the server
  - Queyr vritual DOM using jQuery selectors

Where to run tests:
- Browser
  - Karma, Testem
- Headless browser (no UI)
  - PhantomJS
- In-memory DOM
  - JSDOM

Where do test files belong:
- Centralized (separate folder)
  - Less "noise" in src folder
  - Deploymnet confusion
  - Inertia
- Alongside
  - Easy imports
  - Clear visibility
  - Convenient to open
  - No recreating folder structure
  - Easily move files

When should tests run?
- For Unit tests should run every time you hit save
  - Rapid feedback
  - Facilitates TDD
  - Automatic = Low friction
  - Increases visibility

## HTTP Calls

Node:
- http
- request

Browser:
- XMLHttpRequest
- jQuery
- Framework-based (Angular/React)
- Fetch

Node & Browser:
- isomorphic-fetch
- xhr
- SuperAgent
- Axios

Centralize API calls:
- Configure all calls
- Handle preloader logic
- Handle errors
- Single seam for mocking

## Mocking HTTP Calls

- Nock
- Static JSON
- Create development webserver
  - api-mock
  - JSON server
  - JSON Schema faker
  - Browsersync
  - Express, etc.

## Project Structure

Tips:
- JS belongs in a .js file
  - Avoid dynamically generating JavaScript logic. Dynamically generate JSON instead.
- Considering organizing by feature
  - Instead of file type
- Extract logic to POJOs
  - Plain Old JavaScript objects
  - Pure logic
  - No framework-specific code

  