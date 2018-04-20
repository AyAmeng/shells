## TSLINT

## LOCATION

```sh

@ROOT_PROJECT/tslint.json

```

```json

{
  "extends": ["tslint-react", "tslint-config-prettier"],
  "defaultSeverity": "warning",
  "linterOptions": {
    "exclude": ["node_modules/**/*"]
  },
  "rules": {
    "ordered-imports": true,
    "jsx-ban-props": [true, "always"],
    "jsx-boolean-value": [true, "always"],
    "jsx-no-bind": true,
    "jsx-no-lambda": false,
    "jsx-no-multiline-js": false,
    "jsx-no-string-ref": true,
    "jsx-self-close": true
  }
}

{
  "extends": ["tslint-react", "tslint-config-prettier"],
  "defaultSeverity": "warning",
  "linterOptions": {
    "exclude": ["node_modules/**/*"]
  },
  "rules": {
    "ordered-imports": true,
    "jsx-ban-props": [true, "always"],
    "jsx-boolean-value": [true, "always"],
    "jsx-no-bind": true,
    "jsx-no-lambda": false,
    "jsx-no-multiline-js": false,
    "jsx-no-string-ref": true,
    "jsx-self-close": true
  }
}


```
