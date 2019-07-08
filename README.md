# CSS Variables for ie11!
Custom Properties polyfill for IE11


## It can:
- handle dynamic added `<style>`, `<link>`-elements
- handle dynamic added html-content
- cascade works
- inheritance works
- chaining `--bar:var(--foo)`
- fallback works `var(--color, blue)`
- :focus, :active, :hover
- js-integration:  
    - `style.setProperty('--x','y')`
    - `style.getPropertyValue('--x')`
    - `getComputedStyle(el).getPropertyValue('--inherited')` !!
- under 2k gziped, who would have thought that?

## Limitations
### styles in element-attributes
There is no way to get the raw content of style-attributes in IE11
I could implement the following if someone needs it: 
`<div style="--color:blue; -ie-color:blue">` OR `<div style="--color:blue" ie-style="--color:blue">` what do you prefer?
### specificity for properties containing "var()"
...is always little highter, cause each selector gets an additional class-selector  
eg. `#header` results in `#header.iecp_u44`

## Demo:
https://rawcdn.githack.com/nuxodin/ie11CustomProperties/450c5a1ba1064679d6d6fe60681dd43a08439800/test.html

## Help wanted!
Please test and report bugs.  
And add a ⭐️ and tweet about if you like it.
