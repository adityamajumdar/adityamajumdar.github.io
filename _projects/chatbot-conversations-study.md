---
layout: page
title: "Mental Health Effects of AI Sycophancy"
description: "A paid Penn State study on how AI chatbots respond when people talk through conflicts with others. What's involved, how our Chrome extension works, and how your data is handled."
img: # assets/img/projects/chatbot-study.png  
importance: 1
category: work
---


<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400..800&family=Source+Serif+4:ital,opsz,wght@0,8..60,400..700;1,8..60,400..700&display=swap" rel="stylesheet">

<style>
.syc {
  --ink: #1A2238; --ink-soft: #4A5470; --paper: #FFFFFF; --paper-2: #F3F6FC; --line: #DCE3F0;
  --blue: #2F5FD6; --blue-soft: #E7EEFD; --sun: #F5B82E; --sun-soft: #FFF3D6; --leaf: #0F7B5C; --leaf-soft: #E2F4EC;
  --head: "Bricolage Grotesque", "Segoe UI", system-ui, sans-serif;
  --body: "Source Serif 4", Georgia, "Times New Roman", serif;
  font-family: var(--body); font-size: 1.075rem; line-height: 1.72; color: var(--ink);
}
html[data-theme="dark"] .syc {
  --ink: #E8ECF6; --ink-soft: #AEB7CC; --paper: #1C2233; --paper-2: #232A3E; --line: #343D57;
  --blue: #8AAAFF; --blue-soft: #24304F; --sun: #F7C552; --sun-soft: #3A3220; --leaf: #5CD3A6; --leaf-soft: #1C3A30;
}
.syc p, .syc li, .syc dd { max-width: 68ch; }
.syc h1, .syc h2, .syc h3 { font-family: var(--head); color: var(--ink); letter-spacing: -0.02em; }
.syc h2 { font-size: clamp(1.6rem, 3vw, 2.1rem); font-weight: 760; line-height: 1.15; margin: 4rem 0 1rem; }
.syc h3 { font-size: 1.2rem; font-weight: 700; margin: 1.6rem 0 .4rem; }
.syc strong { color: var(--blue); font-weight: 680; }
.syc a { color: var(--blue); text-decoration: underline; text-underline-offset: 3px; text-decoration-thickness: 1.5px; }
.syc a:hover { text-decoration-thickness: 2.5px; }
.syc a:focus-visible, .syc summary:focus-visible { outline: 3px solid var(--sun); outline-offset: 3px; border-radius: 4px; }
.syc .paid { background: linear-gradient(transparent 52%, var(--sun) 52%); color: var(--ink); font-weight: 750; padding: 0 .1em; }
.syc .todo { background: var(--sun-soft); outline: 1.5px dashed var(--sun); border-radius: 3px; padding: 0 .3em; color: var(--ink); font-style: normal; }
/* ---------- hero ---------- */
.syc-hero { display: grid; grid-template-columns: 1.15fr .85fr; gap: 2.5rem; align-items: center; margin: 1rem 0 1rem; }
.syc-hero h1 { font-size: clamp(2.6rem, 6.5vw, 4.2rem); font-weight: 800; line-height: .98; letter-spacing: -0.035em; margin: 0 0 1.1rem; }
.syc-hero .lede { font-size: 1.2rem; color: var(--ink-soft); margin-bottom: 1.5rem; }
.syc-pay { display: flex; align-items: center; gap: 1rem; background: var(--sun-soft); border: 2px solid var(--sun); border-radius: 14px; padding: .9rem 1.2rem; margin-bottom: 1.4rem; max-width: 30rem; }
.syc-pay .amt { font-family: var(--head); font-weight: 800; font-size: 2.3rem; line-height: 1; color: var(--ink); white-space: nowrap; }
.syc-pay .what { font-family: var(--head); font-size: 1rem; line-height: 1.35; color: var(--ink); }
.syc-pay .what b { display: block; font-size: 1.1rem; }
.syc-btn { display: inline-block; font-family: var(--head); font-weight: 700; font-size: 1.1rem; background: var(--blue); color: #fff !important; padding: .85rem 1.7rem; border-radius: 999px; text-decoration: none !important; transition: transform .15s ease, box-shadow .15s ease; }
html[data-theme="dark"] .syc-btn { color: #10162A !important; }
.syc-btn:hover { transform: translateY(-1px); box-shadow: 0 6px 18px -6px var(--blue); }
.syc .fine { font-size: .92rem; color: var(--ink-soft); margin-top: .9rem; }
/* chat illustration */
.syc-chat { background: var(--paper-2); border: 1px solid var(--line); border-radius: 22px; padding: 1.4rem 1.1rem; display: flex; flex-direction: column; gap: .8rem; font-family: var(--head); font-size: .98rem; line-height: 1.4; }
.syc-chat .b { max-width: 85%; padding: .7rem 1rem; border-radius: 18px; opacity: 0; transform: translateY(8px); animation: syc-in .45s ease-out forwards; }
.syc-chat .me { align-self: flex-end; background: var(--blue); color: #fff; border-bottom-right-radius: 5px; }
html[data-theme="dark"] .syc-chat .me { color: #10162A; }
.syc-chat .ai { align-self: flex-start; background: var(--paper); border: 1.5px solid var(--line); border-bottom-left-radius: 5px; }
.syc-chat .b1 { animation-delay: .3s; } .syc-chat .b2 { animation-delay: 1.4s; } .syc-chat .b3 { animation-delay: 2.6s; }
.syc-chat .cap { font-family: var(--body); font-style: italic; font-size: .85rem; color: var(--ink-soft); text-align: center; margin-top: .3rem; }
@keyframes syc-in { to { opacity: 1; transform: none; } }
@media (prefers-reduced-motion: reduce) { .syc-chat .b { animation: none; opacity: 1; transform: none; } .syc-btn { transition: none; } }
/* ---------- note / callout ---------- */
.syc-note { border-left: 4px solid var(--blue); background: var(--blue-soft); padding: 1rem 1.3rem; border-radius: 0 10px 10px 0; margin: 1.6rem 0; }
.syc-note p:last-child { margin-bottom: 0; }
/* ---------- steps (a real sequence) ---------- */
.syc-steps { list-style: none; counter-reset: step; padding: 0; margin: 1.5rem 0; }
.syc-steps li { counter-increment: step; position: relative; padding: 0 0 1.5rem 3.6rem; }
.syc-steps li::before { content: counter(step); position: absolute; left: 0; top: -.1rem; width: 2.4rem; height: 2.4rem; border-radius: 50%; background: var(--ink); color: var(--paper); font-family: var(--head); font-weight: 750; display: grid; place-items: center; }
.syc-steps li::after { content: ""; position: absolute; left: 1.15rem; top: 2.5rem; bottom: .2rem; width: 2px; background: var(--line); }
.syc-steps li:last-child::after { display: none; }
.syc-steps .t { font-family: var(--head); font-weight: 700; font-size: 1.12rem; display: block; }
.syc-steps .d { color: var(--ink-soft); }
/* ---------- extension ---------- */
.syc-two { display: grid; grid-template-columns: 1fr 1fr; gap: 2rem; align-items: start; }
.syc-dodont { display: grid; grid-template-columns: 1fr 1fr; gap: 1.2rem; margin: 1.6rem 0; }
.syc-dodont > div { border-radius: 14px; padding: 1.1rem 1.3rem; }
.syc-dodont .does { background: var(--blue-soft); }
.syc-dodont .never { background: var(--leaf-soft); }
.syc-dodont h3 { margin-top: 0; }
.syc-dodont ul { padding-left: 1.1rem; margin: 0; }
.syc-dodont li { margin-bottom: .45rem; }
.syc figure { margin: 1.5rem 0; }
.syc figcaption { font-size: .88rem; color: var(--ink-soft); font-style: italic; text-align: center; margin-top: .5rem; }
/* svg tokens */
.syc svg .f-paper { fill: var(--paper); } .syc svg .f-paper2 { fill: var(--paper-2); }
.syc svg .f-line { fill: var(--line); } .syc svg .s-line { stroke: var(--line); }
.syc svg .f-blue { fill: var(--blue); } .syc svg .f-bluesoft { fill: var(--blue-soft); }
.syc svg .f-ink { fill: var(--ink); } .syc svg .f-inksoft { fill: var(--ink-soft); }
.syc svg .f-leaf { fill: var(--leaf); } .syc svg .s-leaf { stroke: var(--leaf); }
.syc svg .f-leafsoft { fill: var(--leaf-soft); } .syc svg .f-sun { fill: var(--sun); }
.syc svg .s-ink { stroke: var(--ink-soft); }
.syc svg text { font-family: var(--head); }
/* ---------- data list ---------- */
.syc-data { display: grid; grid-template-columns: 12rem 1fr; gap: 0; margin: 1.5rem 0; border-top: 1px solid var(--line); }
.syc-data dt, .syc-data dd { padding: .9rem 0; border-bottom: 1px solid var(--line); margin: 0; }
.syc-data dt { font-family: var(--head); font-weight: 700; padding-right: 1rem; }
/* ---------- faq ---------- */
.syc details { border-bottom: 1px solid var(--line); padding: .9rem 0; }
.syc summary { font-family: var(--head); font-weight: 650; font-size: 1.08rem; cursor: pointer; list-style: none; display: flex; justify-content: space-between; gap: 1rem; }
.syc summary::-webkit-details-marker { display: none; }
.syc summary::after { content: "+"; font-size: 1.4rem; line-height: 1; color: var(--blue); transition: transform .2s ease; }
.syc details[open] summary::after { transform: rotate(45deg); }
.syc details p { margin: .7rem 0 0; color: var(--ink-soft); }
/* ---------- support + resources ---------- */
.syc-support { background: var(--leaf-soft); border-radius: 14px; padding: 1.2rem 1.4rem; margin: 1.5rem 0; }
.syc-support h3 { margin-top: 0; color: var(--leaf); }
.syc-res { list-style: none; padding: 0; }
.syc-res li { padding: .7rem 0; border-bottom: 1px solid var(--line); }
.syc-res .src { display: block; font-size: .9rem; color: var(--ink-soft); }
/* ---------- closing ---------- */
.syc-end { margin-top: 4rem; background: var(--ink); color: var(--paper); border-radius: 22px; padding: 2.2rem 2rem; }
.syc-end h2 { color: var(--paper); margin-top: 0; }
.syc-end p { color: var(--paper); opacity: .9; }
.syc-end .paid { color: var(--ink); }
.syc-end .syc-btn { background: var(--sun); color: #1A2238 !important; }
.syc-end a:not(.syc-btn) { color: var(--sun); }
.syc-meta { font-size: .9rem; color: var(--ink-soft); margin-top: 2rem; }
@media (max-width: 760px) {
  .syc-hero, .syc-two, .syc-dodont { grid-template-columns: 1fr; }
  .syc-data { grid-template-columns: 1fr; }
  .syc-data dt { border-bottom: none; padding-bottom: 0; }
  .syc-end { padding: 1.6rem 1.3rem; }
}
</style>

<div class="syc">
<!-- ===================== HERO ===================== -->
<section class="syc-hero">
  <div>
    <h1>Do you vent to chatbots?</h1>
    <p class="lede">If you've ever asked ChatGPT, Claude, or Gemini for advice about a friend, partner, coworker, or family member, we'd like to learn from your experience.</p>
    <div class="syc-pay">
      <span class="amt"><span class="todo">$10</span></span>
      <span class="what"><b>This is a paid study.</b>About <span class="todo">30 minutes</span>, online, paid as a <span class="todo"> amazon gift card</span>.</span>
    </div>
    <a class="syc-btn" href="https://pennstate.qualtrics.com/jfe/form/SV_0uLXRTukNBcAox8" target="_blank" rel="noopener">Take the survey</a>
  </div>
  <div class="syc-chat" aria-hidden="true">
    <div class="b me b1">She ignored me in front of the whole team. Am I wrong for being upset?</div>
    <div class="b ai b2">You're absolutely right to feel that way. That was genuinely disrespectful of her.</div>
    <div class="b me b3">Thanks. I knew I wasn't overreacting.</div>
    <div class="cap">The kind of conversation this study is about</div>
  </div>
</section>
<!-- ===================== ABOUT ===================== -->
<h2>What we're studying</h2>
<p>A lot of people now turn to AI chatbots when something goes wrong between them and someone else. Chatbots are always available, never judge, and usually take your side.</p>
<p>That last part is what we want to understand. Research shows that AI chatbots tend to <strong>agree with and validate the person they're talking to</strong>, sometimes even when that person's account is one-sided. Researchers call this <strong>sycophancy</strong>. In a conflict, hearing only your side reflected back can feel good in the moment. We don't yet know how it relates to how people feel over time, how they see the other person, or where else they turn for support.</p>
<p>This study looks at <strong>real conversations people have already had with chatbots</strong> about interpersonal situations, alongside survey questions about wellbeing, relationships, and help-seeking. We're not testing you or judging how you use AI. There are no right answers.</p>
<div class="syc-note">
  <p><strong>Why real conversations?</strong> Most research on chatbot sycophancy uses made-up prompts in a lab. How people actually talk to chatbots about their own lives is messier and more personal, and that's exactly why it matters to study it carefully, and why we built tools to keep you in control of what you share.</p>
</div>
<!-- ===================== STEPS ===================== -->
<h2>What you'll do</h2>
<ol class="syc-steps">
  <li><span class="d">You need to be <span class="todo">18 or older</span> and have used an AI chatbot to talk about a situation with another person. <span class="todo">You are willing to download our custom built chrome extension. </span></span></li>
  <li><span class="t">Install our Chrome extension</span><span class="d">The <strong>LLM Chat Exporter</strong> is a free extension from the <a href="CHROME_STORE_LINK" target="_blank" rel="noopener">Chrome Web Store</a>. It takes about a minute to set up.</span></li>
  <li><span class="t">Export a conversation and redact anything you want</span><span class="d">Open a past chatbot conversation, export it with the extension, and <strong>black out any message or detail</strong> you'd rather keep private, like names or places. <span class="todo">You are expected to upload atleast 3 conversations, but can upload upto 10 conversations.</span></span></li>
  <li><span class="t">Upload the file and answer the survey</span><span class="d">You upload the file yourself, then answer questions about your chatbot use, your relationships, and how you've been feeling lately.</span></li>
  <li><span class="t">Get paid</span><span class="d">You'll receive <span class="paid"><span class="todo">$10</span></span> as a <span class="todo"> amazon gift card</span> within <span class="todo">5 business days</span>. Afterward, you can uninstall the extension.</span></li>
</ol>

<!-- ===================== EXTENSION ===================== -->

<h2>About the Chrome extension</h2>
<div class="syc-two">
  <div>
    <p>Chatbot sites don't make it easy to save a full conversation in a clean, readable form. The <strong>LLM Chat Exporter</strong> is a <strong>formatting tool that runs only on your computer</strong>. It turns a conversation on your screen into a file you can review, redact, and then choose to upload.</p>
    <p>It works with <span class="todo">ChatGPT, Claude, Gemini</span> in the Chrome browser on a computer.</p>
  </div>
  <figure>
    <svg viewBox="0 0 420 300" role="img" aria-labelledby="ext-t" style="width:100%;height:auto;">
      <title id="ext-t">A browser window showing a chatbot conversation with one message blacked out, and the exporter saving a file named with a participant ID</title>
      <rect x="6" y="6" width="408" height="250" rx="14" class="f-paper2 s-line" stroke-width="2"/>
      <rect x="6" y="6" width="408" height="34" rx="14" class="f-line"/>
      <rect x="6" y="26" width="408" height="14" class="f-line"/>
      <circle cx="26" cy="23" r="5" class="f-paper"/><circle cx="42" cy="23" r="5" class="f-paper"/><circle cx="58" cy="23" r="5" class="f-paper"/>
      <rect x="80" y="14" width="200" height="18" rx="9" class="f-paper"/>
      <rect x="370" y="13" width="22" height="20" rx="5" class="f-blue"/>
      <path d="M376 23 h10 M381 18 v10" stroke="#fff" stroke-width="2.2" stroke-linecap="round"/>
      <rect x="196" y="58" width="196" height="40" rx="14" class="f-blue"/>
      <rect x="210" y="70" width="150" height="6" rx="3" fill="#fff" opacity=".85"/>
      <rect x="210" y="82" width="110" height="6" rx="3" fill="#fff" opacity=".85"/>
      <rect x="28" y="110" width="220" height="40" rx="14" class="f-paper s-line" stroke-width="1.5"/>
      <rect x="42" y="122" width="170" height="6" rx="3" class="f-inksoft" opacity=".55"/>
      <rect x="42" y="134" width="120" height="6" rx="3" class="f-inksoft" opacity=".55"/>
      <rect x="166" y="162" width="226" height="40" rx="14" class="f-ink"/>
      <text x="279" y="187" text-anchor="middle" font-size="13" font-weight="700" class="f-sun">redacted by you</text>
      <rect x="28" y="214" width="190" height="28" rx="12" class="f-paper s-line" stroke-width="1.5"/>
      <rect x="42" y="225" width="140" height="6" rx="3" class="f-inksoft" opacity=".55"/>
      <path d="M210 262 v14" class="s-ink" stroke-width="2" stroke-dasharray="3 4"/>
      <rect x="130" y="276" width="160" height="22" rx="11" class="f-leafsoft s-leaf" stroke-width="1.5"/>
      <text x="210" y="291" text-anchor="middle" font-size="12" font-weight="700" class="f-leaf">chat_P1042 saved to your computer</text>
    </svg>
    <figcaption>You see and control exactly what goes into the file.</figcaption>
  </figure>
</div>
<div class="syc-dodont">
  <div class="does">
    <h3>What it does</h3>
    <ul>
      <li>Scrolls through the conversation you choose, so the <strong>whole chat</strong> is captured, not just what fits on screen</li>
      <li>Lets you <strong>redact any message or part of a message</strong> before saving</li>
      <li>Adds your <strong>participant ID</strong> so we can match the file to your survey without your name</li>
      <li>Saves a file <strong>to your own computer</strong></li>
    </ul>
  </div>
  <div class="never">
    <h3>What it doesn't do</h3>
    <ul>
      <li>Send anything to us, the chatbot company, or anyone else</li>
      <li>Read conversations you don't open and export yourself</li>
      <li>Run on other websites or track your browsing</li>
      <li>Ask for your chatbot password or account login</li>
    </ul>
  </div>
</div>

<!-- ===================== DATA ===================== -->

<h2>What happens to your data</h2>
<p>Your conversation <strong>only leaves your computer when you upload it</strong>, and only after you've had the chance to review and redact it.</p>
<figure>
  <svg viewBox="0 0 680 190" role="img" aria-labelledby="flow-t" style="width:100%;height:auto;">
    <title id="flow-t">Data flow: the extension formats and redacts in your browser, saves a file on your computer, you upload it to the Qualtrics survey, and the Penn State research team analyzes it</title>
    <defs><marker id="syc-arr" markerWidth="8" markerHeight="8" refX="7" refY="4" orient="auto"><path d="M0,0 L8,4 L0,8 z" class="f-inksoft"/></marker></defs>
    <rect x="10" y="20" width="660" height="92" rx="12" class="f-paper2"/>
    <rect x="22" y="34" width="140" height="64" rx="10" class="f-paper s-line" stroke-width="1.5"/>
    <text x="92" y="61" text-anchor="middle" font-size="14" font-weight="700" class="f-ink">Your browser</text>
    <text x="92" y="80" text-anchor="middle" font-size="11" class="f-inksoft">format + redact</text>
    <line x1="166" y1="66" x2="186" y2="66" class="s-ink" stroke-width="2" marker-end="url(#syc-arr)"/>
    <rect x="190" y="34" width="140" height="64" rx="10" class="f-paper s-line" stroke-width="1.5"/>
    <text x="260" y="61" text-anchor="middle" font-size="14" font-weight="700" class="f-ink">File on your</text>
    <text x="260" y="78" text-anchor="middle" font-size="14" font-weight="700" class="f-ink">computer</text>
    <line x1="334" y1="66" x2="354" y2="66" class="s-ink" stroke-width="2" marker-end="url(#syc-arr)"/>
    <rect x="358" y="34" width="140" height="64" rx="10" class="f-bluesoft"/>
    <text x="428" y="61" text-anchor="middle" font-size="14" font-weight="700" class="f-ink">Qualtrics survey</text>
    <text x="428" y="80" text-anchor="middle" font-size="11" class="f-inksoft">you upload it</text>
    <line x1="502" y1="66" x2="522" y2="66" class="s-ink" stroke-width="2" marker-end="url(#syc-arr)"/>
    <rect x="526" y="34" width="134" height="64" rx="10" class="f-bluesoft"/>
    <text x="593" y="61" text-anchor="middle" font-size="14" font-weight="700" class="f-ink">Research team</text>
    <text x="593" y="80" text-anchor="middle" font-size="11" class="f-inksoft">Penn State</text>
    <path d="M22 128 h308" class="s-leaf" stroke-width="3" stroke-linecap="round"/>
    <text x="176" y="152" text-anchor="middle" font-size="13" font-weight="700" class="f-leaf">Stays on your device. You're in control.</text>
    <path d="M358 128 h302" class="s-ink" stroke-width="3" stroke-linecap="round" opacity=".5"/>
    <text x="509" y="152" text-anchor="middle" font-size="13" font-weight="700" class="f-inksoft">Only what you choose to share</text>
  </svg>
</figure>
<dl class="syc-data">
  <dt>What we collect</dt>
  <dd>Your survey answers and the conversation file(s) you upload, <strong>after your redactions</strong>, linked by a participant ID.</dd>
  <dt>Your identity</dt>
  <dd>Your name isn't attached to your responses. <span class="todo">We only ask for your email to send you the amazon giftcard and if you opt in for our optional interview.</span></dd>
  <dt>Where it's stored</dt>
  <dd><span class="todo">All your information is stored in Qualtrics, a Penn State-approved secure storage system.</span></dd>
  <dt>Who can see it</dt>
  <dd>Only the study's research team. In papers and talks, we report <strong>patterns across many people</strong>. <span class="todo">State whether short de-identified excerpts may be quoted.</span></dd>
  <dt>Changing your mind</dt>
  <dd>Taking part is <strong>completely voluntary</strong>. You can stop at any time.</dd>
</dl>
<div class="syc-support">
  <h3>If any of this brings up something hard</h3>
  <p>Some questions ask about loneliness, mood, and relationships. If you're struggling, you can call or text <strong>988</strong> (<a href="https://988lifeline.org" target="_blank" rel="noopener">988 Suicide &amp; Crisis Lifeline</a>) any time. Penn State students can also reach the <strong>Penn State Crisis Line at 877-229-6400</strong> or <a href="https://studentaffairs.psu.edu/counseling" target="_blank" rel="noopener">Counseling and Psychological Services (CAPS)</a>.</p>
</div>

<!-- ===================== FAQ ===================== -->
<h2>Questions people ask</h2>
<details>
  <summary>Do I have to be a Penn State student?</summary>
  <p>No, anyone in the United States can participate in this study.</p>
</details>
<details>
  <summary>I mostly use the chatbot app on my phone. Can I still take part?</summary>
  <p>Yes, as long as you can sign in to the same chatbot account in Chrome on a computer. Most chatbots sync your past conversations to their website, so you can export them from there.</p>
</details>
<details>
  <summary>Will the chatbot company know I'm in this study?</summary>
  <p>No. This study is run independently by researchers at Penn State, and the extension doesn't share anything with the chatbot company.</p>
</details>
<details>
  <summary>What if my conversation has really personal details in it?</summary>
  <p>That's expected, and it's why the extension lets you redact anything before saving. You choose what's in the file, and you can review it before uploading.</p>
</details>
<details>
  <summary>Do I need to keep the extension installed?</summary>
  <p>No. Once you've uploaded your file, you can remove it from Chrome like any other extension.</p>
</details>
<details>
  <summary>Who reviewed this study?</summary>
  <p>This study was reviewed by the Penn State Institutional Review Board (IRB), protocol <strong>STUDY00029720</strong>. For questions about your rights as a participant, you can contact Penn State's <a href="https://www.research.psu.edu/irb" target="_blank" rel="noopener">Human Research Protection Program</a>.</p>
</details>

<!-- ===================== CLOSING CTA ===================== -->
<section class="syc-end">
  <h2>Ready to take part?</h2>
  <p>It takes about <span class="todo">30 minutes</span>, and you'll receive <span class="paid"><span class="todo">$10</span></span> for completing it. Questions first? Email <a href="mailto:adity@psu.edu">adity [at] psu [dot] edu</a>.</p>
  <a class="syc-btn" href="https://pennstate.qualtrics.com/jfe/form/SV_0uLXRTukNBcAox8" target="_blank" rel="noopener">Take the survey</a>
</section>
<p class="syc-meta">Run by <strong>Aditya Majumdar</strong> and <strong>Prof. Sarah Rajtmajer</strong> in the <span class="todo">Rajtmajer Lab</span>, College of Information Sciences and Technology, Penn State.</p>
</div>
