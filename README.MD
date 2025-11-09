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
├── 001.json
├── 002.json
├── ...
├── 114.json
└── index.json
```

### 🧾 `index.json`
Provides a lightweight overview of all 114 surahs — ideal for quick listing or lazy loading in apps.

```json
{
  "1": {
    "surah": 1,
    "file": "001.json",
    "name_en": "The Opening",
    "name_id": "Al-Fatihah",
    "revelation": "Mekah",
    "total": 7
  }
}
```

---

### 🕋 Surah Files (001–114)
Each surah folder contains one or more JSON files split by verse range, e.g.:

surah/
├── 001/
│ ├── 001_1_7.json
├── 002/
│ ├── 002_1_50.json
│ ├── 002_51_100.json
│ └── ...


Each chunk file (e.g. `001/001_1_7.json`) contains:
- Arabic text  
- Transliteration (EN & ID)  
- Translation (EN & ID)

Example — **`001/001_1_7.json`**:
```json
[
  {
    "ayat": 1,
    "arabic": "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ",
    "transliteration_en": "Bismillaahir Rahmaanir Raheem",
    "transliteration_id": "Bismillāhir-raḥmānir-raḥīm",
    "translation_en": "In the name of Allah, the Entirely Merciful, the Especially Merciful.",
    "translation_id": "Dengan nama Allah Yang Maha Pengasih, Maha Penyayang."
  },
  {
    "ayat": 2,
    "arabic": "الْحَمْدُ لِلَّهِ رَبِّ الْعَالَمِينَ",
    "transliteration_en": "Alhamdu lillaahi Rabbil 'aalameen",
    "transliteration_id": "Al-ḥamdu lillāhi rabbil-‘ālamīn(a)",
    "translation_en": "[All] praise is [due] to Allah, Lord of the worlds.",
    "translation_id": "Segala puji bagi Allah, Tuhan semesta alam."
  }
]
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
