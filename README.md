# Awara Haji — Links

پەڕەی لینکەکانی ئاوارە حاجی (@awarahaji) — وەک Linktree، بە HTML و CSS و JavaScript-ی سادە دروستکراوە. هیچ build یان framework-ێکی پێویست نییە.

A simple, static link-in-bio page for Awara Haji, built with plain HTML/CSS/JS.

## پێکهاتە / Structure

```
index.html          ← پەڕەکە و هەموو لینکەکان
style.css           ← دیزاین
script.js           ← دوگمەی هاوبەشکردن (share / copy link)
assets/
  background.jpg    ← وێنەی گوڵەکە (باکگراوند)
  avatar.jpg        ← وێنەی پرۆفایل
  thumbs/           ← وێنە بچووکەکانی ناو لینکەکان
```

## گۆڕینی لینکێک

لە `index.html` هەر لینکێک بەم شێوەیەیە — تەنها `href` و `data-url` بگۆڕە:

```html
<a class="link" href="https://t.me/Awarahaji" ...>
...
<button class="more" ... data-url="https://t.me/Awarahaji" ...>
```

## 1. پووشکردن بۆ GitHub

```bash
cd ~/Downloads/awara_haji_portfolio
git init
git add .
git commit -m "Awara Haji link page"
git branch -M main
git remote add origin https://github.com/<USERNAME>/awara-haji.git
git push -u origin main
```

(سەرەتا لە github.com ڕیپۆیەکی نوێی **Public** بە ناوی `awara-haji` دروست بکە، بەبێ README.)

## 2. بڵاوکردنەوە لە Vercel

1. بچۆ بۆ vercel.com ← **Add New → Project**
2. ڕیپۆی `awara-haji` هەڵبژێرە ← **Import**
3. Framework Preset: **Other** — هیچ شتێکی تر مەگۆڕە ← **Deploy**

دوای چەند چرکەیەک لینکێکی وەک `https://awara-haji.vercel.app` وەردەگریت.
هەر جارێک `git push` بکەیت، Vercel خۆکارانە نوێی دەکاتەوە.

## 3. دوای وەرگرتنی لینکی Vercel

- لە `index.html` ئەم دێڕە بگۆڕە بۆ لینکی تەواو، بۆ ئەوەی وێنەکە لە واتسئەپ/تێلێگرام دەربکەوێت:
  ```html
  <meta property="og:image" content="https://awara-haji.vercel.app/assets/avatar.jpg">
  ```
- **QR کۆد:** QR-ی ستاتیک (static) ڕاستەوخۆ لینکەکە لەخۆ دەگرێت، بۆیە هەتاهەتاییە و بەسەرناچێت — بە مەرجێک لینکی Vercel-ەکە نەگۆڕێت. لە خزمەتگوزارییە «dynamic»-ەکان دووربکەوەرەوە، چونکە زۆربەیان دوای ماوەیەک دەوەستن یان پارە داوا دەکەن.
