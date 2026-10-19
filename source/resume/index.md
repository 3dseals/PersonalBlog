---
title: 个人简历
date: 2025-12-30 11:00:00
comments: false
---

<style>
/* ========== 下载PDF按钮 ========== */
.resume-header-top {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
  position: relative;
  z-index: 1;
}
.pdf-download-btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 8px 20px;
  background: rgba(255,255,255,0.15);
  color: #7dd3fc;
  border: 1px solid rgba(125,211,252,0.3);
  border-radius: 24px;
  font-size: 0.85em;
  font-family: inherit;
  cursor: pointer;
  backdrop-filter: blur(4px);
  transition: all 0.3s ease;
  text-decoration: none;
  white-space: nowrap;
}
.pdf-download-btn:hover {
  background: rgba(255,255,255,0.25);
  color: #fff;
  border-color: rgba(255,255,255,0.5);
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(125,211,252,0.25);
}

/* ========== 打印/PDF导出样式 ========== */
@media print {
  /* 隐藏tranquilpeak主题导航与装饰元素 */
  #sidebar, .sidebar,
  #header, header,
  #bottom-bar, .post-bottom-bar,
  .post-header-cover, .header-cover,
  .share-options-bar,
  .post-actions-wrap, .post-footer,
  .post-meta, .post-header,
  .pagination, footer, .footer,
  nav, #main-nav, .main-nav,
  .cover, .about,
  .share-options, .post-nav,
  .comment, .comments, #comments,
  .pdf-download-btn,
  .post-toc, .toc,
  .alert {
    display: none !important;
  }

  body, html {
    margin: 0 !important;
    padding: 0 !important;
    background: #fff !important;
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
  }

  #blog, #main {
    margin: 0 !important;
    padding: 0 !important;
  }

  .post, .post-content, .post-body, .page, .main {
    margin: 0 !important;
    padding: 0 !important;
    max-width: 100% !important;
    width: 100% !important;
    box-shadow: none !important;
    border: none !important;
  }

  .resume-header {
    margin: 0 0 20px 0 !important;
    border-radius: 0 !important;
    padding: 30px 20px !important;
  }

  .timeline-item, .project-card, .advantage-card {
    break-inside: avoid;
    page-break-inside: avoid;
  }

  .section-title {
    break-after: avoid;
    page-break-after: avoid;
    margin: 24px 0 16px 0 !important;
  }

  @page {
    margin: 1cm;
    size: A4;
  }
}

/* ========== 简历全局美化样式 ========== */
.post-body {
  font-family: 'PingFang SC', 'Microsoft YaHei', -apple-system, BlinkMacSystemFont, sans-serif;
}

/* 简历头部区域 */
.resume-header {
  text-align: center;
  padding: 40px 30px;
  background: linear-gradient(135deg, #0f2027 0%, #203a43 50%, #2c5364 100%);
  border-radius: 16px;
  margin-bottom: 32px;
  position: relative;
  overflow: hidden;
}
.resume-header::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255,255,255,0.05) 0%, transparent 70%);
  animation: headerGlow 8s ease-in-out infinite;
}
@keyframes headerGlow {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(5%, 5%); }
}
.resume-header h1 {
  color: #fff !important;
  font-size: 2.4em !important;
  margin: 0 0 12px 0 !important;
  letter-spacing: 4px;
  position: relative;
  z-index: 1;
  border: none !important;
}
.resume-header .subtitle {
  color: rgba(255,255,255,0.75);
  font-size: 1.05em;
  letter-spacing: 2px;
  position: relative;
  z-index: 1;
}
.resume-header .tag-list {
  margin-top: 18px;
  position: relative;
  z-index: 1;
}
.resume-header .tag-list span {
  display: inline-block;
  background: rgba(255,255,255,0.12);
  color: #7dd3fc;
  padding: 5px 16px;
  border-radius: 20px;
  font-size: 0.85em;
  margin: 4px 6px;
  backdrop-filter: blur(4px);
  border: 1px solid rgba(125,211,252,0.2);
}

/* 通用Section标题 */
.section-title {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1.5em !important;
  color: #1e3a5f !important;
  border-bottom: 3px solid;
  border-image: linear-gradient(90deg, #3b82f6, #06b6d4, transparent) 1;
  padding-bottom: 10px;
  margin: 40px 0 24px 0 !important;
}
.section-title .icon {
  font-size: 1.2em;
}

/* 信息卡片网格 */
.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 14px;
  margin-bottom: 24px;
}
.info-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 14px 18px;
  background: linear-gradient(135deg, #f8fafc, #f1f5f9);
  border-radius: 10px;
  border-left: 3px solid #3b82f6;
  transition: all 0.3s ease;
}
.info-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(59,130,246,0.12);
}
.info-item .label {
  font-size: 0.85em;
  color: #64748b;
  min-width: 60px;
}
.info-item .value {
  font-weight: 600;
  color: #1e293b;
}
.info-item .value a {
  color: #3b82f6;
  text-decoration: none;
}
.info-item .value a:hover {
  text-decoration: underline;
}

/* 联系方式卡片 */
.contact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 12px;
  margin-bottom: 24px;
}
.contact-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 12px 16px;
  background: #fff;
  border-radius: 10px;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
}
.contact-item:hover {
  border-color: #3b82f6;
  box-shadow: 0 2px 8px rgba(59,130,246,0.1);
}
.contact-item .contact-icon {
  font-size: 1.4em;
  width: 36px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #eff6ff, #dbeafe);
  border-radius: 8px;
}
.contact-item .contact-text {
  color: #334155;
  font-size: 0.95em;
}
.contact-item .contact-text a {
  color: #3b82f6;
  text-decoration: none;
}

/* 核心优势卡片 */
.advantage-cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin-bottom: 24px;
}
.advantage-card {
  padding: 24px;
  border-radius: 12px;
  background: #fff;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}
.advantage-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
}
.advantage-card:nth-child(1)::before { background: linear-gradient(90deg, #3b82f6, #06b6d4); }
.advantage-card:nth-child(2)::before { background: linear-gradient(90deg, #8b5cf6, #ec4899); }
.advantage-card:nth-child(3)::before { background: linear-gradient(90deg, #f59e0b, #ef4444); }
.advantage-card:nth-child(4)::before { background: linear-gradient(90deg, #10b981, #06b6d4); }
.advantage-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.08);
}
.advantage-card h4 {
  margin: 0 0 14px 0 !important;
  font-size: 1.1em;
  color: #1e293b;
}
.advantage-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.advantage-card ul li {
  padding: 5px 0;
  color: #475569;
  font-size: 0.92em;
  position: relative;
  padding-left: 18px;
}
.advantage-card ul li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: #3b82f6;
  font-weight: bold;
}

/* 技术栈区域 */
.tech-section {
  margin-bottom: 28px;
}
.tech-category {
  margin-bottom: 24px;
}
.tech-category h4 {
  color: #334155 !important;
  font-size: 1em;
  margin-bottom: 12px !important;
  padding-left: 12px;
  border-left: 3px solid #3b82f6;
}
.skill-bar {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
  gap: 12px;
}
.skill-name {
  min-width: 120px;
  font-size: 0.9em;
  color: #475569;
  font-weight: 500;
}
.skill-track {
  flex: 1;
  height: 22px;
  background: #f1f5f9;
  border-radius: 11px;
  overflow: hidden;
  position: relative;
}
.skill-fill {
  height: 100%;
  border-radius: 11px;
  transition: width 1.5s ease;
  position: relative;
}
.skill-fill.expert { background: linear-gradient(90deg, #3b82f6, #06b6d4); }
.skill-fill.proficient { background: linear-gradient(90deg, #8b5cf6, #a78bfa); }
.skill-fill.skilled { background: linear-gradient(90deg, #f59e0b, #fbbf24); }
.skill-level {
  font-size: 0.78em;
  color: #94a3b8;
  min-width: 36px;
  text-align: right;
}

/* 工作经历时间线 */
.timeline {
  position: relative;
  padding-left: 32px;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 10px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: linear-gradient(180deg, #3b82f6, #06b6d4, #8b5cf6);
}
.timeline-item {
  position: relative;
  margin-bottom: 32px;
  padding: 24px;
  background: #fff;
  border-radius: 12px;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
}
.timeline-item:hover {
  box-shadow: 0 4px 16px rgba(0,0,0,0.06);
  border-color: #93c5fd;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: -28px;
  top: 28px;
  width: 12px;
  height: 12px;
  background: #3b82f6;
  border-radius: 50%;
  border: 3px solid #dbeafe;
  z-index: 1;
}
.timeline-item .period {
  display: inline-block;
  background: linear-gradient(135deg, #3b82f6, #2563eb);
  color: #fff;
  padding: 4px 14px;
  border-radius: 20px;
  font-size: 0.85em;
  margin-bottom: 8px;
}
.timeline-item .company {
  font-size: 1.2em;
  font-weight: 700;
  color: #1e293b;
  margin: 6px 0;
}
.timeline-item .position {
  color: #3b82f6;
  font-weight: 600;
  font-size: 0.95em;
  margin-bottom: 8px;
}
.timeline-item .company-desc {
  color: #64748b;
  font-size: 0.88em;
  font-style: italic;
  margin-bottom: 12px;
  padding: 8px 12px;
  background: #f8fafc;
  border-radius: 8px;
}
.timeline-item .duties {
  list-style: none;
  padding: 0;
  margin: 0;
}
.timeline-item .duties li {
  padding: 4px 0 4px 20px;
  color: #475569;
  font-size: 0.92em;
  position: relative;
}
.timeline-item .duties li::before {
  content: '✦';
  position: absolute;
  left: 0;
  color: #06b6d4;
  font-size: 0.7em;
  top: 7px;
}
.timeline-item .highlight {
  color: #ea580c !important;
  font-weight: 600;
}

/* 项目经历卡片 */
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
  gap: 20px;
  margin-bottom: 24px;
}
.project-card {
  padding: 24px;
  border-radius: 12px;
  background: #fff;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}
.project-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.08);
}
.project-card .project-year {
  position: absolute;
  top: 16px;
  right: 16px;
  background: linear-gradient(135deg, #f1f5f9, #e2e8f0);
  color: #475569;
  padding: 3px 12px;
  border-radius: 12px;
  font-size: 0.8em;
  font-weight: 600;
}
.project-card .project-name {
  font-size: 1.2em;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 6px;
}
.project-card .project-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 14px;
}
.project-card .project-meta span {
  display: inline-block;
  padding: 3px 10px;
  border-radius: 6px;
  font-size: 0.78em;
  font-weight: 500;
}
.project-card .project-meta .type {
  background: #eff6ff;
  color: #2563eb;
}
.project-card .project-meta .role {
  background: #f0fdf4;
  color: #16a34a;
}
.project-card .project-meta .revenue {
  background: #fff7ed;
  color: #ea580c;
}
.project-card .tech-list {
  list-style: none;
  padding: 0;
  margin: 0;
}
.project-card .tech-list > li {
  padding: 4px 0 4px 16px;
  color: #475569;
  font-size: 0.88em;
  position: relative;
}
.project-card .tech-list > li::before {
  content: '›';
  position: absolute;
  left: 2px;
  color: #3b82f6;
  font-weight: bold;
  font-size: 1.2em;
  top: 2px;
}
.project-card .tech-list ul {
  list-style: none;
  padding: 2px 0 4px 8px;
  margin: 0;
}
.project-card .tech-list ul li {
  padding: 2px 0 2px 14px;
  color: #64748b;
  font-size: 0.96em;
  position: relative;
}
.project-card .tech-list ul li::before {
  content: '•';
  position: absolute;
  left: 2px;
  color: #06b6d4;
  font-size: 0.9em;
  top: 1px;
}

/* 技术总结表格 */
.tech-summary-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 1px 3px rgba(0,0,0,0.06);
  margin-bottom: 24px;
}
.tech-summary-table thead th {
  background: linear-gradient(135deg, #1e3a5f, #2c5364);
  color: #fff;
  padding: 14px 18px;
  font-weight: 600;
  font-size: 0.95em;
  text-align: left;
}
.tech-summary-table tbody td {
  padding: 12px 18px;
  border-bottom: 1px solid #f1f5f9;
  font-size: 0.9em;
}
.tech-summary-table tbody tr:nth-child(even) {
  background: #f8fafc;
}
.tech-summary-table tbody tr:hover {
  background: #eff6ff;
}
.tech-summary-table tbody td:first-child {
  font-weight: 600;
  color: #1e3a5f;
  white-space: nowrap;
}
.tech-summary-table tbody td:last-child {
  color: #475569;
}

/* 致谢区域 */
.thanks-section {
  text-align: center;
  padding: 36px 30px;
  background: linear-gradient(135deg, #f8fafc, #eff6ff);
  border-radius: 16px;
  margin-top: 32px;
  border: 1px solid #dbeafe;
}
.thanks-section p {
  color: #475569;
  line-height: 1.8;
  max-width: 640px;
  margin: 0 auto 12px auto;
  font-size: 0.95em;
}
.thanks-section .signature {
  font-weight: 700;
  color: #1e3a5f;
  font-size: 1.1em;
  margin-top: 16px;
}

/* 响应式 */
@media (max-width: 640px) {
  .resume-header h1 { font-size: 1.6em !important; }
  .info-grid, .contact-grid { grid-template-columns: 1fr; }
  .advantage-cards { grid-template-columns: 1fr; }
  .project-grid { grid-template-columns: 1fr; }
  .timeline { padding-left: 24px; }
  .skill-name { min-width: 90px; font-size: 0.82em; }
}
</style>

<div class="resume-header">
  <div class="resume-header-top">
    <h1>王子亮</h1>
    <button class="pdf-download-btn" onclick="window.print()" title="点击后在打印对话框中选择另存为PDF">&#128196; 下载PDF</button>
  </div>
  <div class="subtitle">Unity全栈开发工程师</div>
  <div class="tag-list">
    <span>15年+研发经验</span>
    <span>游戏 / 社交 / AI</span>
    <span>Unity全栈开发</span>
  </div>
</div>

<h2 class="section-title"><span class="icon">📋</span> 基本信息</h2>

<div class="info-grid">
  <div class="info-item">
    <span class="label">姓名</span>
    <span class="value">王子亮 / 男 / 1987</span>
  </div>
  <div class="info-item">
    <span class="label">学历</span>
    <span class="value">本科 211 · 哈尔滨工程大学 · 计算机科学与技术</span>
  </div>
  <div class="info-item">
    <span class="label">工作年限</span>
    <span class="value">15年+</span>
  </div>
  <div class="info-item">
    <span class="label">期望职位</span>
    <span class="value">游戏全栈开发工程师</span>
  </div>
  <div class="info-item">
    <span class="label">期望薪资</span>
    <span class="value">20K - 30K</span>
  </div>
  <div class="info-item">
    <span class="label">期望城市</span>
    <span class="value">成都</span>
  </div>
</div>

<h2 class="section-title"><span class="icon">📞</span> 联系方式</h2>

<div class="contact-grid">
  <div class="contact-item">
    <div class="contact-icon">📱</div>
    <div class="contact-text">15802857662</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">📧</div>
    <div class="contact-text">lional.king@gmail.com</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">💬</div>
    <div class="contact-text">QQ: 870966629</div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">🔗</div>
    <div class="contact-text"><a href="https://ibunnyteam.github.io" target="_blank">ibunnyteam.github.io</a></div>
  </div>
  <div class="contact-item">
    <div class="contact-icon">🐙</div>
    <div class="contact-text"><a href="https://github.com/3dseals" target="_blank">github.com/3dseals</a></div>
  </div>
</div>

<br>
<br>
<br>
<br>

<h2 class="section-title"><span class="icon">💡</span> 核心优势</h2>

<div class="advantage-cards">
  <div class="advantage-card">
    <h4>🎯 全栈技术覆盖</h4>
    <ul>
      <li><strong>客户端</strong>：精通 Unity3D (C#) / Cocos Creator (TS/JS) / Cocos2d-x (C++)</li>
      <li><strong>服务端</strong>：熟练运用 C# (.NET) / Golang / Java / Skynet / C++</li>
      <li><strong>高并发 & 数据</strong>：MySQL / Redis / MongoDB / 分布式长连接 / 内存优化</li>
      <li><strong>工程化</strong>：Git / Docker / CI/CD 自动化流水线 / 跨平台底层 SDK 接入</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>⚡ 核心架构与技术攻坚</h4>
    <ul>
      <li><strong>网络与同步</strong>：主导自研高并发 WebSocket / Socket 实时对战与房间同步架构</li>
      <li><strong>性能深度调优</strong>：深谙 DrawCall 优化、内存泄漏定位、对象池与包体瘦身</li>
      <li><strong>热更新与底层</strong>：精通 华佗 (HybridCLR) / ILRuntime / Lua 热更引擎框架及 C++ 引擎绑定实战</li>
      <li><strong>业务闭环能力</strong>：具备从底层引擎、核心玩法、高并发网络到运营落地的全链路开发能力</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>📊 业务与实战成果</h4>
    <ul>
      <li>累计参与商业化项目流水超 <strong>1亿+</strong>，单项目最高年流水 <strong>5000万+</strong></li>
      <li>主导 <strong>10+</strong> 款游戏从 0 到 1 架构设计与全栈研发上线</li>
      <li>品类覆盖广泛：<strong>3D虚拟社交对战 / SLG策略 / 商业手游 / H5小游戏矩阵</strong></li>
      <li>具备敏锐的商业化意识与数值运营思维，保障线上系统高可用与低延时</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>⚔️ Unity3D 核心战斗与 MMO 架构</h4>
    <ul>
      <li><strong>战斗模块研发</strong>：深度掌握 MMORPG 核心战斗系统，包括状态机 (FSM)、技能管线 (CD/弹道/判定/Buff结算) 及动作打击感与硬直反馈</li>
      <li><strong>MMORPG 状态同步</strong>：精通高频状态同步 (State Sync)、航位推测与插值平滑算法，设计弱网位置预测与抗抖动机制，彻底消除位移拉扯</li>
      <li><strong>Unity3D 引擎底蕴</strong>：精通 C# 底层机制与 GC 深度优化，熟练掌握 URP 管线、DrawCall 优化及内存治理</li>
    </ul>
  </div>
</div>

<br>


<h2 class="section-title"><span class="icon">💼</span> 工作经历</h2>

<div class="timeline">

<div class="timeline-item">
  <span class="period">2024.07 - 至今</span>
  <div class="company">四川循东科技有限公司</div>
  <div class="position">游戏全栈开发工程师</div>
  <div class="company-desc">专注于AI驱动的虚拟社交和数字娱乐领域的创新科技公司（Cocos Creator + Node.js）</div>
  <ul class="duties">
    <li>负责基于 Cocos Creator 的小游戏平台架构设计与全栈研发，涵盖多种H5小游戏、Block等休闲游戏品类</li>
    <li>负责核心游戏逻辑、客户端交互（Cocos Creator / TypeScript）及服务端接口设计与开发</li>
    <li>深度实践AI辅助编程（Cursor/Claude Code等），实现高质量敏捷交付与效率跃升</li>
    <li>构建小游戏聚合分发平台，打通运营、数据分析与用户增长链路</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2023.03 - 2024.06</span>
  <div class="company">麓卓互动科技有限公司（成都分公司）</div>
  <div class="position">游戏全栈开发工程师</div>
  <div class="company-desc">专注于AI社交和元宇宙领域，打造3D虚拟社交直播游戏应用《Party Yoo》（Unity3D + C#）</div>
  <ul class="duties">
    <li>负责3D虚拟社交直播游戏应用的游戏模块（Unity3D客户端）及服务端架构设计与研发</li>
    <li>设计并实现直播间实时互动游戏系统，支持主播与观众的多人实时对战互动</li>
    <li>负责高并发网络通信、状态同步与游戏核心逻辑开发</li>
    <li>保障产品在印尼等海外市场的稳定运行与持续迭代</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2013.05 - 2023.02</span>
  <div class="company">成都黑骑士网络科技</div>
  <div class="position">游戏全栈开发工程师</div>
  <div class="company-desc">创业型手游公司，拥有多款上线游戏</div>
  <ul class="duties">
    <li>主导多款商业手游全栈开发（Unity3D客户端 + Golang服务端架构）</li>
    <li>负责游戏核心架构设计、底层系统封装、性能深度优化与线上运维</li>
    <li><span class="highlight">核心项目流水累计超5000万</span></li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2011.12 - 2013.04</span>
  <div class="company">上海慕和网络</div>
  <div class="position">游戏开发工程师</div>
  <div class="company-desc">手游公司，2013年被凤凰传媒收购，月流水达1500万</div>
  <ul class="duties">
    <li>参与多款SLG游戏开发</li>
    <li>参与游戏引擎研发与平台SDK研发</li>
    <li>公司从50人发展到400人的高速成长期</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2010.07 - 2011.11</span>
  <div class="company">TCL通讯</div>
  <div class="position">Android开发工程师</div>
  <div class="company-desc">专注于Android手机研发，与阿尔卡特、黑莓等厂商合作</div>
  <ul class="duties">
    <li>负责Contacts、Launcher等核心模块开发</li>
  </ul>
</div>

</div>

<h2 class="section-title"><span class="icon">🎮</span> 项目经历</h2>

<div class="project-grid">

<div class="project-card">
  <span class="project-year">2024 - 至今</span>
  <div class="project-name">休闲游戏平台 & H5游戏矩阵</div>
  <div class="project-meta">
    <span class="type">休闲游戏平台 / 休闲游戏</span>
    <span class="role">游戏全栈开发</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Cocos Creator (TypeScript) + React.js + Node.js + Redis</li>
    <li><strong>核心职责</strong>：主导小游戏聚合分发平台架构设计，以及多款休闲小游戏（Block消除、益智解谜等）全栈研发。</li>
    <li><strong>性能调优与攻坚</strong>：
      <ul>
        <li>首包加载优化：采用分包加载策略、动态合图（AutoAtlas）与远程资源按需加载，首屏启动耗时由 4.2s 降至 1s 内。</li>
        <li>渲染与GC调优：设计通用对象池管理器，消除频繁实例化产生的内存抖动，DrawCall 降低 45%，全机型稳定 60 FPS。</li>
      </ul>
    </li>
    <li><strong>AI提效实践</strong>：深度结合 Cursor/Claude Code 进行模块代码与单元测试生成，迭代效率提升 50%+。</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2023 - 2024</span>
  <div class="project-name">Party Yoo</div>
  <div class="project-meta">
    <span class="type">3D虚拟社交直播游戏</span>
    <span class="role">全栈开发工程师</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Unity3D (C#) + C# (.NET) + WebSocket + Redis</li>
    <li><strong>核心职责</strong>：负责 3D 虚拟人直播间实时互动游戏模块（Unity3D）及高并发服务端（C#）全栈开发。</li>
    <li><strong>高并发与网络攻坚</strong>：
      <ul>
        <li>实时状态同步：设计基于 C# 的高并发 WebSocket 游戏房间系统，支持主播与上千观众毫秒级对战互动。</li>
        <li>弱网与断线重连：针对海外（印尼等）弱网环境，设计客户端状态平滑插值与快速重连补偿机制，网络卡顿率降低 50%。</li>
      </ul>
    </li>
    <li><strong>客户端渲染</strong>：优化 Unity3D 角色骨骼动画合批与 UI 层级，有效控制移动端发热与显存占用。</li>
  </ul>
</div>

<br>

<div class="project-card">
  <span class="project-year">2020</span>
  <div class="project-name">无尽之界</div>
  <div class="project-meta">
    <span class="type">沙盒冒险MMO</span>
    <span class="role">Unity游戏开发</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Unity3D (C#) + Golang + Redis + RPC通信</li>
    <li><strong>核心职责</strong>：负责客户端核心战斗系统、表现层渲染与服务端全栈开发。</li>
    <li><strong>核心攻坚与解决问题</strong>：
      <ul>
        <li>双端一致性与防作弊：采用客户端逐帧推演渲染 + 服务端关键帧轻量校验与离线收益推导，彻底杜绝篡改作弊。</li>
        <li>高吞吐并发设计：利用 Golang 异步机制配合 Redis 内存级高频 IO 缓存，单服支撑数万玩家在线高频结算。</li>
      </ul>
    </li>
    <li><strong>Shader定制</strong>：编写专属轻量级 Shader 与打击光影特效，兼顾低端机流畅度与视觉打击感。</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2019</span>
  <div class="project-name">三国诸侯纷争</div>
  <div class="project-meta">
    <span class="type">SLG策略游戏</span>
    <span class="role">全栈开发工程师</span>
    <span class="revenue">💰 200万+/半年</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Unity3D + ILRuntime + Java NIO + Protobuf</li>
    <li><strong>核心职责</strong>：负责游戏热更新底层框架、大地图视野同步与网络通信层开发。</li>
    <li><strong>核心攻坚与解决问题</strong>：
      <ul>
        <li>ILRuntime热更架构：基于纯 C# 构建跨平台热更体系，实现业务逻辑与资源全量热更，保障线上事故 0 停机修复。</li>
        <li>大地图视野与AOI算法：设计九宫格视野同步与视锥体剔除，大幅降低同屏数千单位渲染与网络同步压力。</li>
        <li>协议压缩：采用 Protobuf 二进制协议，网络包体吞吐量优化 60% 以上。</li>
      </ul>
    </li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2017</span>
  <div class="project-name">Survive 活下去</div>
  <div class="project-meta">
    <span class="type">丧尸生存角色扮演</span>
    <span class="role">客户端开发工程师</span>
    <span class="revenue">💰 500万+/年</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Cocos Creator (JS/TS) + Socket / HTTP + 本地持久化</li>
    <li><strong>核心职责</strong>：负责客户端整体架构搭建、核心生存机制实现、网络通信层封装与性能调优。</li>
    <li><strong>核心攻坚与解决问题</strong>：
      <ul>
        <li>复杂事件流与数据驱动：构建数据驱动的生存事件引擎，高效承载数十万字剧情与庞大数值系统。</li>
        <li>内存管理与防作弊：针对长生命周期游戏排查修复多处闭包与纹理泄漏；实现本地存档动态 AES 加密校验。</li>
        <li>双通道网络容灾：封装 HTTP/Socket 双通道网络通信，支持弱网智能重试与离线消息队列。</li>
      </ul>
    </li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2016</span>
  <div class="project-name">沙巴克传奇</div>
  <div class="project-meta">
    <span class="type">传奇类MMORPG</span>
    <span class="role">全栈开发</span>
    <span class="revenue">💰 500万+/半年</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Cocos2d-Lua + C++ + Lua + PHP</li>
    <li><strong>核心职责</strong>：负责客户端核心战斗表现、同屏渲染优化与服务端活动热更系统开发。</li>
    <li><strong>同屏渲染与热更攻坚</strong>：
      <ul>
        <li>万人同屏渲染优化：采用动态合图与同类角色动作缓存共享机制，主城与攻城战同屏渲染效率提升 80%。</li>
        <li>服务端动态热更：利用 C++ 底层嵌入 Lua 虚拟机，实现在线动态热更新运营活动与数值，无需重启服务器。</li>
      </ul>
    </li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2014</span>
  <div class="project-name">魔卡世纪</div>
  <div class="project-meta">
    <span class="type">即时对战卡牌</span>
    <span class="role">客户端主程</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Cocos2d-x (C++) + OpenGL ES</li>
    <li><strong>核心职责</strong>：负责首款原创卡牌手游的客户端底层搭建与核心战斗逻辑实现（加拿大 AppStore 首发上线）。</li>
    <li><strong>底层技术攻坚</strong>：
      <ul>
        <li>底层组件适配：自主重构引擎底层多语言文本排版、动态灰度 Shader、软键盘输入与骨骼动画播放组件。</li>
        <li>纹理内存优化：采用 PVRTC/ETC 格式深度压缩贴图，显存占用降低 50% 以上。</li>
      </ul>
    </li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2012</span>
  <div class="project-name">Ejecta-X 跨平台游戏引擎</div>
  <div class="project-meta">
    <span class="type">开源跨平台引擎</span>
    <span class="role">核心底层开发</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：C++ + OpenGL ES + JavaScript (V8/SpiderMonkey)</li>
    <li><strong>核心职责</strong>：负责将 iOS 端 Ejecta 引擎移植重构至 Android 平台，实现跨平台 H5 原生加速。</li>
    <li><strong>底层技术攻坚</strong>：
      <ul>
        <li>C++ 绑定与渲染加速：将 JS Canvas API 映射绑定至 C++ 底层，直接调用 OpenGL ES 进行管线渲染，运行性能提升 3-5 倍。</li>
        <li>跨端调试：支持在 Chrome 中直接断点调试 JS 代码，一键打包发布至移动端原生运行。</li>
      </ul>
    </li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2010</span>
  <div class="project-name">阿尔卡特 & 黑莓手机研发</div>
  <div class="project-meta">
    <span class="type">Android 系统级开发</span>
    <span class="role">核心模块开发</span>
  </div>
  <ul class="tech-list">
    <li><strong>技术栈</strong>：Android Framework / Java / C / Linux Kernel</li>
    <li><strong>核心职责</strong>：负责国际品牌（Alcatel / BlackBerry）定制机 Launcher 与 Contacts 核心系统应用开发。</li>
    <li><strong>底层沉淀</strong>：深入理解 Android 系统启动流程、Handler 机制、Binder IPC 通信与渲染管线，奠定深厚底层功底。</li>
  </ul>
</div>

</div>

<br>
<br>
<br>

<br>
<br>
<br>

<br>
<br>
<br>
<br>

<h2 class="section-title"><span class="icon">📚</span> 技术总结</h2>

<table class="tech-summary-table">
<thead>
<tr><th>技术领域</th><th>深度掌握与实践技术栈</th></tr>
</thead>
<tbody>
<tr><td>游戏客户端</td><td><strong>Unity3D (C#)</strong>、<strong>Cocos Creator (TypeScript/JavaScript)</strong>、Cocos2d-x (C++)、<strong>HybridCLR (华佗)</strong> / ILRuntime、Shader</td></tr>
<tr><td>服务端架构</td><td><strong>C# (.NET)</strong>、<strong>Node.js</strong>、<strong>Go</strong>、Java (Spring Cloud)、Skynet、C++、高并发分布式长连接</td></tr>
<tr><td>数据与缓存</td><td><strong>MySQL</strong> (索引优化/分库分表)、<strong>Redis</strong> (高频IO/分布式锁/缓存设计)、MongoDB、Memcached</td></tr>
<tr><td>网络与协议</td><td><strong>WebSocket</strong> (房间状态同步)、<strong>Socket</strong> (TCP/UDP)、Protobuf、HTTP/HTTPS、RPC 通信</td></tr>
<tr><td>工程化 & DevOps</td><td>Git、Docker、Jenkins CI/CD 自动化流水线、对象池管理、内存分析 (Profiler/Memory Profiler)</td></tr>
<tr><td>AI 辅助开发</td><td><strong>Cursor / Claude Code / Codex / Antigravity</strong> (AI Agent 极速编程落地，效能提升 50%+)</td></tr>
<tr><td>平台与底层</td><td>AppStore、Google Play、微信/抖音小游戏平台接入、Android NDK/JNI 底层绑定、聚合支付 SDK</td></tr>
</tbody>
</table>

<div class="thanks-section">
  <h2 style="color: #1e3a5f; margin-bottom: 12px;">🙏 致谢</h2>
  <p>感谢您阅读我的简历。15年+全栈研发深耕，热爱技术，期待有机会与您携手共创价值！</p>
  <div class="signature">— 王子亮</div>
</div>