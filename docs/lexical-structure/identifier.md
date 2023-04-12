> **<sup>Lexer:<sup>**<br>
> IDENTIFIER_OR_KEYWORD :<br>
> &nbsp;&nbsp;&nbsp;&nbsp; (XID_Start | `_`) XID_Continue<sup>\*</sup>
>
> RAW_IDENTIFIER :<br>
> &nbsp;&nbsp;&nbsp;&nbsp;  `` ` `` IDENTIFIER_OR_KEYWORD `` ` ``
>
> IDENTIFIER :<br>
> &nbsp;&nbsp;&nbsp;&nbsp; IDENTIFIER_OR_KEYWORD <sub>*Except keyword*</sub><br>
> &nbsp;&nbsp;&nbsp;&nbsp; | RAW_IDENTIFIER

## Raw identifier
A raw identifier is like a string, but with `` ` `` instead of `"`. Unlike a normal identifier, a raw identifier may be any reserved keyword and still have no conflicts. It may also have whitespaces inside. Here are some examples:
```ry
`test`
`pub`
`valid raw identifier`
``
```

> * Note that raw identifiers behave the same as usual ones. So usual identifier `test` and raw identifier `` `test` `` are the same thing for the parser.

> * Empty raw identifier is **valid**.
> ```ry hl_lines="4"
> `test`
> `pub`
> `valid raw identifier`
> ``
> ```

There is some analogy with Rust that also has raw identifiers:

=== "Ry"

    ```ry
    `test`
    `pub`
    `valid raw identifier`
    ``
    ```

=== "Rust"

    ``` c++
    r#test
    r#pub
    // no way
    // no way
    ```