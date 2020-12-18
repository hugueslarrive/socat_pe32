# socat_pe32

socat extracted from cygwin for use as serial terminal within WSL 2.

My serial adapter COM3 is mapped to /dev/ttyS2 in cygwin so ttyS number seems to be COM number -1.

```
$ ldd /usr/bin/socat.exe
        ntdll.dll => /cygdrive/c/Windows/SYSTEM32/ntdll.dll (0x7ff821b90000)
        KERNEL32.DLL => /cygdrive/c/Windows/System32/KERNEL32.DLL (0x7ff820bd000
0)
        KERNELBASE.dll => /cygdrive/c/Windows/System32/KERNELBASE.dll (0x7ff81f5
e0000)
        cygwin1.dll => /usr/bin/cygwin1.dll (0x180040000)
        cygcrypto-1.0.0.dll => /usr/bin/cygcrypto-1.0.0.dll (0x3ffd00000)
        cygssl-1.0.0.dll => /usr/bin/cygssl-1.0.0.dll (0x3ff110000)
        cygwrap-0.dll => /usr/bin/cygwrap-0.dll (0x3fee70000)
        cygreadline7.dll => /usr/bin/cygreadline7.dll (0x3ff1c0000)
        cygz.dll => /usr/bin/cygz.dll (0x3fee50000)
        cygncursesw-10.dll => /usr/bin/cygncursesw-10.dll (0x3ff3e0000)
$ cp /usr/bin/cygwin1.dll  /usr/bin/cygcrypto-1.0.0.dll /usr/bin/cygssl-1.0.0.dll /usr/bin/cygwrap-0.dll /usr/bin/cygreadline7.dll /usr/bin/cygz.dll /usr/bin/cygncursesw-10.dll /usr/bin/socat.exe .
```
