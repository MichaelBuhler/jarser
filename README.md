# jarser

`jarser` is a parser. `jarser` is _not_ a parser generator.

## A quick lesson in compilation

A _scanner_ converts a file into a sequence of characters. (If using Node.js,
you can rely on the built-in `fs` modules for this.)

A _lexer_ (or _tokenizer_) parses a sequence of characters into a sequence of
_tokens_, using a defined set of rules. (I recommend `jexer` for this stage: 
[`jexer` on npm](https://npmjs.com/jexer)
[`jexer` on GitHub](https://github.com/MichaelBuhler/jexer))

A _parser_ parses a sequence of tokens into an _abstract syntax tree_, using a
defined set of rules. (This is what `jarser` does.)

The abstract syntax tree is then converted into the target code. (This is the
fun part that you get to do yourself! Check out `c.js` as an example:
[`c.js` on GitHub](https://github.com/MichaelBuhler/c.js))

## Installation

Install `jarser` with npm.

```bash
$ npm install [--save] jarser
```