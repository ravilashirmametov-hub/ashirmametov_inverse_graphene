# ashirmametov_inverse_graphene
Repository for paper "Two-Stage Inverse Design of Chemically Functionalized Graphene for Tailoring Thermomechanical Properties", 2026 by Ashirmametov R. et al.

Authors: Ravil Ashirmametov, Konstantinos Kostas, Siamac Fazli, Yousefi Farrokh.

Corresponding author: Ravil Ashirmametov, https://www.linkedin.com/in/ravil-ashirmametov/, ravil.ashirmametov@kaust.edu.sa

Structure of the repository:
'\Datasets' - contains three directories with 9 datasets in total;
'\lammps' - contains two directories with samples of thermal and mechanical simulation;
'\examples' - contains the label encoded vector and lammps compatible .data file for three reported cases of the optimized graphene structure (reported in the article);
'\models' - contains the hyperparameters of the optimized regression models used for the inverse design of mixed-family graphene.


Datasets are structured as follows:
  For Label encoding:
    1 - Carbon atom with no functionalization;
    2 - Carbon with hydrogen group at the top side;
    3 - Carbon with hydrogen group at the bottom side; 
    4 - Carbon with methyl group at the top side;
    5 - Carbon with methyl group at the bottom side;
    6 - Carbon with ethyl group at the top side;
    7 - Carbon with ethyl group at the bottom side.
    
  For Bag-of-Words encoding: 
    2nd column - number of carbon atoms with no functionalization;
    3rd column - number of hydrogen atoms on the top surface;
    4th column - number of hydrogen atoms on the bottom surface;
    5th column - number of methyl groups on the top surface;
    6th column - number of methyl groups on the bottom surface;
    7th column - number of ethyl groups on the top surface;
    8th column - number of ethyl groups on the bottom surface.

  For statistical encoding:
    Please consult the information available in the article or contact the corresponding author.

All datasets have 5 property columns at the end of each file and these properties are as follows:
1. Thermal conductivity in W/mK;
2. Young's modulus in GPa;
3. Maximum stress in GPa;
4. Strain at maximum stress;
5. Strain at fracture.

Datasets feature in total 800 graphene structures (1600 MD simulations [800 thermal and 800 mechanical]):
1. 400 graphene functionalized with hydrogen+methyl (up to 10% functionalization of each group, resulting in 100 unique percentage combinations and 4 different representations of same combination);
1. 400 graphene functionalized with hydrogen+ethyl (up to 10% functionalization of each group, resulting in 100 unique percentage combinations and 4 different representations of same combination);

Samples of the LAMMPS scripts are as follows:
  1 mechanical sample script with graphene functionalized with 6% methyl and 10% hydrogen. This input file generates a log.lammps file from which we extract Young's modulus, maximum stress, strain at maximum stress, and fracture strain.
  1 thermal sample script with graphene functionalized with 3% ethyl and 5% hydrogen. This input file generates a log.lammps file from which we extract thermal conductivity.

To go from integer (Label) encoding to lammps data file and vice versa please see our previous related article https://pubs.rsc.org/ra/article/15/52/44423/908886/Determining-the-structure-of-functionalized
