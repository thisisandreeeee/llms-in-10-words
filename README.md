# LLMs in 10 words

A quick-reference guide to LLM concepts in ~10 words each—focused on the core mechanism, using simple base verbs, minimal jargon, and no filler.

## Transformers

- **Rotary positional embeddings (RoPE):** Encode token position by rotating query and key vectors
- **Attention:** Weight token representations by relevance to each other
- **Query, key, value projections:** Transform tokens into vectors for matching and information retrieval
- **Multi-head attention (MHA):** Attend to different token relationships with multiple heads
- **Multi-query attention (MQA):** Share one KV head across multiple query heads
- **Grouped-query attention (GQA):** Share fewer KV heads across multiple query heads
- **Residual connections:** Add earlier representations back into later layers
- **Attention residuals:** Combine attention outputs with earlier hidden representations
- **Mixture of Experts (MoE):** Route each token through a subset of experts
- **Latent MoE:** Route compressed latent representations through expert pathways

## LLM training stages

- **Pretraining:** Learn general language patterns from large unlabeled corpora
- **Continued pretraining (CPT):** Continue pretraining on new or domain-specific data
- **Supervised fine-tuning (SFT):** Train on input-output examples with supervised loss
- **Direct Preference Optimization (DPO):** Train on preferred versus rejected responses directly
- **Masked Language Modeling:** Predict masked tokens from surrounding context
- **Causal Language Modeling:** Predict the next token from previous tokens
- **RLHF:** Optimize model behavior using rewards from human preferences
- **RLAIF:** Optimize model behavior using rewards from AI preferences
- **Distillation:** Train a smaller model to imitate a stronger model
- **Abliteration:** Remove targeted behavioral directions from model activations or weights
- **LoRA:** Train low-rank weight updates instead of full weights
- **QLoRA:** Train LoRA adapters on a quantized base model

## Inference

- **Prefill:** Process the full prompt and build the initial KV cache
- **Decode:** Generate tokens one at a time using cached context
- **Arithmetic intensity:** Measure computation performed per byte of memory moved
- **KV caching:** Reuse past keys and values during decoding
- **PagedAttention:** Store KV cache in non-contiguous memory blocks
- **Prefix caching:** Reuse KV cache for identical prompt prefixes
- **FlashAttention:** Compute attention with less memory movement
- **Quantization:** Represent weights or activations with fewer bits
- **Speculative decoding:** Generate candidate tokens with a smaller model and verify them
- **Continuous batching:** Add new requests as existing requests finish

## Distributed training and inference

- **Data parallelism:** Replicate the model and split data across devices
- **Tensor parallelism:** Split individual tensor operations across devices
- **Pipeline parallelism:** Split model layers into stages across devices
- **Expert parallelism:** Place different MoE experts on different devices
- **Model parallelism:** Split one model across multiple devices
