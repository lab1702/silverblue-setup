# sliverblue-setup

Various scripts and notes for setting up Fedora Silverblue.

## Enabling Flathub

    flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo

## Install MEGAsync

    flatpak install flathub nz.mega.MEGAsync

### Run MEGAsync from command line

    flatpak run nz.mega.MEGAsync

## Create a toolbox

    toolbox create name

### Enter a toolbox

    toolbox enter name

### Update everything in the toolbox

    sudo dnf update --refresh

### Install some common tools inside the toolbox

    sudo dnf install btop htop cpufetch

### Install R, RStudio Desktop and Fira Code font inside the toolbox

    sudo dnf install R fira-code-fonts rstudio-desktop

### Install GnuCOBOL inside the toobox

    sudo dnf install gnucobol

### Install Visual Studio Code inside the toolbox

    sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
    sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
    sudo dnf check-update
    sudo dnf install code
