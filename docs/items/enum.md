> **<sup>Syntax</sup>**<br>
> _EnumDeclaration_ :<br>
> &nbsp;&nbsp; `pub`<sup>?</sup> `enum`
>   [IDENTIFIER]
>   `{` _EnumVariants_<sup>?</sup> `}`
> 
> _EnumVariants_ :<br>
> &nbsp;&nbsp; [IDENTIFIER] (`,` [IDENTIFIER])<sup>\*</sup> `,`<sup>?</sup>

Example:
```ry
enum RGB {
    Red,
    Green,
    Blue
}
```

[IDENTIFIER]: ../lexical-structure/identifier.md