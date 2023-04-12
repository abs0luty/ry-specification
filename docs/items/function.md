> **<sup>Syntax</sup>**<br>
> _Function_ :<br>
> &nbsp;&nbsp; `pub`<sup>?</sup> `fun`
>   [IDENTIFIER]
>   [_Generics_]<sup>?</sup>
>   `(` _FunctionArguments_ `)`
>   [_WhereClause_]<sup>?</sup>
>   ( [_StatementsBlock_] | `;` )
> 
> _FunctionArguments_ :<br>
> &nbsp;&nbsp; _FunctionArgument_ (`,` _FunctionArgument_)<sup>\*</sup> (`,` `...`)<sup>?</sup> `,`<sup>`?`</sup>
> 
> _FunctionArgument_ :<br>
> &nbsp;&nbsp; [IDENTIFIER] `:` [_Type_]

Examples:

```ry
pub fun sum[T: Numeric](a: T, b: T): T {
    a + b
}

pub fun len(s: string): usize {
    s.len()
}
```

```ry title="std/fmt.ry" 
pub fun print(format: string, ...);
```

[IDENTIFIER]: ../lexical-structure/identifier.md
[_Generics_]: generics.md
[_WhereClause_]: where_clause.md
[_Type_]: type.md
[_StatementsBlock_]: statements_block.md