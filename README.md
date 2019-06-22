# MS2PIP-for-DIA
Dear,

First of all, I would like to thank you for showing your interest into our GitHuB page.

In close collaboration with the CompOmics group of Lennart Martens we worked out a complete workflow to use MS²PIP predicted libraries for wide window DIA data extraction. Please refer to our manuscript posted on BioArchive !!

To enjoy all embedded features of MS²PIP, a full installation is required. 
Here, I would like to refer to the GitHub page of MS²PIP: https://github.com/compomics/ms2pip_c/ 

For this manuscript, a Linux operated machine with a virtual environment of Python3 was used.(Thx to Yannick) 
If you wouldn't have acces to a server or Linux operated machine. I would recommend you to install the VirtualBox software to create a virtual clone on your Windows/iOS operated machine. 

Once MS²PIP is installed, you can install ELUDE from the Percolator GitHuB: https://github.com/percolator/percolator/releases
ELUDE is embedded in one of the folders of the percolator repository. It can easily be installed (after unpacking the folder) with following command: 
sudo dpkg -i elude-v3-02-linux-amd64.deb (Linux operated machine) | dpkg -i  Ubuntu64.deb

Once everything is installed you can start predicting spectral libraries using one single command:
Python3 “fasta2speclib.py” [-h] [-o OUTPUT_FILENAME] [-c CONFIG_FILENAME] “fasta_filename”
On our Github repository you can find our ELUDE retention model, as well as the configuration file used in this manuscript. 

If older versions of MS²PIP are used, the retention time is not on a separate line and therefore requires parsing. The script to convert the RT is available on our GitHub.  

Installing EncyclopeDIA 
Please install EncyclopeDIA 0.8.2 from https://bitbucket.org/searleb/encyclopedia/downloads/?tab=downloads.
Using the CONVERT MSP/SPTXT to Library function, you can convert MS²PIP .msp files to a .dlib file. 

If you would have any issues during the installment please contact us and we will try to help you wherever we can. 

Bart Van Puyvelde
Email: bart.vanpuyvelde@ugent.be
This research was mainly funded by a mandate from the Research Foundation Flanders (FWO) awarded to BVP [grant number 11B4518N]



