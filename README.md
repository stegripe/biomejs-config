# biomejs-config
> A BiomeJS [shareable configuration](https://biomejs.dev/) package that we used in our projects.

<div align="center">
<a href="https://www.npmjs.com/package/@stegripe/biomejs-config">
  <img src="https://img.shields.io/npm/v/@stegripe/biomejs-config?maxAge=3600" alt="npm version" ></a>
  <img src="https://img.shields.io/npm/dt/@stegripe/biomejs-config?maxAge=3600" alt="npm downloads">
</div>

## Install
```sh-session
npm install -D @stegripe/biomejs-config # npm
pnpm add -D @stegripe/biomejs-config # pnpm
yarn add -D @stegripe/biomejs-config # yarn
```

## Usage
This package requires BiomeJS Configuration File.

### Configuration
Create an `biome.json/biome.jsonc` file in the root of your project and add the following code:
```json
{
  "extends": ["@stegripe/biomejs-config"]
}
```

### Extending Rules
You can also extend specific rules by adding them to the `biome.json/biome.jsonc` file. For example:
```json
{
    "extends": ["@stegripe/biomejs-config"],
    "linter": {
        "rules": {
            "nursery": {
                "useExplicitType": "off"
            }
        }
    }
}
```

### Unstable Rules
This configuration uses some rules that are still Work-in-Progress (WIP) and categorized under the [`nursery`](https://biomejs.dev/linter/#nursery).

* [`nursery/noFloatingPromises`](https://biomejs.dev/linter/rules/no-floating-promises): DRequire Promise-like statements to be handled appropriately.
* [`nursery/useExplicitType`](https://biomejs.dev/linter/rules/use-explicit-type): Enforce types in functions, methods, variables, and parameters.