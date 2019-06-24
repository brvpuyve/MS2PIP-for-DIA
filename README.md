# The future of peptide-centric DIA is predicted 
Dear,

First of all, I would like to thank you for showing your interest into our GitHub page.

In close collaboration with the CompOmics group of Lennart Martens we worked out a complete workflow to use MS²PIP predicted libraries for wide window DIA data extraction. Please refer to our manuscript posted on BioRxiv!

To enjoy all embedded features of MS²PIP, a full installation is required. 
Here, I would like to refer to the [GitHub page of MS²PIP](https://github.com/compomics/ms2pip_c/releases/latest).

For this manuscript, a Linux operated machine with a virtual environment of Python3 was used. (Thx to Yannick) 
If you wouldn't have access to a server or Linux operated machine. I would recommend you to install the VirtualBox software to create a virtual clone on your Windows/iOS operated machine.

Once MS²PIP is installed, you can install ELUDE from the Percolator GitHub: https://github.com/percolator/percolator/releases. ELUDE is embedded in one of the folders of the percolator repository. It can easily be installed (after unpacking the folder) with following command:
```
sudo dpkg -i elude-v3-02-linux-amd64.deb (Linux operated machine) | dpkg -i  Ubuntu64.deb
```

Once everything is installed you can start predicting spectral libraries using one single command:
```
python3 “fasta2speclib.py” [-h] [-o OUTPUT_FILENAME] [-c CONFIG_FILENAME] “fasta_filename”
```
On our Github repository you can find our ELUDE retention model, as well as the configuration file used in this manuscript.

If older versions of MS²PIP are used, the retention time is not on a separate line and therefore requires parsing. The script to convert the RT is available on this GitHub repository.  

The predicted spectral libraries (Human, Yeast) are available via https://cmbcloud.ugent.be/index.php/s/rkPx4qJ6jT25JWT?path=%2FSpectral_libraries

Installing EncyclopeDIA:
Please install EncyclopeDIA 0.8.2 from https://bitbucket.org/searleb/encyclopedia/downloads/?tab=downloads.
Using the CONVERT MSP/SPTXT to Library function, you can convert MS²PIP .msp files to a .dlib file. 

If you would have any issues during the installment please contact us and we will try to help you wherever we can. 

In our GitHub repository you can find a DIY practical exercise (on a Yeast dataset of the Chromatogram Library paper of B.Searle). Please try it yourself and send us your results using social media. 

Bart Van Puyvelde ([bart.vanpuyvelde@ugent.be](mailto:bart.vanpuyvelde@ugent.be)) and
Maarten Dhaenens ([maarten.dhaenens@ugent.be](mailto:maarten.dhaenens@ugent.be))

