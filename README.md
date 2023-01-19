# Stacks, Queues - LIFO, FIFO
## Monty


**Authors:** *Surina Singh and Ruven Pillay*

## Description
Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

## Compilation
*Your code will be compiled this way:
```$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty```

---

## Commands
1. ```push```
Pushes an integer onto the stack.
2. ```pall```
Prints all integers on the stack, starting at the top..
3. ```pint```
Prints the integer at the top of the stack.
4. ```pop```
Removes top element of stack.
5. ```swap```
Swaps top two elements of the stack.
6. ```add```
Add top two elements of the stack, remove them, and push result onto stack.
7. ```sub```
Subtract top two elements of the stack, remove them, and push result onto stack.
8. ```div```
Integer divide top two elements of the stack, remove them, and push result onto stack.
9. ```mul```
Multiply top two elements of the stack, remove them, and push result onto stack.
10. ```mod```
Integer division remainder top two elements, remove them, push result onto stack.
11. ```pchar```
Print the ascii character based on top integer in stack.
12. ```pstr```
Print the ascii characters related to integers in stack until 0 or >255.
13. ```rotl```
Rotate stack. Top element becomes last. Second from top becomes top.
14. ```rotr```
Rotate stack. Last element becomes top, Top element becomes second from top.
15. ```stack```
Changes mode to first in first out (the default behavior). Front of queue becomes top of stack.
16. ```queue```
Changes mode to last in first out. Top of stack becomes front of queue.

## Getting started
Clone the repository and run "gcc -o monty *.c". Then run "./monty \<scriptname\>"

## Usage Examples
The simplest usage is to push a few values onto the stack then print them all. Lets say we have a file like so:
```
push 1
push 2
push 3
pall
```
When we run this with "./monty scriptfile" we get the output:
```
3
2
1
```
To use some of the math functions, we can write a script like so:
```
push 1
push 2
push 3
pall
add
add
pall
```
This nets us an output:
```
3
2
1
6
```
If we want to print numbers as a string, we can have a script like:
```
push 49
push 50
push 51
pstr
```
This gets the output "321"
~