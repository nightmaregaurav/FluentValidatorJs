# FluentValidatorJs

FluentValidatorJs is a TypeScript utility library that provides a fluent, readable, and intuitive way to perform value validations and collect error messages. With its easy-to-use chaining methods, you can define and execute complex validation rules with minimal effort.

## Installation
```bash
npm install @nightmaregaurav/fluent-validator-js
````

## Usage

```typescript
import { Ensure } from '@nightmaregaurav/fluent-validator-js';

const result = Ensure.given("Hello, World!")
    .isString()
    .hasAtLeastLength(10)
    .matchesRegex(/^[A-Z]/)
    .evaluate();

console.log("Is Valid:", result.isValid);
console.log("Errors:", result.errors);
```

## Features

- Chainable and fluent syntax for defining validation rules.
- Comprehensive set of validation methods for various data types and conditions.
- Error message collection for easy debugging and reporting.

## Examples

Here are a few examples demonstrating how to use FluentValidatorJs for validation:

### Validate String Length

```typescript
const result = Ensure.given("Hello, World!")
    .isString()
    .hasAtLeastLength(10)
    .evaluate();

console.log("Is Valid:", result.isValid); // false
console.log("Errors:", result.errors); // ["Value must have a length of 10 at minimum."]
```

### Validate Numeric Range

```typescript
const result = Ensure.given(42)
    .isNumber()
    .isGreaterThan(30)
    .isLessThan(50)
    .evaluate();

console.log("Is Valid:", result.isValid); // true
```

### Validate Array Contents

```typescript
const result = Ensure.given([1, 2, 3])
    .isArray()
    .contains(2)
    .doesNotContain(4)
    .evaluate();

console.log("Is Valid:", result.isValid); // true
```

## License

FluentValidatorJs is released under the MIT License. You can find the full license details in the [LICENSE](LICENSE) file.

Made with ❤️ by [NightmareGaurav](https://github.com/nightmaregaurav).

---
Open For Contribution
---
