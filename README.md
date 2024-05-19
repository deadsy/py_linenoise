# py_linenoise

A port of linenoise to Python (because sometimes readline doesn't cut it...)

See: http://github.com/antirez/linenoise

## Standard Features
 * Single line editing
 * Multiline editing
 * Input from files/pipes
 * Input from unsupported terminals
 * History
 * Completions
 * Hints

## Other Features
 * Line buffer initialization: Set an initial buffer string for editing.
 * Hot keys: Set a special hot key for exiting line editing.
 * Loop Functions: Call a function in a loop until an exit key is pressed.

## Examples

### example1.py

Matches the example code in the C version of the linenoise library.

### example2.py

Implements a heirarchical command line interface using cli.py and the linenoise library.

### example_non_blocking.py

Shows how the non-blocking API can be used.

## Motiviation

The GNU readline library is a standard package in Python, but sometimes it's hard to use:

 * How do you have a hot key exit the line editing so you can offer context sensitive help?
 * How do you call a polling function during line editing so you can check for other things?

Having a simple, hackable, native Python implementation of line editing makes these things much easier.
The linenoise library in C already offers a simple alternative.
Porting these functions to Python makes it even easier to use on any system with a POSIX compatible terminal environment.
