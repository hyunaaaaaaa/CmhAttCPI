## A bidirectional Interpretable compound-protein interaction prediction framework based on cross attention

## Scripts
# Performance evaluation on BindingDB, DrugBank and GPCR datasets
step1- './preprocessing_data.py': converting SMILES to molecular graph and constructing word dictionary for protein sequence 
step2- './train.py': training model

# Generalization evaluation in the unseen setting for cluster-cross validation
step1- './unseen setting/file_preparation.py': preparating files for clustering
step2- './unseen setting/clustering.py': clustering for compounds and proteins
step3- './unseen setting/split_dataset_according_clustering.py': spliting dataset based on clustering
step4- './preprocessing_data.py': scenario should be 'unseen setting', cluster_cross_validation_setting and cluster_threshold should be set a fixed value from ['compound clustering', 'protein clustering'] and [0.3,0.4,0.5], respectively
step5- './train.py': scenario should be 'unseen setting', cluster_cross_validation_setting and cluster_threshold should be set a fixed value from ['compound clustering', 'protein clustering'] and [0.3,0.4,0.5], respectively

## data
# 5 fold data of BindingDB, DrugBank, GPCR and Davis
./dataset/BindingDB/5fold data/*.txt
./dataset/DrugBank/5fold data/*.txt
./dataset/GPCR/5fold data/*.txt
./dataset/Davis/5fold data/*.txt

# 5 fold data of BindingDB based on compound clustering
./unseen setting/data/compound clustering/*.txt

# 5 fold data of BindingDB based on protein clustering
./unseen setting/data/protein clustering/*.txt

# investigational or experimental drugs in DrugBank
./dataset/case study/experimental_drugs.csv

# driver genes of breast cancer
./dataset/case study/driver_genes.csv


