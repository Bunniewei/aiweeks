<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>雙周報</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700&family=Space+Grotesk:wght@400;500;600;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #eef2f8;
    --surface: #ffffff;
    --surface2: #f4f7fc;
    --border: #dde4f0;
    --border2: #b8c8e8;
    --text: #0e1526;
    --muted: #6b7a99;
    --cyan: #00b4d8;
    --blue: #0077e6;
    --indigo: #3b5bdb;
    --green: #0ca678;
    --yellow: #f59f00;
    --red: #e03131;
    --glow-cyan: rgba(0,180,216,.15);
    --glow-blue: rgba(0,119,230,.1);
  }

  body {
    font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
    background: var(--bg);
    color: var(--text);
    height: 100vh;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    position: relative;
  }

  /* Grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,119,230,.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,119,230,.04) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  /* Glow orbs */
  body::after {
    content: '';
    position: fixed;
    top: -100px; right: -100px;
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(0,180,216,.12) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  .glow-bottom {
    position: fixed;
    bottom: -80px; left: -80px;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(59,91,219,.08) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  /* Progress */
  .progress-bar {
    height: 2px;
    background: var(--border);
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
  }
  .progress-fill {
    height: 100%;
    background: linear-gradient(90deg, var(--cyan), var(--blue));
    transition: width .4s cubic-bezier(.4,0,.2,1);
    box-shadow: 0 0 8px var(--cyan);
  }

  .slides-wrapper { flex: 1; position: relative; overflow: hidden; z-index: 1; }

  .slide {
    position: absolute; inset: 0;
    display: flex; align-items: center; justify-content: center;
    padding: 2rem;
    opacity: 0; pointer-events: none;
    transition: opacity .35s ease, transform .35s cubic-bezier(.4,0,.2,1);
    transform: translateX(40px);
  }
  .slide.active { opacity: 1; pointer-events: all; transform: translateX(0); }
  .slide.exit-left { opacity: 0; transform: translateX(-40px); pointer-events: none; }
  .slide-inner { width: 100%; max-width: 720px; }

  /* Nav */
  .nav-bar {
    display: flex; align-items: center; justify-content: space-between;
    padding: .9rem 2rem;
    border-top: 1px solid var(--border2);
    background: rgba(255,255,255,.85);
    backdrop-filter: blur(12px);
    flex-shrink: 0;
    z-index: 10;
    position: relative;
  }
  .nav-btn {
    background: var(--surface);
    border: 1px solid var(--border2);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    font-size: .68rem;
    letter-spacing: .08em;
    padding: .55rem 1.1rem;
    border-radius: 6px;
    cursor: pointer;
    transition: all .2s;
    min-width: 90px;
    position: relative;
    overflow: hidden;
  }
  .nav-btn::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, var(--cyan), var(--blue));
    opacity: 0;
    transition: opacity .2s;
  }
  .nav-btn:hover:not(:disabled)::before { opacity: 1; }
  .nav-btn:hover:not(:disabled) { color: #fff; border-color: transparent; box-shadow: 0 4px 16px var(--glow-blue); }
  .nav-btn span { position: relative; z-index: 1; }
  .nav-btn:disabled { opacity: .3; cursor: not-allowed; }
  .nav-center { display: flex; flex-direction: column; align-items: center; gap: .45rem; }
  .nav-dots { display: flex; gap: .5rem; }
  .nav-dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    background: var(--border2);
    cursor: pointer;
    transition: all .25s;
    border: 1px solid transparent;
  }
  .nav-dot.active {
    background: var(--cyan);
    width: 24px;
    border-radius: 4px;
    box-shadow: 0 0 8px var(--glow-cyan);
  }
  .nav-counter {
    font-family: 'Space Mono', monospace;
    font-size: .62rem;
    color: var(--muted);
    letter-spacing: .12em;
  }

  /* ══ COVER ══ */
  .cover-slide { position: relative; }
  .cover-card {
    background: var(--surface);
    border: 1px solid var(--border2);
    border-radius: 16px;
    padding: 2.8rem;
    position: relative;
    overflow: hidden;
    box-shadow: 0 4px 32px rgba(0,119,230,.08), 0 1px 4px rgba(0,0,0,.04);
  }
  .cover-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--cyan), var(--blue), var(--indigo));
  }
  .cover-card::after {
    content: '';
    position: absolute;
    top: -100px; right: -100px;
    width: 280px; height: 280px;
    background: radial-gradient(circle, rgba(0,180,216,.08) 0%, transparent 70%);
    pointer-events: none;
  }
  .cover-chip {
    display: inline-flex;
    align-items: center;
    gap: .4rem;
    background: linear-gradient(135deg, rgba(0,180,216,.1), rgba(0,119,230,.1));
    border: 1px solid rgba(0,180,216,.25);
    color: var(--blue);
    font-family: 'Space Mono', monospace;
    font-size: .65rem;
    letter-spacing: .12em;
    padding: .3rem .8rem;
    border-radius: 20px;
    margin-bottom: 1.2rem;
  }
  .cover-chip::before {
    content: '';
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--cyan);
    box-shadow: 0 0 6px var(--cyan);
    animation: blink 1.5s ease infinite;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:.3} }

  .cover-title {
    font-size: 3.5rem;
    font-weight: 700;
    color: var(--text);
    line-height: 1.05;
    margin-bottom: .5rem;
    letter-spacing: -.02em;
  }
  .cover-title .highlight {
    background: linear-gradient(135deg, var(--cyan), var(--blue));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .cover-subtitle {
    font-size: .83rem;
    color: var(--muted);
    margin-bottom: 2rem;
    font-family: 'Space Mono', monospace;
    letter-spacing: .05em;
  }
  .cover-stats {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: .8rem;
  }
  .cover-stat {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: .9rem;
    position: relative;
    overflow: hidden;
  }
  .cover-stat::before {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--cyan), transparent);
  }
  .cover-stat-label {
    font-family: 'Space Mono', monospace;
    font-size: .55rem;
    color: var(--muted);
    letter-spacing: .15em;
    text-transform: uppercase;
    margin-bottom: .3rem;
  }
  .cover-stat-value {
    font-weight: 600;
    font-size: .88rem;
    color: var(--text);
    letter-spacing: -.01em;
  }

  /* ══ SECTION ══ */
  .section-chip {
    display: inline-flex;
    align-items: center;
    gap: .4rem;
    font-family: 'Space Mono', monospace;
    font-size: .6rem;
    letter-spacing: .15em;
    color: var(--cyan);
    margin-bottom: .4rem;
    text-transform: uppercase;
  }
  .section-chip::before { content: '◆'; font-size: .5rem; }
  .slide-title {
    font-size: 2rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 1.2rem;
    letter-spacing: -.02em;
    display: flex;
    align-items: center;
    gap: .7rem;
  }
  .slide-title-bar {
    width: 3px; height: 1.8rem;
    background: linear-gradient(180deg, var(--cyan), var(--blue));
    border-radius: 2px;
    flex-shrink: 0;
  }

  /* ══ ITEMS ══ */
  .item-list { display: flex; flex-direction: column; gap: .5rem; }
  .item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
    cursor: pointer;
    transition: all .2s;
    box-shadow: 0 1px 4px rgba(0,0,0,.04);
    position: relative;
  }
  .item::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--border2);
    transition: background .2s, width .2s;
  }
  .item:hover { border-color: rgba(0,180,216,.3); box-shadow: 0 4px 16px var(--glow-cyan); }
  .item:hover::before { background: var(--cyan); }
  .item.open { border-color: rgba(0,119,230,.3); box-shadow: 0 4px 20px var(--glow-blue); }
  .item.open::before { background: linear-gradient(180deg, var(--cyan), var(--blue)); width: 3px; }

  .item-header {
    display: flex; gap: .9rem; align-items: center;
    padding: .85rem 1rem .85rem 1.2rem;
  }
  .item-idx {
    font-family: 'Space Mono', monospace;
    font-size: .65rem;
    color: var(--border2);
    flex-shrink: 0;
    width: 22px;
    text-align: right;
    transition: color .2s;
  }
  .item.open .item-idx { color: var(--cyan); }
  .item-main { flex: 1; display: flex; align-items: center; justify-content: space-between; gap: .8rem; }
  .item-left { flex: 1; }
  .item-title { font-size: .88rem; font-weight: 600; color: var(--text); letter-spacing: -.01em; }
  .item-hint { font-family: 'Space Mono', monospace; font-size: .6rem; color: var(--muted); margin-top: .1rem; letter-spacing: .03em; }
  .item-right { display: flex; align-items: center; gap: .6rem; flex-shrink: 0; }
  .item-tag {
    font-family: 'Space Mono', monospace;
    font-size: .58rem;
    padding: .18rem .55rem;
    border-radius: 20px;
    letter-spacing: .06em;
    white-space: nowrap;
    border: 1px solid;
  }
  .tag-done { color: var(--green); border-color: rgba(12,166,120,.3); background: rgba(12,166,120,.08); }
  .tag-progress { color: var(--blue); border-color: rgba(0,119,230,.3); background: rgba(0,119,230,.08); }
  .tag-pending { color: var(--yellow); border-color: rgba(245,159,0,.3); background: rgba(245,159,0,.08); }
  .item-chevron { font-size: .7rem; color: var(--muted); transition: transform .3s, color .2s; }
  .item.open .item-chevron { transform: rotate(180deg); color: var(--blue); }

  .item-body {
    max-height: 0; overflow: hidden;
    transition: max-height .35s cubic-bezier(.4,0,.2,1), padding .3s;
    padding: 0 1rem 0 3.2rem;
    background: linear-gradient(135deg, rgba(0,180,216,.03), rgba(0,119,230,.04));
  }
  .item.open .item-body {
    max-height: 150px;
    padding: .7rem 1rem .8rem 3.2rem;
    border-top: 1px solid rgba(0,119,230,.08);
  }
  .item-desc { font-size: .8rem; color: #2a3a5c; line-height: 1.75; }

  /* ══ PROBLEM CARDS ══ */
  .problem-hint {
    font-family: 'Space Mono', monospace;
    font-size: .6rem;
    color: var(--muted);
    letter-spacing: .08em;
    margin-bottom: .8rem;
    display: flex;
    align-items: center;
    gap: .4rem;
  }
  .problem-hint::before { content: '◆'; color: var(--cyan); font-size: .5rem; }

  .problem-card {
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
    margin-bottom: .5rem;
    cursor: pointer;
    transition: all .2s;
    box-shadow: 0 1px 4px rgba(0,0,0,.04);
    background: var(--surface);
  }
  .problem-card:hover { border-color: rgba(224,49,49,.25); box-shadow: 0 4px 16px rgba(224,49,49,.08); }
  .problem-card.open { border-color: rgba(0,119,230,.25); box-shadow: 0 4px 16px var(--glow-blue); }

  .problem-top {
    display: flex; gap: .7rem; align-items: center;
    padding: .8rem 1rem;
    background: #fff;
  }
  .p-label {
    font-family: 'Space Mono', monospace;
    font-size: .6rem;
    font-weight: 700;
    letter-spacing: .1em;
    flex-shrink: 0;
    padding: .15rem .5rem;
    border-radius: 4px;
    margin-top: .05rem;
  }
  .l-issue { color: var(--red); background: rgba(224,49,49,.08); border: 1px solid rgba(224,49,49,.2); }
  .l-solve { color: var(--green); background: rgba(12,166,120,.08); border: 1px solid rgba(12,166,120,.2); }
  .p-text { font-size: .79rem; color: var(--text); line-height: 1.65; flex: 1; }
  .p-arrow { font-size: .65rem; color: var(--muted); transition: transform .3s, color .2s; flex-shrink: 0; }
  .problem-card.open .p-arrow { transform: rotate(180deg); color: var(--blue); }

  .problem-bottom {
    max-height: 0; overflow: hidden;
    transition: max-height .35s cubic-bezier(.4,0,.2,1), padding .3s;
    padding: 0 1rem;
    display: flex; gap: .7rem; align-items: flex-start;
    background: linear-gradient(135deg, rgba(12,166,120,.04), rgba(0,180,216,.04));
  }
  .problem-card.open .problem-bottom {
    max-height: 150px;
    padding: .8rem 1rem;
    border-top: 1px solid rgba(12,166,120,.15);
  }
  .p-text-solve { font-size: .79rem; color: #0b4f3a; line-height: 1.7; }

  /* ══ AI CARD ══ */
  .ai-card {
    border-radius: 14px;
    overflow: hidden;
    border: 1px solid rgba(0,180,216,.25);
    box-shadow: 0 8px 40px rgba(0,119,230,.12), 0 0 0 1px rgba(0,180,216,.1);
    position: relative;
  }
  .ai-card-top-bar {
    height: 3px;
    background: linear-gradient(90deg, var(--cyan), var(--blue), var(--indigo));
  }
  .ai-card-inner {
    background: linear-gradient(135deg, #f0f7ff 0%, #e8f4fd 50%, #f0f0ff 100%);
    padding: 1.8rem;
    position: relative;
    overflow: hidden;
  }
  .ai-card-inner::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 250px; height: 250px;
    background: radial-gradient(circle, rgba(0,180,216,.15) 0%, transparent 70%);
  }
  .ai-card-inner::after {
    content: 'AI';
    position: absolute;
    right: 1.5rem; bottom: -1rem;
    font-size: 7rem;
    font-weight: 700;
    color: rgba(0,119,230,.06);
    line-height: 1;
    letter-spacing: -.04em;
  }
  .ai-chip {
    display: inline-flex;
    align-items: center;
    gap: .4rem;
    background: linear-gradient(135deg, rgba(0,180,216,.15), rgba(0,119,230,.15));
    border: 1px solid rgba(0,180,216,.3);
    color: var(--blue);
    font-family: 'Space Mono', monospace;
    font-size: .6rem;
    letter-spacing: .12em;
    padding: .25rem .7rem;
    border-radius: 20px;
    margin-bottom: .7rem;
  }
  .ai-chip::before { content: '★'; color: var(--cyan); }
  .ai-title {
    font-size: 2.2rem;
    font-weight: 700;
    color: var(--text);
    letter-spacing: -.02em;
    margin-bottom: .6rem;
    line-height: 1.1;
  }
  .ai-title .grad {
    background: linear-gradient(135deg, var(--cyan), var(--blue));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .ai-desc {
    font-size: .82rem;
    line-height: 1.8;
    color: #2a3a5c;
    margin-bottom: 1.2rem;
    padding: .8rem 1rem;
    background: rgba(255,255,255,.6);
    border-radius: 8px;
    border-left: 3px solid var(--cyan);
    backdrop-filter: blur(4px);
    position: relative;
  }
  .ai-grid { display: grid; grid-template-columns: 1fr 1fr; gap: .5rem; position: relative; }
  .ai-point {
    background: rgba(255,255,255,.7);
    border: 1px solid rgba(0,119,230,.12);
    border-radius: 8px;
    padding: .65rem .8rem;
    font-size: .76rem;
    color: #1a2a4a;
    line-height: 1.5;
    display: flex;
    gap: .5rem;
    align-items: flex-start;
    backdrop-filter: blur(4px);
    transition: all .2s;
  }
  .ai-point:hover { border-color: rgba(0,180,216,.3); box-shadow: 0 2px 8px var(--glow-cyan); }
  .ai-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--cyan); flex-shrink: 0; margin-top: .3rem; box-shadow: 0 0 4px var(--cyan); }

  .key-hint {
    position: fixed; bottom: 70px; right: 1.5rem;
    font-family: 'Space Mono', monospace;
    font-size: .58rem; color: var(--muted);
    opacity: .5; letter-spacing: .05em;
  }

  @media (max-width: 600px) {
    .slide { padding: 1rem; }
    .cover-stats { grid-template-columns: 1fr 1fr; }
    .cover-title { font-size: 2.5rem; }
    .slide-title { font-size: 1.6rem; }
    .nav-bar { padding: .8rem 1rem; }
    .ai-grid { grid-template-columns: 1fr; }
    .key-hint { display: none; }
  }
</style>
</head>
<body>
<div class="glow-bottom"></div>

<div class="progress-bar"><div class="progress-fill" id="progress-fill"></div></div>

<div class="slides-wrapper">

  <!-- Slide 1: Cover -->
  <div class="slide active">
    <div class="slide-inner cover-slide">
      <div class="cover-card">
        <div class="cover-chip">BI-WEEKLY REPORT · 2025</div>
        <div class="cover-title">工作進度<br><span class="highlight">雙周報告</span></div>
        <div class="cover-subtitle">// Progress Update · W05 – W06</div>
        <div class="cover-stats">
          <div class="cover-stat">
            <div class="cover-stat-label">Date</div>
            <div class="cover-stat-value">2025 / 03 / 18</div>
          </div>
          <div class="cover-stat">
            <div class="cover-stat-label">Period</div>
            <div class="cover-stat-value">W05 – W06</div>
          </div>
          <div class="cover-stat">
            <div class="cover-stat-label">Completed</div>
            <div class="cover-stat-value">4 Tasks</div>
          </div>
          <div class="cover-stat">
            <div class="cover-stat-label">Upcoming</div>
            <div class="cover-stat-value">2 Tasks</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Slide 2: 過去兩周 -->
  <div class="slide">
    <div class="slide-inner">
      <div class="section-chip">01 · Completed · 03/05 – 03/18</div>
      <div class="slide-title"><div class="slide-title-bar"></div>過去兩周完成事項</div>
      <div class="item-list">
        <div class="item" onclick="toggleItem(this)">
          <div class="item-header">
            <div class="item-idx">01</div>
            <div class="item-main">
              <div class="item-left"><div class="item-title">GPT 後台管理與論壇審核</div><div class="item-hint">// click to expand</div></div>
              <div class="item-right"><span class="item-tag tag-done">持續進行</span><span class="item-chevron">▼</span></div>
            </div>
          </div>
          <div class="item-body"><div class="item-desc">對自動回流之問題進行審核，並持續優化內容品質，確保論壇回覆的準確性與一致性。</div></div>
        </div>
        <div class="item" onclick="toggleItem(this)">
          <div class="item-header">
            <div class="item-idx">02</div>
            <div class="item-main">
              <div class="item-left"><div class="item-title">WinWay-GPT 題庫建置</div><div class="item-hint">// click to expand</div></div>
              <div class="item-right"><span class="item-tag tag-done">✓ 完成</span><span class="item-chevron">▼</span></div>
            </div>
          </div>
          <div class="item-body"><div class="item-desc">進行各類型題庫建置，並優化與擴充內容品質，提升題目多樣性與涵蓋率。</div></div>
        </div>
        <div class="item" onclick="toggleItem(this)">
          <div class="item-header">
            <div class="item-idx">03</div>
            <div class="item-main">
              <div class="item-left"><div class="item-title">LLM 與 JSON 格式轉換</div><div class="item-hint">// click to expand</div></div>
              <div class="item-right"><span class="item-tag tag-done">✓ 完成</span><span class="item-chevron">▼</span></div>
            </div>
          </div>
          <div class="item-body"><div class="item-desc">結合 LLM 技術，將非結構化資料轉換為標準化 JSON 格式，提升資料處理效率與可維護性。</div></div>
        </div>
        <div class="item" onclick="toggleItem(this)">
          <div class="item-header">
            <div class="item-idx">04</div>
            <div class="item-main">
              <div class="item-left"><div class="item-title">HTML 網頁開發</div><div class="item-hint">// click to expand</div></div>
              <div class="item-right"><span class="item-tag tag-done">✓ 完成</span><span class="item-chevron">▼</span></div>
            </div>
          </div>
          <div class="item-body"><div class="item-desc">完成行程頁面、清單開發與功能擴充，加入 localStorage 記憶功能、Google Maps 連結與每日花費紀錄器。</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- Slide 3: 未來兩周 -->
  <div class="slide">
    <div class="slide-inner">
      <div class="section-chip">02 · Upcoming · 03/19 – 04/02</div>
      <div class="slide-title"><div class="slide-title-bar"></div>未來兩周計畫</div>
      <div class="item-list">
        <div class="item" onclick="toggleItem(this)">
          <div class="item-header">
            <div class="item-idx">01</div>
            <div class="item-main">
              <div class="item-left"><div class="item-title">Python 自動化開發</div><div class="item-hint">// click to expand</div></div>
              <div class="item-right"><span class="item-tag tag-progress">進行中</span><span class="item-chevron">▼</span></div>
            </div>
          </div>
          <div class="item-body"><div class="item-desc">學習 Python 自動化相關工具與套件，實際撰寫測試腳本，探索自動化流程應用於日常工作的可能性。</div></div>
        </div>
        <div class="item" onclick="toggleItem(this)">
          <div class="item-header">
            <div class="item-idx">02</div>
            <div class="item-main">
              <div class="item-left"><div class="item-title">LLM + Python 簡單自動化</div><div class="item-hint">// click to expand</div></div>
              <div class="item-right"><span class="item-tag tag-pending">待開始</span><span class="item-chevron">▼</span></div>
            </div>
          </div>
          <div class="item-body"><div class="item-desc">結合 LLM 與 Python，實作簡單的 AI 自動化流程，例如自動摘要、文字分類或自動回覆，探索 AI 應用於實際工作場景的可能性。</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- Slide 4: 困難與解決 -->
  <div class="slide">
    <div class="slide-inner">
      <div class="section-chip">03 · Challenges & Solutions</div>
      <div class="slide-title"><div class="slide-title-bar"></div>困難與解決方式</div>
      <div class="problem-hint">Click each card to reveal the solution</div>

      <div class="problem-card" onclick="toggleProblem(this)">
        <div class="problem-top">
          <span class="p-label l-issue">ISSUE</span>
          <span class="p-text">HTML 結構標籤未正確關閉，導致「旅程圓滿結束」區塊跑到每個頁面都顯示。</span>
          <span class="p-arrow">▼</span>
        </div>
        <div class="problem-bottom">
          <span class="p-label l-solve">SOLVE</span>
          <span class="p-text-solve">逐層檢查 div 的開合，找到 Day 5 頁面提早關閉 day-page 的問題，將 Final Message 移回正確的父層內。</span>
        </div>
      </div>

      <div class="problem-card" onclick="toggleProblem(this)">
        <div class="problem-top">
          <span class="p-label l-issue">ISSUE</span>
          <span class="p-text">官方網站圖片有防盜連結保護，直接引用 src 無法顯示圖片。</span>
          <span class="p-arrow">▼</span>
        </div>
        <div class="problem-bottom">
          <span class="p-label l-solve">SOLVE</span>
          <span class="p-text-solve">改為自行下載圖片後放入專案資料夾，以本地路徑引用，或改用 emoji 大圖示替代。</span>
        </div>
      </div>

      <div class="problem-card" onclick="toggleProblem(this)">
        <div class="problem-top">
          <span class="p-label l-issue">ISSUE</span>
          <span class="p-text">重新整理後自訂清單與勾選狀態全部消失，使用體驗不佳。</span>
          <span class="p-arrow">▼</span>
        </div>
        <div class="problem-bottom">
          <span class="p-label l-solve">SOLVE</span>
          <span class="p-text-solve">將所有清單資料與勾選狀態改存至 localStorage，並在 DOMContentLoaded 時自動讀取還原。</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Slide 5: AI 趨勢 -->
  <div class="slide">
    <div class="slide-inner">
      <div class="section-chip">04 · AI Trend · 2025</div>
      <div class="slide-title"><div class="slide-title-bar"></div>AI 趨勢工具分享</div>
      <div class="ai-card">
        <div class="ai-card-top-bar"></div>
        <div class="ai-card-inner">
          <div class="ai-chip">TRENDING NOW · 2025</div>
          <div class="ai-title">Vibe <span class="grad">Coding</span></div>
          <div class="ai-desc">由 AI 研究者 Andrej Karpathy 提出的全新開發方式——不需要懂程式語法，用自然語言描述需求，由 AI 負責實作，人負責提需求與測試。大幅降低開發門檻，讓非工程師也能做出完整產品。</div>
          <div class="ai-grid">
            <div class="ai-point"><div class="ai-dot"></div><span>Claude / ChatGPT — 對話式生成與修改程式碼</span></div>
            <div class="ai-point"><div class="ai-dot"></div><span>Cursor — AI 整合進程式編輯器，即時協作開發</span></div>
            <div class="ai-point"><div class="ai-dot"></div><span>Bolt.new / Replit — 直接生成並部署完整專案</span></div>
            <div class="ai-point"><div class="ai-dot"></div><span>未來重點：會跟 AI 溝通需求 > 會寫程式</span></div>
          </div>
        </div>
      </div>
    </div>
  </div>

</div>

<div class="nav-bar">
  <button class="nav-btn" id="btn-prev" onclick="navigate(-1)" disabled><span>← Prev</span></button>
  <div class="nav-center">
    <div class="nav-dots" id="nav-dots"></div>
    <div class="nav-counter" id="nav-counter">01 / 05</div>
  </div>
  <button class="nav-btn" id="btn-next" onclick="navigate(1)"><span>Next →</span></button>
</div>

<div class="key-hint">← → to navigate</div>

<script>
  const slides = document.querySelectorAll('.slide');
  const total = slides.length;
  let current = 0;

  const dotsEl = document.getElementById('nav-dots');
  for (let i = 0; i < total; i++) {
    const d = document.createElement('div');
    d.className = 'nav-dot' + (i === 0 ? ' active' : '');
    d.onclick = () => goTo(i);
    dotsEl.appendChild(d);
  }

  function updateUI() {
    document.getElementById('progress-fill').style.width = ((current + 1) / total * 100) + '%';
    document.getElementById('nav-counter').textContent =
      String(current + 1).padStart(2, '0') + ' / ' + String(total).padStart(2, '0');
    document.querySelectorAll('.nav-dot').forEach((d, i) => d.classList.toggle('active', i === current));
    document.getElementById('btn-prev').disabled = current === 0;
    document.getElementById('btn-next').disabled = current === total - 1;
  }

  function goTo(index) {
    if (index < 0 || index >= total || index === current) return;
    slides[current].classList.remove('active');
    slides[current].classList.add('exit-left');
    const prev = current;
    current = index;
    setTimeout(() => slides[prev].classList.remove('exit-left'), 380);
    slides[current].classList.add('active');
    updateUI();
  }

  function navigate(dir) { goTo(current + dir); }

  document.addEventListener('keydown', e => {
    if (e.key === 'ArrowRight' || e.key === 'ArrowDown') navigate(1);
    if (e.key === 'ArrowLeft' || e.key === 'ArrowUp') navigate(-1);
  });

  function toggleItem(el) {
    const isOpen = el.classList.contains('open');
    el.closest('.item-list').querySelectorAll('.item.open').forEach(i => {
      i.classList.remove('open');
      i.querySelector('.item-hint').textContent = '// click to expand';
    });
    if (!isOpen) {
      el.classList.add('open');
      el.querySelector('.item-hint').textContent = '// click to collapse';
    }
  }

  function toggleProblem(el) { el.classList.toggle('open'); }

  updateUI();
</script>
</body>
</html>
