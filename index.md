---
title: Tantanto Company homepage
description: Tantanto Company（たんたんとカンパニー）のホームページ。スマホアプリなどを作っています。
---

<div style="text-align:right; margin:1em 0;">
  <button id="btn-ja" class="active">日本語</button>
  <button id="btn-en">English</button>
</div>

<section id="lang-ja" class="lang-section active">

# Tantanto Company homepage
スマートフォンのアプリをつくったりしています。  
*たんたんとカンパニー（Tantanto Company）*

---

## なでくまCombo! 🧸
くまのぬいぐるみを「なでて」あそぼう♪  
『なでくまCombo!』は、かわいくてたのしい ぬいぐるみカジュアルゲーム！  

- [iOS (App Store)](https://apps.apple.com/us/app/pat-the-bear/id6747101851)  
- [Android (Google Play)](https://play.google.com/store/apps/details?id=com.toto.NadekumaCombo)  
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

<section id="lang-en" class="lang-section">

# to-to homepage
We create smartphone apps and games.  
*Tantanto Company*

---

## Pat the Bear! 🧸
Let’s play by “petting” the teddy bears!  
**Pat the Bear!** is a cute and fun casual game with adorable stuffed animals.  

- [iOS (App Store)](https://apps.apple.com/us/app/pat-the-bear/id6747101851)  
- [Android (Google Play)](https://play.google.com/store/apps/details?id=com.toto.NadekumaCombo)  
- [Privacy Policy](./nadekuma_policy.html)

---

## Koetron 🎙️
Record your voice and transform it instantly with fun effects like “Ghost” or “Robot”!  

- [Privacy Policy](./VoiceRecEffect/KOETRON_policy.html)
- [Terms of Service](./VoiceRecEffect/terms/)

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
</style>
