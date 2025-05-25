# ⚙️ Typhoon V1 - Recommended Generation Settings

These settings are tuned specifically for Typhoon V1 and will help ensure consistency and visual quality.

---

## 🔧 Base Generation Settings

- **Resolution**:  
  - `512x768` or `576x768` recommended  
  - Avoid 512x512 if you want better compositions

- **Sampler**:  
  - `DPM++ 2M Karras` (preferred)  
  - Alternatives: `Euler` or `Euler A`

- **CFG Scale**:  
  - 0.3 to 0.8 for best aesthetic fidelity  
  - If unsure, use `7` as a default

---

## 🛠️ Hires Fix (Highly Recommended)

- **Enabled**: Yes  
- **Denoising Strength**: `0.7`  
- **Upscale Factor**: `2x`  
- **Upscale Method**: `Latent`  
- **CFG Scale (for Hires pass)**: `7`

---

## 🖼️ VAE Settings

- Use `stabilityai/sd-vae-ft-ema`  
  - This keeps saturation high and prevents muddy colors  
- Or **omit VAE entirely** for the same visual results  
- ⚠️ Do **not** use older `.bin` VAEs (they desaturate the output)

---

## ⚠️ Model-Specific Warnings

- Avoid high aspect ratios (e.g., 1024x512) — model trained on square crops  
- Do **not merge** Typhoon with other models — this breaks its look  
- Performance may vary wildly on third-party generation sites

---

🎉 Use these settings and prompt tags as a starting point to get the most out of Typhoon V1!
