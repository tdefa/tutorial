

# Tutorial for selecting markes genes for image-based spatial transcriptomic experiments
This repository provides a series of Python notebooks designed to assist users in selecting marker
genes for image-based spatial transcriptomic experiments. Due to experimental constraints,
only a limited number of genes can be used in these experiments. Therefore, 
it's crucial to select a small, yet effective subset of genes that can
answer biological questions such as cell type mapping and neighborhood in the tissue.  

Marker genes must be discriminative and robust enough to identify the cell type of interest.
In the absence of cytoplasm staining,  the RNA-cell assignment is complexe.  
Errors in RNA-cell assignment can occur due to irregular cell shapes or RNA expression,
potentially leading to inaccuracies in cell type identification.  

To mitigate these challenges, our notebooks utilize tissue simulation to 
validate the chosen marker genes, estimate potential RNA-cell assignment errors and how it can affect cell type identification. 
The notebooks are designed to be user-friendly, allowing users to easily follow the
steps and adapt the code to their specific data. the workflow is illustrated in the following figure.


The notebooks are written in Python and are divided in the following sections:

1- Marker gene selection: The notebook guide the user in the selection of markers gene from scRNA-seq data.  
2- Marker gene validation: The notebook guide the user in the validation of the selected markers gene using scRNA-seq data.  
3- Tissue simulation: The notebook guide the user in the simulation of the tissue using the selected markers gene. these simulation will be used to validate the selected markers gene 
while taking into account experimental smFISH constrains.  
4-RNA-cell assignement: The notebook guide the user in the assignement
of the RNA to the cells in the simulated tissue.  
5-Assess in-situ cell type calling in smFISH simulation. The notebook guide the user in the assessment of the cell type calling in the simulated tissue, 
using the previously simulated tissue and assigned RNA to the cells. 

The primary objective of using tissue simulation is to validate
the chosen marker genes, considering the constraints of smFISH experiments.
This process takes into account potential RNA-cell assignment errors, which can arise from
irregular cell shapes or RNA expression, particularly when cytoplasm staining is not feasible.

Depending of the final estimated cell type accuracy obtain, the user can choose to adjust its markers gene list.

![Alt text](fig/preparing_experiment4.png?raw=true "Title")

 A - List of user-provided marker genes is used to simulate smFISH images.
 Optionally, realistic RNA levels are drawn from scRNA-seq data. 
 Simulation framework provides cell volumes and nuclei. 
 RNA-to-cell assignment can then be compared quantitatively to the 
 known ground truth with metrics such as Jaccard index  
 B - Marker selection method can be compared in term of in-situ cell type accuracy and RNA-cell assignement error (Jacard index))  
 C - RNA-cell assignement method can also be compared in term of in-situ cell type accuracy and RNA-cell assignement error (Jacard index))
