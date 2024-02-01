# LTPF Project 

## Lexical Analysis and Parsing

This project consists of a simple implementation of lexical analysis and parsing for a programming language implemented in OCaml. The code provided includes functions for lexing and parsing expressions in the language.

### Lexical Analysis

The lexical analysis is performed using functions such as `terminal_lex`, `terminal_key_lex`, and `whitespace`. These functions define how tokens are identified from the input string.

For example:
```ocaml
let terminal_lex : (string -> (token) -> (token, char) ranalist) =
  fun str tok -> terminal_string str -+> epsilon_res tok
;;
```

This function defines a lexer for a specific keyword (`str`) and associates it with a corresponding token (`tok`). The `terminal_key_lex` function is a variant that checks if the keyword is not followed by an alphanumeric character.

### Parsing (AST Generation)

The parser is implemented using functions like `rVAL`, `rVAR`, `rE`, `rWHILE`, `rIF`, etc. These functions define how to parse expressions and statements in the language, generating an Abstract Syntax Tree (AST).

For example:
```ocaml
let rVAL : (bexp, token) ranalist =
  fun l -> match l () with
    | Cons(LexBoolean b, l) -> (Bcst b, l)
    | _ -> raise Echec
;;
```

This function parses a boolean value and constructs the corresponding AST node.

### AST Generation Usage Example

```ocaml
myLangToAST "if(valid == true) then !valid else valid "; 
```

This example demonstrates how to use the lexer and parser to generate the AST for a given input string.

## Warning

This project have been done mostly in french and is not finished.

## Authors 

- [Anastasios Tsiompanidis](https://github.com/AnastasiosTsio)
- [Alexis Noel](https://github.com/alexisnoeluga)
- [Noah Kohrs](https://github.com/noahkohrs)