---
layout: default
---

# Russo.js

Russo is a lightweight JavaScript library that provides transliteration and conversion between the Cyrillic and Latin alphabets. It uses the ISO 9 standard for transliteration, ensuring consistency and accuracy. The library is written using ESM (ECMAScript Modules) and bundled as UMD (Universal Module Definition), making it compatible with various environments, including browsers, ES6 modules, and CommonJS.

**Repository**: [russo.js on GitHub](https://github.com/linuxfandudeguy/russo.js)

## Table of Contents

1. [Installation](#installation)
2. [Usage](#usage)
   - [Browser](#browser)
   - [ES6 Modules](#es6-modules)
   - [CommonJS](#commonjs)
3. [Features](#features)
4. [API Reference](#api-reference)
5. [Inspiration](#inspiration)
6. [License](#license)

## Installation

You can install Russo via its Git URL using NPM:

### Using NPM

```bash
npm install git+https://github.com/linuxfandudeguy/russo.js
```

### Browser Use

If you want to use the library directly in the browser, you can include it via the following URL:

[https://linuxfandudeguy.github.io/russo.js/prod/bundle.js](https://linuxfandudeguy.github.io/russo.js/prod/bundle.js)

Example:

```html
<script src="https://linuxfandudeguy.github.io/russo.js/prod/bundle.js"></script>
<script>
  console.log(Russo.transliterate("Москва")); // "Moskva"
</script>
```

### Why Download Locally?

If you need to maintain a specific version of the library, it is recommended to download it locally. This ensures that the library will not change if the hosted URL is updated. The decision to avoid hosting separate files for each change is to prevent the repository from taking up excessive space. Hosting multiple versions for every small change would make repository management inefficient and overly complex.

### ESM and UMD Compatibility

Russo is written using ESM (ECMAScript Modules) for modern JavaScript development and bundled using UMD (Universal Module Definition). This allows it to work in a variety of environments:

- **Browser**: Include the script via a `<script>` tag and access the Russo object globally.
- **ES6 Modules**: Import the library using `import`.
- **CommonJS**: Require the library using `require` for Node.js or other CommonJS environments.

## Features

### 1. ISO 9 Transliteration

Russo uses the ISO 9 standard for transliteration, ensuring precise mapping between Cyrillic and Latin characters.

- **Cyrillic to Latin**: `Russo.transliterate` converts Cyrillic text to ISO 9 Latin text.
- **Latin to Cyrillic**: `Russo.toRussian` converts Latin text back to Cyrillic.

## Usage

### Browser

Include the library in your HTML file. The Russo object will be globally accessible.

```html
<script src="https://linuxfandudeguy.github.io/russo.js/prod/bundle.js"></script>
<script>
  console.log(Russo.transliterate("Москва")); // "Moskva"
</script>
```

### ES6 Modules

Import the library into your project using ES6 syntax:

```javascript
import Russo from "russo";
console.log(Russo.toRussian("Privet")); // "Привет"
```

### CommonJS

Require the library in a Node.js or CommonJS environment:

```javascript
const Russo = require("russo");
console.log(Russo.transliterate("Привет")); // "Privet"
```

## API Reference

### Russo.transliterate(input: string): string

Converts a string of Cyrillic characters to their Latin transliterated equivalents using the ISO 9 system.
- **Parameters**:
  - `input` (string) – The string containing Cyrillic characters to transliterate.
- **Returns**:
  - A string with Latin transliterated characters.

### Russo.toRussian(input: string): string

Converts a string of Latin characters to their Cyrillic equivalents using the ISO 9 system.
- **Parameters**:
  - `input` (string) – The string containing Latin characters to convert to Cyrillic.
- **Returns**:
  - A string with Cyrillic characters.

## Inspiration

The Russo library was inspired by aromanize.js, a library primarily focused on transliterating various languages. The inspiration for Russo comes from the desire to create a similar library, but for Cyrillic and Latin alphabets, while maintaining the high standards of transliteration accuracy.

Additionally, Russo was developed as an opportunity to explore ESM (ECMAScript Modules), outside of web development, and to create something that could be used across multiple environments, including both browser and server-side environments. The library uses ISO 9 to ensure that the transliteration process is consistent and reliable.

## License

This library is licensed under the MIT License. Feel free to use and modify it as needed.
