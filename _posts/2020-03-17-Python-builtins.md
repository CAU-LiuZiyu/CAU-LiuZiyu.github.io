---
layout: post
title: "Cheat-sheet for Python Builtins"
date: 2020-03-17
---

While learning and using Python, I guess it would be nice to have a cheatsheet about all the builtins.

```
dir(__builtins)

', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'WindowsError', 'ZeroDivisionError', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'breakpoint', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip'
```

### 1. [All Kinds of Exceptions](https://docs.python.org/3/library/exceptions.html#OSError)

All kinds of Exceptions are included in the builtins, i.e. Errors, Warnings, etc. Remember that BaseException class is 'father' of all of them!

- BaseException
    - Exception
        - ArithmeticError
            - FloatingPointError # I don't know whether it's in use now?
            - OverflowError  # way too big numbers
            - ZeroDivisionError
        - BufferError   # haven't met this one yet
        - LookupError
            - IndexError
            - KeyError
        - AssertionError
        - AttributeError
        - EOFError      # EOF = end of file
        - ImportError
            - ModuleNotFoundError
        - MemoryError   # memory is consumed!
        - NameError
            - UnboundLocalError
        - OSError
            - BlockingIOError
            - ChildProcessError
            - ConnectionError
                - BrokenPipeError
                - ConnectionAbortedError
                - ConnectionRefusedError
                - ConnectionResetError
            - EnvironmentError
            - FileExistsError
            - FileNotFoundError
            - IOError
            - InterruptedError
            - IsADirectoryError
            - NotADirectoryError
            - PermissionError
            - ProcessLookupError
            - TimeoutError
            - WindowsError
        - ReferenceError
        - RuntimeError
            - NotImplementedError  # different from 'NotImplemented'
            - RecursionError   # exceed maximum recursion depth
        - StopIteration  # raised by next()
        - StopAsyncIteration
        - SyntaxError
            - IndentationError
                - TabError
        - SystemError  # Error of python interpreter
        - TypeError
        - ValueError
            - UnicodeError
                - UnicodeDecodeError
                - UnicodeEncodeError
                - UnicodeTranslateError
        - Warning
            - BytesWarning
            - DeprecationWarning
            - FutureWarning
            - ImportWarning
            - PendingDeprecationWarning
            - ResourceWarning
            - RuntimeWarning
            - SyntaxWarning
            - UnicodeWarning
            - UserWarning
    - GeneratorExit
    - KeyboardInterrupt   # usually control-c or Delete
    - SystemExit

### 2. [All Kinds of Builtin Constants](https://docs.python.org/3/library/constants.html)

These constants include: 
Ellipsis, '...', usually used in unfinished functions and classes.

False, True, two key bool type value.

None, NoneType, represnet the absence of a value.

NotImplemented, special value.

\__debug__, this constant is true if Python was not started with an -O option

quit, exit, copyright, credits, license

### 3. [All Kinds of Builtin Functions](https://docs.python.org/3/library/functions.html)


abs()

delattr()

hash()

memoryview()

set() 

all()|dict()

help()

min()

setattr()

any()

dir()

hex()

next()

slice()

ascii()

divmod()

id()

object()

sorted()

bin()

enumerate()

input()

oct()

staticmethod()

bool()

eval()

int()

open()

str()

breakpoint()

exec()

isinstance()

ord()

sum()

bytearray()

filter()

issubclass()

pow()

super()

bytes()

float()

iter()

print()

tuple()

callable()

format()

len()

property()

type()

chr()

frozenset()

list()

range()

vars()

classmethod()

getattr()

locals()

repr()

zip()

compile()

globals()

map()

reversed()

\_\_import\_\_()

complex()

hasattr()

max()

round()

(to be continued...)