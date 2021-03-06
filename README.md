# saz2har

Converts SAZ file (from Fiddler) to HAR file.

## Install

```console
$ npm install -g saz2har
```

## API

### convert(input[, output][, options][, callback])

* `input` - path to the input SAZ file
* `output` - path to the output HAR file
* `options` - object with conversion options
    * `validate` - enables validation of HAR output (default: `true`)
    * `write` - write HAR output (default: `false`)
* `callback` - callback function
```js
var saz2har = require("saz2har");

saz2har.convert("foo.saz", {
    validate: false
}, function (err, data) {
    if (err) {
        console.error("Error: ", err);
        
        return;
    }
    
    console.log(data);
});
```

## Bin

```
$ saz2har --help

Usage: saz2har [options] input.saz [output.har]

Options:
    --help          Show help                                       [boolean]
    --version       Show version                                    [boolean]
    --no-validate   Validate the output HAR file (default: true)    [boolean]

Examples:
    saz2har foo.saz bar.har --no-validate
```

## License

MIT
