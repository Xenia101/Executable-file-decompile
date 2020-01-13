# Executable file decompile

Executable file decompile (sample.exe → sample.py)

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

2. Prepare sample.exe file (./build/sample/sample.exe) and install HxD, uncompyle6, pyinstxtractor.py
    - [HxD](https://mh-nexus.de/en/hxd/)
    - ```pip install uncomple6```
    - pyinstxtractor.py at ./pyinstxtractor.py

3. Run pyinstxtractor.py in CMD

    ``` python pyinstxtractor.py sample.exe ```
    
4. 
