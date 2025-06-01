# 📚 Dataset Notes – Typhoon V1 & V2

## Overview

Typhoon has gone through a few data-related… evolutions.

**V1** was built using a large, hand-curated dataset, sourced from multiple aesthetic domains and manually cleaned, tagged, and prepared. All images were cropped to 512×512 — a decision made early on due to limited hardware and to match common SD1.5 training conventions.

**V2**, on the other hand, is the dataset’s redemption arc. The images were upscaled, reprocessed, and recropped to take full advantage of **larger aspect ratios** and to reduce the anatomical sins introduced by V1’s square-bound limitations.

---

## 🧊 Typhoon V1 Dataset

### Resolution & Limitations

Let’s be honest — 512×512 was a bad call in hindsight.

- It simplified things early on and aligned with most LoRA training workflows.
- But it also introduced visible issues with narrow or tall aspect ratios (like 512×768).
- Expect extra limbs, melted fingers, or “what is that elbow doing” moments if you don’t use Hires Fix or compose carefully.

These limitations were a key reason V2 happened.

### Prompt Style & Tagging

V1 was trained on **tag-style captions** — think Danbooru meets fashion moodboards.

- Prompts like `1girl, masterpiece, soft lighting, detailed face` work beautifully.
- Natural language prompts may still work but can lead to muddy or confused generations.

It’s not allergic to full sentences, but you’ll get better results treating it like a tag-driven engine.

### Dataset Size

Let’s just say: it’s big.

- The dataset was split into subsets for specific LoRAs (style, character, theme, etc.).
- Some LoRAs were merged into the final model, others tossed into the abyss.
- About 25% of training runs were failures. Par for the course.

---

## 🔥 Typhoon V2 Dataset

### Resolution & Aspect Ratios

V2 was rebuilt with smarter, higher-fidelity data:

- Images were upscaled and **recropped to 576×832, 640×960**, and similar higher aspect ratios — no more square prison.
- Cropping logic prioritized composition, headroom, and consistent centering (where possible).
- This drastically improved body proportions, hand consistency, and scene layout.

No more guessing what that hand is doing behind someone’s head.

### Tagging & Prompt Style

Still tag-centric — just better.

- The dataset was re-captioned with updated tag vocabularies and improved granularity.
- V2 responds well to the same prompt style as V1, so you don’t need to relearn your phrasing.
- But it does **handle natural language a bit more gracefully** due to improved tagging and captioning variety.

### Quality & Filtering

- Duplicates, poor compositions, and JPEG-abused messes were filtered aggressively.
- More diverse lighting, clothing, poses, and expressions are now baked into the dataset.
- Results feel sharper and more stylistically coherent out of the box.

---

## Closing Notes

Typhoon’s dataset design is a result of trial, error, caffeine, and rework.  
If V1 was a testbed, **V2 is the actual storm**.

---

*Enjoy the storm.*
