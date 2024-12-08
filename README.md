# Sequence-to-Sequence Networks for Multi-Model Text Summarization    

## Overview
This project delves into the use of advanced sequence-to-sequence architectures and transformer models for multi-document summarization in the medical domain. With the rapid expansion of medical literature, efficiently condensing this wealth of information is essential for healthcare professionals, researchers, and policymakers. Our study aims to harness cutting-edge natural language processing (NLP) techniques to produce concise, informative, and coherent summaries of medical documents, addressing the critical need for accessible and actionable insights in the field of healthcare.

## Project Objectives
- **Fine-tune Transformer Models**: Focus on models such as PEGASUS, BART, and BERT to develop a robust framework for summarizing medical research articles effectively.
- **Evaluate Summarization Quality**: Use metrics like ROUGE to quantitatively measure the accuracy, coherence, and conciseness of the generated summaries.
- **Overcome Domain-Specific Challenges**: Address challenges posed by specialized medical jargon, diverse document structures, and the complex nature of medical literature to enhance the usability and applicability of the models.

## Methodology

### Datasets
1. **medical_cord19**:
   - A dataset consisting of research articles specifically focused on COVID-19.
   - Provides full-text articles and their corresponding summaries, sourced from Hugging Face.

2. **medical_meadow_cord19**:
   - Covers a broader range of general medical topics.
   - Useful for evaluating how well the models generalize to medical literature beyond COVID-19, also sourced from Hugging Face.

### Models Implemented
- **BART (Bidirectional and Auto-Regressive Transformers)**
- **BERT (Bidirectional Encoder Representations from Transformers)**
- **PEGASUS**

### Evaluation Metrics
ROUGE metrics evaluate the quality of generated summaries by comparing them to reference summaries:
- **ROUGE-1**: Assesses unigram (single word) overlap, capturing key terms.
- **ROUGE-2**: Measures bigram (two-word) overlap, assessing contextual accuracy.
- **ROUGE-L**: Checks the longest common subsequence for structural similarity and fluency.
- **ROUGE-Lsum**: Extends ROUGE-L to entire multi-sentence summaries for overall coherence and completeness.

## Implementation

1. **Data Preprocessing**:
   - Cleaned and tokenized the medical datasets, ensuring proper formatting for fine-tuning transformer models.
   - Applied dynamic padding and text standardization techniques to enhance training efficiency.

2. **Model Training**:
   - Fine-tuned pre-trained transformer models (PEGASUS, BART, and BERT) on domain-specific datasets.
   - Utilized gradient accumulation and other optimization strategies to address computational constraints.

3. **Evaluation**:
   - Analyzed model performance using ROUGE metrics to evaluate the accuracy, coherence, and relevance of the generated summaries against reference summaries.

4. **Summarization**:
   - Produced concise summaries for biomedical research articles and conducted a qualitative evaluation to assess thematic alignment and contextual accuracy.

## Results and Discussions

### Performance
The fine-tuned models, PEGASUS, BART, and BERT, showed substantial improvements in summarization quality over their baseline counterparts. ROUGE scores highlighted enhanced precision, recall, and F1-scores, with BART achieving the highest performance metrics.

### Challenges
Addressing domain-specific challenges such as complex medical terminology, abbreviations, and diverse document structures was critical. Ensuring the generated summaries were accurate, contextually relevant, and concise required meticulous model fine-tuning and preprocessing.

### Future Work
Future efforts will focus on further optimizing model performance through additional fine-tuning, integrating hybrid approaches, and leveraging external medical ontologies to improve the summarization of highly specialized medical texts.

### Model Results

| Model     | Dataset                | Base ROUGE-1 | Base ROUGE-2 | Base ROUGE-L | Base ROUGE-Lsum | Fine-Tuned ROUGE-1 | Fine-Tuned ROUGE-2 | Fine-Tuned ROUGE-L | Fine-Tuned ROUGE-Lsum |
|-----------|------------------------|--------------|--------------|--------------|------------------|---------------------|---------------------|--------------------|-----------------------|
| PEGASUS   | medical_cord19         | 0.238985     | 0.104768     | 0.185111     | 0.184566         | 0.225052           | 0.090024           | 0.181915          | 0.181877             |
| PEGASUS   | medical_meadow_cord19  | 0.244406     | 0.100007     | 0.180423     | 0.201486         | 0.239664           | 0.103230           | 0.181758          | 0.203918             |
| BART      | medical_cord19         | 0.239091     | 0.091287     | 0.205139     | 0.204514         | 0.307451           | 0.148789           | 0.260546          | 0.259868             |
| BART      | medical_meadow_cord19  | 0.257552     | 0.102131     | 0.218125     | 0.218733         | 0.292813           | 0.139123           | 0.249064          | 0.250171             |
| BERT      | medical_cord19         | 0.226260     | 0.084069     | 0.168998     | 0.168967         | 0.226922           | 0.088106           | 0.170491          | 0.169417             |
| BERT      | medical_meadow_cord19  | 0.226998     | 0.089608     | 0.164004     | 0.164497         | 0.219643           | 0.085449           | 0.158420          | 0.159239             |

## Repository Contents
- **BART_FINAL_Dataset1.ipynb**: Implementation notebook for BART models on Dataset-1.
- **BART_FINAL_Dataset2.ipynb**: Implementation notebook for BART models on Dataset-2.
- **BERT_FINAL_DATASET_2.ipynb**: Implementation notebook for BERT models on Dataset-2.
- **BERT_FINAL_DATASET1.ipynb**: Implementation notebook for BERT models on Dataset-1.
- **Pegasus_model_Dataset_1.ipynb**: Implementation notebook for PEGASUS model on Dataset-1.
- **Pegasus_model_Dataset_2.ipynb**: Implementation notebook for PEGASUS model on Dataset-2.
- **NLP Project Report.pdf**: Detailed project report.
- **Project_presentation_NLP_Final.pptx**: Presentation slides summarizing the project.
- **Recorded-Video-Presentation**: Video presentation of the project..

## Conclusion
This project highlights the transformative potential of fine-tuned transformer models like PEGASUS, BART, and BERT in summarizing complex biomedical texts. By distilling large volumes of medical research into concise and coherent summaries, these models enable healthcare professionals, researchers, and policymakers to stay informed about critical advancements efficiently. The ongoing development and optimization of these models promise to further enhance the accessibility, utility, and dissemination of vital medical knowledge.

## Contact
If you have any questions or suggestions regarding our project, please feel free to reach out at [jjaha1@unh.newhaven.edu](mailto:jjaha1@unh.newhaven.edu) or [rsari1@unh.newhaven.edu](mailto:rsari1@unh.newhaven.edu).
"""
