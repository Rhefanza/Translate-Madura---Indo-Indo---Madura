# Translate-Madura---Indo or Indo---Madura
regional language translation machine
# 🇮🇩➡️🟤 Madura → Indonesia Translation (Fine-tuning Cendol mT5) ✨

Proyek ini melakukan **fine-tuning** model **`indonlp/cendol-mt5-small-inst`** untuk tugas **Machine Translation** dari **Bahasa Madura ke Bahasa Indonesia**, menggunakan dataset **NusaX-MT** (CSV dari GitHub). Evaluasi utama memakai **sacreBLEU** 📈.

---

## 🎯 Tujuan
- Membuat model terjemahan **Madurese → Indonesian**
- Memanfaatkan model instruksi berbasis **mT5 (Cendol)**
- Mengukur performa dengan **BLEU score**

---

## 🧠 Ringkasan
- **Task**: Machine Translation (🟤 Madura → 🇮🇩 Indonesia)
- **Base model**: `indonlp/cendol-mt5-small-inst`
- **Dataset**: NusaX-MT (CSV: train/valid/test) 📚
- **Metric**: sacreBLEU ✅
- **Output**: folder model hasil fine-tuning (mis. `mad2ind_translation_model/`) 💾

---

## 📦 Dataset
Notebook memuat NusaX-MT dari CSV GitHub:

```python
URLS = {
  "train": "https://raw.githubusercontent.com/IndoNLP/nusax/main/datasets/mt/train.csv",
  "validation": "https://raw.githubusercontent.com/IndoNLP/nusax/main/datasets/mt/valid.csv",
  "test": "https://raw.githubusercontent.com/IndoNLP/nusax/main/datasets/mt/test.csv",
}
SRC_COL, TGT_COL = "indonesian", "madurese"
