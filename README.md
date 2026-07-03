# Shakespeare GPT

A small character-level GPT (decoder-only Transformer) trained on Shakespeare
text, following Andrej Karpathy's "nanoGPT" approach. After training it
generates new Shakespeare-style text.

## Model
- Character-level tokenizer built from the training text.
- 4 Transformer blocks, 4 attention heads, 64-dim embeddings, block size 32.
- Trained for 5000 iterations with AdamW.

## Files
| File | Purpose |
|------|---------|
| `gpt.py` | Model definition, training loop, and text generation. |
| `input.txt` | Training corpus (Shakespeare). |
| `more.txt` | Sample generated output. |

## Setup & Run
```bash
pip install torch
python gpt.py
```

## Known issues / to-do
- `gpt.py` uses **hard-coded absolute paths** to `input.txt` and `more.txt`.
  Change these to relative paths so the script runs on any machine.
- `.DS_Store` is committed; remove it and keep it out via `.gitignore`.
