---
title: Tantanto Company homepage
description: Tantanto Company（たんたんとカンパニー）のホームページ。スマホアプリなどを作っています。
---

<div style="text-align:right; margin:1em 0;">
  <button id="btn-ja" class="active">日本語</button>
  <button id="btn-en">English</button>
</div>

<section id="lang-ja" class="lang-section active" markdown="1">

# たんたんとカンパニーです
スマートフォンアプリの開発・運営をしています

---

## なでくまCombo! 🧸
くまのぬいぐるみを「なでて」あそぼう♪  
『なでくまCombo!』は、かわいくてたのしい ぬいぐるみカジュアルゲーム！

<p class="store-badges">
  <a class="badge-appstore" href="https://apps.apple.com/us/app/pat-the-bear/id6747101851">
    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
         alt="Download on the App Store">
  </a>
  <a class="badge-googleplay" href="https://play.google.com/store/apps/details?id=com.toto.NadekumaCombo">
    <img src="https://play.google.com/intl/ja/badges/static/images/badges/ja_badge_web_generic.png"
         alt="Google Play で手に入れよう">
  </a>
</p>

- [プライバシーポリシー](./nadekuma_policy.html)

---

## こえとろん 🎙️
声を録音して「おばけ」「ロボット」などに変身できる、楽しいボイスエフェクトアプリ！

<p class="store-badges">
  <a class="badge-appstore" href="https://apps.apple.com/us/app/koetron/id6751819556">
    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
         alt="Download on the App Store">
  </a>
</p>
- [プライバシーポリシー](./VoiceRecEffect/KOETRON_policy.html)  
- [利用規約](./VoiceRecEffect/terms.html)

---

<section class="social-section" aria-label="Social links">
  <h3 class="social-title">Follow</h3>
  <div class="social-row">
    <!-- X -->
    <a class="social-btn social-x"
       href="https://x.com/suisei1975"
       target="_blank" rel="me noopener noreferrer"
       aria-label="Follow on X (@suisei1975)" title="X（@suisei1975）">
      <span class="icon">
        <!-- X logo (SVG) -->
        <svg viewBox="0 0 24 24" aria-hidden="true">
          <path d="M18.9 3H21l-6.7 7.6L22 21h-7l-5-6.8L4.5 21H3l7.2-8.4L2 3h7l4.6 6.3L18.9 3z"/>
        </svg>
      </span>
      <span class="label">
        <strong>X</strong><span class="sub">@suisei1975</span>
      </span>
    </a>

    <!-- Zenn -->
    <a class="social-btn social-zenn"
       href="https://zenn.dev/toto_tantanto"
       target="_blank" rel="me noopener noreferrer"
       aria-label="Read on Zenn (toto_tantanto)" title="Zenn（toto_tantanto）">
      <span class="icon">
        <!-- シンプルZアイコン -->
        <svg viewBox="0 0 24 24" aria-hidden="true">
          <path d="M5 6h14v3H11l8 9H5v-3h8L5 6z"/>
        </svg>
      </span>
      <span class="label">
        <strong>Zenn</strong><span class="sub">toto_tantanto</span>
      </span>
    </a>
  </div>
</section>


---

## お問い合わせ
Mail : sck54141+githubpages@gmail.com

</section>

<section id="lang-en" class="lang-section" markdown="1">

# Tantanto Company
We create smartphone apps and games.

---

## Pat the Bear! 🧸
Let’s play by “petting” the teddy bears!  
**Pat the Bear!** is a cute and fun casual game with adorable stuffed animals.

<p class="store-badges">
  <a class="badge-appstore" href="https://apps.apple.com/us/app/pat-the-bear/id6747101851">
    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
         alt="Download on the App Store">
  </a>
  <a class="badge-googleplay" href="https://play.google.com/store/apps/details?id=com.toto.NadekumaCombo">
    <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"
         alt="Get it on Google Play">
  </a>
</p>

- [Privacy Policy](./nadekuma_policy.html)

---

## Koetron 🎙️
Record your voice and transform it instantly with fun effects like “Ghost” or “Robot”!
<p class="store-badges">
  <a class="badge-appstore" href="https://apps.apple.com/us/app/koetron/id6751819556">
    <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
         alt="Download on the App Store">
  </a>
</p>
- [Privacy Policy](./VoiceRecEffect/KOETRON_policy.html)  
- [Terms of Service](./VoiceRecEffect/terms.html)

---

X : <a href="https://x.com/suisei1975">https://x.com/suisei1975</a><br>
Zenn : <a href="https://zenn.dev/toto_tantanto">https://zenn.dev/toto_tantanto</a>

---

## Contact
Mail : sck54141+githubpages@gmail.com

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
/* ================= Base (既存UI) ================= */
.lang-section{display:none;}
.lang-section.active{display:block;}
button{padding:4px 10px; margin-left:4px; border:0; border-radius:8px; cursor:pointer;}
button.active{background:#007acc;color:#fff;}

/* バッジ共通レイアウト */
.store-badges {
  display: inline-flex;
  gap: 8px;
  align-items: center;
  line-height: 0;
}
.store-badges .badge-appstore { display:inline-flex; height:38px; }
.store-badges .badge-googleplay { display:inline-flex; height:47px; }
.store-badges .badge-appstore img,
.store-badges .badge-googleplay img {
  height: 100% !important;
  width: auto;
  display: block;
}

/* ================= Theme Tokens ================= */
:root{
  --card-bg: #ffffff;
  --card-fg: #111111;
  --muted:   #6b7280;   /* slate-500 */
  --ring:    #60a5fa;   /* blue-400 */

  --x-bg: #111111;  --x-fg: #ffffff;
  --z-bg: #155e75;  --z-fg: #ffffff; /* 青緑系 */
}
@media (prefers-color-scheme: dark){
  :root{
    --card-bg: #111418;
    --card-fg: #e5e7eb;
    --muted:   #9ca3af;
    --ring:    #60a5fa;

    --x-bg: #0f1114;  --x-fg: #e5e7eb;
    --z-bg: #0b3d46;  --z-fg: #e5e7eb;
  }
}

/* ================= Social Buttons ================= */
.social-section{ margin: 32px 0 20px; }
.social-title{
  margin: 0 0 10px;
  font-size: 1rem;
  font-weight: 700;
  color: var(--muted);
  letter-spacing: .02em;
}

.social-row{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px,1fr));
  gap: 12px;
}

.social-btn{
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px 14px;
  border-radius: 14px;
  text-decoration: none;
  position: relative;
  overflow: clip;
  background: var(--card-bg);
  color: var(--card-fg);
  transition: transform .15s ease, box-shadow .2s ease, background-color .2s ease;
  box-shadow: 0 2px 10px rgba(0,0,0,.06);
  outline: none;
}
.social-btn:focus-visible{ box-shadow: 0 0 0 3px var(--ring); }

.social-btn .icon{
  flex: 0 0 36px;
  width: 36px; height: 36px;
  display: grid; place-items: center;
  border-radius: 10px;
  background: rgba(255,255,255,.12);
  color: inherit;
}
.social-btn .icon svg{ width:22px; height:22px; fill: currentColor; }

/* —— 読みやすさ最優先の文字色（強制上書き） —— */
.social-btn .label,
.social-btn .label strong,
.social-btn .label .sub{
  color: #ffffff !important;
}
.social-btn .label{
  display:flex; flex-direction:column;
  line-height:1.15;
  font-weight:600;
}
.social-btn .label .sub{
  font-size:.9rem;
  font-weight:400;
  color:#f1f5f9 !important; /* 少しだけコントラスト弱め */
}
.social-btn strong{ font-weight:700; }

/* Brand variants */
.social-x{
  background: var(--x-bg);
  color: var(--x-fg);
}
.social-x .icon{
  background: rgba(255,255,255,.14);
  color: var(--x-fg);
}

.social-zenn{
  background: var(--z-bg);
  color: var(--z-fg);
}
.social-zenn .icon{
  background: rgba(0,0,0,.12);
  color: var(--z-fg);
}

/* Hover / active */
@media (hover:hover){
  .social-btn:hover{ transform: translateY(-2px); box-shadow: 0 6px 18px rgba(0,0,0,.15); }
}
.social-btn:active{ transform: translateY(0); box-shadow: 0 2px 10px rgba(0,0,0,.08); }

/* 小さめ画面での余白 */
@media (max-width: 420px){
  .social-row{ grid-template-columns: 1fr; }
}
</style>

