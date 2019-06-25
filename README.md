
# The future of peptide-centric DIA is predicted!

In our manuscript *The future of peptide-centric Data-Independent Acquisition is predicted* we show the benefit of MS²PIP predicted spectral libraries on a HeLa DIA dataset published by Searle et al. ([doi:10.1038/s41467-018-07454-w](https://doi.org/10.1038/s41467-018-07454-w)).

>**The future of peptide-centric Data-Independent Acquisition is predicted**  
>*\*Van Puyvelde, B.\*, Willems, S.\*, Gabriels, R.\*, Daled, S., De Clerck, L., Staes, A., Impens, F., Deforce, D., Martens, L., Degroeve, S., Dhaenens, M.§*  
>
>*Abstract:*  
>Data-Independent Acquisition (DIA) currently generates the most comprehensive and complex mass spectrometric data, which imposes the use of data-dependent acquisition (DDA) libraries for deep peptide-centric detection. We redeem DIA from this dependency by combining predicted fragment intensities and retention times with narrow window DIA.

### Manuscript supporting data
This repository contains all small (<100MB) files that are supporting data for the manuscript. Larger files are available on (Todo:url).

### Do it yourself challenge (and tutorial)
Before putting this story on paper, we evaluated our workflow on both public and in-house datasets. One of these datasets was a public yeast dataset, which was published together with the HeLa dataset. As this dataset is smaller, we provide our workflow as a Do-It-Yourself tutorial on this repository. We would like to challenge you to try out our workflow on the Yeast dataset. That way you can go through the different steps and at the same time see the added value of this new peptide centric approach. 

The Yeast dataset itself can be downloaded online from the MassIVE proteomics repository: [ftp](ftp://massive.ucsd.edu/MSV000082805). The repository contains both raw as peak picked data, so it is up to you whether you want to skip the raw file processing with MSConvertGUI, or not. 

For convenience, we have included all intermediate results to allow you to skip the more computationally expensive steps, such as e.g. MS²PIP spectral library prediction. All steps are outlined in [DIY/tutorial_steps.md](https://github.com/brvpuyve/MS2PIP-for-DIA/blob/master/DIY/tutorial_steps.md).

Please share your results and experiences as much as possible via social media (e.g. Twitter). We would be very grateful to you. You can find us at [@BartVP](https://twitter.com/BartVP) and [@RalfGabriels](https://twitter.com/RalfGabriels). If you encounter any problems, you can also mail us on: [Bart.VanPuyvelde@UGent.be](mailto:Bart.VanPuyvelde@UGent.be). 

The only thing left for us to do is to wish you all the best with the challenge. Good luck!

