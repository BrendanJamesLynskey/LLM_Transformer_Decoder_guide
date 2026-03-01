# Inside the Transformer Decoder — A Visual Deep Dive

An interactive, visual walkthrough of every operation inside a decoder-only transformer, from raw text to generated tokens. Built as a single-page educational guide with animated diagrams, interactive controls, and detailed mathematical notation.

**Live demo:** [brendanjameslynskey.github.io/LLM_Transformer_Decoder_guide](http://brendanjameslynskey.github.io/LLM_Transformer_Decoder_guide/)

## Overview

This guide walks through the complete inference pipeline of a decoder-only transformer (the architecture behind GPT, LLaMA, Claude, and similar LLMs), explaining each stage with visual diagrams, symbol-by-symbol equation breakdowns, and interactive elements.

## Topics Covered

- **Tokenization** — BPE (Byte-Pair Encoding), merge tables, and the token embedding lookup
- **Token Embeddings** — The embedding matrix W_E, stacking sequences into matrices, and learned representations
- **Embedding Space** — Cosine similarity, linear substructure (king − man + woman ≈ queen), distributed representations, and the residual stream
- **Positional Encoding** — Absolute positional embeddings (GPT-2 style) and Rotary Position Embeddings (RoPE)
- **Masked Multi-Head Self-Attention** — Q/K/V projections, scaled dot-product scores, causal masking, softmax weights, multi-head concatenation, and output projection
- **Feed-Forward Networks** — Standard FFN with GELU activation and the SwiGLU gated variant used by modern models
- **Layer Normalization & Residuals** — LayerNorm, RMSNorm, residual connections, and Pre-Norm vs Post-Norm placement
- **Output Projection & Softmax** — Unembedding / LM head, weight tying, and temperature-scaled softmax with an interactive temperature slider
- **Token Sampling & Generation** — Greedy decoding, Top-k, Top-p (nucleus) sampling, the KV cache optimisation, and the full autoregressive generation loop
- **Prefill vs. Decode** — The two phases of LLM inference, compute-bound vs memory-bound characteristics, TTFT, TPS, chunked prefill, continuous batching, speculative decoding, and KV cache memory analysis
- **Glossary** — Quick-reference definitions for every term and symbol used throughout the guide

## Features

- Single self-contained HTML file — no build step, no dependencies
- Interactive attention score matrix with random regeneration
- Temperature slider demonstrating softmax distribution shaping
- Animated pipeline and data-flow diagrams
- Full mathematical notation with plain-English symbol breakdowns for every equation
- Parameter count formulas for complete model sizing

## Usage

Clone the repository and open `index.html` in any modern browser, or visit the live demo link above.

```bash
git clone https://github.com/BrendanJamesLynskey/LLM_Transformer_Decoder_guide.git
cd LLM_Transformer_Decoder_guide
open index.html
```

## Built With

This project was built with the assistance of Claude (Anthropic).

## Author

Brendan Lynskey — [GitHub](https://github.com/BrendanJamesLynskey)
