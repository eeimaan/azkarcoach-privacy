<!doctype html><html lang="en"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Azkar Coach Privacy</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Outfit:wght@500;600;700&family=Figtree:wght@400;500;600&display=swap">
<style>
/* Layout: one calm reading column; glass hero, colour-tinted icon tiles mark each section like the app's goal cards */
:root{
  --bg:#F3F6F1; --surface:#FFFFFF; --glass:rgba(255,255,255,.72); --line:#DCE6D9;
  --fg:#2B3A2C; --muted:#56665A; --sage:#5F7A61; --sage-ink:#3E5640; --gold:#E9C46A; --gold-ink:#6E5110;
  --blob1:#DCE9D8; --blob2:#F6EBC7;
  --t-sun:#F6E3A8; --t-sun-i:#7A5A10; --t-sage:#DDEBD9; --t-sage-i:#3E5640; --t-rose:#F4D6DE; --t-rose-i:#8C3A4C;
  --t-sky:#DCE8F2; --t-sky-i:#2F5573; --t-lilac:#E3E0F4; --t-lilac-i:#4B4380; --t-clay:#F9DCC7; --t-clay-i:#9A4A22;
  --display:"Outfit",ui-sans-serif,system-ui,sans-serif; --body:"Figtree",ui-sans-serif,system-ui,sans-serif;
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --bg:#121813; --surface:#1A221B; --glass:rgba(30,40,31,.72); --line:#2C3A2D;
  --fg:#E7EDE5; --muted:#A3B0A4; --sage:#8FB08F; --sage-ink:#B9D3B7; --gold:#E9C46A; --gold-ink:#F2D58C;
  --blob1:#1E2B20; --blob2:#2A2617;
  --t-sun:#3A3119; --t-sun-i:#F2D58C; --t-sage:#243326; --t-sage-i:#B9D3B7; --t-rose:#3A2329; --t-rose-i:#F0B3C1;
  --t-sky:#1E2C38; --t-sky-i:#A9C9E6; --t-lilac:#2A2740; --t-lilac-i:#C8C1F2; --t-clay:#3A2619; --t-clay-i:#F3BC97;
  color-scheme:dark}}
:root[data-theme="dark"]{
  --bg:#121813; --surface:#1A221B; --glass:rgba(30,40,31,.72); --line:#2C3A2D;
  --fg:#E7EDE5; --muted:#A3B0A4; --sage:#8FB08F; --sage-ink:#B9D3B7; --gold:#E9C46A; --gold-ink:#F2D58C;
  --blob1:#1E2B20; --blob2:#2A2617;
  --t-sun:#3A3119; --t-sun-i:#F2D58C; --t-sage:#243326; --t-sage-i:#B9D3B7; --t-rose:#3A2329; --t-rose-i:#F0B3C1;
  --t-sky:#1E2C38; --t-sky-i:#A9C9E6; --t-lilac:#2A2740; --t-lilac-i:#C8C1F2; --t-clay:#3A2619; --t-clay-i:#F3BC97;
  color-scheme:dark}

body{background:var(--bg);color:var(--fg);font-family:var(--body);font-size:16.5px;line-height:1.65}
.bg{position:fixed;inset:0;pointer-events:none;z-index:0;overflow:hidden}
.bg i{position:absolute;border-radius:50%;filter:blur(80px)}
.bg i:nth-child(1){width:520px;height:520px;background:var(--blob1);left:-160px;top:-120px}
.bg i:nth-child(2){width:460px;height:460px;background:var(--blob2);right:-160px;top:40%}
.wrap{position:relative;z-index:1;max-width:760px;margin:0 auto;padding-block:40px 72px;
  padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));
  display:flex;flex-direction:column;gap:22px}
h1,h2,h3{font-family:var(--display);text-wrap:balance;margin:0;letter-spacing:-.02em}
p{margin:0}
a{color:var(--sage-ink);text-underline-offset:3px}
a:focus-visible,button:focus-visible{outline:2px solid var(--sage);outline-offset:3px;border-radius:8px}

.glass{background:var(--glass);backdrop-filter:blur(20px) saturate(160%);-webkit-backdrop-filter:blur(20px) saturate(160%);
  border:1px solid var(--line);border-radius:28px;box-shadow:0 14px 40px rgba(43,58,44,.07)}

/* hero */
.hero{padding:32px 28px;display:flex;flex-direction:column;gap:18px}
.brand{display:flex;align-items:center;gap:14px}
.mark{width:58px;height:58px;border-radius:18px;background:var(--sage);display:grid;place-items:center;flex:none}
.brand b{font-family:var(--display);font-size:20px;font-weight:600}
.brand span{display:block;font-size:13px;color:var(--muted)}
.hero h1{font-size:clamp(34px,7vw,52px);font-weight:700;line-height:1.04}
.hero h1 em{font-style:normal;color:var(--sage)}
.meta{display:flex;flex-wrap:wrap;gap:8px}
.chip{display:inline-flex;align-items:center;gap:8px;padding:8px 14px;border-radius:999px;background:var(--surface);
  border:1px solid var(--line);font-size:14px;color:var(--muted)}
.chip b{color:var(--fg);font-weight:600}
.chip.todo b{color:var(--gold-ink)}
.copy{font:600 13px var(--body);border:0;background:var(--t-sage);color:var(--t-sage-i);padding:5px 10px;border-radius:999px;cursor:pointer}

nav.toc{display:flex;gap:8px;flex-wrap:wrap}
nav.toc a{font-family:var(--display);font-weight:600;font-size:15px;text-decoration:none;padding:10px 18px;border-radius:999px;
  background:var(--fg);color:var(--bg)}
nav.toc a.alt{background:var(--surface);color:var(--fg);border:1px solid var(--line)}

/* summary tiles */
.summary{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px}
.tile{padding:18px;border-radius:24px;display:flex;flex-direction:column;gap:10px}
.tile p{font-size:15px;line-height:1.45;color:var(--fg)}
.ic{width:46px;height:46px;border-radius:15px;display:grid;place-items:center;flex:none}
.ic svg{width:24px;height:24px}

/* part headers */
.part{display:flex;align-items:flex-end;justify-content:space-between;gap:12px;margin-top:22px}
.part h2{font-size:clamp(28px,5vw,38px);font-weight:700}
.eyebrow{font:600 12px var(--body);letter-spacing:.12em;text-transform:uppercase;color:var(--sage)}

/* sections */
section.card{padding:22px 22px 24px;display:flex;flex-direction:column;gap:12px}
.sh{display:flex;align-items:center;gap:14px}
.sh h3{font-size:21px;font-weight:600}
.num{font:600 13px var(--display);color:var(--muted);letter-spacing:.04em}
.card p,.card li{color:var(--fg);max-width:65ch}
.card .soft{color:var(--muted)}
ul.dots{margin:0;padding:0;list-style:none;display:flex;flex-direction:column;gap:8px}
ul.dots li{position:relative;padding-left:22px}
ul.dots li::before{content:"";position:absolute;left:4px;top:.6em;width:8px;height:8px;border-radius:50%;background:var(--gold)}
.path{font-family:var(--display);font-weight:500;background:var(--t-sage);color:var(--t-sage-i);padding:1px 8px;border-radius:8px;white-space:nowrap}
.none{font:700 30px var(--display);color:var(--sage)}
.callout{padding:14px 16px;border-radius:18px;background:var(--t-rose);color:var(--t-rose-i);font-weight:500}
.callout.sun{background:var(--t-sun);color:var(--t-sun-i)}

.tbl{overflow-x:auto;border-radius:18px;border:1px solid var(--line);background:var(--surface)}
table{border-collapse:collapse;width:100%;font-size:15px;min-width:480px}
th{font:600 12px var(--body);letter-spacing:.08em;text-transform:uppercase;color:var(--muted);text-align:left;padding:12px 16px;background:var(--t-sage)}
td{padding:12px 16px;border-top:1px solid var(--line);vertical-align:top}
td:first-child{font-weight:600;width:42%}

footer{margin-top:18px;text-align:center;display:flex;flex-direction:column;align-items:center;gap:10px}
footer .ar{font-family:"Amiri",serif;font-size:28px;color:var(--sage-ink)}
footer p{color:var(--muted);font-size:14px}

@media (max-width:560px){.summary{grid-template-columns:1fr}.hero{padding:24px 20px}section.card{padding:18px}}
@media (prefers-reduced-motion:no-preference){.copy{transition:transform .15s}.copy:active{transform:scale(.96)}}
</style>

</head><body><div class="bg" aria-hidden="true"><i></i><i></i></div>
<main class="wrap">

<header class="glass hero">
  <div class="brand">
    <div class="mark" aria-hidden="true">
      <svg width="44" height="44" viewBox="0 0 32 32"><circle cx="16" cy="4" r="3" fill="#E9C46A"/><circle cx="22" cy="5.6" r="2" fill="#FFFFFF"/><circle cx="26.4" cy="10" r="2" fill="#FFFFFF"/><circle cx="28" cy="16" r="2" fill="#FFFFFF"/><circle cx="26.4" cy="22" r="2" fill="#FFFFFF"/><circle cx="22" cy="26.4" r="2" fill="#FFFFFF"/><circle cx="16" cy="28" r="2" fill="#FFFFFF"/><circle cx="10" cy="26.4" r="2" fill="#FFFFFF"/><circle cx="5.6" cy="22" r="2" fill="#FFFFFF"/><circle cx="4" cy="16" r="2" fill="#FFFFFF"/><circle cx="5.6" cy="10" r="2" fill="#2F4431"/><circle cx="10" cy="5.6" r="2" fill="#2F4431"/></svg>
    </div>
    <div><b>Azkar Coach</b><span>Dua · Dhikr · Tasbih</span></div>
  </div>
  <h1>Privacy Policy <em>&amp;</em> Terms of Use</h1>
  <div class="meta">
    <span class="chip">Effective <b>26 October 2026</b></span>
    <span class="chip">App <b>Azkar Coach (Android)</b></span>
    <span class="chip todo">Developer <b>[Your name or studio name]</b></span>
    <span class="chip">Contact <b id="mail">imaandev62@gmail.com</b> <button class="copy" type="button" id="copyBtn">Copy</button></span>
  </div>
  <nav class="toc" aria-label="Jump to">
    <a href="#privacy">Privacy Policy</a>
    <a class="alt" href="#terms">Terms of Use</a>
  </nav>
</header>

<!-- ================= PRIVACY ================= -->
<div class="part" id="privacy"><div><div class="eyebrow">Part one</div><h2>Privacy Policy</h2></div></div>

<div class="summary" role="list" aria-label="Summary">
  <div class="glass tile" role="listitem">
    <div class="ic" style="background:var(--t-sage);color:var(--t-sage-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3l8 3v6c0 5-3.5 8-8 9-4.5-1-8-4-8-9V6z"/><path d="M9 12l2 2 4-4"/></svg></div>
    <p>Azkar Coach does <b>not collect, upload, sell or share</b> any personal data.</p>
  </div>
  <div class="glass tile" role="listitem">
    <div class="ic" style="background:var(--t-sun);color:var(--t-sun-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><rect x="6" y="2.5" width="12" height="19" rx="3"/><path d="M11 18.5h2"/></svg></div>
    <p>Everything you enter stays <b>on your phone only</b>.</p>
  </div>
  <div class="glass tile" role="listitem">
    <div class="ic" style="background:var(--t-rose);color:var(--t-rose-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"><circle cx="12" cy="12" r="9"/><path d="M5.6 5.6l12.8 12.8"/></svg></div>
    <p><b>No account, no sign-in, no analytics</b> and no tracking.</p>
  </div>
  <div class="glass tile" role="listitem">
    <div class="ic" style="background:var(--t-sky);color:var(--t-sky-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"><path d="M2 8.5a15 15 0 0 1 4.3-2.9M10 5.1A15 15 0 0 1 22 8.5M5 12a10 10 0 0 1 2.6-1.7M12.5 10a10 10 0 0 1 6.5 2M8.5 15.5a5 5 0 0 1 7 0M3 3l18 18"/></svg></div>
    <p>The app works <b>fully offline</b>.</p>
  </div>
</div>

<section class="glass card" aria-labelledby="p1">
  <div class="sh"><div class="ic" style="background:var(--t-sun);color:var(--t-sun-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><rect x="6" y="2.5" width="12" height="19" rx="3"/><path d="M11 18.5h2"/></svg></div><div><div class="num">01</div><h3 id="p1">Information stored on your device</h3></div></div>
  <p>To work, the app saves the following <b>only in your phone's local storage</b>. The developer cannot see it and it is never sent to any server.</p>
  <div class="tbl"><table>
    <thead><tr><th>Data</th><th>Why it is stored</th></tr></thead>
    <tbody>
      <tr><td>Your first name (optional)</td><td>To greet you on the Home screen</td></tr>
      <tr><td>Your goals (azkar sets, tasbih targets, reminder times)</td><td>To show your goals and send reminders</td></tr>
      <tr><td>Daily progress, streaks and qaza (missed days)</td><td>To show your progress and history</td></tr>
      <tr><td>Mood check-ins (e.g. "calm", "anxious")</td><td>To show a matching note and a gentle weekly message</td></tr>
      <tr><td>Duas or surahs you write yourself</td><td>So you can add them to your goals</td></tr>
      <tr><td>Settings (language, Arabic text size, theme, vibration, quiet hours)</td><td>To remember your preferences</td></tr>
    </tbody>
  </table></div>
  <p class="soft">You are in control of this data:</p>
  <ul class="dots">
    <li><b>Delete everything:</b> uninstall the app, or go to <span class="path">Android Settings → Apps → Azkar Coach → Storage → Clear data</span>.</li>
    <li><b>Delete a single goal:</b> open the goal and tap <span class="path">Delete goal</span>.</li>
  </ul>
</section>

<section class="glass card" aria-labelledby="p2">
  <div class="sh"><div class="ic" style="background:var(--t-sage);color:var(--t-sage-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3l8 3v6c0 5-3.5 8-8 9-4.5-1-8-4-8-9V6z"/><path d="M9 12l2 2 4-4"/></svg></div><div><div class="num">02</div><h3 id="p2">Information we collect</h3></div></div>
  <div class="none">None.</div>
  <p>The app has no servers and no third-party analytics or crash-reporting services. No data is collected automatically or manually, and none is shared with third parties.</p>
</section>

<section class="glass card" aria-labelledby="p3">
  <div class="sh"><div class="ic" style="background:var(--t-sky);color:var(--t-sky-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 16V11a6 6 0 0 1 12 0v5l2 2H4z"/><path d="M10 20a2 2 0 0 0 4 0"/></svg></div><div><div class="num">03</div><h3 id="p3">Permissions</h3></div></div>
  <div class="tbl"><table>
    <thead><tr><th>Permission</th><th>Why it is needed</th></tr></thead>
    <tbody>
      <tr><td>Notifications</td><td>To remind you of your azkar and tasbih goals at the times you choose. You can turn this off at any time in Android settings.</td></tr>
      <tr><td>Vibration</td><td>For tap feedback while counting tasbih. You can turn it off in the app's Settings.</td></tr>
    </tbody>
  </table></div>
  <p class="soft">The app does not access your contacts, location, camera, microphone, photos, files or phone calls.</p>
</section>

<section class="glass card" aria-labelledby="p4">
  <div class="sh"><div class="ic" style="background:var(--t-lilac);color:var(--t-lilac-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M10 14a4 4 0 0 0 5.7 0l3-3a4 4 0 0 0-5.7-5.7l-1 1"/><path d="M14 10a4 4 0 0 0-5.7 0l-3 3a4 4 0 0 0 5.7 5.7l1-1"/></svg></div><div><div class="num">04</div><h3 id="p4">Links</h3></div></div>
  <p>If you tap a link in the app (for example to this policy), it opens in your web browser. That website's own privacy policy then applies.</p>
</section>

<section class="glass card" aria-labelledby="p5">
  <div class="sh"><div class="ic" style="background:var(--t-clay);color:var(--t-clay-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="7" r="3.5"/><path d="M5 21a7 7 0 0 1 14 0"/></svg></div><div><div class="num">05</div><h3 id="p5">Children</h3></div></div>
  <p>Azkar Coach is suitable for all ages. Because the app collects no personal data from anyone, it does not knowingly collect data from children.</p>
</section>

<section class="glass card" aria-labelledby="p6">
  <div class="sh"><div class="ic" style="background:var(--t-sage);color:var(--t-sage-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><rect x="5" y="11" width="14" height="10" rx="2.5"/><path d="M8 11V8a4 4 0 0 1 8 0v3"/></svg></div><div><div class="num">06</div><h3 id="p6">Security</h3></div></div>
  <p>Your data never leaves your device through the app. It is protected by your phone's own security (screen lock, device encryption). If you share your phone, others who can unlock it may be able to see the app's contents.</p>
</section>

<section class="glass card" aria-labelledby="p7">
  <div class="sh"><div class="ic" style="background:var(--t-sun);color:var(--t-sun-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 12a8 8 0 1 1-2.3-5.6L20 8.7"/><path d="M20 4v4.7h-4.7"/></svg></div><div><div class="num">07</div><h3 id="p7">Changes to this policy</h3></div></div>
  <p>If this policy changes, the new version will be published at this same link with a new effective date. Major changes will also be mentioned in the app's update notes on Google Play.</p>
</section>

<section class="glass card" aria-labelledby="p8">
  <div class="sh"><div class="ic" style="background:var(--t-sky);color:var(--t-sky-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="5" width="18" height="14" rx="3"/><path d="M4 7l8 6 8-6"/></svg></div><div><div class="num">08</div><h3 id="p8">Contact</h3></div></div>
  <p>Questions about privacy? Email <b>imaandev62@gmail.com</b>.</p>
</section>

<!-- ================= TERMS ================= -->
<div class="part" id="terms"><div><div class="eyebrow">Part two</div><h2>Terms of Use</h2></div></div>
<p class="soft" style="color:var(--muted)">By installing or using Azkar Coach you agree to these terms.</p>

<section class="glass card" aria-labelledby="t1">
  <div class="sh"><div class="ic" style="background:var(--t-sage);color:var(--t-sage-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"><circle cx="6" cy="7" r="2.6"/><circle cx="12" cy="12" r="2.6"/><circle cx="18" cy="17" r="2.6"/></svg></div><div><div class="num">01</div><h3 id="t1">Purpose of the app</h3></div></div>
  <p>Azkar Coach helps you build a habit of daily azkar, dua and tasbih through reminders, counters and progress tracking. It is a personal worship aid.</p>
</section>

<section class="glass card" aria-labelledby="t2">
  <div class="sh"><div class="ic" style="background:var(--t-sun);color:var(--t-sun-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 5a2 2 0 0 1 2-2h13v16H6a2 2 0 0 0-2 2z"/><path d="M4 19V5M8 7h7"/></svg></div><div><div class="num">02</div><h3 id="t2">Religious content</h3></div></div>
  <ul class="dots">
    <li>The azkar, duas, Quranic verses, translations and references are provided in good faith and come from well-known sources.</li>
    <li>Despite every care, mistakes in text, translation or reference are possible. For religious rulings (fiqh) or anything you are unsure about, please consult a qualified scholar.</li>
    <li>If you find a mistake, please tell us at the contact email above so it can be corrected.</li>
  </ul>
</section>

<section class="glass card" aria-labelledby="t3">
  <div class="sh"><div class="ic" style="background:var(--t-rose);color:var(--t-rose-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linejoin="round"><path d="M12 20s-7-4.5-7-10a4 4 0 0 1 7-2.5A4 4 0 0 1 19 10c0 5.5-7 10-7 10z"/></svg></div><div><div class="num">03</div><h3 id="t3">Not medical or professional advice</h3></div></div>
  <p class="callout">The mood notes and affirmations are spiritual encouragement only. They are <b>not</b> a substitute for medical, psychological or professional help. If you are struggling, please reach out to someone you trust or a qualified professional.</p>
</section>

<section class="glass card" aria-labelledby="t4">
  <div class="sh"><div class="ic" style="background:var(--t-sky);color:var(--t-sky-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 16V11a6 6 0 0 1 12 0v5l2 2H4z"/><path d="M10 20a2 2 0 0 0 4 0"/></svg></div><div><div class="num">04</div><h3 id="t4">Reminders</h3></div></div>
  <p>Reminders depend on your phone's settings (battery saver, "Do not disturb", notification permission). The developer cannot guarantee that every reminder is delivered on time.</p>
</section>

<section class="glass card" aria-labelledby="t5">
  <div class="sh"><div class="ic" style="background:var(--t-lilac);color:var(--t-lilac-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><ellipse cx="12" cy="6" rx="7" ry="3"/><path d="M5 6v12c0 1.7 3.1 3 7 3s7-1.3 7-3V6M5 12c0 1.7 3.1 3 7 3s7-1.3 7-3"/></svg></div><div><div class="num">05</div><h3 id="t5">Your data</h3></div></div>
  <p>All data stays on your device, as described in the Privacy Policy above. You are responsible for it; it is lost if you uninstall the app or clear its data, because there is no cloud backup.</p>
</section>

<section class="glass card" aria-labelledby="t6">
  <div class="sh"><div class="ic" style="background:var(--t-clay);color:var(--t-clay-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3l8 3v6c0 5-3.5 8-8 9-4.5-1-8-4-8-9V6z"/></svg></div><div><div class="num">06</div><h3 id="t6">Acceptable use</h3></div></div>
  <p>Please do not copy, resell or redistribute the app or its design as your own. Sharing the azkar text itself for the sake of Allah is welcome.</p>
</section>

<section class="glass card" aria-labelledby="t7">
  <div class="sh"><div class="ic" style="background:var(--t-sun);color:var(--t-sun-i)"><svg viewBox="0 0 24 24" fill="currentColor" stroke="none"><path d="M4 18h16v2H4zM5 16l-1-9 5 4 3-6 3 6 5-4-1 9z"/></svg></div><div><div class="num">07</div><h3 id="t7">Premium features</h3></div></div>
  <p class="callout sun">Premium learning tracks are free.</p>
</section>

<section class="glass card" aria-labelledby="t8">
  <div class="sh"><div class="ic" style="background:var(--t-sage);color:var(--t-sage-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 8v5M12 16.5v.5"/></svg></div><div><div class="num">08</div><h3 id="t8">Disclaimer</h3></div></div>
  <p>The app is provided "as is", without warranties of any kind. To the extent allowed by law, the developer is not liable for any loss arising from the use of the app.</p>
</section>

<section class="glass card" aria-labelledby="t9">
  <div class="sh"><div class="ic" style="background:var(--t-sky);color:var(--t-sky-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 12a8 8 0 1 1-2.3-5.6L20 8.7"/><path d="M20 4v4.7h-4.7"/></svg></div><div><div class="num">09</div><h3 id="t9">Changes to these terms</h3></div></div>
  <p>These terms may be updated. The latest version is always available at this link. Continuing to use the app after a change means you accept the updated terms.</p>
</section>

<section class="glass card" aria-labelledby="t10">
  <div class="sh"><div class="ic" style="background:var(--t-rose);color:var(--t-rose-i)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="5" width="18" height="14" rx="3"/><path d="M4 7l8 6 8-6"/></svg></div><div><div class="num">10</div><h3 id="t10">Contact</h3></div></div>
  <p><b>imaandev62@gmail.com</b></p>
</section>

<footer>
  <p><i>JazakAllahu khairan for using Azkar Coach.</i></p>
  <p>© 2026 Azkar Coach</p>
</footer>
</main>

<script>
(function(){
  var btn=document.getElementById('copyBtn'), mail=document.getElementById('mail');
  btn.addEventListener('click',function(){
    var t=mail.textContent;
    function done(){btn.textContent='Copied';setTimeout(function(){btn.textContent='Copy'},1600)}
    function select(){var r=document.createRange();r.selectNodeContents(mail);var s=getSelection();s.removeAllRanges();s.addRange(r);btn.textContent='Selected'}
    try{navigator.clipboard.writeText(t).then(done,select)}catch(e){select()}
  });
})();
</script>
</body></html>
