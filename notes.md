### Grammar:

```
expression     → equality ;
equality       → comparison ( ( "!=" | "==" ) comparison )* ;
comparison     → term ( ( ">" | ">=" | "<" | "<=" ) term )* ;
term           → factor ( ( "-" | "+" ) factor )* ;
factor         → unary ( ( "/" | "*" ) unary )* ;
unary          → ( "!" | "-" ) unary | primary ;
primary        → NUMBER | STRING | "true" | "false" | "nil" | "(" expression ")" ;
```

#### Parsing Techniques

- [LL(k)](https://en.wikipedia.org/wiki/LL_parser)
- [LR(1)](https://en.wikipedia.org/wiki/LR_parser)
- [LALR](https://en.wikipedia.org/wiki/LALR_parser)
- [Parser Combinators](https://en.wikipedia.org/wiki/Parser_combinator)
- [Earley Parsers](https://en.wikipedia.org/wiki/Earley_parser)
- [The Shunting Yard Algorithm](https://en.wikipedia.org/wiki/Shunting-yard_algorithm)
- [Packrat Parsing](https://en.wikipedia.org/wiki/Parsing_expression_grammar)
- **[Recursive Descent.]() What is used in this interpreter**

| Grammar notation | Code representation               |
| ---------------- | --------------------------------- |
| Terminal         | Code to match and consume a token |
| Nonterminal      | Call to that rule’s function     |
| `\|`            | `if` or `switch` statement    |
| `*` or `+`   | `while` or `for` loop         |
| `?`            | `if` statement                  |
