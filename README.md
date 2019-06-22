# MS2PIP-for-DIA
Dear,

First of all, I would like to thank you for showing your interest into our GitHuB page.

In close collaboration with the CompOmics group of Lennart Martens we worked out a complete workflow to use MS²PIP predicted libraries for wide window DIA data extraction. Please refer to our manuscript posted on BioArchive !!

Here, we give you a full tutorial to apply this workflow on your biological project. 

First, you have to install MS²PIP to enjoy all embedded features of this magnificent piece of machine learning. 
Here, I would like to refer to the GitHub page of MS²PIP: https://github.com/compomics/ms2pip_c/ 

For this manuscript, I used a Linux operated machine to install MS²PIP in a virtual environment of Python3.(Thx to Yannick) 
If you wouldn't have acces to a server or Linux operated machine. I would recommend you to install the VirtualBox software to create a virtual clone on your Windows/iOS operated machine. 

Once MS²PIP is installed, you can install ELUDE from the Percolator GitHuB: https://github.com/percolator/percolator/releases
ELUDE is embedded in one of the folders of the percolator repository. It can easily be installed (after unpacking the folder) with following command: 
sudo dpkg -i elude-v3-02-linux-amd64.deb (Linux operated machine) | dpkg -i  Ubuntu64.deb

If you would have any issues during the installment please contact us and we will try to help you wherever we can. 

Once everything is installed you can start predicting spectral libraries using one single command:
Python3 “fasta2speclib.py” [-h] [-o OUTPUT_FILENAME] [-c CONFIG_FILENAME] “fasta_filename”
On our Github repository you can find our ELUDE retention model, as well as the configuration file used. 





