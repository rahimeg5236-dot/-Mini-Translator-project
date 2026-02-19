# Mini-Translator-project 
# 🌍 Mini Translator AI 🤖
<div align="center">
    


<!-- Badges Section -->
[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://www.python.org)
[![License](https://img.shields.io/badge/License-License-green?logo=License)](https://opensource.org)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen)](https://github.com)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn)](https://scikit-learn.org)
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-blue?logo=kaggle)](https://www.kaggle.com)

</div>
> **Mini Translator** هو أداة ذكية وخفيفة الوزن مصممة لترجمة النصوص فورياً بين أكثر من 100 لغة، مع دعم كامل لمعالجة البيانات الضخمة وتنسيقات **Kaggle** المخصصة لمشاريع الـ **ML**.

### ✨ Features
*   🚀 **High Performance:** ترجمة سريعة جداً باستخدام `googletrans`.
*   🧠 **Auto-Detection:** التعرف التلقائي على اللغة المصدر دون تدخل.
*   📊 **Scalable:** مهيأ للتعامل مع نصوص ضخمة (NLP Ready).

### 🛠️ Implementation
قم بتثبيت المكتبة أولاً:
```bash
pip install googletrans==4.0.0-rc1
from googletrans import Translator

def translate(text, dest='ar'):
    client = Translator()
    result = client.translate(text, dest=dest)
    return f"[{result.src} -> {result.dest}]: {result.text}"

print(translate("Innovation distinguishes between a leader and a follower."))from googletrans import Translator
import sys

# إعداد كود اللغة الافتراضي (يمكنك تغييره من هنا)
TARGET_LANGUAGE = 'ar'

def start_translator():
    """
    الدالة الأساسية لتشغيل المترجم الذكي
    """
    # تهيئة كائن المترجم
    client = Translator()
    
    print("\n" + "═"*50)
    print(" 🌍 Mini Translator AI - محرك الترجمة الذكي")
    print("═"*50 + "\n")
    
    # النص المراد ترجمته (يمكنك تغييره أو جعله مدخلاً من المستخدم)
    sample_text = "Innovation distinguishes between a leader and a follower."
    
    print(f"📡 جاري معالجة النص: '{sample_text}'")
    
    try:
        # تنفيذ عملية الترجمة مع الكشف التلقائي عن اللغة
        result = client.translate(sample_text, dest=TARGET_LANGUAGE)
        
        # عرض النتائج بشكل احترافي
        print("\n✅ تم التحويل بنجاح:")
        print(f"   [ المصدر ] ({result.src.upper()}): {sample_text}")
        print(f"   [ الترجمة ] ({result.dest.upper()}): {result.text}")
        
    except Exception as e:
        print(f"\n❌ حدث خطأ أثناء الاتصال بالخادم!")
        print(f"💬 تفاصيل الخطأ: {str(e)}")
        print("💡 نصيحة: تأكد من تثبيت مكتبة googletrans==4.0.0-rc1 ومن اتصالك بالإنترنت.")

if __name__ == "__main__":
    start_translator()
