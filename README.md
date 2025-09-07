# Overview
This project analyzes textual data using advanced machine learning techniques to classify and cluster messages based on their **Jaccard similarity scores**. The pipeline combines **feature engineering, text encoding, clustering, and visualization** to derive meaningful insights.

## Data Preparation
Two datasets were used:
1. **LLM Binary Complete Dataset** – Contains binary features with Jaccard similarity scores.  
2. **Ushahidi Message Dataset** – Contains text descriptions of messages.

Steps:
- Preprocessed Jaccard similarity scores.  
- Created binary classifications: **Zero Jaccard** and **Non-zero Jaccard**.  

## Jaccard Score Classification
- **Zero Jaccard Scores** → Represent **no similarity**.  
- **Non-zero Jaccard Scores** → Represent **some similarity**.  

This classification was used to guide clustering.

## Message Encoding
- Messages from the Ushahidi dataset were **encoded with the T5 Encoder Model**.  
- Each message was transformed into a **512-dimensional vector**.  

## Clustering Analysis
- **DBSCAN** was applied separately to Zero and Non-zero Jaccard groups.  
- Results:  
  - **Zero Jaccard** → 7 clusters  
  - **Non-zero Jaccard** → 3 clusters  

## Dimensionality Reduction & Visualization
- **Principal Component Analysis (PCA)** reduced 512-dimensional embeddings to 2D.  
- **Scatter plots** were generated to visualize message clusters, color-coded by group.  

## Results
- **Shape of `llm_df`**: (1472, 76)  
- **Shape of `encoded_messages`**: (2020, 512)  
- **Cluster Counts**:  
  - Zero Jaccard → 7 high-level concept clusters  
  - Non-zero Jaccard → 3 high-level concept clusters  

## Conclusion
The project successfully:  
- Classified messages based on Jaccard similarity scores.  
- Encoded text with T5.  
- Clustered messages using DBSCAN.  
- Visualized results with PCA.  

These insights form a strong foundation for further **natural language processing** and **concept-level text analysis** tasks.
