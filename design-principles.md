# Google Sheets Formula Design Principles

## Structure
- **LET for clarity**: Name intermediate values. Makes logic parsable, debuggable.
- **HSTACK/VSTACK over {}**: Explicit array construction, less ambiguous.
- **Build diagnostics first**: Test intermediate outputs before full formula. Use VSTACK to inspect dimensions, values.

## Array Operations
- **MAP for element-wise**: When built-ins aren't array-aware (TEXT, IF), wrap in MAP.
- **FILTER conditions**: 
  - AND: multiply conditions `(cond1)*(cond2)`
  - OR: add conditions `(cond1)+(cond2)`
- **INDEX(array, 0, col)**: Extract entire column.
- **BYROW/BYCOL + LAMBDA**: Process each row/column independently.

## Common Patterns
- **Densify sparse data**: `FILTER(range, BYROW(range, LAMBDA(r, COUNTA(r) > 0)))`
- **Multi-column filtering**: Multiply boolean arrays for simultaneous matches.
- **Custom aggregation**: UNIQUE + BYROW + LAMBDA + FILTER pipeline.
- **Text from arrays**: MAP to format, then TEXTJOIN.

## Debugging Strategy
1. Build simple diagnostic showing intermediate dimensions/values
2. Isolate failing component 
3. Fix with proper array handling (MAP, ARRAYFORMULA, or restructure)
4. Reintegrate into full formula

## Avoid
- Assuming functions are array-aware without testing
- Nested {} syntax when HSTACK/VSTACK clearer
- Fixing errors without understanding root cause
- Premature optimization over readability