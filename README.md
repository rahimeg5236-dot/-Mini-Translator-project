# Mini-Translator-project

# 🌍 Mini Translator AI 🤖

# اسم المشروع الخاص بك

<!-- Badges Section -->
[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://www.python.org)
[![License](https://img.shields.io)](https://opensource.org)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen)](https://github.com)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn)](https://scikit-learn.org)
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-blue?logo=kaggle)](https://www.kaggle.com)

> **Mini Translator** هو أداة ذكية وخفيفة الوزن مصممة لترجمة النصوص فورياً بين أكثر من 100 لغة، مع دعم كامل لمعالجة البيانات الضخمة وتنسيقات **Kaggle** المخصصة لمشاريع الـ **ML**.

### ✨ Features
*   🚀 **High Performance:** ترجمة سريعة جداً باستخدام `googletrans`.
*   🧠 **Auto-Detection:** التعرف التلقائي على اللغة المصدر دون تدخل.
*   📊 **Scalable:** مهيأ للتعامل مع نصوص ضخمة (NLP Ready).

### 🛠️ Implementation
قم بتثبيت المكتبة أولاً:
```bash
pip install googletrans==4.0.0-rc1
from googletrans import Translator

def translate(text, dest='ar'):
    client = Translator()
    result = client.translate(text, dest=dest)
    return f"[{result.src} -> {result.dest}]: {result.text}"

print(translate("Innovation distinguishes between a leader and a follower."))
