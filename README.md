# eslint-config-greasemonkey

This package provides an eslint shared config which defines all additional variables supported by Geasemonkey/Tampermonkey/Violentmonkey 's API in its  `globals` property. It's very useful when you use eslint to lint your xxxmonkey scripts that use these variable without having to define the used variables yourself in your eslint configuration.

## Installation
```bash
npm i -D eslint-config-greasemonkey
```

## Usage
Add `greasemonkey` to the `extends` property in your eslint configuration. Example of a configuration file in JSON format:
```json
// .eslintrc.json
{
    "extends": [
        "greasemonkey"
    ],
    "globals": {
        "GM_info": "off" // you can disable the unneeded variables
    }
}
```

The default shared config provided by this package shares variables in `readonly` mode so that you can not overwrite these variables. You can extend another config `greasemonkey/writable` which allow the variables to be overwritten.
```json
// .eslintrc.json
{
    "extends": [
        "greasemonkey/writable"
    ]
}
```

## License
[MIT License](./LICENSE)
