Putative Disease Gene Identification and Drug Repurposing for Osteoporosis

This repository contains code, analysis, and results for a project that applies network biology to uncover new candidate genes and drug repurposing opportunities for osteoporosis. By combining interactome reconstruction, disease gene mapping, predictive algorithms, enrichment analysis, and drug–gene interaction data, this work provides a reproducible framework for exploring therapeutic strategies in complex diseases.

🔬 Overview

Osteoporosis is a progressive bone disease characterized by reduced bone density and increased fracture risk. Current therapies are limited, motivating the search for novel targets and repurposable drugs.

This project:

Reconstructs the human interactome from BioGRID.

Maps curated osteoporosis-associated genes onto the interactome.

Applies multiple algorithms to predict new putative disease genes.

Validates predictions through enrichment analysis (GO, KEGG, Reactome).

Links prioritized genes to approved drugs via DGIdb.

Cross-checks drug relevance with clinical trial data.

🛠️ Methods

Interactome Construction

Downloaded protein–protein interactions from BioGRID.

Filtered for Homo sapiens and physical interactions.

Extracted the largest connected component (LCC).

Gene–Disease Associations (GDA)

Osteoporosis-related genes curated from DISEASES database.

Mapped onto the interactome to form the disease LCC.

Candidate Gene Prediction

Algorithms tested:

DIAMOnD (best performing)

DiaBLE

Diffusion-based

Evaluated with 5-fold cross-validation using precision, recall, and F1-score.

Enrichment Analysis

Compared known vs. predicted gene sets with Enrichr.

Assessed GO terms, KEGG pathways, Reactome pathways.

Drug Repurposing

Queried DGIdb for drug–gene interactions.

Validated hits using ClinicalTrials.gov.

📊 Key Results

100 putative disease genes predicted by DIAMOnD.

Enrichment analysis revealed significant overlap with known osteoporosis pathways.

Drug repurposing identified several candidate drugs, including:

Lamivudine and Tenofovir (validated in clinical trials).

CDK2-linked drugs (e.g., Paclitaxel, Lovastatin, Dexamethasone).

Comparison with ProConSuL algorithm confirmed robustness of prioritized genes.

📚 Data Sources

BioGRID – Protein–Protein Interactions

DISEASES – Curated Gene–Disease Associations

Enrichr – Enrichment Analysis

DGIdb – Drug–Gene Interactions

ClinicalTrials.gov – Validation

⚠️ Raw data is not stored in this repository.

📜 License

This project is released under the MIT License.
