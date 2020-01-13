# Executable file decompile

Executable file decompile 

## Decompile란?
>A decompiler is a computer program that takes an executable file as input, and attempts to create a high level source file which can be recompiled successfully. It is therefore the opposite of a compiler, which takes a source file and makes an executable. Decompilers are usually unable to perfectly reconstruct the original source code, and as such, will frequently produce obfuscated code. Nonetheless, decompilers remain an important tool in the reverse engineering of computer software.
[WIKIPEDIA](https://en.wikipedia.org/wiki/Decompiler)

## EXAMPLE

1. First, make an EXE file ```pyinstaller sample.py```

```python
# sample (./sample.py)

def Hello():
    print('Hello World !')

if __name__ == '__main__':
    Hello()
```
