# utilscss
A set of css utilities, like grid, spacing (margin, padding), sizing, flexbox, etc.

## Responsive prefixes
Css selectors which has multiple versions for different breakpoints has a prefix.   
For example a column:

```
.col-4
.sm:col-4
.md:col-4
.lg:col-4
.xlg:col-4
```
An example usage:

```
<div class="sm:col-6 md:col-4"></div>
```

Default sizes:

```
sm: 576px,
md: 768px,
lg: 992px,
xlg: 1200px
```

Default spacing values:

```
0: 0
xs: 5px
sm: 10px
md: 15px
lg: 20px
xlg: 30px
auto: auto
```

Example: `<div class="pt-md mr-xs md:mr-auto"></div>`

Which means:
- Padding top medium (15px) for all sizes
- Margin right extra small (5px) for all sizes
- Margin right auto above 768px

Media queries defined with `min-width`. For the `sm` prefix the following will be defined:
```
@media (min-width: 576px) {
    ...
}
```

## Responsive prefixed categories:

|Category | Example |
|-----|-------|
|Display|`md:d-block sm:d-none`|
|Column|`md:col-4 sm:col-4`|
|Margin|`md:mt-10 sm:mt-5`|
|Padding|`md:pt-10 sm:pt-5`|
|Flex|`md:d-flex md:items-center md:flex-row flex-column`|


## Selectors

### Grid
```
- row
- col-[1-12]
- sm:col-[1-12]
- ...
```

**Example:**  
`<div class="col-6 md:col-4">`

Explanation: 
 - Using 6 column width on all screen sizes
 - When screen sizes is above `"md"` using 4 column width

### Margin and padding
Build up with the following syntax: `{property}{side}-{size}`.

Properties one of:
- `m`: as margin
- `p`: as padding

Sides is one of:
- `t`: as top
- `b`: as bottom
- `l`: as left
- `r`: as right
- `x`: as horizontal
- `y`: as vertical

**Example:**  
`<div class="mb-lg px-xs py-sm></div>`
