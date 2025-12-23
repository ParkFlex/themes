# ParkFlex Themes

SCSS themes for ParkFlex application, automatically compiled and published via GitHub Actions.

## Features

- 🎨 Custom PrimeReact theme styling
- 🚀 Automated build and publishing via GitHub Actions
- 📦 Available as npm package via GitHub Packages
- 🔄 Automatic versioning and releases

## Installation

### From GitHub Packages

1. Create or update `.npmrc` in your project root:

```
@parkflex:registry=https://npm.pkg.github.com
//npm.pkg.github.com/:_authToken=${GITHUB_TOKEN}
```

2. Install the package:

```bash
npm install @parkflex/themes
```

### From GitHub Releases

Download pre-built CSS files from the [Releases page](https://github.com/parkflex/themes/releases).

## Usage

### In your application

```typescript
// Import compiled CSS
import '@parkflex/themes/dist/theme.css';
// Or minified version
import '@parkflex/themes/dist/theme.min.css';
```

### Development

```bash
# Install dependencies
npm install

# Build CSS
npm run build

# Watch for changes
npm run watch

# Build with source maps
npm run build:css:dev
```

## Project Structure

```
src/
├── mytheme/          # Custom theme variables and extensions
│   ├── theme.scss    # Main theme entry point
│   ├── _variables.scss
│   ├── _fonts.scss
│   └── _extensions.scss
└── theme-base/       # PrimeReact base components
    ├── _components.scss
    ├── _mixins.scss
    └── components/   # Individual component styles
```

## Publishing

### Automatic (Recommended)

1. Update version in `package.json`
2. Create and push a git tag:

```bash
git tag v1.0.1
git push origin v1.0.1
```

3. GitHub Actions will automatically:
   - Build the CSS
   - Publish to GitHub Packages
   - Create a GitHub Release with artifacts

### Manual

```bash
npm run build
npm publish
```

## CI/CD Pipeline

The GitHub Actions workflow automatically:

- ✅ Builds CSS on every push and PR
- 📦 Publishes to GitHub Packages on version tags
- 🎁 Creates GitHub Releases with compiled assets
- 🔍 Uploads build artifacts for review

## License

MIT
