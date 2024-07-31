### Microbe-drug-disease dataset 

#### Introduction

We collected relevant data on microbes, drugs, and diseases to form the Microbe Drug Disease (MDD) dataset. 

#### Content

##### Drug-related data

We collected 1209 drugs-related data from multiple databases and form multiple drug features.

* drug_name.txt

  Drug name file

* drug2smile.npy

  Collecting 1209 drug smiles from databases [aBiofilm](https://bioinfo.imtech.res.in/manojk/abiofilm/index.php) and [DrugBank](https://go.drugbank.com/) and form dictionary file of drug to smile

* drug_struct_simi.txt

  Using [SIMCOMP](https://www.genome.jp/tools/simcomp/) tool to compute drug structure similarity

* drug_fringer_simi.txt

  Using python [rdkit](https://www.rdkit.org/docs/GettingStartedInPython.html) tool to compute drug fingerprint similarity

* drug_interact.txt

  Searching 10783 drug-drug interaction from [DrugBank](https://go.drugbank.com/), where the first and second columns correspond to drug name, and the third column corresponds to interaction information

* drug_interact_adj.txt

  Searching 10783 drug-drug interaction from [DrugBank](https://go.drugbank.com/), where the first and second columns correspond to drug index

##### Microbe-related data

We collected 172 microbe-related data from multiple databases and form multiple microbe features.

* microbe_name.txt

  Microbe name file

* microbe_ani_simi.txt

  Using [FastANI](https://github.com/ParBLiSS/FastANI) tool to compute consistency of microbe gene sequences

* microbe_emb.txt

  Collecting complete gene sequence from  [NCBI](https://www.ncbi.nlm.nih.gov/datasets/genome/) database and encoding microbe gene sequences through one hot encoding, then we used PCA to reduce to 128 embedding vectors

* microbe_gene_simi.txt

  The similarity matrix obtained by calculating cosine similarity of microbe embedding vectors

* microbe_interact.txt

  The interaction information between microbes obtained from the [MIND](https://visant-new.bu.edu/mind/mind_home.html#) dataset, where the first and second columns correspond to microbe name, and the third column corresponds to interaction values

* microbe_interact_adj.txt

  The interaction information between microbes obtained from the [MIND](https://visant-new.bu.edu/mind/mind_home.html#) dataset, where the first and second columns correspond to microbe index, and the third column corresponds to interaction values

##### Disease-related data

Integrating drug-disease and  microbe-disease data, we collected 154 disease data.

* disease_name.txt

  Disease name file

* disease_dag_simi.txt

  Querying the lineage structure of diseases through the [MeSH](https://id.nlm.nih.gov/mesh/) database, we construct directed acyclic graphs disease-related to calculate the similarity between diseases.

##### Drug-microbe data

We integrated the MDAD, [aBiofilm](https://bioinfo.imtech.res.in/manojk/abiofilm/index.php), [DrugVirus](https://www.drugvirus.info/) datasets and literatures to form 2268 microbe-drug associations.

* microbe_drug.txt

  Microbe-drug association file

* microbe_drug_adj.txt

  Index file corresponding to microbe-drug associations

##### Drug-disease data

We collected 700 drug-disease associations from the [CTD](https://ctdbase.org/) dataset.

* drug_disease.txt

  Drug-disease association file

* drug_disease_adj.txt

  Index file corresponding to drug-disease associations

##### Microbe-Disease data

We collected 435 microbe-disease associations from dataset [Peryton](https://dianalab.e-ce.uth.gr/peryton/#/associations)，[GutMDisorder](http://bio-annotation.cn/gutMDisorder/)，[HMDAD](https://www.cuilab.cn/hmdad).

* microbe_disease.txt

  Microbe-disease association file

* microbe_disease_adj.txt

  Index file corresponding to microbe-disease associations

#### Supplementary

* Microbe-drug association collected from literatures
  

#### Contributor

* Jing Gu
* Dongliang Chen
* Chunhong Guan
* Rui Wang
* Yuxin Zhang
* Zelong Xu
