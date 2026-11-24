# Unique Gadget Collection (UGC) — Android Studio Project

এই প্রজেক্টটি আপনার দেওয়া সর্বশেষ UGC HTML অ্যাপকে Android WebView অ্যাপের মধ্যে চালানোর জন্য তৈরি। কমলা-ক্রিম 3D UI, এমবেডেড UGC লোগো, পণ্য/স্টক, বিক্রি/মেমো, কাস্টমার ফোন-ঠিকানা, কাস্টমার বকেয়া, ব্যাকআপ/রিস্টোর UI এবং 58mm/80mm/A4 কাগজের সেটিং মূল HTML থেকে রাখা হয়েছে।

## Android Studio দিয়ে চালানো
1. কম্পিউটারে Android Studio (SDK 35 সহ) ইনস্টল করুন।
2. Android Studio → Open → এই ফোল্ডার `UGC_Android_Studio_Project` নির্বাচন করুন।
3. Gradle Sync শেষ হলে Build → Build APK(s) নির্বাচন করুন।
4. APK তৈরি হলে Android Studio-এর Build output থেকে APK নিন এবং নিজের ফোনে ইনস্টল করুন।

## Bluetooth প্রিন্টার
- ফোনের Settings → Bluetooth থেকে প্রিন্টার Pair করুন।
- অ্যাপের Printer → Connect Printer থেকে Pair করা ডিভাইস নির্বাচন করুন।
- Native SPP/ESC-POS সংযোগের প্রাথমিক কোড যুক্ত আছে। প্রিন্টারের মডেল না জানা পর্যন্ত সব প্রিন্টারে সামঞ্জস্য নিশ্চিত করা যায় না।
- বাংলা অক্ষর প্রিন্ট হওয়া নির্ভর করবে প্রিন্টারের firmware/code page-এর ওপর। কিছু মডেলে বাংলা ঠিকভাবে নাও আসতে পারে।
- A4 প্রিন্টের জন্য Android system print/PDF পথ আলাদা করে সম্পূর্ণ করতে হবে; এই সংস্করণে 58/80mm Bluetooth পথের প্রাথমিক সংযোগ আছে।

## গুরুত্বপূর্ণ অসম্পূর্ণ বিষয়
- এই পরিবেশে Android SDK/Gradle build tool নেই, তাই এখানে APK compile ও বাস্তব ফোনে পরীক্ষা করা সম্ভব হয়নি। এটি Android Studio source project, তৈরি APK নয়।
- Google Drive sign-in/OAuth ও Drive backup এখনো সংযুক্ত করা হয়নি।
- HTML-এর Backup/Restore অংশ JSON ফাইলের UI হিসেবে আছে; Android file picker এবং automatic daily backup workflow চূড়ান্ত করতে হবে।
- Login screen-এর বর্তমান HTML আচরণকে production-grade secure authentication হিসেবে ধরা যাবে না।

কোনো বাস্তব দোকানের ডেটা ব্যবহারের আগে test data দিয়ে বিক্রি, বকেয়া, restore এবং printer পরীক্ষা করুন।
