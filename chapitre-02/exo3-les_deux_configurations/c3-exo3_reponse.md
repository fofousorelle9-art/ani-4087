1- Construction en Debug


Laeti@Laeti MINGW64 ~/desktop/jenga/sorelle (main)
$ jenga build --config Debug

╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║                ██╗███████╗███╗   ██╗ ██████╗  █████╗             ║
║                ██║██╔════╝████╗  ██║██╔════╝ ██╔══██╗            ║
║                ██║█████╗  ██╔██╗ ██║██║  ███╗███████║            ║
║           ██   ██║██╔══╝  ██║╚██╗██║██║   ██║██╔══██║            ║
║           ╚█████╔╝███████╗██║ ╚████║╚██████╔╝██║  ██║            ║
║            ╚════╝ ╚══════╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝  ╚═╝            ║
║                                                                  ║
║             Multi-platform C/C++ Build System v2.8.1             ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝

Loading workspace...

Configuration: Debug
Target:        Windows x86_64
Toolchain:     mingw

Build Order (1 projects):
  1. Salle [WINDOWED_APP]


╔══════════════════════════════════════════════════════════════════════════
════════════════════╗
║  Project: Salle
Kind: WINDOWED_APP  ║
╚══════════════════════════════════════════════════════════════════════════
════════════════════╝

ℹ Found 1 source file(s)
✓   [1/1] Compiled: main.cpp
ℹ Linking...
✓ Built: bin\Debug\Windows\Salle.exe

┌──────────────────────────────────────────────────────────────────────────
────────────────────┐
│  ✓ Build Successful
       Time: 0.34s  │
└──────────────────────────────────────────────────────────────────────────
────────────────────┘

═══════════════════════════════════════════════════════════════════════════
═════
                                BUILD COMPLETED

═══════════════════════════════════════════════════════════════════════════
═════
Projects Built:  1/1
Time:           0.34s
Status:         ✓ SUCCESS
═══════════════════════════════════════════════════════════════════════════
═════


Laeti@Laeti MINGW64 ~/desktop/jenga/sorelle (main)
$ stat -c "%s %n" bin/Debug/Windows/Salle.exe
122771 bin/Debug/Windows/Salle.exe



2- Construction en Release

Laeti@Laeti MINGW64 ~/desktop/jenga/sorelle (main)
$ jenga build --config Release

╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║                ██╗███████╗███╗   ██╗ ██████╗  █████╗             ║
║                ██║██╔════╝████╗  ██║██╔════╝ ██╔══██╗            ║
║                ██║█████╗  ██╔██╗ ██║██║  ███╗███████║            ║
║           ██   ██║██╔══╝  ██║╚██╗██║██║   ██║██╔══██║            ║
║           ╚█████╔╝███████╗██║ ╚████║╚██████╔╝██║  ██║            ║
║            ╚════╝ ╚══════╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝  ╚═╝            ║
║                                                                  ║
║             Multi-platform C/C++ Build System v2.8.1             ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝

Loading workspace...

Configuration: Release
Target:        Windows x86_64
Toolchain:     mingw

Build Order (1 projects):
  1. Salle [WINDOWED_APP]


╔══════════════════════════════════════════════════════════════════════════
════════════════════╗
║  Project: Salle
Kind: WINDOWED_APP  ║
╚══════════════════════════════════════════════════════════════════════════
════════════════════╝

ℹ Found 1 source file(s)
✓   [1/1] Compiled: main.cpp
ℹ Linking...
✓ Built: bin\Release\Windows\Salle.exe

┌──────────────────────────────────────────────────────────────────────────
────────────────────┐
│  ✓ Build Successful
       Time: 0.29s  │
└──────────────────────────────────────────────────────────────────────────
────────────────────┘

═══════════════════════════════════════════════════════════════════════════
═════
                                BUILD COMPLETED

═══════════════════════════════════════════════════════════════════════════
═════
Projects Built:  1/1
Time:           0.30s
Status:         ✓ SUCCESS
═══════════════════════════════════════════════════════════════════════════
═════


Laeti@Laeti MINGW64 ~/desktop/jenga/sorelle (main)
$ stat -c "%s %n" bin/Release/Windows/Salle.exe
122771 bin/Release/Windows/Salle.exe

Laeti@Laeti MINGW64 ~/desktop/jenga/sorelle (main)




3- Comparaison
  a- Debug : 0.34s ; 122771 o
  b- Release : 0.30s ; 122771 o
