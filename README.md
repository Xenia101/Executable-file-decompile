# Executable file decompile

Executable file decompile (sample.exe → sample.py)

## Decompile란?
>A decompiler is a computer program that takes an executable file as input, and attempts to create a high level source file which can be recompiled successfully. It is therefore the opposite of a compiler, which takes a source file and makes an executable. Decompilers are usually unable to perfectly reconstruct the original source code, and as such, will frequently produce obfuscated code. Nonetheless, decompilers remain an important tool in the reverse engineering of computer software.
[WIKIPEDIA](https://en.wikipedia.org/wiki/Decompiler)

## Example

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
    - ```pyinstxtractor.py``` at ./pyinstxtractor.py

3. Run ```pyinstxtractor.py``` in CMD

    ``` python pyinstxtractor.py ./build/sample/sample.exe ```

4. Find magic number using HxD..

- Any file in sample.exe_extracted ex) pyimod01_os_path

<p align=center>
    <img src="https://github.com/Xenia101/Executable-file-decompile/blob/master/img/pyimod01_os_path.PNG?raw=true"/>
</p>

- origin file sample (A file named sample)

<p align=center>
    <img src="https://github.com/Xenia101/Executable-file-decompile/blob/master/img/sample.PNG?raw=true"/>
</p>

**E3 is magic number** Copy it and put it in front of origin file E3. Then save the origin file as **.pyc**

5. Look at the final folder with sample.pyc (./final) and Run ```change_to_py_sample.py```

6. Finally, look at the output ```sample.py```

    ```python
    # uncompyle6 version 3.6.2
    # Python bytecode 3.6 (3379)
    # Decompiled from: Python 3.6.2 (v3.6.2:5fd33b5, Jul  8 2017, 04:57:36) [MSC v.1900 64 bit (AMD64)]
    # Embedded file name: sample.py
    # Compiled at: 1995-09-28 01:18:56
    # Size of source mod 2**32: 3062 bytes

    def Hello():
        print('Hello World !')
        
    if __name__ == '__main__':
        Hello()
    ```

