How to install LaTeX Worskshop on Arch:

1. download: https://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz
2. unpack and change into directory
3. run: sudo perl ./install-tl-20240505/install-tl
	select Insall
	wait . . . 
4. at the end of the installation it gives you paths for PATH, MANPATH and INFOPATH 
   add them by writing the following lines at the end of ~/.bashrc:
	    export PATH=$PATH:/usr/local/texlive/2024/bin/x86_64-linux
	    export MANPATH=$MANPATH:/usr/local/texlive/2024/texmf-dist/doc/man
	    export INFOPATH=$INFOPATH:/usr/local/texlive/2024/texmf-dist/doc/info
	
	use the paths given in your terminal
	
sudo pacman -S texlive-binextra
	to install Latexmk
	
  sudo pacman -S texlive-latex
  for ztot package

 5. install the extension in VSCode

source: https://wiki.archlinux.org/title/TeX_Live#Installation









## LaTeX Workshop on Arch Linux

This guide gets you up and running with LaTeX Workshop in your favorite code editor, Visual Studio Code (VS Code). Follow these steps to install the necessary LaTeX tools and configure VS Code for a seamless LaTeX experience.

*Prerequisites*

    A running Arch Linux system
    Basic familiarity with the terminal

*Installation*

    Download TeX Live:

    TeX Live is a comprehensive LaTeX distribution. We'll download the network installer script for a more flexible installation.

    In your terminal, run the following command:
    Bash

    curl -LO https://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz

    Verwende den Code mit Vorsicht.

*Install TeX Live:*

Extract the downloaded archive and run the installer script. This will guide you through a selection process for the LaTeX packages you want. We recommend choosing a full installation for a complete setup.

Open your terminal and run these commands:
Bash

tar -xf install-tl-unx.tar.gz
cd install-tl-20240505  # Replace with the actual directory name (check the folder name)
sudo perl ./install-tl

Verwende den Code mit Vorsicht.

Follow the installer prompts and select "Install" to begin the download and installation process. This might take some time depending on your internet speed and the number of packages you choose.

*Set Environment Variables:*

Once the installation is complete, the installer will provide you with the necessary paths for PATH, MANPATH, and INFOPATH.  Add these paths to your shell configuration file (e.g., ~/.bashrc). Open your preferred text editor and append the following lines, replacing the placeholders with the actual paths provided by the installer:
Bash

export PATH=$PATH:/usr/local/texlive/2024/bin/x86_64-linux  # Replace with your actual path
export MANPATH=$MANPATH:/usr/local/texlive/2024/texmf-dist/doc/man  # Replace with your actual path
export INFOPATH=$INFOPATH:/usr/local/texlive/2024/texmf-dist/doc/info  # Replace with your actual path

Verwende den Code mit Vorsicht.

Save the changes and reload your shell configuration by running:
Bash

source ~/.bashrc

Verwende den Code mit Vorsicht.

*Install Missing Packages:*

Use sudo pacman to install additional packages needed for specific LaTeX features:

In your terminal, run these commands:
```
Bash

sudo pacman -S texlive-binextra  # For Latexmk
sudo pacman -S texlive-latex    # For additional LaTeX packages (optional)
```
Verwende den Code mit Vorsicht.

The texlive-binextra package includes latexmk, a popular tool for compiling LaTeX documents. The texlive-latex package is optional but provides a broader selection of LaTeX packages if needed.

*Install LaTeX Workshop Extension:*

Open VS Code and navigate to the Extensions tab (Ctrl+Shift+X). Search for "LaTeX Workshop" and install the official extension by James Yu.