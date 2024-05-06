## LaTeX Workshop on Arch Linux

This guide gets you up and running with LaTeX Workshop in your favorite code editor, Visual Studio Code (VS Code). Follow these steps to install the necessary LaTeX tools and configure VS Code for a seamless LaTeX experience.

*Prerequisites*

A running Arch Linux system
Basic familiarity with the terminal

*Installation*

Download TeX Live:

TeX Live is a comprehensive LaTeX distribution. We'll download the network installer script for a more flexible installation.

Simply paste the following into a search engine of your choice
```
https://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz
```

*Install TeX Live:*

Extract the downloaded archive and run the installer script. This will guide you through a selection process for the LaTeX packages you want. We recommend choosing a full installation for a complete setup.

Open your terminal and run these commands:
```
cd install-tl-20240505  # Replace with the actual directory name (check the folder name)
sudo perl ./install-tl
```


Follow the installer prompts and select "Install" to begin the download and installation process. This will take a lot of time as a lot of packages are beeing downloaded.

*Set Environment Variables:*

Once the installation is complete, the installer will provide you with the necessary paths for PATH, MANPATH, and INFOPATH.  Add these paths to your shell configuration file (e.g., ~/.bashrc). Open your preferred text editor and append the following lines, replacing the placeholders with the actual paths provided by the installer:

```
export PATH=$PATH:/usr/local/texlive/2024/bin/x86_64-linux  # Replace with your actual path
export MANPATH=$MANPATH:/usr/local/texlive/2024/texmf-dist/doc/man  # Replace with your actual path
export INFOPATH=$INFOPATH:/usr/local/texlive/2024/texmf-dist/doc/info  # Replace with your actual path
```


Save the changes and reload your shell configuration by running:
```
source ~/.bashrc
```


*Install Missing Packages:*

Use sudo pacman to install additional packages needed for specific LaTeX features:

In your terminal, run these commands:
```
sudo pacman -S texlive-binextra  # For Latexmk
sudo pacman -S texlive-latex    # For additional LaTeX packages
```

The texlive-binextra package includes latexmk, a popular tool for compiling LaTeX documents. The texlive-latex package is needed for the template to work.

*Install LaTeX Workshop Extension:*

Open VS Code and navigate to the Extensions tab (Ctrl+Shift+X). Search for "LaTeX Workshop" and install the official extension by James Yu.