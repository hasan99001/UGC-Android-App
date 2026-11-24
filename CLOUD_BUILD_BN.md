# UGC APK ক্লাউডে তৈরি

এই ZIP-এ GitHub Actions workflow যোগ করা হয়েছে। GitHub-এ প্রজেক্টের ফাইলগুলো repository-তে আপলোড করে `Actions` ট্যাব থেকে `Build UGC Android APK` চালালে APK তৈরি হবে।

## ফোন দিয়ে করার সংক্ষিপ্ত ধাপ
1. GitHub অ্যাকাউন্টে সাইন ইন করে নতুন private repository তৈরি করুন (যেমন `ugc-android-app`)।
2. ZIP-টি ফোনে extract করুন। GitHub-এর ওয়েবসাইটে repository খুলে `Add file` → `Upload files` দিয়ে `UGC_Android_Studio_Project` ফোল্ডারের ভেতরের সব ফাইল ও `.github` ফোল্ডারসহ আপলোড করুন। ফোল্ডার/পাথ ঠিক রেখে আপলোড নিশ্চিত করুন।
3. Commit changes দিন। এরপর repository-র `Actions` ট্যাবে `Build UGC Android APK` workflow বেছে `Run workflow` চাপুন।
4. Build সফল হলে workflow run খুলে `Artifacts` থেকে `UGC-debug-APK` ডাউনলোড করুন। ZIP extract করে `app-debug.apk` ইনস্টল করুন। প্রথমবার Android-এ unknown apps থেকে install অনুমতি চাইতে পারে।

## নোট
- এটি debug APK; Play Store release/signing নয়। নিজের ফোনে পরীক্ষার জন্য।
- workflow-টি compile চালাবে, কিন্তু APK-র বাস্তব ব্যবহার, Bluetooth printer, A4 print, Google Drive backup, automatic daily backup, নিরাপদ লগইন—এসব আলাদা করে পরীক্ষা/সম্পূর্ণ করতে হবে।
- GitHub-এ repository private রাখুন, কারণ এতে দোকানের অ্যাপের source code রয়েছে। কোনো বাস্তব customer data repository-তে আপলোড করবেন না।
