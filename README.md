# Eseljik
Eseljik is based on [Stackylogic](http://codegolf.stackexchange.com/questions/84851/run-stackylogic), a "programming" language by Helka Homba.

Eseljik adds many new commands, possibly to help shorten programs, or be more useful.

Eseljik may be a golfing lang; A truth machine takes 3 bytes, a cat takes 4 bytes.

(The name comes from ***S*** tacky ***l*** o ***gic***.)

Input is saved in the variable, "a"
Variables only contain a string of ones and zeroes.
the position along a variable is reset each time the program is reset, while the content is not.

|Command|Usage                     |
|-------|--------------------------|
|last move|Not actually a command; each time the pointer moves this variable is set to the direction it moves|
|move   |Not actually a command;  what a 1 or 0 will be referred to as|
|(something that /[A-Za-z]+/g matches)|Variable reference. makes the variable denoted by the name the active variable. a is initially the active variable|
|1      |moves the pointer up one  |
|0      |moves the pointer down one|
|?      |subs with a move from active variable, move one along the variable (using the next move next ?)|
|<      |signals the start of the program. A program without one starts at the first stack with a question mark at the start, or should no stacks fulfil that, it starts on the first non-empty stack
|\|     |subs last move (last move is 1 or 0, and changes everytime the pointer moves)|
|_      |subs inverse of last move|
|#      |Restarts the program, with the active variable active by default|
|*      |Same as #, except it prints the latest move|
|@      |dumps all the content of the variable that the var pointer is across from (only useful when looping)|
|(      |adds "1" to the start of a the active variable|
|)      | (, but with 0|
|[|same as (, but at the end of active variable
|]|same as ), but at the end of active variable
|&|dumps active variable (active variable = '')|
|^|subs 0 if active variable is empty, else 1|
|=|the next command used is executed but the pointer stays stationary, but the latest move value changes
|:|subs with a move from active variable, without moving along the variable|
|;|moves one along the active variable|
|\\|subs 0 if last move was 1, else don't move|
|/|subs 1 if last move was 0, else don't move|
