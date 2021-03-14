Paraview Flatpak
====================

This Flatpak manifest file is work in progress.
Need Numpy, Matplotlib, Exaamples, etc.
 
Flatpak is a utility for software deployment and package management for Linux. 
It offers a sandbox environment in which users can run application software in isolation from the rest of the system.

Building and running org.paraview.Paraview
----------------------------------------------------

1. Create new working folder.
2. Install flatpak-builder, for Ubuntu, `sudo apt install flatpak-builder`
3. Install KDE Sdk, choose version 5.15 (system), `flatpak install org.kde.Platform org.kde.Sdk io.qt.qtwebengine.BaseApp`
4. Clone sub-modules, these sub-modules are pre-made Flatpak manifest that commonly use, we will be using glew, `git clone git://github.com/flathub/shared-modules.git`
5. Download `org.paraview.Paraview.yaml` and `tbb_cmake.patch` from my github repo, put them in same folder.
6. `flatpak-builder --install --user build org.paraview.Paraview.yaml --force-clean`
7. Wait until finish and run with, `flatpak run org.paraview.Paraview`

