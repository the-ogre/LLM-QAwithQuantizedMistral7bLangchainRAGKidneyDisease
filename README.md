# LLM-QAwithQuantizedMistral7bLangchainRAGKidneyDisease
### This repo is about pulling data from external urls, using them as knowledge base, and anwering questions on kidney disease.


# Project Description

The project involves the utilization of Mistral-7B and LangChain for creating an OA system. Below is a breakdown of the project components:

1. **Environment Setup:**
   - CUDA Version: 11.8
   - Compiler: NVIDIA CUDA compiler driver, version 11.8.89
   
2. **Library Installation:**
   - PyTorch is installed using the command `pip install torch --index-url https://download.pytorch.org/whl/cu118`.
   - Other libraries, including LangChain, Playwright, Html2Text, Sentence Transformers, FAISS-GPU, Peft, BitsAndBytes, and TRL, are installed.

3. **Model Configuration:**
   - A 7B-instruct MistralAI model is used, and its configuration includes 4-bit precision base model loading with nested quantization.
   - GPU compatibility with bfloat16 is checked, and if supported, training acceleration with bf16 is recommended.

4. **Model Loading and Inference:**
   - The MistralAI model is loaded for causal language modeling, and a text generation pipeline is created.
   - A prompt template is provided for answering questions related to kidney failure and artificial kidneys.

5. **Data Processing and Indexing:**
   - Articles related to kidney disease and artificial kidneys are indexed using a combination of LangChain components, including loaders, transformers, and embeddings.
   - The indexed documents are chunked and loaded into the FAISS index for efficient retrieval.

6. **Question Answering:**
   - A variety of questions on kidney disease and artificial kidney are posed to the model using the Rag (Retrieval-Augmented Generation) approach.
   - The answers are generated and printed.
