# Activity 1: Dev Environment Setup

- Installed VS Code and the Microsoft C/C++ extension.
- Installed MinGW-w64 (GCC 16.2.0) through MSYS2 using pacman.
- Problem: gcc still reported the old MinGW 6.3.0 after installing MSYS2.
- Cause: `C:\MinGW\bin` was in the System PATH, which has priority over the User PATH entry for MSYS2.
- Fix: removed `C:\MinGW\bin` from the System PATH and restarted VS Code.
- Problem: linker error "cannot open output file hello.exe: Permission denied". Fix: deleted the old hello.exe and recompiled.
- Verified with `gcc --version` and ran hello.c successfully.