# Biological Background

High-grade serous ovarian carcinoma (HGSOC) is the most lethal gynaecological malignancy, primarily due to its late detection and aggressive metastasis. Scientific consensus regarding HGSOC development has evolved over the past decade, shifting the identified site of origin from the ovarian surface to secretory epithelial cells within the distal fallopian tube. Current models suggest that these cells undergo sequential transformation into Serous Tubal Intraepithelial Carcinoma (STIC) lesions, which are the direct precursors to invasive cancer. This process is often driven by chronic inflammatory or oxidative stress. Significantly, molecular aberrations often occur prior to structural changes. This establishes a field effect, wherein tissue that appears morphologically benign actually possesses a hidden potential for malignancy. Characterizing the transcriptomic profile of these early transitional states is therefore essential for uncovering the mechanisms initiating carcinogenesis and identifying biomarkers for earlier intervention.

# Analytical Pipeline Overview


<img width="625" height="714" alt="Screenshot 2026-02-07 at 10 52 04" src="https://github.com/user-attachments/assets/7ceb6f08-2148-4bd3-91f6-15402cfb1901" />




The analytical workflow began with quality control to exclude low-quality libraries and doublet artifacts, followed by global scaling normalization and the selection of highly variable genes. Dimensionality reduction was performed using Principal Component Analysis (PCA) to drive unsupervised Leiden clustering and UMAP visualization. This enabled the annotation of distinct cellular identities via canonical lineage markers. To characterize the functional trajectory of the secretory epithelium, we used Differential Gene Expression (DGE) analysis and Gene Set Enrichment Analysis (GSEA), complemented by gene co-expression networking to identify regulatory modules. We then quantified cellular plasticity by calculating transcriptional Shannon entropy, validating the dedifferentiation gradient from benign to pre-malignant states using Bayesian statistical inference. Finally, we developed a predictive machine learning model targeting the intermediate Secretory Epithelial-2 population, employing a Random Forest classifier with SMOTE oversampling and Boruta feature selection to identify robust transcriptomic biomarkers of late-stage disease.


# Summary

This study used single-cell transcriptomics to map the cellular origins of HGSOC within the fallopian tube. We identified a trajectory of cellular plasticity where SE2 serves as a critical intermediate state between stable progenitors and pre-malignant STIC lesions. Bayesian analysis validated a significant entropy gradient (SE1<SE2<STIC), confirming that progressive dedifferentiation drives early carcinogenesis. Biologically, SE2 was defined by heightened metabolic stress and inflammatory signalling, distinct from the homeostatic profile of SE1. Most notably, predictive modelling demonstrated that these morphologically benign SE2 cells harbour detectable signatures of advanced disease; a Random Forest classifier distinguished Stage IV patients from benign controls with 97.5% accuracy using markers like WFDC2 and IGFBP7. These results support the existence of a field effect, suggesting that interrogating specific benign secretory populations could enable the early detection of ovarian cancer before visible lesions manifest.



