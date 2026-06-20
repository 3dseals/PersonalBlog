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
.project-card .tech-list li {
  padding: 4px 0 4px 16px;
  color: #475569;
  font-size: 0.88em;
  position: relative;
}
.project-card .tech-list li::before {
  content: '›';
  position: absolute;
  left: 2px;
  color: #3b82f6;
  font-weight: bold;
  font-size: 1.2em;
  top: 2px;
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
  <div class="subtitle">研发技术总监 · 全栈架构师</div>
  <div class="tag-list">
    <span>15年+研发经验</span>
    <span>游戏 / 社交 / AI</span>
    <span>团队管理</span>
    <span>全栈架构</span>
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
    <span class="value">研发类技术总监</span>
  </div>
  <div class="info-item">
    <span class="label">期望薪资</span>
    <span class="value">30K</span>
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

<h2 class="section-title"><span class="icon">💡</span> 核心优势</h2>

<div class="advantage-cards">
  <div class="advantage-card">
    <h4>🎯 全栈技术覆盖</h4>
    <ul>
      <li><strong>客户端</strong>：Unity3D / Cocos2d-x / Cocos Creator / React.js</li>
      <li><strong>服务端</strong>：Node.js / Go / Java / Skynet / C++</li>
      <li><strong>数据层</strong>：MySQL / Redis / MongoDB / 高并发IO设计</li>
      <li><strong>DevOps</strong>：Jenkins / Docker / Git / 自动化部署</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>🤝 团队协同能力</h4>
    <ul>
      <li>主导多个从0到1的项目架构设计与团队搭建</li>
      <li>建立规范化开发流程（OKR/Redmine/代码审查）</li>
      <li>跨部门协作经验：策划、美术、运营、测试</li>
      <li>AI辅助编程实践，提升团队研发效率</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>📊 业务成果</h4>
    <ul>
      <li>累计参与项目流水超 <strong>1亿+</strong></li>
      <li>主导多款游戏从研发到上线全流程</li>
      <li>具备游戏运营思维，理解商业化设计</li>
      <li>覆盖手游、直播游戏、H5小游戏等多品类</li>
      <li>从大型项目支撑、需求规划、代码修复、团队协作、成本控制五维度全面评估</li>
    </ul>
  </div>
  <div class="advantage-card">
    <h4>🤖 AI工具深度实践</h4>
    <ul>
      <li>深度使用 <strong>Cursor / Claude Code / Codex / Antigravity</strong> 四大主流AI编程工具</li>
      <li>推动AI Agent编程落地实践，实现团队研发效率 <strong>提升50%+</strong></li>
      <li>建立AI辅助编程最佳实践规范，赋能5-20人开发团队高效协作</li>
    </ul>
  </div>
</div>

<h2 class="section-title"><span class="icon">🛠️</span> 技术栈</h2>

<div class="tech-section">

<div class="tech-category">
<h4>客户端开发</h4>
<div class="skill-bar">
  <span class="skill-name">Unity3D</span>
  <div class="skill-track"><div class="skill-fill expert" style="width:95%"></div></div>
  <span class="skill-level">精通</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Cocos2d-x</span>
  <div class="skill-track"><div class="skill-fill expert" style="width:95%"></div></div>
  <span class="skill-level">精通</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Cocos Creator</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:80%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">React.js</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:70%"></div></div>
  <span class="skill-level">熟练</span>
</div>
</div>

<div class="tech-category">
<h4>服务端开发</h4>
<div class="skill-bar">
  <span class="skill-name">Node.js</span>
  <div class="skill-track"><div class="skill-fill expert" style="width:95%"></div></div>
  <span class="skill-level">精通</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Go</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:80%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Java</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:80%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Spring Cloud</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:78%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Skynet/Lua</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:78%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">C++</span>
  <div class="skill-track"><div class="skill-fill skilled" style="width:65%"></div></div>
  <span class="skill-level">熟练</span>
</div>
</div>

<div class="tech-category">
<h4>数据库 & 中间件</h4>
<div class="skill-bar">
  <span class="skill-name">MySQL</span>
  <div class="skill-track"><div class="skill-fill expert" style="width:95%"></div></div>
  <span class="skill-level">精通</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Redis</span>
  <div class="skill-track"><div class="skill-fill expert" style="width:95%"></div></div>
  <span class="skill-level">精通</span>
</div>
<div class="skill-bar">
  <span class="skill-name">MongoDB</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:78%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">消息队列(MQ)</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:78%"></div></div>
  <span class="skill-level">熟练</span>
</div>
</div>

<div class="tech-category">
<h4>微服务 & 分布式</h4>
<div class="skill-bar">
  <span class="skill-name">Spring Cloud</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:80%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">XXL-Job</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:78%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Seata</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:75%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Nacos/Eureka</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:78%"></div></div>
  <span class="skill-level">熟练</span>
</div>
</div>

<div class="tech-category">
<h4>工具链 & DevOps</h4>
<div class="skill-bar">
  <span class="skill-name">Git/SVN</span>
  <div class="skill-track"><div class="skill-fill expert" style="width:95%"></div></div>
  <span class="skill-level">精通</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Jenkins</span>
  <div class="skill-track"><div class="skill-fill proficient" style="width:78%"></div></div>
  <span class="skill-level">熟练</span>
</div>
<div class="skill-bar">
  <span class="skill-name">Docker</span>
  <div class="skill-track"><div class="skill-fill skilled" style="width:65%"></div></div>
  <span class="skill-level">熟练</span>
</div>
</div>

</div>

<h2 class="section-title"><span class="icon">💼</span> 工作经历</h2>

<div class="timeline">

<div class="timeline-item">
  <span class="period">2024.07 - 至今</span>
  <div class="company">四川循东科技有限公司</div>
  <div class="position">技术负责人</div>
  <div class="company-desc">专注于AI驱动的虚拟社交和数字娱乐领域的创新科技公司</div>
  <ul class="duties">
    <li>负责技术团队管理，建立规范化开发流程与管理机制</li>
    <li>推动AI辅助编程实践（Cursor等），提升团队研发效率</li>
    <li>主导产品技术架构设计与技术选型</li>
    <li>负责小游戏平台架构设计与开发，涵盖多种H5小游戏、Block等休闲游戏品类</li>
    <li>构建小游戏聚合分发平台，打通运营、数据分析与用户增长链路</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2023.03 - 2024.06</span>
  <div class="company">麓卓互动科技有限公司（成都分公司）</div>
  <div class="position">服务端技术负责人</div>
  <div class="company-desc">专注于AI社交和元宇宙领域，打造3D虚拟社交直播游戏应用《Party Yoo》</div>
  <ul class="duties">
    <li>负责AI社交产品服务端架构设计与开发</li>
    <li>参与3D虚拟社交直播游戏应用的游戏模块开发，融合直播互动与游戏玩法</li>
    <li>设计并实现直播间实时互动游戏系统，支持主播与观众的多人实时游戏对战</li>
    <li>推行OKR绩效管理，优化团队协作流程</li>
    <li>产品已在印尼等国际市场内测上线</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2013.05 - 2023.02</span>
  <div class="company">成都黑骑士网络科技</div>
  <div class="position">技术合伙人 / 技术总监</div>
  <div class="company-desc">创业型手游公司，拥有多款上线游戏</div>
  <ul class="duties">
    <li>从0到1搭建技术团队，建立完整开发流程</li>
    <li>主导多款游戏全栈开发（客户端+服务端）</li>
    <li>负责技术架构设计、性能优化、线上运维</li>
    <li>参与游戏运营策略制定，理解商业化设计</li>
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
    <li>见证公司从50人发展到400人的高速成长期</li>
  </ul>
</div>

<div class="timeline-item">
  <span class="period">2010.07 - 2011.11</span>
  <div class="company">TCL通讯</div>
  <div class="position">Android开发工程师</div>
  <div class="company-desc">专注于Android手机研发，与阿尔卡特、黑莓等厂商合作</div>
  <ul class="duties">
    <li>参与Android系统上层应用定制开发</li>
    <li>负责Contacts、Launcher等核心模块开发</li>
    <li>深入理解Android底层机制，为后续移动开发奠定基础</li>
  </ul>
</div>

</div>

<h2 class="section-title"><span class="icon">🎮</span> 项目经历</h2>

<div class="project-grid">

<div class="project-card">
  <span class="project-year">2024 - 至今</span>
  <div class="project-name">小游戏平台 & H5游戏矩阵</div>
  <div class="project-meta">
    <span class="type">小游戏平台 / H5游戏</span>
    <span class="role">技术负责人</span>
  </div>
  <ul class="tech-list">
    <li>构建小游戏聚合平台，支持多品类H5小游戏上架与分发</li>
    <li>开发多款H5休闲小游戏，涵盖Block消除、益智解谜等热门品类</li>
    <li>技术栈：Cocos Creator / React.js / Node.js</li>
    <li>实现游戏数据埋点与用户行为分析系统</li>
    <li>搭建统一的游戏资源管理与版本热更新机制</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2023</span>
  <div class="project-name">Party Yoo</div>
  <div class="project-meta">
    <span class="type">3D虚拟社交直播游戏</span>
    <span class="role">服务端技术负责人</span>
  </div>
  <ul class="tech-list">
    <li>3D虚拟形象 + 直播互动 + 多人实时游戏融合玩法</li>
    <li>服务端：Java Spring Cloud微服务架构</li>
    <li>实时互动：WebSocket + 自研游戏房间管理系统</li>
    <li>支持直播间内嵌多种小游戏，主播与观众实时对战</li>
    <li>面向海外市场（印尼等东南亚地区），支持多语言与本地化</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2020</span>
  <div class="project-name">无尽之界</div>
  <div class="project-meta">
    <span class="type">挂机对战冒险游戏</span>
    <span class="role">技术负责人</span>
  </div>
  <ul class="tech-list">
    <li>客户端：Unity3D + 战斗模块 + 逐帧验证 + 热更新</li>
    <li>服务端：Node.js分布式架构 + Redis高并发IO + RPC通信</li>
    <li>特色：灯光Shader、网络协议优化、战斗服/挂机合成设计</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2019</span>
  <div class="project-name">三国诸侯纷争</div>
  <div class="project-meta">
    <span class="type">SLG策略游戏</span>
    <span class="role">全栈开发</span>
    <span class="revenue">💰 200万+/半年</span>
  </div>
  <ul class="tech-list">
    <li>客户端：Unity3D + ILRuntime热更新</li>
    <li>服务端：Java NIO + Protobuf协议</li>
    <li>职责：多平台对接、支付系统、后台功能开发</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2017</span>
  <div class="project-name">Survive 活下去</div>
  <div class="project-meta">
    <span class="type">丧尸生存游戏</span>
    <span class="role">技术负责人</span>
    <span class="revenue">💰 500万+/年</span>
  </div>
  <ul class="tech-list">
    <li>首次采用JS作为业务逻辑语言</li>
    <li>多服架构 + HTTP/Socket双通信</li>
    <li>全球唯一服 + 消息推送系统</li>
    <li>建立完整工具链与开发流程（Redmine工作流）</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2016</span>
  <div class="project-name">沙巴克传奇</div>
  <div class="project-meta">
    <span class="type">传奇类RPG</span>
    <span class="role">全栈开发</span>
    <span class="revenue">💰 500万+/半年</span>
  </div>
  <ul class="tech-list">
    <li>客户端：Cocos2d-Lua + 热更新 + 逐帧动画</li>
    <li>服务端：C++ + Lua热更新（活动系统）</li>
    <li>后台：PHP支付登录平台，解耦业务逻辑</li>
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
    <li>Cocos2d-x (C++) 早期版本</li>
    <li>解决大量引擎底层问题：动画、灰度图、输入框、热更新</li>
    <li>加拿大AppStore上线，首款原创游戏</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2013</span>
  <div class="project-name">Ejecta-X 引擎</div>
  <div class="project-meta">
    <span class="type">跨平台游戏引擎</span>
    <span class="role">核心开发</span>
  </div>
  <ul class="tech-list">
    <li>基于Ejecta原理，用C++重写支持Android</li>
    <li>H5代码绑定到C++，通过OpenGL渲染Canvas</li>
    <li>支持Chrome调试后直接移植到移动端</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2012</span>
  <div class="project-name">支付中心SDK平台</div>
  <div class="project-meta">
    <span class="type">SDK聚合平台</span>
    <span class="role">架构设计 & 核心开发</span>
  </div>
  <ul class="tech-list">
    <li>支持100+款游戏接入</li>
    <li>统一管理支付、分享、广告接口</li>
    <li>多人协作完成市面主流SDK集成</li>
  </ul>
</div>

<div class="project-card">
  <span class="project-year">2010</span>
  <div class="project-name">阿尔卡特 & 黑莓手机研发</div>
  <div class="project-meta">
    <span class="type">Android手机定制开发</span>
    <span class="role">核心模块开发</span>
  </div>
  <ul class="tech-list">
    <li>负责Launcher桌面模块开发，定制化主屏交互体验</li>
    <li>负责Contacts联系人模块开发，实现通讯录核心功能</li>
    <li>深入Android系统底层，积累扎实的移动端开发基础</li>
  </ul>
</div>

</div>

<h2 class="section-title"><span class="icon">📚</span> 技术总结</h2>

<table class="tech-summary-table">
<thead>
<tr><th>领域</th><th>技术栈</th></tr>
</thead>
<tbody>
<tr><td>游戏引擎</td><td>Unity3D / Cocos2d-x / Cocos2d-Lua / Cocos Creator</td></tr>
<tr><td>服务端框架</td><td>Skynet / Pinus / ThinkJS / Go / Spring Cloud</td></tr>
<tr><td>微服务组件</td><td>Nacos / Gateway / Feign / XXL-Job / Seata</td></tr>
<tr><td>消息队列</td><td>RabbitMQ / Kafka / RocketMQ</td></tr>
<tr><td>Web开发</td><td>React.js / Node.js / PHP / HTML5</td></tr>
<tr><td>数据库</td><td>MySQL / Redis / MongoDB / Memcached</td></tr>
<tr><td>协议 & 通信</td><td>Protobuf / WebSocket / HTTP / RPC</td></tr>
<tr><td>工具链</td><td>Webpack / Gulp / Python脚本</td></tr>
<tr><td>DevOps</td><td>Git / SVN / Jenkins / Redmine / Doxygen</td></tr>
<tr><td>平台对接</td><td>AppStore / Google Play / 微信 / 微博 / 各类SDK</td></tr>
</tbody>
</table>

<div class="thanks-section">
  <h2 style="color: #1e3a5f; margin-bottom: 16px;">🙏 致谢</h2>
  <p>感谢您花时间阅读我的简历。</p>
  <p>15年+的技术积累让我具备了从客户端到服务端、从架构设计到团队管理的全栈能力。我热爱技术，享受解决复杂问题的过程，也乐于带领团队一起成长。</p>
  <p>期待能有机会与您共事，共同创造价值。</p>
  <div class="signature">— 王子亮</div>
</div>
