<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>雙周報</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;600&family=DM+Serif+Display&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink: #1a1a2e;
    --mid: #6b7280;
    --light: #f0f4f8;
    --accent: #2563eb;
    --accent-light: #eff6ff;
    --border: #e5e7eb;
    --white: #ffffff;
    --success: #059669;
    --warning: #d97706;
  }

  body {
    font-family: 'Noto Sans TC', sans-serif;
    background: var(--light);
    color: var(--ink);
    min-height: 100vh;
    padding: 2rem 1rem;
  }

  .container {
    max-width: 780px;
    margin: 0 auto;
  }

  /* Header */
  .report-header {
    background: var(--white);
    border-radius: 12px;
    padding: 2.5rem;
    margin-bottom: 1.5rem;
    border-left: 4px solid var(--accent);
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 1rem;
  }
  .report-title {
    font-family: 'DM Serif Display', serif;
    font-size: 2rem;
    color: var(--ink);
    line-height: 1.2;
    margin-bottom: .4rem;
  }
  .report-subtitle {
    font-size: .85rem;
    color: var(--mid);
    letter-spacing: .05em;
  }
  .report-meta {
    text-align: right;
    flex-shrink: 0;
  }
  .report-date {
    font-size: .8rem;
    color: var(--mid);
    margin-bottom: .3rem;
  }
  .report-badge {
    display: inline-block;
    background: var(--accent-light);
    color: var(--accent);
    font-size: .75rem;
    font-weight: 600;
    padding: .3rem .8rem;
    border-radius: 20px;
    letter-spacing: .05em;
  }

  /* Section */
  .section {
    background: var(--white);
    border-radius: 12px;
    padding: 2rem;
    margin-bottom: 1.5rem;
  }
  .section-header {
    display: flex;
    align-items: center;
    gap: .75rem;
    margin-bottom: 1.5rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid var(--border);
  }
  .section-icon {
    width: 36px;
    height: 36px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.1rem;
    flex-shrink: 0;
  }
  .icon-blue { background: var(--accent-light); }
  .icon-green { background: #ecfdf5; }
  .icon-yellow { background: #fffbeb; }
  .icon-purple { background: #f5f3ff; }

  .section-title {
    font-size: 1rem;
    font-weight: 600;
    color: var(--ink);
  }
  .section-period {
    font-size: .75rem;
    color: var(--mid);
    margin-left: auto;
  }

  /* Items */
  .item-list { display: flex; flex-direction: column; gap: .8rem; }
  .item {
    display: flex;
    gap: .8rem;
    align-items: flex-start;
    padding: .9rem 1rem;
    background: var(--light);
    border-radius: 8px;
    transition: background .2s;
  }
  .item:hover { background: #e8edf2; }
  .item-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    margin-top: .4rem;
    flex-shrink: 0;
  }
  .dot-blue { background: var(--accent); }
  .dot-green { background: var(--success); }
  .dot-yellow { background: var(--warning); }
  .dot-purple { background: #7c3aed; }

  .item-content { flex: 1; }
  .item-title {
    font-size: .88rem;
    font-weight: 500;
    color: var(--ink);
    margin-bottom: .2rem;
  }
  .item-desc {
    font-size: .8rem;
    color: var(--mid);
    line-height: 1.6;
  }
  .item-tag {
    display: inline-block;
    font-size: .7rem;
    padding: .15rem .5rem;
    border-radius: 4px;
    margin-top: .3rem;
    font-weight: 500;
  }
  .tag-done { background: #ecfdf5; color: var(--success); }
  .tag-progress { background: var(--accent-light); color: var(--accent); }
  .tag-pending { background: #fffbeb; color: var(--warning); }

  /* Problem & Solution */
  .problem-card {
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
    margin-bottom: .8rem;
  }
  .problem-top {
    padding: .9rem 1rem;
    background: #fff7ed;
    border-bottom: 1px solid #fed7aa;
    display: flex;
    gap: .6rem;
    align-items: flex-start;
  }
  .problem-bottom {
    padding: .9rem 1rem;
    background: #f0fdf4;
    display: flex;
    gap: .6rem;
    align-items: flex-start;
  }
  .problem-label {
    font-size: .7rem;
    font-weight: 600;
    letter-spacing: .08em;
    flex-shrink: 0;
    margin-top: .1rem;
  }
  .label-problem { color: var(--warning); }
  .label-solution { color: var(--success); }
  .problem-text {
    font-size: .83rem;
    color: var(--ink);
    line-height: 1.6;
  }

  /* AI Section */
  .ai-card {
    background: linear-gradient(135deg, #1e3a5f 0%, #1e40af 100%);
    border-radius: 10px;
    padding: 1.5rem;
    color: white;
    position: relative;
    overflow: hidden;
  }
  .ai-card::before {
    content: '';
    position: absolute;
    top: -30px; right: -30px;
    width: 120px; height: 120px;
    border-radius: 50%;
    background: rgba(255,255,255,.05);
  }
  .ai-card-title {
    font-size: 1rem;
    font-weight: 600;
    margin-bottom: .4rem;
    display: flex;
    align-items: center;
    gap: .5rem;
  }
  .ai-card-tag {
    font-size: .7rem;
    background: rgba(255,255,255,.2);
    padding: .2rem .6rem;
    border-radius: 20px;
    letter-spacing: .05em;
  }
  .ai-card-desc {
    font-size: .83rem;
    line-height: 1.8;
    opacity: .9;
    margin-bottom: 1rem;
  }
  .ai-card-points {
    display: flex;
    flex-direction: column;
    gap: .4rem;
  }
  .ai-point {
    font-size: .78rem;
    opacity: .85;
    display: flex;
    gap: .5rem;
  }
  .ai-point::before { content: '→'; opacity: .6; flex-shrink: 0; }

  /* Footer */
  .report-footer {
    text-align: center;
    padding: 1.5rem;
    font-size: .75rem;
    color: var(--mid);
  }

  @media (max-width: 600px) {
    .report-header { flex-direction: column; }
    .report-meta { text-align: left; }
    .section { padding: 1.5rem; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- Header -->
  <div class="report-header">
    <div>
      <div class="report-title">雙周報</div>
      <div class="report-subtitle">Bi-Weekly Report · 工作進度更新</div>
    </div>
    <div class="report-meta">
      <div class="report-date">2025 / 03 / 17</div>
      <div class="report-badge">Week 05 – 06</div>
    </div>
  </div>

  <!-- 過去兩周 -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-blue">📋</div>
      <div>
        <div class="section-title">過去兩周完成事項</div>
      </div>
      <div class="section-period">03/03 – 03/16</div>
    </div>
    <div class="item-list">
      <div class="item">
        <div class="item-dot dot-blue"></div>
        <div class="item-content">
          <div class="item-title">旅遊網頁開發</div>
          <div class="item-desc">完成五天行程頁面、購物清單、行李清單，並加入 localStorage 記憶功能與 Google Maps 連結。</div>
          <span class="item-tag tag-done">✓ 完成</span>
        </div>
      </div>
      <div class="item">
        <div class="item-dot dot-blue"></div>
        <div class="item-content">
          <div class="item-title">每日花費紀錄器</div>
          <div class="item-desc">為每個行程日新增花費輸入與自動加總功能，資料儲存至 localStorage。</div>
          <span class="item-tag tag-done">✓ 完成</span>
        </div>
      </div>
      <div class="item">
        <div class="item-dot dot-blue"></div>
        <div class="item-content">
          <div class="item-title">旅遊須知頁面擴充</div>
          <div class="item-desc">新增 72 小時地鐵券、Skyliner、Suica 西瓜卡使用指南區塊。</div>
          <span class="item-tag tag-done">✓ 完成</span>
        </div>
      </div>
      <div class="item">
        <div class="item-dot dot-blue"></div>
        <div class="item-content">
          <div class="item-title">手機版按鈕跑版修復</div>
          <div class="item-desc">修正自訂清單輸入框在手機上新增按鈕消失的問題，加入 flex-shrink 與 min-width 修正。</div>
          <span class="item-tag tag-done">✓ 完成</span>
        </div>
      </div>
    </div>
  </div>

  <!-- 未來兩周 -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-green">🎯</div>
      <div>
        <div class="section-title">未來兩周計畫</div>
      </div>
      <div class="section-period">03/17 – 03/30</div>
    </div>
    <div class="item-list">
      <div class="item">
        <div class="item-dot dot-green"></div>
        <div class="item-content">
          <div class="item-title">旅遊備忘錄功能開發</div>
          <div class="item-desc">新增每日備忘錄區塊，支援輸入與 localStorage 儲存，方便旅途中記錄臨時事項。</div>
          <span class="item-tag tag-progress">進行中</span>
        </div>
      </div>
      <div class="item">
        <div class="item-dot dot-green"></div>
        <div class="item-content">
          <div class="item-title">預算計算器頁面</div>
          <div class="item-desc">新增獨立預算頁面，可設定總預算，並自動加總各天花費，顯示剩餘預算。</div>
          <span class="item-tag tag-pending">待開始</span>
        </div>
      </div>
      <div class="item">
        <div class="item-dot dot-green"></div>
        <div class="item-content">
          <div class="item-title">出發前提醒清單</div>
          <div class="item-desc">規劃出發當天必做事項清單，例如確認護照、充電、列印票券等，並支援勾選記憶。</div>
          <span class="item-tag tag-pending">待開始</span>
        </div>
      </div>
    </div>
  </div>

  <!-- 困難與解決 -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-yellow">⚠️</div>
      <div>
        <div class="section-title">遇到的困難與解決方式</div>
      </div>
    </div>

    <div class="problem-card">
      <div class="problem-top">
        <span class="problem-label label-problem">困難</span>
        <span class="problem-text">HTML 結構標籤未正確關閉，導致「旅程圓滿結束」區塊跑到每個頁面都顯示。</span>
      </div>
      <div class="problem-bottom">
        <span class="problem-label label-solution">解決</span>
        <span class="problem-text">逐層檢查 div 的開合，找到 Day 5 頁面提早關閉 day-page 的問題，將 Final Message 移回正確的父層內。</span>
      </div>
    </div>

    <div class="problem-card">
      <div class="problem-top">
        <span class="problem-label label-problem">困難</span>
        <span class="problem-text">官方網站圖片有防盜連結保護，直接引用 src 無法顯示圖片。</span>
      </div>
      <div class="problem-bottom">
        <span class="problem-label label-solution">解決</span>
        <span class="problem-text">改為自行下載圖片後放入專案資料夾，以本地路徑引用，或改用 emoji 大圖示替代。</span>
      </div>
    </div>

    <div class="problem-card">
      <div class="problem-top">
        <span class="problem-label label-problem">困難</span>
        <span class="problem-text">重新整理後自訂清單與勾選狀態全部消失，使用體驗不佳。</span>
      </div>
      <div class="problem-bottom">
        <span class="problem-label label-solution">解決</span>
        <span class="problem-text">將所有清單資料與勾選狀態改存至 localStorage，並在 DOMContentLoaded 時自動讀取還原。</span>
      </div>
    </div>
  </div>

  <!-- AI 趨勢 -->
  <div class="section">
    <div class="section-header">
      <div class="section-icon icon-purple">🤖</div>
      <div>
        <div class="section-title">AI 趨勢工具分享</div>
      </div>
    </div>
    <div class="ai-card">
      <div class="ai-card-title">
        Vibe Coding
        <span class="ai-card-tag">2025 趨勢</span>
      </div>
      <div class="ai-card-desc">
        由 AI 研究者 Andrej Karpathy 提出的全新開發方式——不需要懂程式語法，用自然語言描述需求，由 AI 負責實作，人負責提需求與測試。大幅降低開發門檻，讓非工程師也能做出完整產品。
      </div>
      <div class="ai-card-points">
        <div class="ai-point">Claude / ChatGPT — 對話式生成與修改程式碼</div>
        <div class="ai-point">Cursor — AI 整合進程式編輯器，即時協作開發</div>
        <div class="ai-point">Bolt.new / Replit — 直接生成並部署完整網頁專案</div>
        <div class="ai-point">未來重點不是「會不會寫程式」，而是「會不會跟 AI 溝通需求」</div>
      </div>
    </div>
  </div>

  <div class="report-footer">
    © 2025 雙周報 · Bi-Weekly Report
  </div>

</div>
</body>
</html>
