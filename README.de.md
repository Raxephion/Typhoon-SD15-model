# 🌪️ Typhoon (SD1.5)

Ein chaotisches Liebesprojekt mit viel Herzblut — **Typhoon** ist ein fein abgestimmtes und experimentell trainiertes Stable Diffusion 1.5 Modell, das Charaktertreue, Gesichtsdetails und ein ganz bestimmtes ästhetisches Empfinden balanciert. Es wurde trainiert, zerstört, neu trainiert, zusammengeführt, auseinandergenommen, verflucht – und schließlich freigelassen. Jetzt dürft ihr es genießen.

> _Hinweis: Dies ist die SD1.5-Version. Gleiche Seele, zwei Ausprägungen._

---

## 🆕 UPDATE: **Typhoon V2 jetzt verfügbar!**

Typhoon V2 ist ab sofort erhältlich – mit deutlich größeren Datensätzen, verbessertem Prompt-Verständnis, besserer Anatomie und größeren Trainingsauflösungen. Siehe Details weiter unten.

---

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![GitHub Repo](https://img.shields.io/badge/GitHub-Raxephion/Typhoon--SD15--model-181717?logo=github)](https://github.com/Raxephion/Typhoon-SD15-model)  
[![Hugging Face](https://img.shields.io/badge/HuggingFace-Raxephion/Typhoon--SD1.5--V1-orange?logo=huggingface)](https://huggingface.co/Raxephion/Typhoon-SD1.5-V1)  
![HF Downloads](https://img.shields.io/badge/Downloads-100%2B-orange?logo=huggingface)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

---

## 🧪 Live-Integration

Du willst Typhoon direkt in Aktion sehen – mit einer voll ausgestatteten, optimierten WebUI?

Dann schau dir **CipherCore-SD-1.5-WebUI** an — eine schlanke, schnelle Oberfläche mit Typhoon als Standardmodell:

👉 [Raxephion/CipherCore-SD-1.5-WebUI](https://github.com/Raxephion/CipherCore-SD-1.5-WebUI)

Dieses Repository bietet dir:

- Eingebaute Typhoon-Unterstützung  
- Optimierte SD1.5-Workflows  
- Sauberes UI ohne Ballast  
- Voreinstellungen, die exakt aufs Modell abgestimmt sind  
- Optimiert für CPU  
- Kostenlos für den privaten Offline-/Lokalgebrauch

---

## 📷 Beispielbilder

Alle Bilder wurden mit aktivierter "hires fix"-Option erzeugt (wie oben beschrieben). Keine LoRAs verwendet – was du siehst, ist das, was du bekommst.

<table> <tr> <td><img src="./images/00003.png" width="160"/></td> <td><img src="./images/00006.png" width="160"/></td> <td><img src="./images/00008.png" width="160"/></td> <td><img src="./images/00015.png" width="160"/></td> <td><img src="./images/00020.png" width="160"/></td> </tr> <tr> <td><img src="./images/00024.png" width="160"/></td> <td><img src="./images/00031.png" width="160"/></td> <td><img src="./images/00033.png" width="160"/></td> <td><img src="./images/00034.png" width="160"/></td> <td><img src="./images/00035.png" width="160"/></td> </tr> </table>

---

## 🧠 Über das Modell

Typhoon begann ganz harmlos — und eskalierte schnell. Nach mehreren gescheiterten Trainingsversuchen (3 von 4 Runs gingen baden) und etlichen Miet-GPU-Stunden entstand schließlich ein Modell, das sich in Portraits und stilisierten Renderings erstaunlich gut schlägt.

Das Training erfolgte durch Finetuning des ersten Checkpoints, gefolgt von speziell angepasstem LoRA-Training. Diese LoRAs wurden anschließend sorgfältig zurück ins Basismodell gemerged – mit viel Trial & Error (und einem Taschenrechner). Zur Unterstützung dieses Chaos wurden auch eigene Analyse-Tools entwickelt:

- [LoRA Strength Analyzer](https://github.com/Raxephion/loRA-Strength-Analyser)  
- [LoRA Epoch Analyzer](https://github.com/Raxephion/loRA-Epoch-Analyser)

Beide befinden sich noch im Alpha-Stadium. Mathematik passiert.

---

## 🔧 Entwicklungs- & Trainingsnotizen

### Typhoon V1
- Trainingsdaten wurden auf **512x512** gecroppt – schnell, aber limitiert.  
- Probleme mit Anatomie, Händen und schmalen Bildverhältnissen (z. B. 512x768) treten gelegentlich auf.  
- Prompting funktioniert besser mit kurzen, tag-artigen Eingaben.  
- Natürliche Sprache wird teilweise ignoriert oder inkonsistent umgesetzt.  

### Typhoon V2
- Deutlich größere Trainingsauflösungen: z. B. 576×832, 640×960  
- Verbesserte Kompositionsvielfalt und Seitenverhältnisse  
- Stärkere semantische Prompt-Adhärenz – auch bei natürlichsprachlicher Eingabe  
- Anatomie, Hände und Detailtreue wurden deutlich verbessert  
- Neues Tagging-System für ausgewogenere Ergebnisse

---

## 📐 Empfohlene Einstellungen

Typhoon funktioniert mit vielen Samplern und Settings – hier die getesteten Empfehlungen:

- **Auflösung:**  
  - V1: 512x768 oder 576x768 (mit Hires Fix)  
  - V2: bis zu 640x960 nativ (auch ohne Hires Fix stabil)  
- **CFG Scale:**  
  - V1: 6.5–7  
  - V2: 6 (etwas neutraler, stabiler bei höheren Steps)  
- **Sampler:**  
  - DPM++ 2M (Karras), Euler, Euler a  
- **Hires Fix (nur falls nötig):**  
  - Denoising Strength: **0.65–0.7**  
  - Upscale: **2x (Latent)**  
  - CFG: gleich wie oben

---

## 🧠 Prompting-Tipps

Typhoon V2 versteht Prompts deutlich besser als V1 – auch bei längeren oder natürlichsprachlichen Eingaben. Dennoch gilt:

- Kurze, klare Prompts bringen konsistentere Resultate.  
- Tags wie `"masterpiece, best quality, 1girl, solo"` wirken nach wie vor stark.  
- Für V1: besser tag-basiert prompten  
- Für V2: beides möglich – tags oder natürliche Sprache

---

## ⚠️ Einschränkungen

- V1: Anatomie-Fehler bei ungewöhnlichen Seitenverhältnissen möglich  
- V1: Prompting inkonsistent bei langen Sätzen  
- V2: Deutlich robuster, aber sehr komplexe Konzepte können vereinzelt noch vereinfacht werden  
- Keine Merge-Freigabe – siehe Lizenz

---

## 🚫 Nutzungsbeschränkungen

Dieses Modell wird unter einer modifizierten CreativeML Open RAIL-M Lizenz bereitgestellt:

- ✅ Persönliche, private Nutzung ist erlaubt.  
- ❌ **Keine Merges** mit anderen Checkpoints oder LoRAs – das ruiniert die beabsichtigte Ästhetik und Balance.  
- ❌ **Nicht hochladen** auf Drittanbieter-Plattformen oder öffentliche Bots.

Alle Details findest du in der [LICENSE](./LICENSE).

---

## 📍 Attribution

- Basis: Stable Diffusion 1.5 (v1-5-pruned-emaonly)  
- VAE: [stabilityai/sd-vae-ft-ema](https://huggingface.co/stabilityai/sd-vae-ft-ema)  
- LoRA-Analysetools: [GitHub](https://github.com/Raxephion)  
- Diffusers-Workflow: [Raxephion/Typhoon-SD1.5-V1](https://huggingface.co/Raxephion/Typhoon-SD1.5-V1) – für lokale Inferenz, Experimente und ernsthaftes Basteln

---

### 🌩️ Viel Spaß im Sturm.
