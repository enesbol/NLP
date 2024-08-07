# NLP

https://github.com/mlabonne/llm-course

**Greedy Search & Beam Search & Top-k sampling & Nucleus sampling**
https://mlabonne.github.io/blog/posts/2023-06-07-Decoding_strategies.html


**llama**: 

https://arxiv.org/pdf/2307.09288.pdf: Llama 2: Open Foundation and Fine-Tuned Chat Models

- *Fine-tuning with PEFT*
  
https://medium.com/@ogbanugot/notes-on-fine-tuning-llama-2-using-qlora-a-detailed-breakdown-370be42ccca1 Notes on fine-tuning Llama 2 using QLoRA: A detailed breakdown

https://trojrobert.medium.com/4-easier-ways-for-fine-tuning-llama-2-and-other-open-source-llms-eb3218657f6e 2 easy ways for fine-tuning LLAMA-v2 and other Open source LLMs

**QLORA**:

https://arxiv.org/pdf/2305.14314.pdf: QLORA: Efficient Finetuning of Quantized LLMs
- Computation Data Type: Usually BFloat16
- Low-Precision Storage Data Type: 4-bit
- Reduces memory usage for finetuning a 65B model on a single 48GB GPU while maintaining full 16-bit fine-tuning task performance.
- NF4 (4-bit NormalFloat): Optimal for normally distributed weights.
- Double quantization reduces average memory footprint.
- Paged optimizers manage memory spikes.

  *Paged optimizers*: Prevent memory spikes we abruptly get a really long input, especially when we're working with a single GPU. Fix: state of the optimizer ex: Adam moved from GPU memory to CPU memory till the long seq. is read. then when the GPU memory is free, the optimizer state is moved back to the GPU. paged optimizers is a part of bitsandbytes library and can be enabled using flag .is_paged from Optimizer8bit class.

**RLHF - PPO VS DPO**

https://arxiv.org/abs/2305.18290: Direct Preference Optimization: Your Language Model is Secretly a Reward Model
https://www.youtube.com/watch?v=QXVCqtAZAn4&ab_channel=DeepLearningAI: Aligning LLMs with Direct Preference Optimization

**llmlingua** (Prompt Compression):

- Natural language is redundant, amount of information varies.

- LLMs can understand compressed prompt.

- There is a trade-off between language completeness and compression ratio. (LLMLingua)

- GPT-4 can recover all the key information from a compressed prompt-emergent ability. (LLMLingua)

- The density and position of key information in a prompt affect the performance of downstream tasks. (LongLLMLingua)

https://arxiv.org/abs/2310.05736 LLMLingua: Compressing Prompts for Accelerated Inference of Large Language Models

https://arxiv.org/abs/2310.06839 LongLLMLingua: Accelerating and Enhancing LLMs in Long Context Scenarios via Prompt Compression

https://github.com/run-llama/llama_index/blob/main/llama_index/postprocessor/longllmlingua.py LongLLMLingua is now part of the LlamaIndex pipeline, a widely-used RAG framework. 

**LLM Compherensive Analysis Papers**

https://arxiv.org/pdf/2402.06196.pdf Large Language Models: A Survey


**Embedding**

https://arxiv.org/abs/2205.13147: Matryoshka Representation Learning

- After further testing, the most exciting feature (for us) is that the 256-dimensional version of text-embedding-3-large can outperform the 1536-dimensional Ada 002. That is a 6x reduction in vector size.
- OpenAI confirmed (after some prodding) that they achieved this via Matryoshka Representation Learning.
- MRL encodes information at different embedding dimensionalities. As per the paper, this enables up to 14x smaller embedding sizes with negligible degradation in accuracy.



- MTEB: This benchmark covers 56 different tasks, including retrieval, classification, re-ranking, clustering, summarization, and more. Depending on your goals, you can look at the precise subset of tasks representing your use case.

- BEIR: This benchmark focuses on the retrieval task and adds complexity in the form of different types and domains of questions, such as fact-checking, biomedical questions, or detecting duplicate questions. MTEB is largely a superset of the BEIR benchmark,




https://arxiv.org/pdf/1909.10351.pdf: TINYBERT: DISTILLING BERT FOR NATURAL LANGUAGE UNDERSTANDING
https://arxiv.org/pdf/1910.01108.pdf: DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter

https://medium.com/towards-data-science/extract-knowledge-from-text-end-to-end-information-extraction-pipeline-with-spacy-and-neo4j-502b2b1e0754

https://ai.googleblog.com/2022/04/pathways-language-model-palm-scaling-to.html Pathways Language Model (PaLM): Scaling to 540 Billion Parameters for Breakthrough Performance

https://arxiv.org/abs/2203.12533 PATHWAYS: ASYNCHRONOUS DISTRIBUTED DATAFLOW FOR ML

https://arxiv.org/abs/2204.02311 PaLM: Scaling Language Modeling with Pathways

https://arxiv.org/abs/1906.08237 XLNet: Generalized Autoregressive Pretraining for Language Understanding










