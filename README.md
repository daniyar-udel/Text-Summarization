# Text-Summarization
## Project Overview
This project focuses on the development of deep learning models for **abstractive text summarization** using **GPT-2** and **T5**.  
The models generate concise summaries for news articles, leveraging pre-trained language models and NLP evaluation metrics to measure performance.

**Dataset**: Inshorts Cleaned Data (news dataset with full articles and human-written summaries).  
**Task**: Generate human-like summaries of news articles.  

- ~70,000+ news samples (depending on dataset split)  
- Abstractive summarization (not extractive)  
- Evaluation with **ROUGE** and **BERTScore**  

## Methodology
**Dataset:**  
- Inshorts Cleaned Data (Excel format).  
- Preprocessed to remove missing values, renamed columns, and converted text for model input.  

**Preprocessing:**  
- Data cleaning and formatting.  
- Tokenization using **SentencePiece**.  
- Train-validation split.  

**Modeling approach:**  
- **GPT-2** fine-tuned for abstractive summarization.  
- **T5 (Text-to-Text Transfer Transformer)** fine-tuned for summarization tasks.  
- Comparison of model performance.  

**Training setup:**  
- Device: GPU.  
- Loss function: Cross-Entropy.  
- Optimizers: Adam.  

**Evaluation metric:**  
- ROUGE (ROUGE-1, ROUGE-2, ROUGE-L).  
- BERTScore for semantic similarity.  

## Results

| Model   | ROUGE-1 | ROUGE-2 | ROUGE-L | BERTScore | Notes |
|---------|---------|---------|---------|-----------|-------|
| **GPT-2** | ~0.37   | ~0.15   | ~0.34   | ~0.82     | Generates fluent summaries, sometimes misses key facts |
| **T5**   | ~0.44   | ~0.21   | ~0.41   | ~0.87     | Produces more accurate and human-like summaries |

✅ **T5 outperforms GPT-2** across all metrics, producing higher-quality abstractive summaries.  

## Business Impact
- Enables automatic summarization of large volumes of news articles.  
- Saves time for readers by providing concise summaries.  
- Can be applied in news aggregation apps, research tools, and content recommendation systems.  
- Provides a scalable NLP-driven foundation for journalism, education, and knowledge management.  
