> **<sup>Syntax</sup>**<br>
> _Import_ :<br>
> &nbsp;&nbsp; `import` _ImportPath_ `;`
> 
> _ImportPath_ :<br>
> &nbsp;&nbsp; [IDENTIFIER] (`.` [IDENTIFIER])<sup>\*</sup>

Examples:
```ry
import std.io.println;
import std.fs.File;
```

In this case _ImportPath_ represents absolute path to a **concrete item** like function, trait, struct, etc or **module**.

Ry firstly checks if a path begins with `std` and if it does, then it searches for modules inside the folder `$RYPATH/std/`.

If it doesn't, then it goes to `$RYPATH/site-packages/`. It stores them in such format: `package_name@version_number`. Ry compiler chooses the version written down in `dependencies.toml`.

[IDENTIFIER]: ../lexical-structure/identifier.md