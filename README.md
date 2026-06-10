# Currency Format JSON

![License](https://img.shields.io/github/license/xsolla/currency-format)

## Overview

`currency-format` is a JSON dataset describing the world's currencies: ISO 4217 codes, names, graphemes (symbols), fraction sizes, and formatting templates (symbol position and writing direction). It is the shared data source used by Xsolla's currency-formatting libraries.

It is intended for developers who need consistent, locale-aware currency metadata without hand-maintaining it.

## Requirements

- A JSON-capable environment (any language/runtime can read the file)

## Install

Copy `currency-format.json` into your project, or install via a package manager:

```bash
npm install currency-format
# or: bower install currency-format
```

## Usage

Read a currency entry by its ISO 4217 code:

```javascript
import currencyFormat from 'currency-format';

const amd = currencyFormat['AMD'];
console.log(amd.name);             // "Armenian Dram"
console.log(amd.fractionSize);     // 2
console.log(amd.symbol.grapheme);  // "դր."
console.log(amd.symbol.template);  // "1 $"  (symbol position)
```

`symbol` / `uniqSymbol` is `null` when the currency has no symbol. Currency codes follow [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217).

## Documentation

The dataset is self-documenting — each entry's structure is described above. See the JSON file for the full list of currencies.

## Support

- **GitHub Issues:** [github.com/xsolla/currency-format/issues](https://github.com/xsolla/currency-format/issues)

## License

MIT License. See [LICENSE](./LICENSE).
