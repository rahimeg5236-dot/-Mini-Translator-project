# Mini-Translator-project

# 🌍 Mini Translator AI 🤖

<p align="center">
  <img src="https://capsule-render.vercel.app" />
</p>

<p align="center">
[![Python](https://img.shields.io)](https://www.python.org)
[![Scikit-Learn](https://img.shields.io)](https://scikit-learn.org)
[![Kaggle](https://img.shields.io)](https://www.kaggle.com)
</p>

---

### 📖 Overview
هذا المشروع ليس مجرد مترجم، بل هو أداة ذكية تعتمد على **Natural Language Processing (NLP)** لترجمة النصوص بدقة عالية مع التعرف التلقائي على اللغة. تم تصميمه ليكون خفيفاً وسريعاً جداً.

### 🚀 Features
- 🧠 **Smart Detection:** اكتشاف تلقائي للغة المصدر.
- ⚡ **High Speed:** استجابة فورية بفضل تكامل API متطور.
- 📊 **Dataset Ready:** الكود مهيأ للتعامل مع بيانات ضخمة (Kaggle Ready).
- 🎨 **Elegant Interface:** واجهة Terminal ملونة وسهلة الاستخدام.

### 🛠️ Installation
للحصول على أفضل أداء، تأكد من تثبيت المكتبات المطلوبة:
```bash
pip install googletrans==4.0.0-rc1 scikit-learn pandas
# كود المترجم الذكي باختصار
from googletrans import Translator

def translate_smart(text, target='ar'):
    ts = Translator()
    return ts.translate(text, dest=target).text

print(f"Result: {translate_smart('Hello World', 'ar')}")
---

### 2. الكود البرنس (mini_translator_pro.py) 🚀
هذا الكود "أنظف" وأكثر تنظيماً، ويستخدم لمسات جمالية في الـ Terminal:

```python
import sys
from googletrans import Translator, LANGUAGES

def main():
    # تصميم بسيط للترحيب
    print("\033[95m" + "="*30)
    print("🌍 MINI TRANSLATOR PRO 🌍")
    print("="*30 + "\033[0m")

    translator = Translator()

    try:
        text = input("📝 Enter Text: ")
        if not text: return
        
        target = input("🎯 Target Language (default 'ar'): ") or 'ar'
        
        # عملية الترجمة
        print("\033[94m" + "⏳ Translating..." + "\033[0m")
        translation = translator.translate(text, dest=target)

        # النتيجة بشكل مبهر
        print("\n" + "✅" + "-"*20)
        print(f"🔹 From ({translation.src.upper()}): {text}")
        print(f"🔸 To   ({translation.dest.upper()}): {translation.text}")
        print("-"*22)

    except Exception as e:
        print(f"\033[91m❌ Error: {e}\033[0m")

if __name__ == "__main__":
    main()
