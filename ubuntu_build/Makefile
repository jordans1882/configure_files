## Author: Jordan Schupbach
## Description:  A makefile for building my 
##               ubuntu 16.04 machine (to be
##               used in case of the need to
##               rebuild my machine)
## Date: March 25, 2017
## TODO:
##  - Add checks for need to install
##  - Associate a configure file?
##    * What might I need to check for? (Hardware?)
##  - GPU check
##  - Install GPU tools?
##  - Build dependencies
##     * R to R-Studio
##  - Write make clean
##  - Move config files (awesome) to .config
##  - Download git repos
##  - Add uninstall scripts (i.e., vimclean)
##  - Add git config
all: vim r rstudio 
vim:    # Install Vim 8.0
	add-apt-repository ppa:jonathonf/vim
	apt update
	apt install vim
r:      # Install R (newest?)
	echo "deb http://cran.rstudio.com/bin/linux/ubuntu xenial/" | sudo tee -a /etc/apt/sources.list
	gpg --keyserver keyserver.ubuntu.com --recv-key E084DAB9
	gpg -a --export E084DAB9 | sudo apt-key add -
	apt-get update
	apt-get install r-base r-base-dev
rstudio:
	sudo apt-get install gdebi-core
	wget https://download1.rstudio.org/rstudio-1.0.136-amd64.deb
	sudo gdebi -n rstudio-1.0.136-amd64.deb
	rm rstudio-1.0.136-amd64.deb
