# can i haz blockchain?

A CONTRACT-ORIENTD, HIGH-LEVEL LANGUAGE WHOSE SYNTAX IZ SIMILAR 2 DAT OV [LOLCODE](http://lolcode.org/) AN IT DESIGND 2 TARGET TEH ETHEREUM VIRTUAL MACHINE (EVM)

## BUT HOW THO?
1. Define some syntax.
1. Map to required EVM bytecode.

### Lexing & Parsing
- Very halpful: [An Overview of Lexing & Parsing](http://savage.net.au/Ron/html/graphviz2.marpa/Lexing.and.Parsing.Overview.html#An_Overview_of_Lexing_and_Parsing)
  **LEXING**
  - They happen in alphabetical order: Lexing then Parsing
  - [Wikipedia](https://en.wikipedia.org/wiki/Lexical_analysis)**lexing** is tokenising a stream of text, which means chopping that input stream into discrete tokens, and identifying the type of each token. The output is a new stream, this time of stand-alone tokens.
  - for each recognized token, 2 items will be output:
    - The type of the token
    - The value of the token
    ```js
      {
        count: 'integer',     // 1 .. N.
        name: '',           // Unused.
        type: 'string',     // The type of the token.
        value: 'value',     // The value from the input stream.
      }
    ```
  **PARSING**
  - [Wikipedia](https://en.wikipedia.org/wiki/Parsing) - The **parser** concerns itself with the context in which each token appears, which is a way of saying it cares about whether or not the sequence and combination of tokens actually detected fits the expected grammar.


### Links & Resources
- Deeply inspired by [kosamari](https://twitter.com/kosamari)'s work: How to be* a compiler — make a compiler with JavaScript: [Article](https://medium.com/@kosamari/how-to-be-a-compiler-make-a-compiler-with-javascript-4a8a13d473b4), [StrangeLoop Presentation](https://www.youtube.com/watch?v=-xlbfBUZN5s)
- LOLCODE: [documentation](http://lolcode.org/), [Wikipedia](https://en.wikipedia.org/wiki/LOLCODE)
- Solidity [Documentation](https://solidity.readthedocs.io/en/develop/), [Github](https://github.com/ethereum/solidity)
- [LOLCAT translator](http://speaklolcat.com/)
- [An Introduction to KP Language](http://www.cs.cmu.edu/~taey/pub/knit.pdf)
- [Stack Exchange: How to Write a Very Basic Compiler](https://softwareengineering.stackexchange.com/questions/165543/how-to-write-a-very-basic-compiler)
- [DOT language outline](http://www.graphviz.org/content/dot-language)
