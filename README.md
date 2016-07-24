# Eseljik
Eseljik is based on Stackylogic, a "programming" language by Helka Homba.

Eseljik adds many new commands, possibly to help shorten programs, or be more useful.

Eseljik may be a golfing lang; A truth machine takes 3 bytes, a cat takes 4 bytes.

|Command|Usage                     |
|-------|--------------------------|
|last move|Not actually a command; each time the pointer moveds this variable is set to the direction it moves|
|move   |Not actually a command;  what a 1 or 0 will be referred to as|
|1      |moves the pointer up one  |
|0      |moves the pointer down one|
|?      |subs with a move from input|
|<      |signals the start of the program. A program without one starts at the first stack with a question mark at the start, or should no stacks fulfil that, it starts on the first non-empty stack
|\|     |subs last move (last move is 1 or 0, and changes everytime the pointer moves)|
|_      |subs inverse of last move|
|#      |Restarts the program, and goes back to the start of input, and self_input|
|*      |Same as #, except it prints the latest move|
|@      |dumps all the input already used (only useful when looping)|
|(      |adds "1" to the start of a special variable, self-input. Self-input is used as input before main input is accessed, next run|
|)      | (, but with 0|
|[|same as (, but at the end of self_input
|]|same as ), but at the end of self_input
|&|dumps original input|
|%|dumps self-input
|^|subs 0 if self-input is empty, else 1|
|:|subs 0 if regular input is empty, else 1|
|=|the next command used is executed but the pointer stays stationary, but the latest move value changes
|\\|subs 0 if last move was 1, else don't move
|/|subs 1 if last move was 0, else don't move
