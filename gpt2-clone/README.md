GPT-2 Clone (from scratch)

**What:** A miniature GPT-2-style Transformer language model built entirely in PyTorch.  
**Why:** To learn the internals of attention, residual connections, and layer normalization by re-implementing them manually.

-Features
   Byte-level BPE tokenizer (Hugging Face)
   Causal multi-head self-attention with masking
   Pre-LayerNorm residual blocks with GELU MLP
   Weight tying between embeddings and output layer
  Training loop with AdamW, dropout, and gradient clipping
  Text generation script with temperature + top-k sampling

-Results
   Tiny config (6 layers, 6 heads, 384 hidden dim, context=512):  
   Validation perplexity: XX after N steps  
   Generates coherent short sequences

-How to Run
```bash
pip install -r ../env/requirements.txt
python src/train.py --config configs/tiny.yml
python src/generate.py --prompt "The meaning of life is"
