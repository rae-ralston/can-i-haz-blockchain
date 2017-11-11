# Lexing & Parsing
Very halpful: [An Overview of Lexing & Parsing](http://savage.net.au/Ron/html/graphviz2.marpa/Lexing.and.Parsing.Overview.html#An_Overview_of_Lexing_and_Parsing). They happen in alphabetical order: Lexing then Parsing

## LEXING
  - [Wikipedia](https://en.wikipedia.org/wiki/Lexical_analysis)**lexing** is tokenising a stream of text, which means chopping that input stream into discrete tokens, and identifying the type of each token. The output is a new stream, this time of stand-alone tokens.
  - Analysis generally occurs in one pass.
  - Lexing can be divided into two stages:
    - the scanning, which segments the input string into syntactic units called *lexemes* and categorizes these into token classesA lexeme is a sequence of characters in the source program that matches the pattern for a token and is identified by the lexical analyzer as an instance of that token.
    - the evaluating, which converts lexemes into processed values.
    ![](./tokenValuesExample.png)
  So this:
  ```js
  x = a + b * 2;
  ```
  once it's lexed yields something like this:
  ```js
  [(identifier, x), (operator, =), (identifier, a), (operator, +), (identifier, b), (operator, *), (literal, 2), (separator, ;)]
  ```
  - for the string `The quick brown fox jumps over the lazy dog`
    - The tokens could be represented in XML,
      ```
      <sentence>
        <word>The</word>
        <word>quick</word>
        <word>brown</word>
        <word>fox</word>
        <word>jumps</word>
        <word>over</word>
        <word>the</word>
        <word>lazy</word>
        <word>dog</word>
      </sentence>
      ```
    - or as an [s-expression](https://en.wikipedia.org/wiki/S-expression) (for "symbolic expression", a notation for nested list (tree-structured) data)
      ```
      (sentence
        (word The)
        (word quick)
        (word brown)
        (word fox)
        (word jumps)
        (word over)
        (word the)
        (word lazy)
        (word dog))
      ```
  - For each recognized token, 2 items will be output:
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
## PARSING
  - [Wikipedia](https://en.wikipedia.org/wiki/Parsing) - The **parser** concerns itself with the context in which each token appears, which is a way of saying it cares about whether or not the sequence and combination of tokens actually detected fits the expected grammar.
