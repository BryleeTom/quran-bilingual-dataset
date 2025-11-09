# 📖 Qur’an Bilingual Dataset (Arabic + English + Indonesian)

This dataset contains the **complete 114 Surahs of the Qur’an** with bilingual translations and transliterations in **English** and **Bahasa Indonesia**.

Built automatically from:
- 🇮🇩 [EQuran.id API](https://equran.id/api/v2) → Arabic, Transliteration (ID), Translation (ID)  
- 🇬🇧 [AlQuranCloud API](https://alquran.cloud/api) → Transliteration (EN), Translation (EN, Sahih International)

---

## 📦 Output Structure

```
surah/
├── 001.json
├── 002.json
├── ...
├── 114.json
├── 001/
│   ├── 001_1_7.json
│   └── ...
└── index.json
```

---

### 🧾 `index.json`

A lightweight summary of all surahs — ideal for mobile lazy-loading.

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

Each surah file (`001.json`, etc.) includes:

- Arabic text  
- Transliteration (EN & ID)  
- Translation (EN & ID)

Example:
```json
{
  "surah": 1,
  "name": { "arabic": "الفاتحة", "en": "Al-Fatihah", "id": "Al-Fatihah" },
  "translation": { "en": "The Opening", "id": "Pembukaan" },
  "revelationPlace": "Mekah",
  "total_verse": 7,
  "verses": [
    {
      "ayat": 1,
      "arabic": "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ",
      "transliteration_en": "In the name of Allah, the Entirely Merciful, the Especially Merciful.",
      "transliteration_id": "Bismillāhir-raḥmānir-raḥīm",
      "translation_en": "In the name of Allah, the Entirely Merciful, the Especially Merciful.",
      "translation_id": "Dengan nama Allah Yang Maha Pengasih, Maha Penyayang."
    }
  ]
}
```

---

### 🪶 Attribution

**Data sourced and combined from:**

- [EQuran.id](https://equran.id/api/v2)  
  © Open Source API for Indonesian Qur’an translation  

- [AlQuranCloud.com](https://alquran.cloud/api)  
  © Public API for English Qur’an translation (Sahih International)

Arabic text is based on the **standard Uthmani script**.

---

### ⚖️ License

This dataset is distributed under the **MIT License**.  
Attribution to both EQuran.id and AlQuranCloud is required if redistributed.

See [`LICENSE`](./LICENSE) for details.

