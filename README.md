# Installation
1) Set up labelme (https://labelme.io/)
- You should set up a conda environment and then install labelme on command line
- You can follow the following template:
///

conda create -n phenogpt2 python=3.11

conda activate phenogpt2

conda install pandas numpy matplotlib PIL

pip install labelme

pip install opencv-python-headless

pip install --upgrade pyqt5_tools

labelme

///
Next time, when you come back for annotating.

You just need to open terminal line, copy and paste these 2 lines:
///

conda activate phenogpt2

labelme

///
The application should be popped up. If not, ask Quan.
2) GMDB Dataset
- It's simply a dataset that contains more than 7,000 images of patients with rare diseases. One patient may have multiple images but in terms of longitudal. 
- Each image will have predefined phenotypes, which may be incorrect. Your goal is to fix these errors and label the regions.
- You can access the image here https://chop365-my.sharepoint.com/:f:/r/personal/nguyenqm_chop_edu/Documents/Shared/GMDB/image_ann?csf=1&web=1&e=ZKZGGu
- You should download each folder and annotate batch by batch.
- You can also apply for GMDB access or send Quan (nguyenqm@chop.edu) for additional details.
3) Assignment
- First, you need to open the labelme window and upload the image for annotating
- Each of them will be assigned for hundreds to thousands of images (which may take one min in average for a patient's image).
- You should access google colab here: https://colab.research.google.com/drive/19zJ4HHfw8S18OiRAJcxZVAuLJoqu1VuN?usp=sharing
- You should download the phenotypic information from gmdb_phenogpt2.csv file (sent via email). Then upload on google colab.
- Provide the image_id (filename) in the 3rd cell. Make sure that you provide the correct filename that you use for labelme.
- If the cell is error or returns '{}', this means there is no predefined phenotypes for this patient, please annotate them
- If the cell returns some phenotypes, they are the predefined phenotypes. Sometimes, they are correct while sometimes not. So, you should fix the error if you found it. Otherwise, just annotate the affected area for them.

4) Output
- We would like to check whether the predefined phenotypes are correct or not (you can search google for confirmation).
- In addition, you should create a polygon/color the affected area for the corresponding phenotypes.
    For example: if patient presents palate cleft, you should shade the cleft area and name the cluster to be 'cleft palate'.
  
    The name of the cluster has to be from the list of Human Phenotype Ontology database. You can access https://hpo.jax.org/
- If the term is incorrectly defined, you need to figure out what the correct term for this phenotype and assign the correct name. 
- Once you finish annotating one image, please save the output as the JSON file and rename it to 'filename_annotated.json'



If you use Google Colab, then ask Quan for the colab notebook (phenotype_checking.ipynb).
1) Upload the gmdb_phenogpt2.csv
2) Provide the image id to view the phenotypes
