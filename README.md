# prettier-setup
Setup instructions of Prettier Code formatter

Prettier uses [cosmiconfig](https://github.com/davidtheclark/cosmiconfig) for configuration file support. This means you can configure prettier via:

- A `.prettierrc` file, written in YAML or JSON, with optional extensions: `.yaml/.yml/.json`.
- A `.prettierrc.toml` file, written in TOML (the `.toml` extension is _required_).
- A `prettier.config.js` or `.prettierrc.js` file that exports an object.
- A `"prettier"` key in your `package.json` file.

The configuration file will be resolved starting from the location of the file being formatted, and searching up the file tree until a config file is (or isn't) found.

The options to the configuration file are the same as the [API options](options.md).


### example configuration
```
{
  "arrowParens": "avoid",
  "bracketSpacing": false,
  "jsxBracketSameLine": false,
  "printWidth": 80,
  "proseWrap": "preserve",
  "requirePragma": false,
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "all",
  "useTabs": false,
  "overrides": [
    {
      "files": "*.json",
      "options": {
        "printWidth": 200
      }
    }
  ]
}

```

#### Note the above config is only an example and most popularly used config... you may want to update it.
https://prettier.io/docs/en/configuration.html 
