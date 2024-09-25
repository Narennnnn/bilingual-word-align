# Cross-Lingual Word Embedding Alignment

## Overview
This repository contains an implementation of a supervised cross-lingual word embedding alignment system for English and Hindi using the Procrustes method. The goal is to create a shared embedding space that enhances multilingual natural language processing (NLP) tasks.

## Key Features
- **Data Preparation**: Utilizes pre-trained FastText word embeddings for English and Hindi, along with a bilingual lexicon sourced from the MUSE dataset.
- **Embedding Alignment**: Implements the Procrustes method to align the embeddings, ensuring that the mapping is orthogonal to maintain the semantic relationships between words.
- **Evaluation**: Assesses the accuracy of translations using Precision@1 and Precision@5 metrics, alongside cosine similarity analyses to evaluate cross-lingual semantic similarity.
- **Ablation Study**: Investigates the impact of varying bilingual lexicon sizes on alignment quality by experimenting with different training dictionary sizes.

## Steps
### 1. Data Preparation
- **Download Pre-trained Embeddings**: Utilizes FastText embeddings for both English and Hindi.
- **Bilingual Lexicon**: Loads translation pairs from the MUSE dataset to facilitate supervised alignment.

### 2. Embedding Alignment
- **Procrustes Method**: Aligns the English and Hindi embeddings using the bilingual lexicon, ensuring orthogonality in the transformation.

### 3. Evaluation
- **Word Translation**: Translates words from English to Hindi using the aligned embeddings.
- **Accuracy Metrics**: Reports Precision@1 and Precision@5 based on a test lexicon.
- **Cosine Similarity Analysis**: Computes and analyzes similarities between aligned word pairs.
- **Ablation Study**: Evaluates alignment quality across different bilingual lexicon sizes.

## Usage
To run the code, follow these steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/Narennnnn/bilingual-word-align.git
   cd bilingual-word-align 

## Resources
- [MUSE dataset and pre-trained embeddings](https://github.com/facebookresearch/MUSE)
- [FastText](https://fasttext.cc/)
- Procrustes alignment method: Described in ["Word Translation Without Parallel Data" by Conneau et al. (2017)](https://arxiv.org/pdf/1710.04087)
