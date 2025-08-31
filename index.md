---
title: Tantanto Company homepage
description: Tantanto Company（たんたんとカンパニー）のホームページ。スマホアプリなどを作っています。
---

<div style="text-align:right; margin:1em 0;">
  <button id="btn-ja" class="active">日本語</button>
  <button id="btn-en">English</button>
</div>

<section id="lang-ja" class="lang-section active" markdown="1">

# たんたんとカンパニー homepage
スマートフォンのアプリをつくったりしています。

---

## なでくまCombo! 🧸
くまのぬいぐるみを「なでて」あそぼう♪  
『なでくまCombo!』は、かわいくてたのしい ぬいぐるみカジュアルゲーム！

<p>
  <a href="https://apps.apple.com/us/app/pat-the-bear/id6747101851">
    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
         alt="Download on the App Store"
         class="store-badge">
  </a>
  &nbsp;
  <a href="https://play.google.com/store/apps/details?id=com.toto.NadekumaCombo">
    <img src="https://play.google.com/intl/ja/badges/static/images/badges/ja_badge_web_generic.png"
         alt="Google Play で手に入れよう"
         class="store-badge">
  </a>
</p>

- [プライバシーポリシー](./nadekuma_policy.html)

---

## こえとろん 🎙️
声を録音して「おばけ」「ロボット」などに変身できる、楽しいボイスエフェクトアプリ！

- [プライバシーポリシー](./VoiceRecEffect/KOETRON_policy.html)  
- [利用規約](./VoiceRecEffect/terms.html)

---

## お問い合わせ
Mail: sck54141+githubpages@gmail.com

</section>

<section id="lang-en" class="lang-section" markdown="1">

# Tantanto Company homepage
We create smartphone apps and games.

---

## Pat the Bear! 🧸
Let’s play by “petting” the teddy bears!  
**Pat the Bear!** is a cute and fun casual game with adorable stuffed animals.

<p>
  <a href="https://apps.apple.com/us/app/pat-the-bear/id6747101851">
    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
         alt="Download on the App Store"
         class="store-badge">
  </a>
  &nbsp;
  <a href="https://play.google.com/store/apps/details?id=com.toto.NadekumaCombo">
    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"
         alt="Get it on Google Play"
         class="store-badge">
  </a>
</p>

- [Privacy Policy](./nadekuma_policy.html)

---

## Koetron 🎙️
Record your voice and transform it instantly with fun effects like “Ghost” or “Robot”!

- [Privacy Policy](./VoiceRecEffect/KOETRON_policy.html)  
- [Terms of Service](./VoiceRecEffect/terms.html)

---

## Contact
Mail: sck54141+githubpages@gmail.com

</section>

<script>
const btnJa = document.getElementById('btn-ja');
const btnEn = document.getElementById('btn-en');
const secJa = document.getElementById('lang-ja');
const secEn = document.getElementById('lang-en');

function applyLang(lang) {
  const isJa = lang === 'ja';
  secJa.classList.toggle('active', isJa);
  secEn.classList.toggle('active', !isJa);
  btnJa.classList.toggle('active', isJa);
  btnEn.classList.toggle('active', !isJa);
  document.documentElement.setAttribute('lang', isJa ? 'ja' : 'en');
  try { localStorage.setItem('siteLang', lang); } catch(e) {}
}

btnJa.addEventListener('click', () => applyLang('ja'));
btnEn.addEventListener('click', () => applyLang('en'));

(function initLang(){
  try {
    const saved = localStorage.getItem('siteLang');
    if(saved){ return applyLang(saved); }
  } catch(e){}
  const nav = (navigator.language||'ja').toLowerCase();
  applyLang(nav.startsWith('ja') ? 'ja' : 'en');
})();
</script>

<style>
.lang-section{display:none;}
.lang-section.active{display:block;}
button{padding:4px 10px; margin-left:4px;}
button.active{background:#007acc;color:#fff;}
.store-badge{height:56px; vertical-align:middle;}
</style>
