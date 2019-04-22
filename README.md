# jarser

`jarser` is a parser.

`jarser` is not a parser generator. [`yacc`](http://openbsd.su/src/usr.bin/yacc/)
and [`bison`](https://www.gnu.org/software/bison/) are classic examples of parser
generators.

Currently, rule configuration and parsing are performed at runtime.

## Installation

Install `jarser` with npm.

```bash
$ npm install [--save] jarser
```

## Usage

```js
const Jarser = require('jarser');
const jarser = new Jarser();
jarser.addRule(...);
const rootNode = jarser.parse(tokens);
```

## A quick lesson in compilation

A _scanner_ scans a file into a sequence of characters. (If using Node.js,
you can rely on the built-in `fs` module for this.)

A _lexer_ (or _tokenizer_) lexes a sequence of characters into a sequence of
_tokens_, using a defined set of rules. (I recommend `jexer` for this stage: 
[`jexer` on npm](https://npmjs.com/jexer)
[`jexer` on GitHub](https://github.com/MichaelBuhler/jexer))

A _parser_ parses a sequence of tokens into a _syntax tree_, using a defined
set of rules. (This is what `jarser` does.)

A _compiler_ compiles the syntax tree into target code, such as _assembly_.

An _assembler_ assembles that code into _machine code_, which a processor can
execute directly.
