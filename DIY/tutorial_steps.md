# DIY: Using MS²PIP predicted spectral libraries for DIA data extraction

In close collaboration with the [CompOmics group](https://www.compomics.com) of Lennart Martens we worked out a complete workflow to use MS²PIP predicted libraries for wide window DIA data extraction.

This document outlines all required steps to try out the analysis yourself. In the methods section of our preprint *[The future of peptide-centric Data-Independent Acquisition is predicted](https://www.biorxiv.org/content/10.1101/681429v1)*, you can find a more detailed description of all steps.

### Installation
For this manuscript, a Linux operated machine with a Python 3 virtual environment was used. If you do not have access to a server or Linux operated machine, we recommend you to install the VirtualBox software to create a virtual clone on your Windows/macOS operated PC. We can also highly recommend the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) which is implemented on all Windows 10 PCs.

#### MS²PIP and fasta2speclib
MS²PIP can be downloaded from [GitHub page of MS²PIP](https://github.com/compomics/ms2pip_c/releases/latest). A detailed installation guide can be found on [Extended Install Instructions](https://github.com/compomics/ms2pip_c/wiki/Extended_install_instructions).

#### Elude
Elude is shipped with the installation of Percolator. It can be downloaded from the Percolator [GitHub repository](https://github.com/percolator/percolator/releases). To install Elude, after unzipping the folder, run the following command:
```
sudo dpkg -i elude-v3-02-linux-amd64.deb (Linux operated machine) | dpkg -i  Ubuntu64.deb
```

#### EncyclopeDIA:
EncyclopeDIA 0.8.2 can be downloaded from https://bitbucket.org/searleb/encyclopedia/downloads/?tab=downloads.

### Run the pipeline
#### Input files
- The Yeast dataset itself can be downloaded from the MassIVE proteomics repository: [ftp://massive.ucsd.edu/MSV000082805]((ftp://massive.ucsd.edu/MSV000082805). The repository contains both raw as peak picked data, so it is up to you whether you want to skip the raw file processing with MSConvertGUI, or not.
- We shared the yeast FASTA file on this repository: [DIY/YEAS8_iRT.fasta](https://github.com/brvpuyve/MS2PIP-for-DIA/blob/master/DIY/YEAS8_iRT.fasta). It can also be downloaded from UniProt.
- The Elude model we used can also be found on this repository: [ELUDE/ELUDE_PAN_HUMAN.model](https://github.com/brvpuyve/MS2PIP-for-DIA/blob/master/ELUDE/ELUDE_PAN_HUMAN.model)
- The fasta2speclib config file we used can be found here: [Config_file/fasta2speclib_config_HCD_2missed_ELUDE.json](https://github.com/brvpuyve/MS2PIP-for-DIA/blob/master/Config_file/fasta2speclib_config_HCD_2missed_ELUDE.json)

#### fasta2speclib
Once everything is installed you can start predicting spectral libraries using one single command:
```
python3 “fasta2speclib.py” [-h] [-o OUTPUT_FILENAME] [-c CONFIG_FILENAME] “fasta_filename”
```
If you want to skip this step, you can download the predicted spectral libraries (Human, Yeast) in .dlib format on 
[genesis.ugent.be/uvpublicdata/MS2PIP-for-DIA/](http://genesis.ugent.be/uvpublicdata/MS2PIP-for-DIA/)

#### EncyclopeDIA
Using the EncyclopeDIA *CONVERT MSP/SPTXT to Library* function, you can convert the fasta2speclib .msp files to a .dlib file. This .dlib file can then be used in the EncyclopeDIA analysis to make a chromatogram library. Next, the wide window runs can be analyzed with the chromatogram library.

---
### Contact:
If you would have any issues, please contact us and we will try to help you wherever we can. 
- Bart Van Puyvelde ([bart.vanpuyvelde@ugent.be](mailto:bart.vanpuyvelde@ugent.be), [@BartVP](https://twitter.com/BartVP))
- Maarten Dhaenens ([maarten.dhaenens@ugent.be](mailto:maarten.dhaenens@ugent.be))
