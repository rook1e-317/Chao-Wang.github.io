---
layout: home
title: 姓名xx的个人主页
subtitle: 学历xxx | 学校xxx
---

<div class="container">
  <!-- 个人信息板块 -->
  <section class="profile-section">
    <h2>👤 个人信息</h2>
    <div class="profile-grid">
      <div class="profile-item">
        <span class="label">姓名：</span>{{ site.author.name }}
      </div>
      <div class="profile-item">
        <span class="label">学历：</span>{{ site.author.education }}
      </div>
      <div class="profile-item">
        <span class="label">院校：</span>{{ site.author.university }}
      </div>
      <div class="profile-item">
        <span class="label">地址：</span>{{ site.author.address }}
      </div>
      <div class="profile-item">
        <span class="label">邮箱：</span>
        <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>
      </div>
    </div>
  </section>

  <!-- 荣誉奖励板块 -->
  <section class="awards-section">
    <h2>🏆 荣誉奖励</h2>
    <div class="award-card">
      <h3>奖学金</h3>
      <p class="meta">获奖时间/机构</p>
    </div>
  </section>

  <!-- 最新动态板块 -->
  <section class="news-section">
    <h2>📢 最新动态</h2>
    <div class="news-alert">
      <span class="date">2023-07-20</span>
      <p>消息1xxx（请补充具体内容）</p>
    </div>
  </section>

  <!-- 研究方向板块 -->
  <section class="research-section">
    <h2>🔍 研究方向</h2>
    <div class="tag-cloud">
      {% for area in site.author.research_areas %}
        <span class="research-tag">{{ area }}</span>
      {% endfor %}
    </div>
  </section>

  <!-- 学术成果板块 -->
  <section class="publications-section">
    <h2>📚 学术成果</h2>
    <div class="publication-item">
      <h3>论文标题（请修改）</h3>
      <p class="authors">作者列表（请补充）</p>
      <p class="venue">会议/期刊名称，年份</p>
      <a href="#" class="btn-pdf">查看PDF</a>
    </div>
  </section>
</div>

<style>
  /* 基础布局 */
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }

  /* 个人信息网格布局 */
  .profile-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
    background: #f8f9fa;
    padding: 20px;
    border-radius: 8px;
  }

  .profile-item {
    display: flex;
    align-items: center;
  }

  .label {
    font-weight: 600;
    min-width: 60px;
  }

  /* 荣誉卡片样式 */
  .award-card {
    background: white;
    border-radius: 8px;
    padding: 15px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    margin: 10px 0;
  }

  /* 研究方向标签 */
  .tag-cloud {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .research-tag {
    background: #007bff;
    color: white;
    padding: 5px 15px;
    border-radius: 20px;
    font-size: 0.9em;
  }

  /* 学术成果样式 */
  .publication-item {
    border-bottom: 1px solid #eee;
    padding: 15px 0;
  }

  .btn-pdf {
    display: inline-block;
    background: #dc3545;
    color: white!important;
    padding: 5px 15px;
    border-radius: 4px;
    text-decoration: none;
    margin-top: 10px;
  }
</style>
