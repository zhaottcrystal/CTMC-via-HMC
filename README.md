Summary
--------------------
Synthetic and real data for paper "User-friendly Bayesian analysis of continuous time Markov chains"

Introduction
-------------------
There are three folders in the repository. Each folder contains the data files for one section of the paper. The name of the folders is consistent with the section name in the paper. For example, files in folder "Sec7.3Accuracy" refers to the data that are used in Section 7.3 in the original paper. 

###Real Data Description: Sec7.5RealData
In this folder, "RealDataalignmenttotal.txt" refers to the alignment in the protein kinase domain family. The starting sequence is selected to be the kinase domain present in the mouse Titin protein taken from the PDB file 1TKI, which also includes some of the flanking sequence, allows for a more computationally feasible example. This alignment data contained 641 sequences and each sequence has 415 sites. "RealDatatree.nwk.txt" is the inferred unrooted phylogenetic tree using MrBayes which has a more complete and efficient set of tree resampling moves.

###Synthetic Data Description: Sec7.3Accuracy and Sec7.4Efficiency
All the synthetic data in both folders "Sec7.3Accuracy" and "Sec7.4Efficiency" are generated under the same tree topology which is given in the subfolder named "FourModelsComparison" under "Sec7.3Accuracy". This is an unrooted tree with ten sequences. In "FourModelsComparison", we generate sixty datasets under the same rate matrix which is given in file "RateMatrix.txt" under a continuous time Markov chain. It represents the rate of substitutions between any two states specified in the row and column names. The weights used to generate this rate matrix is in "weightsJSON.txt" in the same folder. The sequences have sites ranging from 100 sites to 1500 sites with stepsize 100. We generate them under four different random seeds. The file named "numSites5000alignsimutreeSeed1.txt" and "numSites2000alginsimutreeSeed1.txt"  refer to the alignments with ten tips having 5000 and 2000 sites separately in each sequence generated under the same tree topology and rate matrix with random seed one. "numSites2000alginsimutreeSeed1.txt" is generated to evaluate the computational efficiency of the HMC method versus the classical MCMC method under a normal proposal with bandwidth 0.01. 

