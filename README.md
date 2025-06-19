# Digital Deception Detection: An ML Solution for Phishing URL Classification

Digital Deception Detection: An ML Solution for Phishing URL Classification
A comprehensive machine learning approach to detect phishing websites using URL structure, content analysis, and external service features. This project achieves 96.8% accuracy in distinguishing between legitimate and phishing URLs using an optimized XGBoost classifier.

🎯 Project Overview
Phishing attacks represent the #1 reported cybercrime, with nearly 300,000 complaints and $12.5 billion in losses reported in 2023. This project develops an automated machine learning solution that can:


    ✅ Classify URLs as phishing or legitimate in real-time

    ✅ Achieve 96.8% accuracy with only 2.6% false negative rate

    ✅ Scale to internet-level traffic with AWS deployment
  
    ✅ Adapt to new phishing patterns through continuous learning

🗂️ Dataset

This project uses the Web Page Phishing Detection Dataset by Hannousse & Yahiouche (2021):

Source: Mendeley Data Repository
Size: 11,430 URLs (perfectly balanced: 50% phishing, 50% legitimate)

Features: 87 extracted features across three categories:

56 URL Structure Features: Domain characteristics, URL syntax patterns
24 Content Features: HTML/JavaScript analysis, page structure
7 External Service Features: Search engine indexing, reputation scores


Collection Date: May 2020

Citation:
Hannousse, Abdelhakim; Yahiouche, Salima (2021), 
"Web page phishing detection", Mendeley Data, V3, 
doi: 10.17632/c2gw7fy2j4.3


# 🚀 Quick Start 

## Prerequisites

**bash**
```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
```

## Running the Model

```bash
# Clone the repository
git clone https://github.com/gurlv/AAI510-PhishingDataset.git

# Navigate into the project directory
cd AAI510-PhishingDataset

# Run the complete pipeline on jupyter 
```


# 🔧 Model Architecture 

## Feature Engineering

**Feature Selection**: Top 50 features selected via correlation analysis

**Categories Analyzed**: URL structure, domain features, content characteristics

**No Scaling Required**: XGBoost handles mixed feature types naturally

## XGBoost Optimization

**Baseline Model**: 96.2% accuracy with default parameters

**Hyperparameter Tuning**: GridSearchCV with 3-fold cross-validation


# 📈 Model Performance Analysis
## Business Impact

Phishing Detection: 97.4% of malicious URLs caught

User Experience: Only 3.7% of legitimate sites incorrectly blocked

Risk Mitigation: Out of 1,143 phishing attempts, model catches 1,113


## Feature Importance
Top predictive features include:

1. google_index - Search engine indexing status
2. page_rank - Website authority score
3. nb_www - Subdomain patterns
4. ratio_digits_url - Suspicious character patterns
5. domain_in_title - Content-URL consistency

# 🏗️ Deployment Architecture
## AWS Cloud Infrastructure
Browser Extension → API Gateway → Lambda Function → SageMaker Endpoint
                                      ↓
                              Feature Extraction (50 features)
                                      ↓
                              XGBoost Classification
                                      ↓
                              Real-time Response
## Components

API Gateway: Public endpoint for URL classification requests

Lambda Function: Feature extraction and preprocessing

SageMaker: Hosted ML model for inference

MLOps Pipeline: Continuous monitoring and retraining



# 📚 References & Citations

## Dataset Source:

Hannousse, A., & Yahiouche, S. (2021). Web page phishing detection 
[Dataset]. Mendeley Data, V3. https://doi.org/10.17632/c2gw7fy2j4.3

FBI Internet Crime Report 2023: IC3 Annual Report https://www.ic3.gov/Media/PDF/AnnualReport/2023_IC3Report.pdf


# 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
# 👥 Authors

Gurleen Virk - Co-Developer

Alexander Padin - Co-Developer

Christopher Alleyne - Co-Developer

**Course**: AAI 510 - Machine Learning: Fundamentals and Applications

**Instructor**: Professor William Pasfield

**Institution**: University of San Diego

**Date**: June 2025
