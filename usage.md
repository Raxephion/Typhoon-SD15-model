# 🌀 Typhoon V1 – Usage Guide

Typhoon is a stylized, expressive SD 1.5-based model. While it works well out-of-the-box, here are the recommended settings to get the best out of it.

---

## 🔧 Prompting Style

- Typhoon responds **best to short, tag-like prompts**.
- Natural language descriptions may result in less consistent results — this is due to the tagged nature of the training datasets.
- Example:
  - ✅ `"masterpiece, best quality, solo, dynamic angle, scenic background"`
  - ❌ `"a photo of a person sitting alone in a beautiful field with dynamic lighting"`

---

## 🧠 CFG & Sampling Settings

- **CFG Scale**: `0.3–0.8` recommended
  - Best results found around `0.6–0.7`, but can vary
- **Samplers**: Use "the usual suspects":
  - `DPM++ 2M Karras` (preferred)
  - `Euler` / `Euler A` also perform well

---

## 🖼️ Resolution Tips

- Base generation resolution:  
  `576×768` (slightly less narrow than 512×768)  
  - You *can* use 512×640 or 512×704 too, but narrow resolutions increase risk of anatomical glitches
- **Hi-Res Fix is recommended**:
  - `Upscale by`: 2  
  - `Denoising strength`: 0.7  
  - `Upscaler`: Latent  
  - `Hi-res CFG`: 7  
  - Regular CFG should match: `7`

Note: While hires fix isn’t strictly post-processing, it’s used in all sample images. It improves detail and reduces artifacting.

---

## 👁️ ADetailer & Face Restoration

- Not necessary in most cases
- **Do NOT use ADetailer for close-ups** — it tends to ruin the high-quality eyes Typhoon already renders well
- Only use face correction tools **when the output clearly struggles**

---

## ⚠️ Caveats

- **NSFW content**: The base model was NSFW-crippled. Typhoon tries, but results vary. Sometimes it works, sometimes it’s comically bad.
- **VAE Note**: Images look significantly better with a proper VAE.
  - Use the [official SD1.5 VAE](https://huggingface.co/stabilityai/sd-vae-ft-ema)
  - Older or unknown VAEs may cause dull/desaturated outputs

---

## 🚫 Do Not:

- **Do not merge this model** with others — the architecture and LoRA merges are delicate and merging will likely break its aesthetic.
- **Do not use this model on third-party generation sites** (e.g., CivitAI-hosted tools, AI hubs) unless permission is granted.
- **Private use only** without explicit permission.

---

*Enjoy the storm.*
