# CSC_791_Geospatial_AI: Exploring Explainability and Fairness in FireRisk  

**Analyzing Low Accuracy Results in Remote Sensing with XAI and Fairness**  
**Team Members**: Amitesh, Meet, & Azeeza  

This repository focuses on exploring explainability and fairness in the context of FireRisk classification. Our aim is to analyze and improve low accuracy results in remote sensing tasks by integrating explainable AI (XAI) techniques and fairness algorithms.  

**Overleaf Paper**: [Access here](https://www.overleaf.com/5629446458xgdbhdwsxqzk#1b3451)  

---

## General Configuration  

### Instructions for Kaggle Setup  

1. **Upload Notebook**: Start by uploading the project notebook to Kaggle.  
2. **Dataset**: Use the provided dataset uploaded on Kaggle:  
   [Fire Risk All Samples](https://www.kaggle.com/datasets/meetvora090201/fire-risk-all-samples).  
3. **Checkpoint**: Load the model checkpoint uploaded by our team:  
   [FireRisk Checkpoint](https://www.kaggle.com/models/meetvora090201/mm).  
4. **Accelerator Configuration**:  
   - Under the *Accelerator* section, select **GPUXT4** (dual GPU setup) to facilitate distributed learning, as it might be difficult getting all the data of 16 GB under one GPU.
5. **Subset of Data**: Upload the 10% sample dataset available here:  
   [FireRisk Classification Sample Data](https://www.kaggle.com/datasets/meetvora090201/fire-risk-classification/data).  

---

### Folder Structure  

1. **Baseline**  
   - Contains the notebook: `full_dataset_fire_risk_baseline.ipynb`.  
   - Follow the general configuration setup and execute the notebook up to the section **Plot the confusion matrix and classification report**.  

2. **Experiment_S1_S2_S3**  
   - Includes three notebooks:  
     - `full-dataset-fire-risk_s1.ipynb`  
     - `full-dataset-fire-risk_s2.ipynb`  
     - `full-dataset-fire-risk_s3.ipynb`  
   - Each represents approaches S1, S2, and S3 detailed in the paper.  
   - Run the entire notebooks to view the results for each approach.  

3. **ResNet50_Exp1**  
   - Contains the file: `fire-risk.ipynb`.  
   - Use this notebook with the 10% sample dataset.  
   - Execute all the cells in the notebook.

4. **AE**
   - Contains the file: `Auto_Encoder_10%_data.ipynb`.  
   - Use this notebook with the 10% sample dataset.
   - Execute all the cells in the notebook.
     
5. **XAI**  
   - Contains the file: `full_dataset_fire_risk_xai_tsne.ipynb`.  
   - Use the full dataset and run the notebook up to the section **Custom model**.  
   - This notebook produces activation maps and t-SNE plots:  
     - If GPU RAM usage causes an error while generating t-SNE plots, restart the kernel.  
     - Skip the explainability section and directly execute the code for t-SNE plots, as these processes are independent.

6. Fairness
  - Contains the three notebooks:
    - `final-project-csc-791-geospatial-initial.ipynb`
    - `class-re-weighting.ipynb`
    - `fairlearn-mitigator.ipynb`
  - Run `final-project-csc-791-geospatial-initial.ipynb` to get initial results of fairness.
  - Run `class-re-weighting.ipynb` to get the class weight results.
  - Run `fairlearn-mitigator.ipynb` to get the fairness mitagator results.

---

**Note**: Ensure you update the path variables in the code to correctly locate and connect to the datasets.  
