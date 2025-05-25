# Dataset Notes – Typhoon V1

## Overview

Typhoon V1 was developed using a large, custom-curated dataset. The data was sourced from multiple aesthetic domains, then cleaned, tagged, and prepared manually. Each image was cropped to 512×512 resolution — a decision made early on due to limited hardware and for consistency with typical SD1.5 training workflows.

### Resolution & Dataset Limitations

Admittedly, this fixed 512×512 size was… a mistake.

- While it simplified processing and was aligned with many LoRA training norms, it also introduced anatomical oddities in generations at narrower aspect ratios (e.g., 512×768).
- Expect some occasional extra limbs or warped hands unless you guide the composition carefully or upscale with Hires Fix.
- These quirks will be addressed in **Typhoon V2**, as datasets are currently being reworked to support **larger aspect ratios** and improved compositional flexibility.

### Prompt Style & Dataset Tagging

Prompting in Typhoon V1 is **tag-leaning**:
- Due to the way images were captioned and tagged during dataset prep (using tag-style prompts), the model performs better with shorter, more direct prompt structures.
- Natural language prompts may be hit-and-miss, especially if they’re too verbose.

This doesn’t mean it can’t understand full sentences — just that the output quality is more consistent with tag-heavy prompts. It’s not ChatGPT with a paintbrush… it’s more like Danbooru with an art degree.

### Dataset Size

Without getting too granular:
- The dataset is **substantial**.
- Several subsets were used to create individual LoRAs (character-centric, style, thematic, etc.), which were then tested and selectively merged into the base model.
- Many training runs failed along the way — about 1 in 4 didn’t yield usable results. Trial-and-error was a constant theme.

## Notes for V2

Work is already underway for Typhoon V2:
- Datasets are being **upscaled and recropped** to higher resolutions (e.g., 576×832, 640×960, etc.).
- Improved balance and better coverage of composition types will be a priority.
- Natural prompt understanding will also be revisited during tagging and finetuning.

Stay tuned.

---

*Enjoy the storm.*
