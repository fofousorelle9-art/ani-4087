

Laeti@Laeti MINGW64 ~/desktop/jenga/sorelle (main)
$ jenga info

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

=========================== Jenga Workspace: Sorelle ======================
=====

Location: C:\Users\Laeti\Desktop\Jenga\Sorelle
Entry file: C:\Users\Laeti\Desktop\Jenga\Sorelle\Sorelle.jenga
Configurations: Debug, Release
Platforms: Windows
Target OSes: Windows, Linux
Target Architectures: x86_64


Projects
------------------------------------------------------------
Name    Kind          Language   Test   External
================================================
Salle   WindowedApp   C++        No     No


Available Toolchains
------------------------------------------------------------
Name       Family   Target OS   Arch     Env
==============================================
host-gcc   gcc      Windows     x86_64   mingw
mingw      gcc      Windows     x86_64   mingw


Daemon
------------------------------------------------------------
Status: Not running





La commande "jenga info" nous apprend :
    a- le chemin de stockage du projet
    b- le système de l'ordinateur (windows)
    c- les propriétés du projet (le test, projet marqué externe)

De même, nous remarquons que Platforms: Windows, pourtant les systèmes cibles étaient Windows, Linux et MacOs
Ainsi, le programme détecte automatiquement le système utilisé et le désigne comme plateforme d'éxecution
