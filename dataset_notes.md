# Dataset Notes for Typhoon SD1.5 (V1)

## Overview

This model was trained on a diverse and highly curated dataset, originally formatted and cropped to **512x512** resolution due to early assumptions about SD1.5's requirements. This ultimately limited the native resolution range of the base model and influenced prompt responsiveness and anatomical fidelity in wider aspect ratios.

## Contents

The dataset was composed of:

* Character-centric images
* Stylized artworks
* Some realism-focused subsets
* Mixed-quality sources, manually cleaned

### Tagging Style

Data was tagged using **booru-style tags** rather than natural language descriptions. As a result, the model responds better to short, structured prompts or semi-tagged phrases, and may be less responsive to verbose, natural language prompts.

### Known Limitations

* Cropping to 512x512 affected how the model generalizes wider compositions.
* Dataset was predominantly NSFW-disabled, so erotic/explicit prompts are hit or miss.
* Natural language prompts often yield unpredictable results.

## Future Work

For **Typhoon V2**, dataset resolution will be expanded (e.g., 768x768 and 576x768) to allow for better aspect ratio generalization and improved anatomical structure. Work is already underway.
