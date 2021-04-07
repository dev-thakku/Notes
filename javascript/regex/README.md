# Regular Expressions
Regular Expressions (`regex` or `regexp`) are mainly used to match, search, and replace patterns. Regular expressions are very powerful, but can be hard to read because they use special characters to make more complex, flexible matches.

expression are enclosed in `\`. 

Exapmle:
```javascript
let regex = /expression/;
```

## Test Method
Test Method `.test()` returns `true` if it matches and `false` if it doesn't.

Syntax:
```javascript
regex.test(str);
```
>**Note:** *`str` pretends to be a string and `regex` prentended to be a regular expression.*

## Match Method
Match Method `.match()` returns the exact matches.

Syntax:
```javascript
str.match(regex);
```
>**Note:** *`str` pretends to be a string and `regex` prentended to be a regular expression.*

## Flags
They are added after the closing of `/` in *regex*.

- `i` flag: used to **ignore cases**.
- `g` flag: used to **extract a pattern**.

Syntax:
```javascript
let regex = /expression/gi;
```
>**Note:** *We can use more than one flag simultaneously.*

## Wild Card
The wildcard character `.` will match any one character. The wildcard is also called `dot` and `period`.

For example, if you wanted to match hug, huh, hut, and hum, you can use the regex /hu./ to match all four words:
```javascript
let humStr = "I'll hum a song";
let hugStr = "Bear hug";

let huRegex = /hu./;

huRegex.test(humStr);
huRegex.test(hugStr);
```
Both of these `test()` calls would return `true`.

## Character Sets
They are used to specify a set of Characters in *regex*.

Example:
```javascript
const str1 = "Bag";
const str2 = "Big";
const str3 = "Beg";

const regex = /b[ai]g/;

let r1 = regex.test(str1);
let r2 = regex.test(str2);
let r3 = regex.test(str3);
```
In the above example `r1` will be `true`, `r2` also will be `true` and `r3` will be `false`.

#### With Flag `g`
```javascript
const str1 = "Bag";
const str2 = "Big";
const str3 = "Beg";

const regex = /b[aie]g/g;

let r1 = regex.match(str1);
let r2 = regex.match(str2);
let r3 = regex.match(str3);
```
In the above example `r1` will be `["Bag"]`, `r2` will return `["Big"]` and `r3` will return `["Bag"]`.

### Specifiying Range
We can easily specify a range of characters in the character set using a hyphen `-`.

Example:
```js
const regex = /m[a-z]n/;
```
In the above example the `regex` will be equals to `"man"`, `"mbn"`, `"mcn"`, ..., `"mzn"`.