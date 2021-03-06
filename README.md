LCS-tableau-cilk
================

LCS using Cilk

We always assume the tableau is NxN, so in order to have an empty symbol on position [1, 1] we use strings of length N-1. So, in the program N is the length of the edge of the tableau, the actual string is N-1. 

To compile:
cilk++ code1 -g -O1 -lcilkutil -o code1
cilk++ code1-s -g -O1 -lcilkutil -o code1-s
cilk++ code2 -g -O1 -lcilkutil -o code2
cilk++ code2-s -g -O1 -lcilkutil -o code2-s

To run (examples):

./code1 
runs parallel code1 (2x2 tableau) with n=16

./code1 16 y
runs parallel code1 (2x2 tableau) with n=16 and outputs the tableau

./code1 1024
runs parallel code1 (2x2 tableau) with n=1024


./code1-s 
runs sequential code1-s (2x2 tableau) with n=16

./code1-s 16 y
runs sequential code1-s (2x2 tableau) with n=16 and outputs the tableau

./code-s 1024
runs sequential code1-s (2x2 tableau) with n=1024


./code2
runs parallel code2 (4x4 tableau) with n=16

./code2 16 y
runs parallel code2 (4x4 tableau) with n=16 and outputs the tableau

./code2 1024
runs parallel code2 (4x4 tableau) with n=1024


./code2-s 
runs sequential code2 (4x4 tableau) with n=16

./code2-s 16 y
runs sequential code2 (4x4 tableau) with n=16 and outputs the tableau

./code2-s 1024
runs sequential code2 (4x4 tableau) with n=1024


