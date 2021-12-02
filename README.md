1. Go to windows power shell as administator and use the command:
	wsl --install
2. Restart the machine
3. Wait for the installation then set your username and password
4. Check your Ubuntu version using the following command in linux terminal and make sure it is atleast 20.04 (highest available for windows store at the time of writing. Available distros for download can be checked using the command 'wsl -l -o' in powershell)
	lsb_release -a
4. Use the command:
	sudo apt update
Then input your password to update all the packages of linux distro in your wsl2
5. Close Ubuntu terminal and power shell
6. Open Run (win+r) type services.msc and press enter
7. Find LxssManager service, right click and click on restart
8. Open powershell and use the command:
	wsl --shutdown
9. Open Ubuntu from start menu and run following commands:
	sudo apt update
	sudo apt upgrade
	sudo apt dist-upgrade
	sudo apt autoremove
Input your password when prompted
10. Use following cammand to install nano text editor.
	pip install nano
11. Open release-upgrades using using nano using:
	sudo nano /etc/update-manager/release-upgrades 
and input password if prompted: It will open the release-upgrades file. change the last line from
	Prompt = lts to Prompt = normal
12. Press ctrl+O then enter to save the file. Then press ctrl+x to exit.
13. Use the following command to check if the changes were successful else repeat steps 11 and 12
14. Use the following command to perform upgrade to Ubuntu 20.10
	sudo do-release-upgrade 
If this starts installing 21.10 groovy, you can skip the next step
15. If the above step does not install 21.10 and displays a message ¨terminated with exit status 1¨, run the following command:
	sudo nano /etc/apt/sources.list	
and replace all the terms ¨focal¨ with ¨groovy¨. Make sure to replace all of them by scrolling to the bottom. Once the are all replaced, run following commands:
	sudo apt update
	sudo apt upgrade
	sudo apt full-upgrade
	sudo apt autoremove
16. Restart the ubuntu terminal and check your Ubuntu version using the following command in linux terminal. It should list the release as 20.10 
	lsb_release -a

17. Use the following command to install sagemath:
	sudo apt-get install  bc binutils bzip2 ca-certificates cliquer cmake curl ecl eclib-tools fflas-ffpack flintqs g++ g++ gcc gcc gfan gfortran glpk-utils gmp-ecm lcalc libatomic-ops-dev libboost-dev libbraiding-dev libbrial-dev libbrial-groebner-dev libbz2-dev libcdd-dev libcdd-tools libcliquer-dev libcurl4-openssl-dev libec-dev libecm-dev libffi-dev libflint-arb-dev libflint-dev libfreetype6-dev libgc-dev libgd-dev libgf2x-dev libgiac-dev libgivaro-dev libglpk-dev libgmp-dev libgsl-dev libhomfly-dev libiml-dev liblfunction-dev liblrcalc-dev liblzma-dev libm4rie-dev libmpc-dev libmpfi-dev libmpfr-dev libncurses5-dev libntl-dev libopenblas-dev libpari-dev libpcre3-dev libplanarity-dev libppl-dev libpython3-dev libreadline-dev librw-dev libsqlite3-dev libssl-dev libsuitesparse-dev libsymmetrica2-dev libz-dev libzmq3-dev libzn-poly-dev m4 make nauty openssl palp pari-doc pari-elldata pari-galdata pari-galpol pari-gp2c pari-seadata patch perl pkg-config planarity ppl-dev python3 python3 python3-distutils r-base-dev r-cran-lattice sqlite3 sympow tachyon tar tox xcas xz-utils yasm

	
