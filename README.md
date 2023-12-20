# silverblue-setup

Various scripts and notes for setting up Fedora Silverblue.

## Install to base OS image

### Install Firefox codecs

    sudo rpm-ostree install mozilla-openh264

### Enabling Flathub

    flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo

## Install Flatpaks

### Install MEGAsync

    flatpak install flathub nz.mega.MEGAsync

### Install Steam

    flatpak install flathub com.valvesoftware.Steam

### Install Discord

    flatpak install flathub com.discordapp.Discord
    
## Create a toolbox

    toolbox create name

## Enter a toolbox

    toolbox enter name

### Install some common tools and packages inside the toolbox

    sudo dnf install btop cpufetch

### Install R and RStudio Desktop inside the toolbox

    sudo dnf install fira-code-fonts R rstudio-desktop

### Install Python inside the toolbox

    sudo dnf install python3-virtualenv

### Install GnuCOBOL inside the toobox

    sudo dnf install gnucobol gnucobol-esql

### Install Visual Studio Code inside the toolbox

    sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
    sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
    sudo dnf check-update
    sudo dnf install code
