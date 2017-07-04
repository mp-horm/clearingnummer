## Clearingnummer

[![npm version](https://badge.fury.io/js/clearingnummer.svg)](https://badge.fury.io/js/clearingnummer)
[![Build Status](https://travis-ci.org/believer/clearingnummer.png?branch=master)](https://travis-ci.org/believer/clearingnummer)
[![Code Climate](https://codeclimate.com/github/believer/clearingnummer/badges/gpa.svg)](https://codeclimate.com/github/believer/clearingnummer)
[![Test Coverage](https://codeclimate.com/github/believer/clearingnummer/badges/coverage.svg)](https://codeclimate.com/github/believer/clearingnummer/coverage)

Sort codes, _clearingnummer_ in Swedish, are four or five digit identifiers for Swedish banks. This package helps you find the bank related to a specific number. All clearing numbers are taken from [Wikipedia](http://www.wikiwand.com/sv/Lista_%C3%B6ver_clearingnummer_till_svenska_banker) and [Swedish Bankers Association](http://www.swedishbankers.se/media/1253/1601_clearingnummer.pdf).

### Installation
```
yarn add clearingnummer
```

### Services

#### bankName()
```js
bankName(string | number): string
```

Retrieve bank name for a given number

##### Example
```js
import clearingnummer from 'clearingnummer'

clearingnummer.bankName(5202)
// 'SEB'
```

#### clearingNumbers()
```js
clearingNumbers(string): { min: string | number, max: string | number }[]
```

Retrieve clearing numbers for a given bank name

##### Example
```js
import clearingnummer from 'clearingnummer'

clearingnummer.clearingNumbers('Ålandsbanken')
// [{
     "min": 2310,
     "max": 2310
   }]
```

#### allBanks
```js
allBanks(): string[]
```

Retrieve the names of all banks in the listing

```js
import clearingnummer from 'clearingnummer'

clearingnummer.allBanks()
// [
  'ABN AMRO',
  'Avanza Bank'
  ...
]
```

### Tests
```
npm test
```
