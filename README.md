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
