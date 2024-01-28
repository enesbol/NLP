# NLP

*llama*:

https://medium.com/@ogbanugot/notes-on-fine-tuning-llama-2-using-qlora-a-detailed-breakdown-370be42ccca1 Notes on fine-tuning Llama 2 using QLoRA: A detailed breakdown
https://trojrobert.medium.com/4-easier-ways-for-fine-tuning-llama-2-and-other-open-source-llms-eb3218657f6e 2 easy ways for fine-tuning LLAMA-v2 and other Open source LLMs

*QLORA*:

https://arxiv.org/pdf/2305.14314.pdf: QLORA: Efficient Finetuning of Quantized LLMs
- Reduces memory usage for finetuning a 65B model on a single 48GB GPU while maintaining full 16-bit fine-tuning task performance.
- NF4 (4-bit NormalFloat): Optimal for normally distributed weights.
- Double quantization reduces average memory footprint.
- Paged optimizers manage memory spikes.


*llmlingua* (Prompt Compression):

- Natural language is redundant, amount of information varies.

- LLMs can understand compressed prompt.

- There is a trade-off between language completeness and compression ratio. (LLMLingua)

- GPT-4 can recover all the key information from a compressed prompt-emergent ability. (LLMLingua)

- The density and position of key information in a prompt affect the performance of downstream tasks. (LongLLMLingua)

https://arxiv.org/abs/2310.05736 LLMLingua: Compressing Prompts for Accelerated Inference of Large Language Models

https://arxiv.org/abs/2310.06839 LongLLMLingua: Accelerating and Enhancing LLMs in Long Context Scenarios via Prompt Compression

https://github.com/run-llama/llama_index/blob/main/llama_index/postprocessor/longllmlingua.py LongLLMLingua is now part of the LlamaIndex pipeline, a widely-used RAG framework. 


https://medium.com/towards-data-science/extract-knowledge-from-text-end-to-end-information-extraction-pipeline-with-spacy-and-neo4j-502b2b1e0754

https://ai.googleblog.com/2022/04/pathways-language-model-palm-scaling-to.html Pathways Language Model (PaLM): Scaling to 540 Billion Parameters for Breakthrough Performance

https://arxiv.org/abs/2203.12533 PATHWAYS: ASYNCHRONOUS DISTRIBUTED DATAFLOW FOR ML

https://arxiv.org/abs/2204.02311 PaLM: Scaling Language Modeling with Pathways

https://arxiv.org/abs/1906.08237 XLNet: Generalized Autoregressive Pretraining for Language Understanding











