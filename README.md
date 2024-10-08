# Dynamic-Bayesian-Networks
As an undergraduate researcher in the Bathe BioNanoLab at MIT, this project is meant to test the scaling laws of using static Bayesian networks to infer molecular pathways from high-throughput proteomic data. The code is written in R, and uses the BNLearn package to produce bayesian networks from simulated data. We also investigated a way to create a dynamic bayesian network, taking account pseudo-time dependent data using a library called cell rank, which is traditionally used for single-cell RNA seq. We then decoded the probability matrix outputed by cell rank into a probability matrix of protein dependencies. 

## File Descriptions
### Notebooks
  #### Bayesian_Network_Simulations.rmd
  - R Notebook that creates simulated proteomic data given transition matrix (this output used for cell rank)
  - Tests sensitivity and scoring of static bayesian networks
  - Tests scaling laws of static bayesian networks (performance as number of nodes/edges increases)
  
  #### CellRank.ipynb
  - Google colab that uses Cell Rank library to turn pseudo-time proteomic data into a cell to cell transition matrix 
  
  #### Decoding_CellRank.ipynb
  - Jupyter notebook that decodes cell rank matrix to a protein-to-protein transition matrix
  
### Data
  #### linstep_data2.csv
  - Pseudo-time dependent proteomic data generated by Bayesian_Network_Simulations.rmd
  #### sparse_matrix2.npz
  - Sparse cell-to-cell matrix generated by CellRank.ipynb
  #### final_matrix.csv
  - Protein-to-protein transition matrix decoded from CellRank


  


