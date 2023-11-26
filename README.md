# BERT-Text-Summarization-COVID
## Introduction
Due to the unique nature of the COVID-19 pandemic, text data related to it has exhibited explosive growth in scale within a short period. This data is characterized by its diversity and significant variations. To comprehensively study this textual information and better understand the virus's development trends and mutation directions, automatic summarization techniques play a crucial role. In this project, a fine-tuned BERT model is applied to generate medical text summaries based on publicly available literature data. The model framework consists mainly of encoder, decoder, and training modules. The core components for abstract generation include an encoder and decoder structure with BERT Embedding and BiLSTM, along with a multi-layer neural network connecting different modules to enable multi-task learning. Various attention mechanisms are also employed in the model.

## Model
BERT is a language model capable of unsupervised pre-training using a large amount of text data, forming the foundation of this summarization generation model. BERT features a bidirectional Transformer encoding layer, allowing for the pre-training of deep bidirectional representations of unlabeled data through a conditioned pre-processing procedure. This enables a better capture of bidirectional relationships within input sentences.

The summarization generation model structure proposed in this report consists of two core modules: an encoder and a decoder.

![image](https://github.com/kaamava/BERT-Text-Summarization-COVID/assets/106901273/953c4138-e094-42c8-b517-306876622a8d)

The structural details of the encoder and decoder are presented in BERT-COVID-text.pdf.


## Dataset and Pre-processing
The dataset used in this report is primarily obtained by retrieving keywords related to COVID-19 from published literature data, including journals such as "Chinese Medical Journal," "Journal of Southern Medical University," and "Journal of Peking University. Medical Edition." The report collects abstracts and titles from these publications and performs data preprocessing to clean the collected data. Subsequently, the Chinese text is reorganized into word sequences using the Jieba word segmentation library for in-depth analysis. During the data preprocessing, entries with title lengths outside the range [10, 70] and corresponding abstract lengths outside the range [200, 1100] are removed. Additionally, information irrelevant to the summarization task, such as literature authors and publication sources, is filtered out.






