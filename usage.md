# 🌀 Usage Guide for Typhoon V1

Typhoon V1 is a visually expressive, artistically biased model trained for creative, high-quality generations. This guide outlines how to get the best results out of it, whether you're using `.ckpt` or the `diffusers` version.

---

## 🧠 General Prompting Advice

Typhoon responds better to **shorter, tag-like prompts**, a byproduct of the way the training data was structured. Natural language prompts *can* work, but tags are more reliable.

**Example:**

`masterpiece, best quality, dramatic lighting, ultra-detailed, solo, medium shot, looking at viewer`

> Note: No trigger words are required.

---

## 🛠 Base Settings

- **CFG**: `0.3` to `0.8` (try `7` for general use)
- **Sampler**: `DPM++ 2M Karras`, `Euler`, or `Euler a`
- **Base Resolution**: `512x768` (see resolution notes below)
- **Hires Fix**: Highly recommended  
  - Denoising strength: `0.7`  
  - Upscale by: `2`  
  - Upscaler: `Latent`  
  - Hires CFG: `7`

---

## 🧾 Notes on Hires Fix

Hires fix significantly improves anatomical consistency and detail, especially in complex compositions or full-body shots. Closeups, particularly of the eyes, are rendered with impressive clarity even without ADetailer or face restoration.

---

## 🖼 Resolution Notes

The model was trained on datasets cropped to `512x512`. As a result:

- Best base resolution: `512x768` (or `576x768` for slightly wider results)
- Wider or more custom aspect ratios may introduce errors (extra limbs, fingers, etc.)
- These limitations will be addressed in Typhoon V2

---

## 🧨 Using Diffusers (Hugging Face Transformers)

Typhoon is available in `diffusers` format for Python-based workflows.

👉 **[View on Hugging Face](https://huggingface.co/Raxephion/typhoon-v1-diffusers)**

```python
from diffusers import StableDiffusionPipeline
import torch

pipe = StableDiffusionPipeline.from_pretrained(
    "Raxephion/typhoon-v1-diffusers", torch_dtype=torch.float16
)
pipe = pipe.to("cuda")

prompt = "masterpiece, best quality, solo, dramatic lighting"
image = pipe(prompt).images[0]
image.show()
```

---

## 🔍 VAE Info

- Recommended: `vae-ft-ema` from [`stabilityai/sd-vae-ft-ema`](https://huggingface.co/stabilityai/sd-vae-ft-ema)
- Using this or **no VAE at all** yields sharp, saturated results
- Avoid old `.bin` VAE files (some may dull colors or desaturate the image)

---

## 🔒 Usage Restrictions

Please **do not**:
- Use this model on third-party generation websites
- Merge it into other models
- Re-upload or redistribute it under a different name

**Why?**  
Typhoon has a very specific aesthetic, balanced through a fragile process of finetuning and merging. Merging it will likely break its style and degrade performance.

✅ You **can** use it freely for **private and personal** use.

If you’d like to use it commercially, or in a public project, please contact me directly.

---

Enjoy the storm.  
— **Raxephion**
