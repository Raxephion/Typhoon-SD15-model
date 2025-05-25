# Sample Image Generation Info – Typhoon V1

This file provides details about how the sample images were generated and post-processed.

## Generation Settings

All samples were produced using **Typhoon V1 (SD1.5)** without any LoRAs or embeddings. No ADetailer or face restoration tools were used unless explicitly noted.

### Base Generation Resolution

- **512×768**  
  This was the most commonly used resolution during generation. It offers a decent vertical layout but sometimes causes anatomical issues (extra limbs, distorted hands, etc.) — especially due to the 512×512 dataset crop constraint during training.

### Upscaling & Hires Fix

- **Hires Fix: ON**
- **Upscaler:** Latent
- **Upscale By:** 2
- **Denoising Strength:** 0.7
- **Hires CFG Scale:** 7.0 (same as base CFG)

Hires Fix is **strongly recommended** with Typhoon V1. It improves structural integrity and detail, especially for larger compositions or full-body shots.

### CFG and Samplers

- **CFG Scale:** 7.0 (base + hires)
- **Sampler:** DPM++ 2M Karras (primary)
- **Other compatible samplers:** Euler, Euler A, DPM++ 2M (non-Karras)

### Prompting Style

Due to the tagging style used in training:
- **Shorter, tag-based prompts work best.**
- Natural language prompts can be hit-and-miss or less precise in results.

## Color & Clarity Note

All samples were re-generated after a VAE switch. The original VAE (a `.bin` file of unknown origin) introduced mild desaturation and softness.

- **New VAE used:** `sd-vae-ft-ema.safetensors` (official from StabilityAI)
- **Results:** Sharper, crisper colors, better contrast.

Leaving the VAE out entirely results in **identical quality** to the official VAE. The old `.bin` one has been fully retired.

---

*Enjoy the storm.*
