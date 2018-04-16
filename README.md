# predictDB_mesa_peer_pc_combos
running elastic net on mesa populations with combinations of peer factors and pcs

Instructions: how to run elastic net combos
**all data found in /home/lauren/files_for_revisions_plosgen/en_v7

1. There are 3 directories in /en_v7/prepare_data and contain the processed data ready to use 
  -/en_v7/prepare_data/covariates
  -/en_v7/prepare_data/expression
  -/en_v7/prepare_data/genotypes
 
2. /en_v7/new_output will contain all processed elnet files

3./en_v7/dbs will have the new db files for running models with PrediXcan

4./en_v7/model_training/scripts/ has all the scripts needed to run elastic net and generate models from mesa
  -There are three files needed to run combos adjust these to run models accordingly 
    1. mesa_pops2.txt
    2. mesa_peers.txt
    3. mesa_covars.txt
  -adjust pop_train_combos.R to contain the correct paths to file directories (prepare_data files)
    *this file calls gtex_v7_nested_cv_elnet_combo.R 
  -run train_models_jobs_combo.sh 
    *this calls pop_train_models_combo.pbs and inputs the correct variables to run models
    
    

