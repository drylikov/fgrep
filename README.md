# fgrep

Search for a given string in specified files.

## USAGE

```javascript
var fgrep = require('fgrep')

// options:
// - limit: defaults to 10, how many files to read at once
// - nocase: defaults false, do a case-insensitive search
fgrep(string, filenames, options)
  .on('data', function (match) {
    // match is { filename, linenumber, line }
  })
  .on('end', function () {
    // done matching
  })

// or if you prefer being classy, but it's the same thing
var FGrep = require('fgrep')
var fg = new FGrep(string, filenames, limit)
```
