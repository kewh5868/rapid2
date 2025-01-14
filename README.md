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

### Click this button [![Binder](https://notebooks.gesis.org/binder/badge_logo.svg)](https://notebooks.gesis.org/binder/v2/gh/darkreactions/rapid2/HEAD?filepath=RAPID2.ipynb) to access the jupyter notebook for visualization of reaction outcomes without downloading/installing

Alternate link if previous link does not work: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/darkreactions/rapid2/HEAD?filepath=RAPID2.ipynb)


## Abstract

A spatiotemporal experimental route is reported for the antisolvent vapor diffusion crystal growth of metal halide perovskites.  A computational analysis combining automated image capture and diffusion modeling enables the determination of the critical concentrations required for nucleation and crystal growth from a single experiment.  Five different solvent systems and ten distinct organic ammonium iodide salts were investigated with lead iodide, from which nine previously unreported compounds were discovered.  Automated image capture of the mother liquor and antisolvent vials were used to determine changes in solution meniscus positions and detect nucleation event location.  Matching the observations to a numerical solution of Fick’s second law diffusion model enables the calculation of reactant, solvent and antisolvent concentrations at both the time and position of the first stable nucleation and crystal growth.  A machine learning model was trained on the resulting data reveals solvent- and amine-specific crystallization tendencies.  Solvent systems that interact more weakly with dissolved lead species promote crystallization, while those with stronger interaction can prevent crystallization through increased solubilities.  Organic amines that interact more strongly with inorganic components and exhibit greater rigidity are more likely to be incorporated into crystalline products.  

## Reaction summary table

| Rxn_ID    | Amine     | Solvent  | Crystal score | 
|-----------|-----------|----------|---------------| 
| MA_333_1  | aep       | DMF      | 4             | 
| MA_333_2  | aep       | DMSO     | 1             | 
| MA_333_3  | aep       | DMF:DMSO | 4             | 
| MA_333_4  | aep       | GBL:DMF  | 4             | 
| MA_336_4  | chma      | GBL      | 4             | 
| MA_336_5  | chma      | DMF      | 1             | 
| MA_336_6  | chma      | DMSO     | 1             | 
| MA_336_7  | chma      | DMF:DMSO | 1             | 
| MA_336_8  | chma      | GBL:DMF  | 1             | 
| MA_350_1  | acet      | GBL      | 4             | 
| MA_350_2  | acet      | DMF      | 1             | 
| MA_350_3  | acet      | DMSO     | 1             | 
| MA_350_4  | acet      | DMF:DMSO | 1             | 
| MA_350_5  | acet      | GBL:DMF  | 4             | 
| MA_351_1  | ea        | GBL      | 4             | 
| MA_351_2  | ea        | DMF      | 1             | 
| MA_351_3  | ea        | DMSO     | 1             | 
| MA_351_4  | ea        | DMF:DMSO | 1             | 
| MA_385_2  | ea        | GBL:DMF  | 1             | 
| MA_354_1  | ma        | GBL      | 4             | 
| MA_354_2  | ma        | DMF      | 4             | 
| MA_354_3  | ma        | DMSO     | 1             | 
| MA_395_1  | ma        | DMF:DMSO | 1             | 
| MA_354_5  | ma        | GBL:DMF  | 4             | 
| MA_355_1b | phenea    | GBL      | 4             | 
| MA_355_2  | phenea    | DMF      | 1             | 
| MA_394_1  | phenea    | DMSO     | 1             | 
| MA_394_2  | phenea    | DMF:DMSO | 1             | 
| MZ_342_1  | phenea    | GBL:DMF  | 1             | 
| MA_356_2  | "1,3-dap" | DMF      | 1             | 
| MA_396_1  | "1,3-dap" | DMSO     | 1             | 
| MA_356_4  | "1,3-dap" | DMF:DMSO | 1             | 
| MA_356_5  | "1,3-dap" | GBL:DMF  | 4             | 
| MA_357_2  | dmed      | DMF      | 4             | 
| MA_380_7  | dmed      | DMSO     | 4             | 
| MA_397_1  | dmed      | DMF:DMSO | 3             | 
| MA_357_5  | dmed      | GBL:DMF  | 4             | 
| MA_338_2  | dedap     | GBL      | 4             | 
| MZ_341_1  | dedap     | DMF      | 1             | 
| MA_338_4  | dedap     | DMSO     | 1             | 
| MZ_341_2  | dedap     | DMF:DMSO | 1             | 
| MZ_341_3  | dedap     | GBL:DMF  | 4             | 
| MA_358_2  | dabz      | DMF      | 4             | 
| MA_334_3  | dabz      | DMSO     | 1             | 
| MA_358_4  | dabz      | DMF:DMSO | 3             | 
| MA_358_5  | dabz      | GBL:DMF  | 4             | 


## Repository contents
The following sections indicate the folders which contain code and related data

### Jupyter notebooks

1. RAPID2.ipynb - Notebook containing all visualizations and reaction outcomes


### Raw data
All raw data files are located in the ```data``` folder

1. Diffusion_rate_and_crystal_height_all_CSV- Contains .csv files of extracted solvent heights and crystal growth time
2. Reaction Summary for github.csv - key file for the reaction ID, amine and solvent used
3. cifs - Contains the Crystallographic Information Files for running Jupyter notebook
4. csv_for_notebook - Contains the .csv files for running Jupyter notebook
5. images - Contains the image files for running Jupyter notebook
6. visible_nucleation_images - Contains the image files of first apperence of nucleation (used for running Jupyter notebook)
7. 0058.perovskitedata.wf3.csv - This escalate generated data file contains ALL the 'Anti-solvent vapor diffusion' experiments, includes "_raw_" features describing experiment details. The csv file is not used for visualization or machine learning.
8. RAPID_2_curated_dataset_SIMPLESOLVENT.csv - This escalate generated curated data file contains selected 'Anti-solvent vapor diffusion' experiments used in this study. The csv file is used for diffusion model and decision tree analysis. Solvent features are not included.
9. RAPID_2_curated_dataset_SIMPLESOLVENT.arff - Converted data set for using in WEKA software
10. diffusion_top_dataset - data set generated from diffusion modeling. Contains concentration profile data used in decision tree model
11. organic_inchikey.csv - inchikey of chemicals
12. reaction_outcome.csv - Contains the reaction outcome information for running Jupyter notebook
13. image_list.json - Keeps track of all image files in the image folder
14. ml_data.pkl - Python pickle file containing ML results
15. inventory.csv - Chemical inventory data
16. organic_inchikey.csv - Inchi keys and chemical names
17. s_spaces.json - Co-ordinates of state space for each amine
18. 'csv_for_notebook' folder contains solvent height and concentration data for visualization of plots in Jupyter notebook

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
