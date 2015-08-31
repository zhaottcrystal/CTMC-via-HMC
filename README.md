Summary
--------------------
In ths repository, we provde the synthetic and real data used in paper "Bayesian analysis of continuous time Markov chains with application to phylogenetic modelling"

Introduction
-------------------
There are three folders in the repository. Each folder contains the data files for one section of the paper. The name of the folders is consistent with the section name in the paper. For example, files in folder "Sec7.3Accuracy" refers to the data used in Section 7.3 in the original paper. 

###Real Data Description: Sec7.5RealData
In this folder, "RealDataalignmenttotal.txt" refers to the alignment in the protein kinase domain family. The starting sequence is selected to be the kinase domain present in the mouse Titin protein taken from the PDB file 1TKI, which also includes some of the flanking sequence, allows for a more computationally feasible example. This alignment data contained 641 sequences and each sequence has 415 sites. "RealDatatree.nwk.txt" is the inferred unrooted phylogenetic tree using MrBayes which has a more complete and efficient set of tree resampling moves.

###Synthetic Data Description: Sec7.3Accuracy and Sec7.4Efficiency
All the synthetic data in both folders "Sec7.3Accuracy" and "Sec7.4Efficiency" are generated under the same tree topology which is given in the subfolder named "FourModelsComparison" under "Sec7.3Accuracy". This is an unrooted tree with ten sequences.  In order to assess the accuracy of our inferred parameters on the synthetic dataset, we select the same number of sites (415) and sequences (641) as in our real data experiments. The synthetic dataset is stored in "numSites415alignsimutreeSeed1.txt" simulated under the rate matrix provided in "rateMtxForFigure1.txt". We use the following metric to evaluate accuracy including the KL divergence between the estimated stationary distribution and the true one, the relative biases of individual transition probabilities without the diagonal elements under different branch lengths as one, two, three and five. In the folder "FourModelsComparison", we generate sixty datasets under the same rate matrix which is given in "RateMatrix.txt" under a continuous time Markov chain. It represents the rate of substitutions between any two states specified in the row and column names. The weights used to generate this rate matrix is in "weightsJSON.txt" in the same folder. The sequences have sites ranging from 100 sites to 1500 sites with stepsize 100. We generate four independent datasets with 1500 sites first. We let the number of sites in each sequence increase from 100 to 1400 with a step size 100 by subsampling from the four independent datasets with 1500 sites. To evaluate the computational efficiency in Section 7.4 of the paper, we use a synthetic dataset  of 2000 sites saved in  "numSites2000alginsimutreeSeed1.txt"  generated under the same tree in Section 7.3 and rate matrix stored in "RateMatrix.txt" in the folder "FourModelsComparison". We use this dataset to evaluate the computational efficiency of the HMC method versus the classical MCMC method under a normal proposal with various bandwidth and an adaptive Normal Metropolis Hastings with a joint proposal guided by an estimated covariance matrix.  The dataset named "numSites500alignsimutreeSeed2.txt" is used to investigate the effectiveness of our Bayesian optimization adaptation scheme in terms of Figure 5 in the paper. 





