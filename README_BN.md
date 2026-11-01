# ⭐ STAR CHAT — Android Studio Starter

এটি STAR CHAT-এর প্রথম Android Studio MVP starter project। এতে Firebase Phone OTP login, ফোন নম্বর দিয়ে chat খোলা, এবং Firestore real-time text messaging-এর প্রাথমিক কাঠামো আছে।

## ১) Android Studio-তে খোলা
1. ZIP extract করুন।
2. Android Studio → Open → `STAR_CHAT_Android_Studio` folder নির্বাচন করুন।
3. Gradle sync শেষ হতে দিন।

## ২) Firebase যুক্ত করুন (অবশ্যই করতে হবে)
1. https://console.firebase.google.com/ এ নতুন Firebase project তৈরি করুন।
2. Android app যোগ করুন; package name: `com.star.chat`
3. Firebase থেকে `google-services.json` ডাউনলোড করে `app/` folder-এ রাখুন।
4. Firebase Authentication → Sign-in method → Phone চালু করুন।
5. Firestore Database তৈরি করুন।
6. Firebase Console-এ Phone Auth-এর জন্য প্রয়োজনীয় SMS region / test phone settings ঠিক করুন।

## ৩) Firestore Security Rules
শুধু development test-এর জন্য উন্মুক্ত rules ব্যবহার করবেন না। Production-এ authenticated user এবং room participant যাচাই করে rules লিখতে হবে। এই starter project ইচ্ছাকৃতভাবে permissive security rules তৈরি করে না।

## ৪) Build APK
Android Studio → Build → Build Bundle(s) / APK(s) → Build APK(s)।
APK সাধারণত `app/build/outputs/apk/debug/app-debug.apk`-এ তৈরি হবে।

## গুরুত্বপূর্ণ সীমাবদ্ধতা
- এই প্রথম সংস্করণে text chat-এর ভিত্তি তৈরি করা হয়েছে।
- Audio/Video call, push notification, contact sync, image/video upload, group chat, block/report এবং production-grade security পরবর্তী ধাপে যোগ করতে হবে।
- Firebase configuration ছাড়া OTP ও cloud chat কাজ করবে না।
- বাস্তব ব্যবহারকারীর জন্য প্রকাশের আগে Firestore rules, abuse prevention, privacy policy এবং data deletion flow সম্পূর্ণ করুন।
