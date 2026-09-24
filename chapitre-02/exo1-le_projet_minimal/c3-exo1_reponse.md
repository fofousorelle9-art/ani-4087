Exerice 1 : le projet minimal

1- le code contenu dans le fichier à construire

from Jenga import *

with workspace("Sorelle", location="."):
    configurations(['Debug', 'Release'])
    targetoses([TargetOS.WINDOWS, TargetOS.LINUX])
    targetarchs([TargetArch.X86_64])
    
    with project("Salle"):
        windowedapp()
        language("C++")
        cppdialect("C++17")
        location(".")
        files(["src/**.cpp"])

        targetdir("bin/%{cfg.buildcfg}/%{cfg.system}")
        objdir("obj/%{cfg.buildcfg}/%{cfg.system}")

        with filter("system:Windows"):
            links(["user32", "gdi32", "opengl32"])
        with filter("system:Linux"):
            links(["pthread", "X11", "GL"])

            


2- la sortie après jenga build :


Laeti@Laeti MINGW64 ~/desktop/jenga/sorelle (main)
$ jenga build

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
       Time: 0.40s  │
└──────────────────────────────────────────────────────────────────────────
────────────────────┘

═══════════════════════════════════════════════════════════════════════════
═════
                                BUILD COMPLETED

═══════════════════════════════════════════════════════════════════════════
═════
Projects Built:  1/1
Time:           0.40s
Status:         ✓ SUCCESS
═══════════════════════════════════════════════════════════════════════════
═════





3- A la sortie, nous remarquons la ligne toolchain : mingw qui nous apprends le type de chaines d'outils configurés pour notre projet
