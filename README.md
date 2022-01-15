# A spatiotemporal route to understanding metal halide perovskite crystallization

<center><h3>Mansoor Ani Najeeb<sup>1</sup>, Rodolfo Keesey<sup>1</sup>, Margaret Zeile<sup>1</sup>, Zhi Li<sup>2</sup>, Venkateswaran Shekar<sup>3</sup>, Nicholas Leiby<sup>4</sup>, Matthias Zeller<sup>5</sup>, Emory Chan<sup>2</sup>, Joshua Schrier<sup>6</sup>, Alexander J. Norquist<sup>1</sup></h3></center>
<br>

1. Department of Chemistry, Haverford College, 370 Lancaster Avenue, Haverford, Pennsylvania 19041, USA
2. Molecular Foundry, Lawrence Berkeley National Laboratory, 1 Cyclotron Road, Berkeley, California 94720, USA
3. Department of Computer Science, Haverford College, 370 Lancaster Avenue, Haverford, Pennsylvania 19041, USA
4. Two Six Technologies, 901 N. Stuart Street, Arlington, Virginia, 22203, USA
5. Department of Chemistry, Purdue University, West Lafayette IN 47907, USA
6. Department of Chemistry, Fordham University, 441 E. Fordham Road, The Bronx, New York, 10458, USA

This repo contains code, data and jupyter notebook related to RAPID_2.

Reaction vial images available upon request.

# Click this button [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/darkreactions/rapid2/HEAD?labpath=RAPID2.ipynb) to access the jupyter notebook for visualization of reaction outcomes without downloading/installing: 


## Repository contents
The following sections indicate the folders which contain code and related data

### Jupyter notebooks

1. RAPID2.ipynb - Notebook containing all visualizations and reaction outcomes

### Raw data
All raw data files are located in the ```data``` folder

1. Diffusion_rate_and_crystal_height_all_CSV- Contains .csv files of extracted solvent heights and crystal growth time
2. cifs - Contains the Crystallographic Information Files for running Jupyter notebook
3. csv_for_notebook - Contains the .csv files for running Jupyter notebook
4. images - Contains the image files for running Jupyter notebook
5. visible_nucleation_images - Contains the image files of first apperence of nucleation (used for running Jupyter notebook)
6. 0058.perovskitedata.wf3.csv - This escalate generated data file contains ALL the 'Anti-solvent vapor diffusion' experiments, includes "_raw_" features describing experiment details. The csv file is not used for visualization or machine learning.
7. RAPID_2_curated_dataset_SIMPLESOLVENT.csv - This escalate generated curated data file contains selected 'Anti-solvent vapor diffusion' experiments used in this study. The csv file is used for diffusion model and decision tree analysis. Solvent features are not included.
8. RAPID_2_curated_dataset_SIMPLESOLVENT.arff - Converted data set for using in WEKA software
9. organic_inchikey.csv - inchikey of chemicals
10. reaction_outcome.csv - Contains the reaction outcome information for running Jupyter notebook
11. image_list.json - Keeps track of all image files in the image folder
12. ml_data.pkl - Python pickle file containing ML results
13. inventory.csv - Chemical inventory data
14. organic_inchikey.csv - Inchi keys and chemical names
15. s_spaces.json - Co-ordinates of state space for each amine
16. 'csv_for_notebook' folder contains solvent height and concentration data for visualization of plots in Jupyter notebook

## Scripts in src folder

The following python scripts are used for data generation in this study

1. get_liquid_height_and_crystal_start.py - code for extracting solvent heights and crystal formation time from the reaction images
2. diffusion_coefficient_measurement.py - code for extracting curve height from the laser diffusion experiment to calculate diffusion coefficient
3. diff_coeff_analysis.ipynb - Script for calculating diffusion coefficient value from the data generated by laser diffusion experiment
4. 'diffusion_model_scripts' folder contains Matlab scripts for running diffusion model

### Scripts in src folder
1. cif_plots.py
2. plots.py
3. rapid1_plots.py

## CAD file
WF3 Diffusion block_Fillet_v1.step - CAD file for the diffusion block

# Todo for SHEKAR
1. Move 'diff_coeff_analysis.ipynb' from 'diffusion_coeff' folder to 'src'
2. Remove xrd folder from data
3. Remove following files from data (if not used anywhere else)

0000.perovskitedata.csv

0052.4-Data-WF3_Iodide.csv

0056.perovskitedata.csv

Final_Results_11_3_20.csv

Reaction Summary - Uniform_Concentration.csv

WF3_Iodides_20191211b.csv

first_pass_decision_tree_rapid2.pdf

only4_diffusion_topcolmn.xlsx

reaction_summary.csv

second_pass_decision_tree_rapid2.pdf

training_set_redone_mansoor.csv

4. Add the following files to 'data' folder instead (shared in slack on 01/15/22)

Reaction Summary for github.csv

RAPID_2_curated_dataset_SIMPLESOLVENT.arff

RAPID_2_curated_dataset_SIMPLESOLVENT.csv

0058.perovskitedata.wf3.csv

diffusion_top_dataset.csv

5. Please add explanations for line (55,56,57) above
6. Please add folder 'CAD' and add the WF3 Diffusion block_Fillet_v1.step file
