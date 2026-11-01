NOVA v8 — GitHub Pages দিয়ে ফ্রিতে মোবাইলে ইনস্টল
====================================================

গুরুত্বপূর্ণ: ZIP ফাইলটা GitHub-এ আপলোড করবেন না! আগে Extract করুন,
তারপর ভেতরের সব ফাইল (ফোল্ডার নয়) আপলোড করুন। index.html অবশ্যই
রিপোজিটরির সবার উপরের লেভেলে থাকবে।

আপলোড করার ফাইল (সবগুলো):
  index.html, sw.js, manifest.webmanifest, hero.webp, favicon.png,
  apple-touch-icon.png, icon-192.png, icon-512.png, icon-maskable-512.png, .nojekyll

ধাপ ১: github.com > New repository > নাম (যেমন nova) > Public > Create
ধাপ ২: "uploading an existing file" > সব ফাইল ড্র্যাগ > Commit changes
ধাপ ৩: Settings > Pages > Source: Deploy from a branch > main / (root) > Save
ধাপ ৪: ১-২ মিনিট পর লিংক: https://আপনার-নাম.github.io/nova/
ধাপ ৫: ফোনের Chrome-এ লিংক খুলুন > উপরের নীল/সবুজ Install (ডাউনলোড তীর) বাটন চাপুন (বা Storage > Install App)

নতুন আইকন দেখতে (গুরুত্বপূর্ণ):
  ফোনে আগের NOVA অ্যাপ থাকলে সেটা Uninstall করুন, Chrome-এর Site settings থেকে
  Clear & reset করুন, তারপর নতুন করে Install করুন। না হলে পুরনো আইকন থেকে যেতে পারে।

নতুন যা আছে:
  - Watching: Release Day ট্যাব (Daily/Sat/Sun/...)। Sat চাপলে শুধু Saturday-র anime আসবে।
    আজকের দিনের ট্যাবে নীল ডট থাকে।
  - Library: যেকোনো anime-র ছবি বা নামে ট্যাপ করুন > Season/Episode সংখ্যা সেট করুন >
    এপিসোডে ভিডিও যোগ করুন, দেখুন, Watched মার্ক করুন। পরে ভেতর থেকেই Seasons/EP/Day বদলানো যায়।
  - Storage: উপরে ডান কোণার ছোট ডাটাবেস আইকন চাপলে শুধু Storage দেখাবে
    (মোট / ব্যবহৃত / বাকি)।
  - ভিডিও প্লেয়ার: ছবি না এলে কারণ দেখায় (যেমন 10-bit বা HEVC) এবং
    "Open in VLC / MX Player" ও "Save to phone" বাটন আছে।

ভিডিওতে "শুধু শব্দ, ছবি নেই" হলে:
  ফোনের Chrome নিচের ফরম্যাট চালাতে পারে না:
    - 10-bit H.264 (Hi10P) — অনেক anime রিলিজে থাকে
    - H.265 / HEVC (বিশেষ করে 10-bit)
    - AC-3 / DTS অডিও
  সমাধান ১: প্লেয়ারে "Open in VLC / MX Player" চাপুন।
  সমাধান ২: ভিডিওটা MP4 (H.264 8-bit + AAC) করে নিন (HandBrake বা ফোনের Video Converter অ্যাপ)।
  একাধিক অডিও ট্র্যাক (Hindi/Japanese) Chrome-এ বদলানো যায় না; সেক্ষেত্রে VLC / MX Player ব্যবহার করুন।

ভিডিও ফোনের ব্রাউজার স্টোরেজে থাকে; ব্রাউজার ডেটা মুছলে চলে যাবে।
Export (JSON) ব্যাকআপে ভিডিও থাকে না।


NOVA v10 — Video playback and performance update
- Fixed mobile playback startup: the player now starts loading and requests playback immediately from the Play button action, before slower codec inspection.
- Improved playback error messages for unsupported formats/codecs.
- Added a low-power rendering mode for selected lower-memory/mobile devices and reduced-motion accessibility support.
- MP4/H.264 + AAC is the broadest browser-compatible format. MKV/AVI/MOV are containers, not guarantees: support depends on the codecs inside each file and on the device/browser.
- For unsupported codecs, use the built-in Share / Save options with a compatible external player such as VLC. No browser-only web app can guarantee playback of every codec without a bundled transcoder or native player.
