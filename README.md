# 🌪️ Typhoon (SD1.5)

A personal labor of chaotic love — **Typhoon** is a finely merged and experimentally-trained Stable Diffusion 1.5 model, balancing character fidelity, facial detail, and a very specific aesthetic sensibility. It’s been trained, broken, retrained, merged, unmerged, cried over, and eventually released into the wild. Now you get to enjoy it.

> _Note: This is the SD1.5 version. Same soul, slightly more finicky temperament._

---

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Raxephion/Typhoon--SD15--model-181717?logo=github)](https://github.com/Raxephion/Typhoon-SD15-model)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-Raxephion/Typhoon--SD1.5--V1-orange?logo=huggingface)](https://huggingface.co/Raxephion/Typhoon-SD1.5-V1)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Downloads](https://huggingface.co/datasets/huggingface/metrics/raw/main/images/downloads-sd.svg)](https://huggingface.co/Raxephion/Typhoon-SD1.5-V1)



## 🧠 About

Typhoon started out simple — until it wasn’t. After multiple failed attempts (3 out of 4 training runs, to be exact) and renting GPUs for hours on end, what emerged was a model that holds up remarkably well in portrait and stylistic renders.

It was trained using a mix of first-stage checkpoint finetuning followed by LoRA training specifically crafted for this project. Those LoRAs were then carefully merged back into the base model using good old-fashioned trial and error (and a calculator). To help make sense of this merging process, I also developed a companion Python script:

- [LoRA Strength Analyzer](https://github.com/Raxephion/loRA-Strength-Analyser)
- [LoRA Epoch Analyzer](https://github.com/Raxephion/loRA-Epoch-Analyser)

Both are in alpha. Math happens.

---

## 🔧 Development & Training Notes

- Finetuning dataset was cropped to **512x512** — a bit of a boo-boo in retrospect.
- Will be corrected in V2 with larger, aspect-ratio-considerate image sets.
- Base model: **v1-5-pruned-emaonly.safetensors** (aka, the last uncorrupted vanilla model I could still find post-RunwayML purge).
- VAE: Official StabilityAI VAE used. Highly recommended. The old one made things… murky.

---

## 📐 Recommended Settings

Typhoon doesn’t need much to look good, but here are my tried-and-tested generation settings:

- **Resolution:** 512x768 (or slightly broader, like 576x768)
- **CFG Scale:** 7 (can range from 0.3–0.8 for experimental results)
- **Sampler:** DPM++ 2M (Karras), Euler, or Euler a — the usual suspects
- **Hires Fix:**  
  - Denoising Strength: **0.7**  
  - Upscale: **2x (Latent)**  
  - CFG: **7**

> No aDetailer or face restoration needed for portraits. The model handles facial details very well — especially close-ups.

---

## 🧠 Prompting Tips

Typhoon responds best to **tag-like prompts** over natural language. This is likely because training data was captioned that way. Short, efficient, clean tags = best results.

---

## 📷 Sample Images

Sample images use hires fix as described above. No LoRAs were applied — what you see is what you get.

---

## ⚠️ Limitations

- NSFW results are **hit and miss**, due to the base model being partially neutered. Typhoon tries. When it works, it works. When it doesn't — you’ll know.
- Tag-heavy prompting works better than prose.
- The anatomy fairy occasionally takes the day off (but is improving).

---

## 🚫 Usage Restrictions

This model is provided under a modified CreativeML Open RAIL-M license:

- ✅ Personal, private use is fine.
- ❌ **Do not merge** this model with other checkpoints or LoRAs — it breaks the intended aesthetic and balance.
- ❌ **Do not upload** this model to third-party generation sites or public bots.
- ✅ You can request transformer links for local use via DM.

See the [LICENSE](./LICENSE) file for full details.

---

## 📍 Attribution

- Base: Stable Diffusion 1.5 (v1-5-pruned-emaonly)  
- VAE: [stabilityai/sd-vae-ft-ema](https://huggingface.co/stabilityai/sd-vae-ft-ema)  
- LoRA analyzers: [GitHub](https://github.com/Raxephion)  
- Diffusers Repo: [Raxephion/Typhoon-SD1.5-V1](https://huggingface.co/Raxephion/Typhoon-SD1.5-V1) — for local inference, diffusers workflows, and serious tinkering

---

### 🌩️ Enjoy the storm.
