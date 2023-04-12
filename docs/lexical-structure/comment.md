> **<sup>Lexer</sup>** <br>
> COMMENT :<br>
> &nbsp;&nbsp;&nbsp;&nbsp; `//` (~\[`/` `!` `\n`] | `//`) ~`\n`<sup>\*</sup><br>
> &nbsp;&nbsp; | `//`
>
> MODULE_DOCSTRING :<br>
> &nbsp;&nbsp; `//!` ~\[`\n` _IsolatedCR_]<sup>\*</sup>
>
> LOCAL_DOCSTRING :<br>
> &nbsp;&nbsp; `///` (~`/` ~\[`\n` _IsolatedCR_]<sup>\*</sup>)<sup>?</sup>
>
> _IsolatedCR_ :<br>
> &nbsp;&nbsp; _A `\r` not followed by a `\n`_

## Examples

``` hl_lines="1 3 6 9 11 15" linenums="1"
//! The module defines Json AST nodes.

/// Json object is a list of key value pairs.
pub struct Json = [JsonKeyValuePair];

/// Json key value pair where key is a string.
pub struct JsonKeyValuePair = Tuple[String, JsonValue];

/// Literal
pub type JsonLiteral = Sum[u64, bool, f64, String];
/// Value
pub type JsonValue = Json | JsonLiteral | JsonArray;

pub struct JsonArray {
    // Vector of json values
    pub inner: [JsonValue]
};

...
```

[Pattern_White_Space]: https://www.unicode.org/reports/tr31/