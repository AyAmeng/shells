# TSCONFIG

## LOCATION

```sh

@ROOT_PROJECT/tsconfig.json

```

## CONFIG

```json

{
  "compileOnSave": false,
  "compilerOptions": {
    "allowSyntheticDefaultImports": true,
    "baseUrl": ".",
    "emitDecoratorMetadata": true,
    "experimentalDecorators": true,
    "forceConsistentCasingInFileNames": true,
    "jsx": "preserve",
    "lib": ["dom", "es2015", "es2016", "es2017", "esnext"],
    "target": "es5",
    "moduleResolution": "node",
    "noImplicitReturns": true,
    "noImplicitThis": true,
    "noUnusedLocals": true,
    "noUnusedParameters": true,
    "paths": {
      "@/*": ["./client/*"],
      "@client/*": ["./client/*"],
      "@locales/*": ["./locales/*"],
      "client/*": ["./client/*"],
      "locales/*": ["./locales/*"]
    },
    "skipLibCheck": true,
    "strictNullChecks": true,
    "suppressExcessPropertyErrors": true,
    "suppressImplicitAnyIndexErrors": true
  },
  "exclude": ["build", "dist", "node_modules"]
}


```
