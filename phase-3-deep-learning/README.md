# 🟣 Phase 3. Deep Learning & PyTorch

**Weeks 9–13 · ~40–45 hours · Month 3**

> Full context and week-by-week table in the [main README](../README.md#-phase-3--deep-learning--pytorch).

## Rule for this month

**Type every line yourself. Never copy-paste.**

Neural nets don't click by reading. They click when your fingers have typed a training loop three times.

## What lives in this folder

```
phase-3-deep-learning/
├── week-9-nn-intuition/      # Forward-pass by hand + 3B1B notes
├── week-10-micrograd/        # Backprop from scratch, ~100 lines
├── week-11-pytorch/          # MNIST classifier in Colab
├── week-12-cnn-transfer/     # Fine-tuned image classifier
├── week-13-makemore/         # Character-level LM generating names
└── milestone-classifier-lm/  # 🎯 Image Classifier + Tiny Language Model
```

## Milestone project. Image Classifier + Tiny Language Model

Two deliverables, one folder:

1. **Fine-tuned image classifier**: pick a domain (dog breeds, plant diseases, architectural styles). Include a demo GIF in the README. Report accuracy honestly with a confusion matrix.
2. **Character-level LM**: train `makemore` on a corpus you find funny (band names, D&D monsters, pizza toppings). Ship 20 sample generations in the README.

After this month you can truthfully say: **"I built neural networks from scratch."**

## Checkpoint before Phase 4

- [ ] I can tell the backprop story (chain rule + gradient downhill)
- [ ] I can write a PyTorch training loop from memory
- [ ] I can explain embeddings
- [ ] I can explain transfer learning

## Getting a free GPU

- **Google Colab**: free T4 GPU, ~12 hrs/day. Runtime → Change runtime type → GPU.
- **Kaggle Notebooks**: free P100 GPU, 30 hrs/week. Slightly faster than Colab.
- **Lightning AI Studios**: free tier with GPU-hours if you want a persistent environment.

Do not buy a GPU this month. You don't need one.
