# Brackets
## `[ ]`
- Is a shell built-in command
- Is POSIX compliant and exists for backward compatibility
- Is equivalent to `test` build-in command
```bash
[ 3 -eq 3 ] && echo 'equal'
test 3 -eq 3 && echo 'equal'
```
- Must use `-a` and `-o` for logical AND and OR
```bash
[ 3 -eq 3 -a 4 -eq 4 ] && echo “Numbers are equal”
```
- Can't use string-operators (`<`, `>`, `()` and so on) without escape characters
```bash
[ 1 \< 2 ] && echo “1 is less than 2”
[ 3 -eq 3 -a \( 2 -eq 2 -a 1 -eq 1 \) ] && echo “Parentheses can be used”
```

## `[[ ]]`
- Is a shell keyword
- Is a convenient alternative to `[ ]` and is not POSIX compliant
- Must use `&&` and `||` for logical AND and OR
```bash
[[ 3 -eq 3 && 4 -eq 4 ]] && echo “Numbers are equal”
```
- Can pattern match
```bash
name=Alice
[[ $name = *c* ]] && echo “Name includes c”
```
- Supports Regex
```bash
name=Alice
[[ $name =~ ^Ali ]] && echo ”Regular expressions can be used”
```