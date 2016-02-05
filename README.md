# Currency Format JSON

JSON with information about currencies: codes (ISO 4217), the names, grapheme (symbols), fraction and formatting.

## Installation

Copy the JSON file into your project or use npm package manager:

- Execute the following command: `npm install currency-format`

## Usage

The structure of the JSON file:

```javascript
{
  'AMD': {                          // ISO 4217 currency code.
     'name': 'Armenian Dram',       // Currency name.
     'fractionSize': 2,             // Fraction size, a number of decimal places.
     'symbol': {                    // Currency symbol information.
         'grapheme': 'դր.',         // Currency symbol.
         'template': '1 $',         // Template showing where the currency symbol should be located (before or after amount).
         'rtl': false               // Writing direction.
     },
     'uniqSymbol': {                // Alternative currency symbol. We recommend to use it when you want to exclude a repetition of symbols in different currencies.
         'grapheme': 'դր.',         // Alternative currency symbol.
         'template': '1 $',         // Template showing where the alternative currency symbol should be located (before or after amount).
         'rtl': false               // Writing direction.
     }
  },
  ...
}
```

Symbol/uniqSymbol field is `null`, when the currency has no symbol/alternative symbol.

## Currency reference

The list of currency codes was taken from https://en.wikipedia.org/wiki/ISO_4217.

## License

The MIT License.

See [LICENSE](https://github.com/xsolla/currency-format/blob/master/LICENSE)