# 🌪️ Typhoon (SD1.5)

Ein chaotisches Liebesprojekt mit viel Herzblut — **Typhoon** ist ein fein abgestimmtes und experimentell trainiertes Stable Diffusion 1.5 Modell, das Charaktertreue, Gesichtsdetails und ein ganz bestimmtes ästhetisches Empfinden balanciert. Es wurde trainiert, zerstört, neu trainiert, zusammengeführt, auseinandergenommen, verflucht – und schließlich freigelassen. Jetzt dürft ihr es genießen.

> _Hinweis: Dies ist die SD1.5-Version. Gleiche Seele, etwas launischer im Umgang._

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

Das Training erfolgte durch Finetuning des ersten Checkpoints, gefolgt von speziell angepasstem LoRA-Training. Diese LoRAs wurden anschließend sorgfältig zurück ins Basismodell gemerged – mit viel Trial & Error (und einem Taschenrechner). Zur Unterstützung dieses Chaos habe ich auch zwei Python-Tools entwickelt:

- [LoRA Strength Analyzer](https://github.com/Raxephion/loRA-Strength-Analyser)  
- [LoRA Epoch Analyzer](https://github.com/Raxephion/loRA-Epoch-Analyser)

Beide befinden sich noch im Alpha-Stadium. Mathematik passiert.

---

## 🔧 Entwicklungs- & Trainingsnotizen

- Das Finetuning-Dataset wurde auf **512x512** gecroppt – im Nachhinein betrachtet eher suboptimal.  
- Wird in Version 2 mit größeren, seitenverhältnisfreundlichen Datensätzen korrigiert.  
- Basis-Modell: **v1-5-pruned-emaonly.safetensors** (aka das letzte unverseuchte Vanilla-Modell nach der RunwayML-Bereinigung).  
- VAE: Offizieller StabilityAI VAE – **dringend empfohlen**. Der alte hat alles irgendwie... vernebelt.

---

## 📐 Empfohlene Einstellungen

Typhoon sieht schon ohne großes Tuning gut aus – aber hier sind meine bewährten Settings:

- **Auflösung:** 512x768 (oder etwas breiter, z. B. 576x768)  
- **CFG Scale:** 7 (experimentell: 0.3–0.8 möglich)  
- **Sampler:** DPM++ 2M (Karras), Euler oder Euler a – also die üblichen Verdächtigen  
- **Hires Fix:**  
  - Denoising Strength: **0.7**  
  - Upscale: **2x (Latent)**  
  - CFG: **7**

> Kein aDetailer oder Face-Restoration nötig – Portraits gelingen auch so erstaunlich gut, vor allem in Nahaufnahmen.

---

## 🧠 Prompting-Tipps

Typhoon reagiert besser auf **tag-artige Prompts** als auf natürlichsprachliche Eingaben. Wahrscheinlich, weil die Trainingsdaten so beschriftet waren. Kurz, sauber, effizient = beste Resultate.

---

## 📷 Beispielbilder

Siehe oben — alle ohne LoRAs, mit aktiviertem "hires fix".

---

## ⚠️ Einschränkungen

- NSFW-Ergebnisse sind **Hit or Miss**, da das Basismodell teilweise entwaffnet wurde. Typhoon *versucht's*. Wenn's klappt, ist’s super – wenn nicht, merkst du’s sofort.  
- Tag-lastiges Prompting > ausformulierte Sätze  
- Die Anatomie-Fee hat gelegentlich Urlaub (aber wird besser)

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
