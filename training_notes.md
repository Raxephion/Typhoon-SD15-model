# Typhoon V1 – Training Notes

This document outlines the development process, training challenges, and methods used to bring Typhoon V1 to life.

---

## ⚙️ Model Development

Typhoon was trained in phases — both as a checkpoint and with supporting LoRAs, which were carefully merged into the final model.

- **Phase 1: Base Checkpoint Training**  
  Initial training started from a base model (`v1-5-pruned-emaonly.safetensors`). This model was chosen due to its lack of modern biases — most newer models were already heavily fine-tuned or crippled in some way. However, this base turned out to be rather limited, and introduced several early struggles.

- **Phase 2: LoRA Training & Merging**  
  Custom LoRAs were trained on cropped 512×512 datasets. Each was designed to improve specific attributes.  
  These LoRAs were then:
  - Evaluated for strength/impact
  - Carefully merged into the base one by one
  - Adjusted for weight balance to avoid overpowering the aesthetic

  This trial-and-error process significantly increased development time and compute cost — **3 out of 4 training runs failed**.

## 🧪 LoRA Analyzer Tooling

These challenges led to the creation of two experimental tools:

- [**LoRA Strength Analyzer**](https://github.com/Raxephion/loRA-Strength-Analyser)  
  A script that compares LoRA generations across different strength values using SSIM and BRISQUE metrics.

- [**LoRA Epoch Analyzer**](https://github.com/Raxephion/loRA-Epoch-Analyser)  
  Helps determine which epoch produces the most aesthetically and structurally sound output.

Both tools are in **alpha** and available publicly on GitHub.

---

## 💸 GPU Rental & Costs

Typhoon’s development wasn’t cheap.

- GPU time was rented due to lack of local hardware.
- Failed checkpoints (3/4) added extra cost.
- Many experiments, reruns, and dataset tweaks extended the timeline.

Safe to say, **this model cost a small storm to make** — but hopefully it’s worth it.

---

## 📝 Dataset Resolution Oversight

All finetuning datasets were cropped to **512×512** resolution. This decision, while convenient, contributed to:
- Poorer anatomical consistency in wide/full-body shots
- Narrow base resolution limitations

**This will be corrected in Typhoon V2**, with datasets upscaled and recropped to larger, more flexible aspect ratios.

---

*Enjoy the storm.*
