# 📖 Qur’an Bilingual Dataset (Arabic + English + Indonesian)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Dataset Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](CHANGELOG.md)

A fully structured **bilingual Qur’an dataset (Arabic • English • Indonesian)**  
designed for use in mobile apps, websites, and research — lightweight, open, and authentic.

Built from:
- 🇮🇩 [EQuran.id API](https://equran.id/api/v2) → Arabic, Transliteration (ID), Translation (ID)  
- 🇬🇧 [AlQuranCloud API](https://alquran.cloud/api) → Transliteration (EN), Translation (EN, Sahih International)

---

## 📦 Dataset Structure

```
surah/
│
├── 001/
│ └── 001_1_7.json
│
├── 002/
│ ├── 002_1_50.json
│ ├── 002_51_100.json
│ ├── 002_101_150.json
│ ├── 002_151_200.json
│ ├── 002_201_250.json
│ └── 002_251_286.json
│
├── 003/
│ ├── 003_1_50.json
│ └── ...
│
└── index.json
```

### 🧾 `index.json`
Provides a lightweight overview of all 114 surahs — ideal for quick listing or lazy loading in apps.

```json
{
  "1": {
    "surah": 1,
    "folder": "001",
    "chunks": [
      {
        "start": 1,
        "end": 7,
        "file": "001_1_7.json"
      }
    ],
    "name_en": "The Opening",
    "name_id": "Al-Fatihah",
    "revelation": "Mekah",
    "total": 7
  },
}
```

### 🪶 Attribution

**Data sourced and combined from:**
- [EQuran.id](https://equran.id/api/v2) — © Open Source API for Indonesian Qur’an translation  
- [AlQuranCloud.com](https://alquran.cloud/api) — © Public API for English Qur’an translation (Sahih International)

Arabic text is based on the **standard Uthmani script**.

---

### ⚖️ License

This dataset is distributed under the **MIT License**.  
Attribution to both EQuran.id and AlQuranCloud is required if redistributed.

See [`LICENSE`](./LICENSE) for details.
