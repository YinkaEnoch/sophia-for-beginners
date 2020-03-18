Introduction
==

Sophia is a functional language used in writing smart contracts on the aeternity block chain. The language is strongly typed, which means the compiler checks for syntax errors during compilation. Sophia uses Python-style layout rules to group declarations and statements. Blocks with a single element can be written on the same line as the previous token. Each element of the block must share the same indentation and no part of an element may be indented less than the indentation of the block.


[Check out the Official Definition](https://github.com/aeternity/aesophia/blob/lima/docs/sophia.md)

[Sophia Layout Blocks](https://github.com/aeternity/aesophia/blob/lima/docs/sophia.md#layout-blocks)


Comment
==

Sophia supports both the single line and multi-line comment (or block comment).

**Single line comment starts with //**

This example uses a single line comment
```sophia

// The function checks if a name exist in the state record

entrypoint nameExists(name: string) : bool =
      Map.member(name, state.hamsters)
```

**Multi-line comments start with /\* and end with \*/**

This example uses a multi-line comment 
```sophia
/*
* Checks if a name exists in the state record
* @param {string} name
* @returns {bool} 
*/

entrypoint nameExists(name: string) : bool =
    Map.member(name, state.hamsters)
```


Variables
==

Variables are declared in Sophia by the keyword `let`

```sophia
let x: int = 4

let userAddress: address = Call.caller

let name: string = 'YinkaEnoch'
```
