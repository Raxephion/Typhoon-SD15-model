# 🌪️ Typhoon (SD1.5)

> **📢 UPDATE: Typhoon V2 ist gelandet!**  
> Jetzt mit korrektem 768px-nativem Training, höherauflösenden LoRAs und weniger anatomischen Fehlgriffen.

Eine persönliche Liebesmüh der chaotischen Art – **Typhoon** ist ein fein abgestimmtes und experimentell trainiertes Stable Diffusion 1.5 Modell, das Charaktertreue, Gesichtsdetails und eine sehr spezifische ästhetische Sensibilität in Einklang bringt. Es wurde trainiert, kaputtgemacht, neu trainiert, zusammengeführt, wieder getrennt, beweint und schließlich in die Wildnis entlassen. Jetzt können Sie es genießen.

> _Hinweis: Dies ist die SD1.5-Version. Die gleiche Seele, leicht unterschiedliche Temperamente über verschiedene Versionen hinweg._

---

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Raxephion/Typhoon--SD15--model-181717?logo=github)](https://github.com/Raxephion/Typhoon-SD15-model)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-Raxephion/Typhoon--SD1.5--V1/V2-orange?logo=huggingface)](https://huggingface.co/Raxephion)
![HF Downloads](https://img.shields.io/badge/Downloads-100%2B-orange?logo=huggingface)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

---

## 🧪 Live Integration

Möchten Sie Typhoon in Aktion mit einer vollständig angepassten WebUI sehen?

Schauen Sie sich **CipherCore-SD-1.5-WebUI** an – eine saubere, schnelle Oberfläche, die um Typhoon als Standardmodell herum aufgebaut ist:

👉 [Raxephion/CipherCore-SD-1.5-WebUI](https://github.com/Raxephion/CipherCore-SD-1.5-WebUI)

Dieses Repo beinhaltet:
- Eingebaute Typhoon-Unterstützung (alle Versionen)
- Optimierte SD1.5-Workflows
- Saubere UI mit minimalem Overhead
- Out-of-the-Box-Einstellungen, die auf das Modell zugeschnitten sind
- Optimiert für CPU
- Kostenlos für den persönlichen Offline- und lokalen Gebrauch

---

## 🧠 Über

Typhoon fing einfach an – bis es das nicht mehr war. Nach mehreren gescheiterten Versuchen (3 von 4 Trainingsläufen, um genau zu sein) und dem viel zu langen Mieten von GPUs entstand schließlich ein Modell, das sich in Porträt- und stilistischen Renderings bemerkenswert gut behauptet.

Es wurde mit einer Mischung aus Folgendem trainiert:
- Vollständiges Fine-Tuning des Checkpoints in der ersten Phase
- LoRA-Training speziell für jedes ästhetische Ziel
- Zusammenführen dieser LoRAs mit... Geduld, Mathematik und Koffein

Um dieses schöne Durcheinander zu verstehen, habe ich auch zwei Tools entwickelt, um die Zusammenführungsqualität zu analysieren:

- [LoRA Strength Analyzer](https://github.com/Raxephion/loRA-Strength-Analyser)
- [LoRA Epoch Analyzer](https://github.com/Raxephion/loRA-Epoch-Analyser)

Sie sind in der Beta-Phase. Das bedeutet, dass Mathematik passiert, aber manchmal seltsam.

---

## 📦 Typhoon-Versionen

### 🌪️ Typhoon V1

- Trainiert auf 512x512 Ausschnitten (Bedauern lebt hier)
- Ausgewogene, verträumte Ästhetik mit starker Gesichtstreue
- Zusammengeführt mit mehreren LoRAs, die für Porträtmalerei und Detailgenauigkeit entwickelt wurden
- Funktioniert überraschend gut über Sampler und CFGs hinweg
- Immer noch großartig für Tag-lastiges Prompting

### 🌪️ Typhoon V2 (SD1.5, 768px Edition)

> 📸 Gleicher Seed. Gleiche Einstellungen. Spürbar schärfer.

Typhoon V2 ist eine vollständige Aktualisierung:
- ✅ **768px-natives** Training (endlich!)
- ✅ Das gesamte Dataset wurde neu verarbeitet, hochskaliert und besser getaggt
- ✅ Sauberere Anatomie, Gesichtssymmetrie und Lichthandhabung
- ✅ Zusammengeführt mit neuen, hochauflösenden LoRAs, die von Grund auf neu trainiert wurden
- ✅ Zuverlässiger mit Konsistenz + stilisierter Wiedergabetreue
- ✅ Immer noch Tag-freundlich – der gleiche Prompting-Stil gilt

Es behält die Seele von V1 – aber mit weniger Eigenheiten, stärkerer Detailwiedergabe und viel besserer High-Res-Handhabung. Sie können es in Ihre aktuellen Workflows einfügen und erwarten, dass es einfach... besser funktioniert.

V2 ist jetzt der **empfohlene Standard**.

---

## 📐 Empfohlene Einstellungen

### V1 Standardeinstellungen
- **Auflösung:** 512x768 (oder 576x768 für ein etwas breiteres Gefühl)
- **CFG-Skala:** 7 (experimentieren Sie mit 0,3–0,8 für eine weichere Ausgabe)
- **Sampler:** DPM++ 2M (Karras), Euler oder Euler a
- **Hires Fix:**
  - Denoising: 0,7
  - Upscale: 2x (Latent)
  - CFG: 7

> Kein aDetailer oder Face-Fix erforderlich. Das Modell verarbeitet Gesichtsdetails gut.

### V2-Anpassungen (werden in `settings.md` fertiggestellt)
- Gleiche Sampler und CFG funktionieren gut
- Die Rauschunterdrückung mit Hires-Fix kann für die beste Kantenerhaltung auf **0,5–0,6** reduziert werden
- Die native 768px-Eingabe ermöglicht bessere Seitenverhältnisse – 768x1152 oder ähnlich

---

## ✨ Prompting-Tipps

Beide Versionen von Typhoon reagieren am besten auf **Tag-ähnliche Prompts** anstelle von natürlicher Sprache. Die Datensätze wurden stark in diesem Stil beschriftet, halten Sie sich also für beste Ergebnisse an saubere, prägnante Tags.

Beispiele:
- `Meisterwerk, 1Mädchen, Solo, detaillierte Augen, weiche Beleuchtung, im Freien`
- `Porträt, Nahaufnahme, geringe Schärfentiefe, 4k, fotorealistisch`

---

## 📷 Beispielbilder

Die Beispielbilder unten verwenden den beschriebenen Hires-Fix.  
**Keine LoRAs** angewendet – was Sie sehen, ist das, was das Modell standardmäßig ausgibt.

<table> <tr> <td><img src="./images/00003.png" width="160"/></td> <td><img src="./images/00006.png" width="160"/></td> <td><img src="./images/00008.png" width="160"/></td> <td><img src="./images/00015.png" width="160"/></td> <td><img src="./images/00020.png" width="160"/></td> </tr> <tr> <td><img src="./images/00024.png" width="160"/></td> <td><img src="./images/00031.png" width="160"/></td> <td><img src="./images/00033.png" width="160"/></td> <td><img src="./images/00034.png" width="160"/></td> <td><img src="./images/00035.png" width="160"/></td> </tr> </table>

---

## ⚠️ Einschränkungen

- NSFW-Ergebnisse sind **Glückssache** – teilweise aufgrund des kastrierten Basismodells. V2 schneidet hier besser ab, aber keine Versprechungen.
- Tag-Style-Prompting funktioniert am besten. Prosaprompts können zu Abweichungen führen.
- Die Anatomie ist nicht perfekt. Aber es wird besser. Die Fee besucht jetzt öfter.

---

## 🚫 Nutzungsbeschränkungen

Dieses Modell wird unter einer modifizierten CreativeML Open RAIL-M-Lizenz bereitgestellt:

- ✅ Persönliche, private Nutzung ist erlaubt und erwünscht.
- ❌ **Führen Sie dieses Modell nicht** mit anderen Checkpoints oder LoRAs **zusammen** – Sie werden die Ästhetik zerstören.
- ❌ **Laden Sie es nicht** auf öffentliche Generierungsseiten oder Bots **hoch**.

Die langweiligen juristischen Details finden Sie in der [LICENSE](./LICENSE)-Datei.

---

## 📍 Namensnennung

- Basis: Stable Diffusion 1.5 (`v1-5-pruned-emaonly`)
- VAE: [stabilityai/sd-vae-ft-ema](https://huggingface.co/stabilityai/sd-vae-ft-ema)
- LoRA-Analysatoren: [Raxephion Tools](https://github.com/Raxephion)
- Diffusers Repo V1: [Raxephion/Typhoon-SD1.5-V1](https://huggingface.co/Raxephion/Typhoon-SD1.5-V1)
- Diffusers Repo V1: [Raxephion/Typhoon-SD1.5-V2](https://huggingface.co/Raxephion/Typhoon-SD15-V2)

---

### 🌩️ Genießen Sie den Sturm.
