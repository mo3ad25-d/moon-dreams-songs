<!-- ⚠️ نسخة منظفة - المفاتيح الفعلية محفوظة محلياً فقط -->

# 🌙 Moon Dreams — Project Context (Full Backup)

آخر تحديث: 27 سبتمبر 2026 - 23:35

## 📌 هوية المشروع
- **الاسم:** Moon Dreams (أحلام القمر)
- **النوع:** تطبيق أطفال تعليمي تفاعلي
- **المحرك:** Godot 4.7.2
- **المسار:** /storage/emulated/0/Documents/lumi-kids
- **المالك:** معاذ
- **حروف الأيقونة:** DM

## 🔑 المفاتيح

### Firebase
- Project ID: moon-dreams-53536
- Project Number: 983504655343
- App ID: 1:983504655343:android:8d3ce51c3385de37905c1a
- Package: com.moondreams.kids
- Storage: moon-dreams-53536.firebasestorage.app
- Admin UID: ADMIN_UID_HERE
- Admin Email: mo3ad.sonyz2@gmail.com

### خارجية
- Gemini Key: GEMINI_KEY_HERE
- Gemini Model: gemini-3.8-flash (via /v1/interactions)
- Hakim Key: HAKIM_KEY_HERE
- Hakim Model: hakim-fast-v1
- Hakim Voices:
  - layla-msa = cmok1nvog000d10arbqznfyxz (عربي فصحى)
  - sarah = cmok1nvnw000710arovur4fzz (إنجليزي - حالي)
  - nour-levantine = cmok1nvqt000l10arvje5twy7 (شامي)
  - reem-khaleeji = cmok1nvqg000h10arx9tcawir (خليجي)
- GitHub: user=mo3ad25-d repo=moon-dreams-songs
- GitHub Token: GITHUB_TOKEN_HERE

## 🏗️ البنية

core/scripts/:
- main.gd (الشاشة الرئيسية)
- ai_teacher.gd (معطل - فيه مشاكل)
- speak_world.gd (قسم النطق - قيد التحسين)
- lumi_songs.gd, lumi_art.gd, lumi_magic.gd
- lumi_settings.gd, lumi_math.gd
- floating_island.gd, avatar_halo.gd
- audio_manager.gd (TTS + queue + generation)
- learning_memory.gd, learning_engine.gd
- ai_content.gd (Cache + AI)
- rewards_manager.gd, video_helper.gd
- language_registry.gd, parent_settings.gd
- lumi_server.py (port 8787)
- firebase/ (config, auth, firestore)
- myworld/ (my_world + player + designer + store + renderer + world_data)
- math/ (6 أقسام)
- games/ (games_world + candy + flappy + match)
- friends/, parent/, settings/

admin_panel/ (Flask port 5000):
- server.py
- templates/songs.html

assets/audio/songs/letters/:
5 ملفات ogv (طم طم، العد 1-10، فواكه، واحد يعني ون، قطار الحروف)

## ✅ الميزات المكتملة

### الأساسيات (من قبل)
1. عالم LUMI الرئيسي
2. الأغاني (مشغل + OGV)
3. المرسم
4. الزر السحري
5. عالم الأرقام
6. قائمة الضبط
7. لوحة الوالدين
8. 9 لغات
9. Edge TTS
10. Firebase (Auth+Firestore+Sync)
11. لوحة تحكم ويب

### عالمي الخاص (مكتمل)
1. توسيع العالم (2.5 شاشة + كاميرا + parallax)
2. 7 حيوانات كاملة الجسم (قطة، كلب، زرافة، أسد، طاووس، فيل، دب)
3. بيت محسّن (سقف، مدخنة، نوافذ، باب، أزهار)
4. نافورة 3 طوابق
5. أشجار (نخلة، صنوبر، شجيرة، عشبة)
6. سماء ديناميكية (120s دورة، شمس، قمر، نجوم، غروب، زر مطر)
7. بركة + قارب + أسماك تسبح

### قسم الألعاب (مكتمل)
1. games_world.gd (قائمة 3 ألعاب)
2. game_candy.gd (6 حلويات، سحب، Combo، خلط)
3. game_flappy.gd (4 مستويات: ⚪🟢🟠😈)
4. game_match.gd (حرف + كلمة، 20 كلمة)

### قسم النطق (قيد التحسين)
- speak_world.gd بتصميم زاهي
- دائرة RMS
- TTS (سارة إنجليزي + ليلى عربي)
- مطابقة صوتية (7 معايير، العتبة 0.50)
- نجح: milk↔مالك, cloud↔كلاود, butterfly↔بترفلاي
- مشاكل: صوت سارة ينطق بعض الكلمات غلط + كلمات قصيرة (eye, bee)

## 🚧 الخطة القادمة

### المرحلة الفورية
1. تجريب أصوات Hakim الإنجليزية الأصلية (ava-en-us, amelia-en-us)
2. تحسين التعرف الصوتي (Whisper API أو Google Speech)
3. اختبار شامل 67 كلمة

### المرحلة الكبيرة
1. قسم الكتابة (لوح بالإصبع، بدون كيبورد)
2. AI Content في كل الأقسام
3. نظام مجاني/مدفوع
4. تحديثات تلقائية (In-App)
5. نشر APK على Google Play

## 🎨 أسلوب العمل
- نافذة 1: أوامر عامة
- نافذة 2: LUMI Server (port 8787)
- Flask Admin (port 5000) عند الحاجة
- أمر-أمرين في كل رد
- اختبار بعد كل خطوة
- بدون شرح طويل

## ⚙️ تفاصيل تقنية
- Portrait 720x1280
- LUMI Server: /chat, /raw_gemini, /tts_hakim, /tts, /health
- AudioManager: queue + generation token
- AIContent: cache في user://ai_cache.cfg
- Firestore Rules: isAdmin() + content + notifications

## 📁 Backup Files
- core/scripts/_backup_failed/ai_teacher.gd.bak
- core/scripts/_backup_failed/speak_world.gd.bak
- core/scripts/audio_manager.gd.bak*
- core/scripts/myworld/my_world.gd.bak*

## 🗣️ تفضيلات المالك
- يحب: النتيجة السريعة، أوامر واحد، بلا تكرار
- يكره: الشرح الطويل، الاستباق
- تطبيق أطفال = ألوان زاهية + متعة + روح

## 📌 آخر موضع توقفنا
قسم النطق (speak_world.gd):
- يعمل: النطق + المطابقة للكلمات المتوسطة والطويلة
- لا يعمل: كلمات قصيرة (eye, bee, dog)
- آخر تعديل: تحويل كل speak_queued(_word, "ar") → "en"

الخطوة التالية:
1. تجريب ava-en-us لصوت إنجليزي أصلي
2. تحسين التعرف الصوتي

## 🚨 للمحادثة القادمة
1. اقرأ هذا الملف
2. اسأل: "هل في تعديلات جديدة؟"
3. ابدأ من speak_world.gd
4. النوافذ: 1=أوامر، 2=lumi_server.py

