# exp10_284 — For Loop Syntax Validator (Lex & Yacc)

Validates the syntax of a C-style `for` loop using Lex and Yacc.

## Files
- `exp10_284.l` — Lex file (tokenizer)
- `exp10_284.y` — Yacc file (grammar rules)


## Build & Run

```bash
yacc -d exp10_284.y
lex exp10_284.l
gcc y.tab.c lex.yy.c -o exp10_284 -ll
./exp10_284
```

## Sample Output

```
Enter a for loop:
for(i=0; i<10; i++)
Valid for loop
```

```
Enter a for loop:
for(i=0 i<10; i++)
Invalid for loop
```
