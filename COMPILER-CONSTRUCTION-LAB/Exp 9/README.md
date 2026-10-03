# Experiment 9 — Desk Calculator (YACC + Lex)

A desk calculator built with Lex (`cal_1284.l`) for tokenizing and Yacc
(`cal_1284.y`) for parsing/evaluating arithmetic expressions
(`+ - * /`, parentheses, operator precedence, division-by-zero and
syntax-error handling).

## Terminal session
```
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ vim cal_1284.l
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ vim cal_1284.y
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ yacc -d cal_1284.y
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ lex cal_1284.l
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ gcc y.tab.c lex.yy.c -o cal_1284 -ll
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ ./cal_1284
Desk Calculator: Enter expressions (Ctrl+C to exit)
10+50
Result = 60
^C
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ ./cal_1284
Desk Calculator: Enter expressions (Ctrl+C to exit)
50*60+2
Result = 3002
^C
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ vim cal_1284.l
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ vim cal_1284.y
sit-lab2-pc29@sit-lab2-pc29-OptiPlex-3280-AIO:~$ ./cal_1284
Desk Calculator: Enter expressions (Ctrl+C to exit)
12*50+95-10/2
Result = 690
```

## Build steps
```
yacc -d cal_1284.y      # generates y.tab.c and y.tab.h
lex cal_1284.l          # generates lex.yy.c
gcc y.tab.c lex.yy.c -o cal_1284 -ll
./cal_1284
```

