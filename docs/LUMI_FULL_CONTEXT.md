# 🌙 Moon Dreams — MASTER CONTEXT v2
# (نسخة كاملة - تحتوي مفاتيح سرية - لا ترفع على GitHub)

آخر تحديث: 28 سبتمبر 2026

═══════════════════════════════════════════════
🚨 تعليمات فورية للمساعد الجديد (اقرأ أولاً)
═══════════════════════════════════════════════

1. لا تخمن أبداً. اقرأ الملفات قبل التعديل.
2. المالك (معاذ) يكره: الاعتذار البارد، الشرح الطويل، الأسئلة الكثيرة.
3. المالك يحب: أوامر تيرمكس مباشرة، نتيجة سريعة، بلا مقدمات.
4. كل أمر يجب أن يكون قابلاً للتنفيذ مباشرة في Termux.
5. لا تحذف ملفات بدون نسخة احتياطية.
6. لا ترفع المفاتيح على GitHub.
7. إذا لم تعرف، اسأل سؤالاً واحداً فقط.

═══════════════════════════════════════════════
1. هوية المشروع
═══════════════════════════════════════════════
- الاسم: Moon Dreams (أحلام القمر)
- النوع: تطبيق أطفال تعليمي تفاعلي
- المحرك: Godot 4.7.2 stable
- المسار: /storage/emulated/0/Documents/lumi-kids
- الواجهة: عربية، عمودية (720x1280)
- المالك: معاذ (mo3ad.sonyz2@gmail.com)
- الجهاز: هاتف أندرويد + Termux (لا كمبيوتر)

═══════════════════════════════════════════════
2. المفاتيح السرية (لا ترفع على GitHub)
═══════════════════════════════════════════════

[Firebase]
Project ID: moon-dreams-53536
Project Number: 983504655343
App ID: 1:983504655343:android:8d3ce51c3385de37905c1a
Package: com.moondreams.kids
Storage: moon-dreams-53536.firebasestorage.app
Admin UID: ADMIN_UID_HERE
Admin Email: mo3ad.sonyz2@gmail.com

[Gemini]
Key: GEMINI_KEY_HERE
Model: gemini-3.8-flash
Endpoint: https://generativelanguage.googleapis.com/v1beta/interactions
Header: x-goog-api-key
Body: {"model":"gemini-3.8-flash","input":"..."}
Note: الموديل القديم gemini-2.0-flash لم يعد متاحاً

[Hakim AI]
Key: HAKIM_KEY_HERE
Endpoint: https://api.tryhakim.ai/v1/audio/speech
Method: POST
Headers: Authorization: Bearer KEY + Content-Type: application/json
Body: {"model":"hakim-fast-v1","voice":"VOICE_ID","input":"نص","response_format":"mp3"}
Model: hakim-fast-v1 (المتاح - 10K حرف/شهر مجاناً)

[GitHub]
User: mo3ad25-d
Repo: moon-dreams-songs
Token: GITHUB_TOKEN_HERE

═══════════════════════════════════════════════
3. أصوات Hakim AI — قائمة كاملة
═══════════════════════════════════════════════
شكل الطلب:
  POST /v1/audio/speech
  {"model":"hakim-fast-v1","voice":"<ID>","input":"text","response_format":"mp3"}

للحصول على القائمة الكاملة: 
  curl -s "https://api.tryhakim.ai/v1/audio/voices" -H "Authorization: Bearer HAKIM_KEY_HERE"

[الأصوات العربية]
اسم                       voice_id
layla-msa                 cmok1nvog000d10arbqznfyxz   ← مستخدم حالياً للعربي
nour-levantine            cmok1nvqt000l10arvje5twy7
reem-khaleeji             cmok1nvqg000h10arx9tcawir
ali-arabic-deep           cmokbc1rs0007vu39x8tcgyty
khalid-msa                cmok1nvqa000f10ar8rpvncj4
nadia-msa-soft            cmokbc1r70001vu39tnmjj9v7
mahmoud-msa-narrative     cmokbc1rd0003vu39gqr7pps1
amir-maghrebi             cmok1nvqz000n10ar5pzc4569
layan-saudi               cmokbc1rj0005vu3915vh4ehn
omar-iraqi                cmok1nvr4000p10arkxbvlnn5
yusuf-egyptian            cmok1nvqn000j10ar8ljluapq

[الأصوات الإنجليزية — للكلمات الإنجليزية]
اسم                       voice_id
sarah                     cmok1nvnw000710arovur4fzz   ← مستخدم حالياً (لكن فيه مشاكل: cup→سوب)
ava-en-us                 cmokbc1to000bvu39y1rb2kes   ← المرشح التالي (American, bright educator)
amelia-en-us              cmok1nvt2000t10arlovgcam6
alex                      cmok1nvnr000510ar3rats3eu
arabella-en-au            cmokbc1wg000pvu39cvoyllhs

[لغات أخرى]
anthony-fr                cmokbc1wm000rvu39gzf7twui
antonio-it                cmokbc1xd000zvu394aofxnz3
anant-ur                  cmokbc2230015vu39q6zas254

═══════════════════════════════════════════════
4. أصوات Edge TTS (fallback)
═══════════════════════════════════════════════
- ar-JO-SanaNeural (الأردنية)
- en-US-AnaNeural (طفلة أمريكية)
- en-GB-MaisieNeural (طفلة بريطانية)
- en-US-AriaNeural
- fr-FR-DeniseNeural
- es-ES-ElviraNeural
- de-DE-KatjaNeural
- tr-TR-EmelNeural
- ja-JP-NanamiNeural
- ko-KR-SunHiNeural
- zh-CN-XiaoxiaoNeural

═══════════════════════════════════════════════
5. بنية المشروع — كل ملف ووظيفته
═══════════════════════════════════════════════

[الشاشة الرئيسية]
main.gd                    الشاشة الرئيسية + navigation
floating_island.gd         الجزيرة + 8 بالونات (تعلّم، أغاني، مرسم، أرقام، سحري، أصدقاء، ألعاب، إعدادات)
avatar_halo.gd             دائرة الأفاتار

[الأقسام المستقلة]
lumi_songs.gd              الأغاني (فيديو OGV + صوت)
lumi_art.gd                المرسم (رسم حر)
lumi_magic.gd              الزر السحري (بطاقات مفاجئة)
lumi_math.gd               عالم الأرقام (قائمة)
lumi_settings.gd           قائمة الضبط
speak_world.gd             قسم النطق (جديد - قيد التحسين)
ai_teacher.gd              المعلم الذكي القديم (معطل - فيه مشاكل)

[قسم عالمي الخاص]
myworld/my_world.gd        العالم الرئيسي (موسّع 2.5 شاشة)
myworld/player_character.gd الشخصية
myworld/character_designer.gd مصمم الشخصية
myworld/virtual_joystick.gd عصا التحكم
myworld/item_store.gd      المخزن (18+ عنصر)
myworld/item_renderer.gd   راسم العناصر (رسم يدوي)
myworld/world_data.gd      حفظ عناصر العالم

[قسم الألعاب]
games/games_world.gd       قائمة الألعاب
games/game_candy.gd        حلوى السقوط (سحب)
games/game_flappy.gd       الطائر الطائر (4 مستويات)
games/game_match.gd        صيد الحروف (وضعان)

[الرياضيات]
math/math_add.gd           الجمع
math/math_sub.gd           الطرح
math/math_mul.gd           الضرب
math/math_div.gd           القسمة
math/math_calc.gd          الآلة الحاسبة
math/math_quiz.gd          الاختبار

[النظام]
audio_manager.gd           TTS + مؤثرات (queue + generation token)
language_registry.gd       9 لغات
learning_memory.gd         ذاكرة التعلم (local)
learning_engine.gd         منطق التعلم
ai_content.gd              طبقة AI + Cache (user://ai_cache.cfg)
rewards_manager.gd         النجوم والمكافآت
video_helper.gd            تحويل الفيديو
parent_settings.gd         إعدادات الوالدين

[Firebase]
firebase/firebase_config.gd    قراءة google-services.json
firebase/firebase_auth.gd      Anonymous + Email + Token refresh
firebase/firestore_manager.gd  مزامنة البيانات

[الأصدقاء والوالدين]
friends/friends_world.gd   AR وهمي
parent/parent_panel.gd     لوحة الوالدين
parent/pin_lock.gd
parent/pin_setup.gd

[خادم LUMI (port 8787)]
lumi_server.py             Gemini + Hakim TTS + Edge TTS

═══════════════════════════════════════════════
6. حالة كل ملف
═══════════════════════════════════════════════

✅ مكتمل ويعمل:
- main.gd, floating_island.gd, avatar_halo.gd
- lumi_songs.gd, lumi_art.gd, lumi_magic.gd, lumi_settings.gd
- lumi_math.gd + كل math/*.gd
- myworld/*.gd (بما فيها التوسيع + الحيوانات + السماء + البركة)
- games/*.gd (3 ألعاب كاملة)
- firebase/*.gd
- audio_manager.gd (يعمل مع queue وgeneration)
- rewards_manager.gd, video_helper.gd, parent_settings.gd
- language_registry.gd
- parent/pin_lock.gd, pin_setup.gd

🚧 قيد التحسين:
- speak_world.gd (قسم النطق) — يعمل جزئياً، بعض الكلمات تفشل
- ai_content.gd (cache) — يعمل لكن يحتاج اختباراً شاملاً

❌ معطل (نسخة احتياطية فقط):
- ai_teacher.gd (المعلم الذكي القديم) — موجود في _backup_failed/
- speak_world.gd.bak (النسخة القديمة)
- audio_manager.gd.bak*
- myworld/my_world.gd.bak*

═══════════════════════════════════════════════
7. تاريخ المشروع (مختصر)
═══════════════════════════════════════════════

المرحلة 1 (قبل هذه المحادثة):
- بناء الأساسيات: 11 ميزة (جزيرة، أغاني، مرسم، رياضيات، ضبط...)
- Firebase Auth + Firestore
- لوحة تحكم Flask

المرحلة 2 (قسم عالمي الخاص):
- توسيع العالم إلى 2.5 شاشة + كاميرا parallax
- 7 حيوانات كاملة الجسم (مرسومة يدوياً بـ _draw)
- بيت محسّن + نافورة 3 طوابق
- أشجار: نخلة، صنوبر، شجيرة، عشبة
- سماء ديناميكية (120s دورة + شمس + قمر + نجوم + مطر)
- بركة + قارب + أسماك تسبح

المرحلة 3 (قسم الألعاب):
- games_world.gd (قائمة)
- game_candy.gd (6 حلويات مرسومة، سحب، Combo)
- game_flappy.gd (4 مستويات ⚪🟢🟠😈)
- game_match.gd (حرف + كلمة)

المرحلة 4 (AI Integration):
- AIContent autoload (cache + Firestore sync)
- /raw_gemini endpoint
- ربط بـ LearningEngine

المرحلة 5 (Hakim AI للصوت):
- استبدال Edge TTS بـ Hakim للجودة
- Cache محلي في ~/.cache/lumi_tts
- /tts_hakim endpoint
- ليلى للعربي، سارة للإنجليزي

المرحلة 6 (قسم النطق - جارية):
- speak_world.gd بتصميم زاهي
- مطابقة صوتية متقدمة (7 معايير)
- نجح: milk، cloud، butterfly، cat
- فشل: eye، bee، dog + كلمات تنطق غلط من سارة

═══════════════════════════════════════════════
8. آخر موضع توقف — بدقة
═══════════════════════════════════════════════

📌 اسم الملف: core/scripts/speak_world.gd
📌 المشكلة الحالية:
   1. صوت سارة ينطق بعض الكلمات الإنجليزية بمخارج عربية غريبة:
      - cup → "سوب" ❌
      - butterfly → نطق غريب ❌
   2. الكلمات القصيرة (eye, bee, dog) تسبب error 7 في التعرف
   3. error 7 متكرر بشكل عام

📌 آخر تعديلات تم تنفيذها:
   - تحويل كل speak_queued(_word, "ar") → speak_queued(_word, "en")
   - إضافة _clean_text لإزالة العلامات الخفية (RTL/LTR)
   - 7 معايير تشابه في _best_similarity
   - العتبة 0.50

📌 الخطوة التالية المخطط لها:
   1. تجريب ava-en-us (cmokbc1to000bvu39y1rb2kes) بدل sarah للإنجليزي
   2. إذا تحسنت، نغيّر في lumi_server.py:
      HAKIM_VOICES["en"] = "cmokbc1to000bvu39y1rb2kes"
   3. اختبار صوت الكلمات: cup, butterfly, eye, bee, dog
   4. إذا استمر error 7 → التفكير في Google Speech API

═══════════════════════════════════════════════
9. خادم LUMI (core/scripts/lumi_server.py)
═══════════════════════════════════════════════
Port: 8787
تشغيل: cd /storage/emulated/0/Documents/lumi-kids/core/scripts && python3 lumi_server.py

Endpoints:
- POST /chat              → Gemini proxy للدردشة
- POST /raw_gemini        → JSON Array (للكلمات)
- POST /tts_hakim         → Hakim TTS (مع cache محلي)
- POST /tts               → Edge TTS fallback
- GET  /health            → {"ok":true,"tts":true,"hakim":true}

Cache: ~/.cache/lumi_tts/*.mp3 (md5 hash للنص+الصوت)

═══════════════════════════════════════════════
10. النوافذ
═══════════════════════════════════════════════
نافذة 1: أوامر عامة (Termux)
نافذة 2: LUMI Server (port 8787) — تُشغّل عادة
نافذة 3 (عند الحاجة): Flask Admin (port 5000)

═══════════════════════════════════════════════
11. القواعد الصارمة للمساعد
═══════════════════════════════════════════════
1. قبل أي تعديل: اقرأ الملف الحالي كاملاً
2. قبل أي تعديل: اعمل نسخة .bak
3. لا تقل "آسف" أكثر من مرة واحدة في الرد
4. لا تشرح أكثر من 5 أسطر
5. لا تسأل أكثر من سؤال واحد في الرد
6. الردود: أمر تيرمكس + نتيجة متوقعة
7. لا تخمن أسماء ملفات أو دوال - اقرأها أولاً
8. إذا فشل أمر، لا تعدله، اسأل عن السبب
9. المفاتيح السرية لا ترفع على GitHub
10. المالك يعمل من هاتف فقط - كل الأوامر يجب أن تعمل في Termux

═══════════════════════════════════════════════
12. الخطة الكبيرة المتبقية
═══════════════════════════════════════════════
□ إكمال قسم النطق (speak_world.gd)
□ بناء قسم الكتابة (write_world.gd) - لوح بالإصبع
□ AI في كل الأقسام (المعلم، الرياضيات، الزر السحري، لعبة الحروف)
□ نظام مجاني/مدفوع (اشتراكات)
□ تحديثات In-App
□ نشر APK على Google Play

═══════════════════════════════════════════════
13. ملفات مرجعية
═══════════════════════════════════════════════
/sdcard/LUMI_MASTER.md             ← هذا الملف (كامل - سري)
/sdcard/LUMI_FULL_CONTEXT.md       ← نسخة أقدم
/sdcard/LUMI_FULL_CONTEXT_clean.md ← نسخة GitHub (بدون مفاتيح)
/sdcard/voice_test/                ← عينات أصوات
/sdcard/LUMI_FULL_DUMP.txt         ← dump ملفات المشروع

═══════════════════════════════════════════════
14. عند بدء محادثة جديدة — الصق هذا:
═══════════════════════════════════════════════

مرحباً، أنا معاذ مالك مشروع Moon Dreams.
ملف السياق الكامل: /sdcard/LUMI_MASTER.md
الرجاء قراءته كاملاً من البداية:
  cat /sdcard/LUMI_MASTER.md
ثم اسألني: "هل هناك تعديلات جديدة؟"
سنكمل من قسم النطق (speak_world.gd).

