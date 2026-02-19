from googletrans import Translator
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
