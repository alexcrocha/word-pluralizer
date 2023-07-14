# Word Pluralizer
[![npm version](https://img.shields.io/npm/v/word-pluralizer.svg)](https://www.npmjs.com/package/word-pluralizer) [![npm downloads](https://img.shields.io/npm/dt/word-pluralizer.svg)](https://www.npmjs.com/package/word-pluralizer)

This is a simple word pluralizer and singularizer npm package. It allows for the conversion of singular words to their plural forms and vice versa. It also handles irregular and uncountable words. One of the key features of this package is that it allows you to create your own rules for words that may not be handled out of the box.

Please note that this package is intended to be used for educational purposes only.

## Installation

To install the package, use the following npm command:

```bash
npm install word-pluralizer
```

## Usage
First, import the module in your JavaScript file:

```javascript
const {pluralize, singularize} = require('word-pluralizer');
```

Then, use the following functions to convert words:

```javascript
pluralize('person'); // returns 'people'
singularize('people'); // returns 'person'
```

## Custom Rules

You can also add custom rules. You can do the following:

```javascript
const {plural, singular, irregular, uncountable} = require('word-pluralizer');
```

### plural
The plural function takes in a regular expression and a replacement string. The regular expression is used to match the word to be pluralized. The replacement string is used to replace the matched word.

```javascript
plural(/(quiz)$/i, '$1zes');
plural(/^(ox)$/i, '$1en');
```

### singular
The singular function takes in a regular expression and a replacement string. The regular expression is used to match the word to be singularized. The replacement string is used to replace the matched word.

```javascript
singular(/(quiz)zes$/i, '$1');
singular(/^(ox)en/i, '$1');
```

### irregular
The irregular function takes in a singular word and its plural form.

```javascript
irregular('person', 'people');
irregular('man', 'men');
```

### uncountable
The uncountable function takes in a word that is uncountable.

```javascript
uncountable('money');
uncountable('rice');
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Links
- [GitHub Repository](https://github.com/alexcrocha/word-pluralizer)
- [Issue Tracker](https://github.com/alexcrocha/word-pluralizer/issues)
- [NPM Package](https://www.npmjs.com/package/word-pluralizer)

## License
The code in this project is licensed under ISC license.
