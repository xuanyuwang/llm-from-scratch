

# LLM Concepts Index

This file lists all foundational concepts needed to understand and implement a Transformer-based Large Language Model from scratch. Each item will be expanded in its own file.

## 1. Tokenization & Representation
- Tokens
- Vocabulary
- Sequence length
- Padding

## 2. Embeddings
- Token embeddings
- Positional embeddings (sinusoidal vs learned)

## 3. Training Objective
- Next-token prediction
- Teacher forcing
- Logits
- Cross-entropy loss

## 4. Attention Mechanism
- Queries (Q), Keys (K), Values (V)
- Attention scores
- Softmax weighting
- Causal masking
- Multi-head attention
- Attention scaling

## 5. Transformer Block Architecture
- Multi-head self-attention layer
- Residual connections
- LayerNorm (Pre-LN vs Post-LN)
- MLP / Feed-forward network
- Dropout

## 6. Model Architecture
- Embedding layer
- Stacked transformer blocks
- Final LayerNorm
- Output projection layer

## 7. Training Mechanics
- Backpropagation
- Adam optimizer
- Learning rate schedule (warmup, decay)
- Batch size
- Overfitting vs underfitting

## 8. Inference & Sampling
- Temperature
- Greedy decoding
- Top-k sampling
- Top-p (nucleus) sampling

## 9. Additional Useful Concepts
- Parameter initialization
- Weight tying
- Gradient clipping
- Context window limits