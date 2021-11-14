# CyclicQuorumSets
This repo contains
 - Appendix.pdf
 - Two_new_quorum_based_algorithms_for_distributed_mutual_exclusion.pdf
 - Heuristic_method_for_large_value_p.ipynb
 - README.MD
 - All_Interest_Sets
   - 4
   - 5
   - ...
   - 52

## [Appendix.pdf](.\Appendix.pdf)

This used to be the appendix of the paper "An Efficient Systematic Approach to Find All Cyclic Quorum Sets with All-pairs Property". Due to the page limit, it is removed from the paper and post here. 

It contains four tables. Table VIII and IX are two parts of a group of quorums that has all-pairs property for p=112. The results are determined using the heuristic method mentioned in the paper. The corresponding implementation is provided in the Jupyter Notebook "Heuristic_method_for_large_value_p.ipynb". 
Table X provides all feasible interest sets for p = 4 to 13, 21, 31 and 57. As mentioned in the paper, our searching strategy CQS_Searching() only produce the results in the left column and those in the right column are calculated accordinly using pairing property.
Table XI is a small part of the appendix of paper "Two new quorum based algorithms for distributed mutual exclusion", which is also provided in this repo. This table is intended for a fast reference for the corresponding n value to those p values mentioned in section V.

## [Two_new_quorum_based_algorithms_for_distributed_mutual_exclusion.pdf](.\Two_new_quorum_based_algorithms_for_distributed_mutual_exclusion.pdf)

This is the first paper, in which the authors Wai-Shing Luk et al. indentified one feasible base set that is feasible to generate a CQS with all-pairs property. The results are provided in the appendix. They are 1-based indexing while the notation in our paper is 0-based indexing.

## Heuristic_method_for_large_value_p.ipynb [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YimingBian/CyclicQuorumSets/blob/main/Heuristic_method_for_large_value_p.ipynb)

This Jupyter Notebook is a simple implementation of our heuristic method. When p is a composite number that can be decomposed to two factors that both fall into the range of 4 to 111. User can use this implementation to do sanity check of two cases mentioned in the paper: 
1) p = 28, p_1 = 4, base_set_1 = [0, 1, 2], p_2 = 7, base_set_2 = [0, 1, 3]
2) p = 112, p_1 = 7, base_set_1 = [0, 1, 3], p_2 = 16, base_set_2 = [0, 1, 2, 5, 8]
  
Also, further implementations on more sophisticated cases could be developed based on this simple version.

## README.MD
 
 This file.

## [All_Interest_Sets](.\All_Interest_Sets)
 
 This folder contains raw results by Naive exhaustive search, just to make sure no feasible interest set is missing. These results reveal the insights of feasible interest sets and we are inspired them to find the pairing property. 
