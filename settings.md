# ⚙️ Typhoon V1 – Recommended Settings

Let’s keep this simple. If you want Typhoon to behave, follow the guide below. It’s not fussy, but it *is* particular.

---

## 🧩 Base Generation

- **Resolution**:  
  - 512x768 or 576x768 (sweet spots)  
  - 512x512 technically works, but why settle?

- **CFG Scale**:  
  - Between 0.3 – 0.8 (aim for 7 if in doubt)  
  - Yes, *that low*. It helps with polish, not chaos.

- **Sampler**:  
  - DPM++ 2M Karras (recommended)  
  - Euler or Euler A also work fine  

---

## 🔨 Hires Fix (Just Use It)

- **Enable it**: Always  
- **Denoise**: 0.7  
- **Upscale**: 2x  
- **Method**: Latent  
- **Hires CFG**: 7  

Hires Fix smooths out weirdness. Without it, things get spicy in the wrong way.

---

## 🎨 VAE Stuff

- Use `stabilityai/sd-vae-ft-ema`  
  - Or no VAE at all (results are basically the same)  
  - Avoid `.bin` VAEs like the plague—they desaturate everything and ruin the mood

---

## ⚠️ Known Quirks

- Don’t go wide: high aspect ratios cause limb soup  
- Do **not** merge this model. Ever. It’s fragile and not built for sharing DNA.  
- Results on third-party generation sites may vary wildly (and not in a good way)  

---

Use it well, and it’ll reward you. Abuse it, and the chaos gods will laugh.
