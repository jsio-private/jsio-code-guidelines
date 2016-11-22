# Typescript

TypeScript is a superset of JavaScript which primarily provides optional static typing, classes and interfaces. One of the big benefits is to enable IDEs to provide a richer environment for spotting common errors as you type the code.

## Installing

`npm install -g typescript`

## Features

### Optional Typing

When there’s a variable or an argument in a function or method call, you can annotate your code with types. To annotate, follow the variable or argument with a colon and followed by it’s type.

```typescript
var myName: string = "Andrew";

function printName(name: string) {
    console.log(name);
}
```

### Interfaces

Interfaces are great ways to set up agreements on the shape of object literals.

```typescript
interface Contact {
    name: string,
    email: string,
    phone: string
}

var addressBook: Contact[] = [];
```

### Classes

TypeScript uses ECMAScript 6 classes and adds a little TypeScript goodness.

```typescript
interface Point {
    x: number,
    y: number
}

class Monster {
    constructor(public name: string, public initialPosition: Point) {

    }
}

var scary = new Monster("Alien", {x: 0, y: 0});
```

## Resources

- [Official docs](https://www.typescriptlang.org/docs/index.html)

### VSCode extensions

- [TSLint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint)
- [Types auto installer](https://marketplace.visualstudio.com/items?itemName=jvitor83.types-autoinstaller)
- [TypeScript Hero](https://marketplace.visualstudio.com/items?itemName=rbbit.typescript-hero)
  - Command: "type", "import"
