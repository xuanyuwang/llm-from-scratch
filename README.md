# LLM From Scratch

A hands-on project to implement a tiny Transformer-based language model from scratch.

---

# 🚀 Roadmap / To-Do List

## Phase 1 — Understand the Concepts (No Coding Yet)
*Goal: Build an intuitive + structural understanding before touching implementation.*

### 📘 Core Concepts to Understand
#### 1. Tokenization & Representation
- [ ] What a token is (character-level vs BPE vs wordpiece)
- [ ] Vocabulary and integer token IDs
- [ ] Sequence length and padding

#### 2. Embeddings
- [ ] Token embeddings as lookup tables
- [ ] Positional embeddings: learned vs sinusoidal
- [ ] Why embeddings convert discrete IDs → continuous vectors

#### 3. The Training Objective
- [ ] Next-token prediction (autoregressive LM)
- [ ] Teacher forcing
- [ ] Cross-entropy loss
- [ ] What logits are

#### 4. Attention Mechanics
- [ ] Query / Key / Value role
- [ ] Attention energy matrix
- [ ] Softmax over sequence dimension
- [ ] Causal masking (upper triangular mask)
- [ ] Multi-head attention intuition (parallel subspaces)

#### 5. Transformer Block Architecture
- [ ] Attention → residual → layernorm
- [ ] MLP → residual → layernorm
- [ ] Why LayerNorm stabilizes deep training
- [ ] Difference between Pre-LN vs Post-LN

#### 6. Full Transformer LM
- [ ] Stacking blocks
- [ ] Final LayerNorm + LM head
- [ ] Logits → probability→ sampling
- [ ] Why this architecture scales well

#### 7. Training Dynamics
- [ ] Gradient descent & backprop
- [ ] Why Adam is standard
- [ ] Overfitting vs underfitting
- [ ] Importance of batch size & learning rate

---

## Phase 2 — Minimal LM Without Attention
*Goal: Build your first working language model end-to-end.*

### 🔧 Implementation Items
- [ ] Create tiny dataset (char-level)
- [ ] Implement dataset → batches
- [ ] Build model (Embedding → Linear → Softmax)
- [ ] Training loop (forward → loss → backward → step)
- [ ] Generate text (greedy sampling)
- [ ] Save notes in `notes/02-training-loop.md`

---

## Phase 3 — Self-Attention (Single-Head)
*Goal: Understand and implement Q/K/V and causal masking.*

### 🔧 Implementation Items
- [ ] Linear projections for Q, K, V
- [ ] Compute attention scores (QKᵀ / √d_k)
- [ ] Apply causal mask
- [ ] Apply softmax → weights
- [ ] Weighted sum with V
- [ ] Implement as `SelfAttentionSingleHead`
- [ ] Add unit tests for shapes
- [ ] Notes in `notes/03-self-attention.md`

---

## Phase 4 — Full Transformer Block
*Goal: Wrap attention into a proper block with MLP, LayerNorm, residuals.*

### 🔧 Implementation Items
- [ ] Implement Multi-Head Attention
- [ ] Implement feed-forward network (2-layer MLP with GELU)
- [ ] Add residual connections
- [ ] Add LayerNorm (Pre-LN recommended)
- [ ] Implement `TransformerBlock`
- [ ] Notes in `notes/04-transformer-block.md`

---

## Phase 5 — Mini GPT-Like LM
*Goal: Put all pieces together.*

### 🔧 Implementation Items
- [ ] Token embeddings + positional embeddings
- [ ] Stack N Transformer blocks
- [ ] Final LayerNorm
- [ ] LM head (linear projection to vocab size)
- [ ] Build `TinyTransformerLM`
- [ ] Notes in `notes/05-mini-gpt.md`

---

## Phase 6 — Training & Text Generation
### 🔧 Implementation Items
- [ ] Prepare dataset (tiny corpus)
- [ ] Train model (hyperparameters, checkpoints)
- [ ] Implement sampling:
  - greedy  
  - temperature  
  - top-k  
- [ ] Evaluate samples
- [ ] Notes in `notes/06-training.md`

---

This README will evolve as the project progresses.
