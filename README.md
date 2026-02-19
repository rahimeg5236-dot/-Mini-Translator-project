🌍 Mini Translator AI 🤖

"Bridging Worlds, One Word at a Time."

<div align="center">

Explore Features • Quick Start • Tech Stack • Developer

</div>

📖 Introduction | مقدمة

Mini Translator AI هو مشروع ذكي يجمع بين البساطة والقوة. تم تصميمه ليكون أداة ترجمة فورية (Real-time) قادرة على التعامل مع نصوص ضخمة، مما يجعله مثالياً لمشاريع معالجة اللغات الطبيعية (NLP) ومهام الـ Machine Learning على منصات مثل Kaggle.

🚀 Key Features | المميزات الرئيسية

🧠 Neural Detection: تعرف تلقائي فائق السرعة على اللغة المصدر.

⚡ High Performance: يعتمد على بروتوكولات googletrans المتطورة لضمان أقل وقت استجابة.

🌐 +100 Languages: يدعم الترجمة بين أكثر من 100 لغة عالمية بضغطة زر.

📊 ML-Ready: مهيأ لمعالجة ملفات الـ CSV والبيانات الضخمة (Big Data) بكفاءة عالية.

🛠️ Built With | الأدوات المستخدمة

Python 3.10 - لغة البرمجة الأساسية.

Googletrans (4.0.0-rc1) - محرك الترجمة العصبي.

NLP Techniques - تقنيات معالجة اللغات الطبيعية.

💻 Implementation | الكود البرمجي

أولاً، تأكد من تثبيت الإصدار الصحيح للمكتبة:

pip install googletrans==4.0.0-rc1


ثم استخدم هذا الكود الاحترافي لتشغيل المترجم:

from googletrans import Translator

def translate_smart(text, target_lang='ar'):
    """
    Advanced translation function with auto-detection
    """
    client = Translator()
    try:
        result = client.translate(text, dest=target_lang)
        
        print(f"📡 Status: Success")
        print(f"🌍 Source Language: {result.src.upper()}")
        print(f"🎯 Target Language: {result.dest.upper()}")
        print("-" * 30)
        return result.text
    except Exception as e:
        return f"❌ Error: {str(e)}"

# Example Usage
quote = "Innovation distinguishes between a leader and a follower."
print(f"📝 Original: {quote}")
print(f"✨ Translation: {translate_smart(quote)}")


📈 Scalability for Kaggle | القابلية للتوسع

يمكنك استخدام هذا المشروع داخل Kaggle Notebooks لترجمة الأعمدة النصية في الـ Dataframes بسهولة:

# Quick hack for pandas dataframes
# df['translated_col'] = df['text_col'].apply(lambda x: translate_smart(x))


🤝 Contributing

نرحب بكل المساهمات! إذا كان لديك فكرة لتطوير المشروع أو إضافة ميزة جديدة، لا تتردد في فتح Issue أو إرسال Pull Request.

<div align="center">
<p>Made with ❤️ by a Creative Developer</p>
<a href="https://www.google.com/search?q=https://github.com/your-username">
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Follow-GitHub-181717%3Fstyle%3Dsocial%26logo%3Dgithub" alt="GitHub Follow">
</a>
</div>
