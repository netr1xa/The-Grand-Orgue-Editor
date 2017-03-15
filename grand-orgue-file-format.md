# **The Grand Orgue file format**

### General Information
#### File Extension
.organ

#### Encoding
ISO-8859-1 or UTF-8 with BOM (Byte Order Mark)

#### Elements
* ##### Comments and empty lines
  Comments start with `;` on the first position of a line. Empty lines are ignored.

* ##### Blocks and settings
  A block is a section that starts with `[` on the first position of a line, followed by the section name and ends with `]`. Each block consists of settings which are key-value pairs separated by `=`.
###### Q: <span style="color:red">Are spaces around `=` ignored?</span>

  Basically settings are grouped in blocks. Each setting may occur only once and is case-sensitive.

No other elements are allowed in the file.

#### File references
Settings may contain references to external files specified by a file path. The file path is treated relative to the location of the .organ file. The directory separator must be `\`. File paths must not contain `/` and should be considered case-sensitive, even if this is not enforced on all platforms.

#### Boolean values
Boolean values are represented as `Y` for `true` and `N` for `false`.

#### Colors
A color can be one of the following values (not case-sensitive):

> `BLACK`, `BLUE`, `DARK BLUE`, `GREEN`, `DARK GREEN`,
`CYAN`, `DARK CYAN`, `RED`, `DARK RED`, `MAGENTA`, `DARK MAGENTA`, `YELLOW`, `DARK YELLOW`, `LIGHT GREY`,
`DARK GREY`, `WHITE`, `BROWN`

Additionally, the HTML color format `#RRGGBB` is supported.
