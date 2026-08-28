# LLMs in 10 words

Complex LLM concepts explained in 10 words or less.

## Transformers

- **Attention:** Weight token representations by relevance to each other
- **Multi-head attention (MHA):** One KV head per query head
- **Multi-query attention (MQA):** One KV head shared by all query heads
- **Grouped-query attention (GQA):** One KV head shared by each query-head group
- **Multi-head latent attention (MLA):** One compressed KV representation shared by all query heads
- **Residual connections:** Add earlier representations back into later layers
- **Attention residuals:** Attend over outputs from all earlier layers
- **Kimi Delta Attention (KDA):** Store compact delta-updated memory instead of full KV history
- **Mixture of Experts (MoE):** Route each token through a subset of experts
- **Latent MoE:** Compress tokens before expert routing and computation
- **Rotary positional embeddings (RoPE):** Encode token position by rotating query and key vectors

## Training

- **Pretraining:** Learn general language patterns from large unlabeled corpora
- **Continued pretraining (CPT):** Continue pretraining on new or domain-specific data
- **Supervised fine-tuning (SFT):** Minimize loss on labeled input-output examples
- **Direct Preference Optimization (DPO):** Minimize loss on preferred-rejected response pairs
- **Masked Language Modeling:** Predict masked tokens from surrounding context
- **Causal Language Modeling:** Predict the next token from previous tokens
- **Reinforcement Learning from Human Feedback (RLHF):** Maximize rewards learned from human-ranked response examples
- **Reinforcement Learning with Verifiable Rewards (RLVR):** Train with rewards from automatically verified outcomes
- **Group Relative Policy Optimization (GRPO):** Reinforce better answers within a group from the same prompt
- **Proximal Policy Optimization (PPO):** Reinforce better answers using value estimates and clipped policy updates
- **Distillation:** Train a smaller model to imitate a stronger model
- **Abliteration:** Remove refusal directions from activations or model weights
- **LoRA:** Train low-rank weight updates instead of full weights

## Inference

- **Prefill:** Process prompt tokens and populate KV cache
- **Chunked prefill:** Split long prefills to avoid blocking short prefills
- **Decode:** Generate tokens one at a time using cached context
- **Guided decoding:** Constrain output tokens by setting out-of-grammar token logits to -inf
- **Prefill-decode disaggregation:** Serve compute-bound prefill and bandwidth-bound decode separately
- **Arithmetic intensity:** Computation performed per byte of memory moved
- **KV caching:** Reuse past keys and values during decoding
- **PagedAttention:** Store KV cache in non-contiguous memory blocks
- **Prefix caching:** Reuse KV cache for identical prompt prefixes
- **FlashAttention:** Compute tiled attention on-chip before writing outputs to memory
- **Quantization:** Reduce floating-point precision to save memory
- **GGUF:** Standardised format for storing model tensors and metadata
- **MLX:** Unified CPU and GPU memory framework on Apple Silicon
- **Speculative decoding:** Draft with smaller model; verify with larger model
- **Continuous batching:** Add new requests as existing requests finish
