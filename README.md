# sliverblue-setup

Various scripts and notes for setting up Fedora Silverblue.

## Enabling Flathub

    flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo

## Install MEGAsync

    flatpak install flathub nz.mega.MEGAsync

### Run MEGAsync from command line

    flatpak run nz.mega.MEGAsync

## Install Visual Studio Code

    flatpak install flathub com.visualstudio.code

### Run Visual Studio Code from command line

    flatpak run com.visualstudio.code

## Create and enter a toolbox for GnuCOBOL

    toolbox create cobol
    toolbox enter cobol

### Install GnuCOBOL inside the toobox

    dnf install gnucobol
