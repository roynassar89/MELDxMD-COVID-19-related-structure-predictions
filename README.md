# MELDxMD-COVID19-related-structure-predictions

Setup:
------

MELD is a Bayesian inference method that guides proteins during MD simulations to structures that are compatible with input data from one or more sources, example: secondary structures from PSIPRED, NMR data, co-evolution or machine learning contacts, etc...

MELD x MD converts distances, angles and contacts from one or more of these data sources into energy restraints, and during the MD trajectory, activates a subset of them to hone in on structures that are compatible with the restraints and the force field (ff14sb + gbNeck2). MELD’s reduction of the vast conformational search to only relevant regions on the landscape has led to many-fold speed up of MELD x MD modeling.

MELD preserves Boltzmann populations and hence infers relative free energies.

MELD runs its Replica Exchange MD (REMD) setup on GPUs and has proven effective in protein folding and protein/ligand binding.

The Uniprot pre-release from April 6 contains sequences for SARS-CoV-2 and SARS-CoV viruses as well as human targets ftp://ftp.uniprot.org/pub/databases/uniprot/pre_release/.

We applied MELD x MD to the Covid-19 protein sequences to generate 3D structure models for both virus and human target proteins. MELD restraints included: (i) secondary structure predictions from PSIPRED, (ii) predicted residue-residue contacts from trRosetta, (iii) hydrophobic associations and strand pairings from the protein sequence.

MELD was also seeded from trRosetta server models as starting points to speed up the folding.

Results:
--------
MELD x MD generated ensembles for 21 Covid related proteins (SARS, SARS2, and Human). The top 5 most dominant structures (cluster representatives) are uploaded here along with their populations. Structural ensembles of 100 conformations taken from each cluster can be obtained by contacting roy.nassar@stonybrook.edu.


References:

[1] Alberto Perez, Justin L MacCallum, and Ken A Dill. Accelerating molecular simulations of proteins using bayesian inference on weak information. Proceedings of the National Academy of Sciences, 112(38):11846–11851, 2015.
[2] Justin L MacCallum, Alberto Perez and Ken A Dill. Determining protein structures by combining semireliable data with atomistic physical models by Bayesian inference. Proceedings of the National Academy of Sciences, 112(22): 6985-6990, 2015.
[3] James C. Robertson, Alberto Perez, and Ken A. Dill. Meld MD folds nonthreadables, giving native structures and populations. Journal of Chemical Theory and Computation, 14(12):6734–6740, 2018. PMID: 30407805.
[4] James Robertson, Roy Nassar, Cong Liu, Emiliano Brini, Ken Dill and Alberto Perez. NMR-assisted protein structure prediction with MELDxMD. Protein: Structure Function and Bioinformatics, 87(12):1333-1340, 2019.
[5] Emiliano Brini, Dima Kozakov and Ken Dill. Predicting protein dimer structures using MELDxMD. J. Chem. Theory Comput., 15(5), 3381-3389, 2019.
[6] Joseph Morrone, Alberto Perez, Justin MacCallum and Ken Dill. Computed binding of peptides to proteins with MELD-accelerated molecular dynamics. J. Chem. Theory Comput., 13(2), 870-876, 2017.
[7] Alberto Perez, Joseph A. Morrone, Emiliano Brini, Justin L. MacCallum, and Ken A. Dill. Blind protein structure prediction using accelerated free-energy simulations. Science Advances, 2(11), 2016.
