# Topic Modeling-Data Mining Project

## Overview

This project focuses on mining topics from Yemeni Saba News articles using various natural language processing (NLP) and machine learning techniques. The main goal is to uncover hidden patterns and trends within the news data. The project involves preprocessing the data, embedding the text, reducing dimensionality, clustering topics, and representing topics using key phrases.

## Techniques Used

### 1. Pre-processing

The initial step involves cleaning and preparing the textual data for analysis. Techniques include:
- Removing URLs
- Replacing digits with a placeholder
- Adding spaces around punctuation
- Removing extra spaces
- Tokenization and lowercasing

### 2. Embedding

Sentence embeddings are generated using the LaBSE (Language-agnostic BERT Sentence Embedding) model. This step converts the text into numerical vectors, capturing semantic relationships between words.

### 3. Dimensionality Reduction

UMAP (Uniform Manifold Approximation and Projection) is employed to reduce the dimensionality of the embeddings while preserving the global structure of the data.

### 4. Clustering

HDBSCAN (Hierarchical Density-Based Spatial Clustering of Applications with Noise) is used for clustering the news articles into topics. The min_cluster_size parameter controls the granularity of topics.

### 5. Vectorization

CountVectorizer is utilized to convert the text data into a bag-of-words representation, enabling further analysis.

### 6. Topic Representation

KeyBERT is employed to extract key phrases that represent each topic, providing insights into the main themes of the clustered articles.

### 7. Topics Modeling

BERTopic, a topic modeling library, is used to perform end-to-end topic modeling. It combines the previously mentioned techniques to create a comprehensive model for topic discovery.
![image](https://github.com/Hamza-ALsaqaf/Data-Mining-Project/assets/91475681/c4be4939-2c76-4516-8550-5a2813fbdfec)

![image](https://github.com/Hamza-ALsaqaf/Data-Mining-Project/assets/91475681/22373a72-532a-46ac-bfe0-3617565db94f)


![image](https://github.com/Hamza-ALsaqaf/Data-Mining-Project/assets/91475681/87245ec1-08df-4b5e-a293-59840fb8874c)



![image](https://github.com/Hamza-ALsaqaf/Data-Mining-Project/assets/91475681/8f05e988-fa3d-4ca4-a7d4-4ec95f064a6d)

## How to Run the Code

1. Open the Jupyter Notebook file `Saba_News_Data-Mining.ipynb` using a Jupyter Notebook environment.

2. Install the required Python packages by running the command `!pip install bertopic==0.16.0 datasets==2.16.1 Arabic-Stopwords==0.4.3`.

3. Execute each cell in the notebook sequentially to load the data, preprocess it, generate embeddings, cluster topics, and visualize the results.

4. Explore the different visualizations and analyses provided in the notebook, such as histograms, heatmaps, and hierarchical topic structures.

## Inference

The code also demonstrates how to use the trained model for topic inference on new news articles. Simply provide a new article as input to obtain its predicted topic and probability.

## Save and Reload

The trained BERTopic model can be saved and reloaded for later use. This allows for easy reuse without the need to retrain the entire model.

---
