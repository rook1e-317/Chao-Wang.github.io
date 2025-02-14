---
layout: home
title: 欢迎来到我的主页
subtitle: 学校xxx | 学历xxx
---

<div class="row">
  <!-- 左侧信息栏 -->
  <div class="col-md-4 border-right">
    ## 📝 个人信息
    **姓名**：{{ site.author.name }}  
    **学历**：{{ site.author.education }}  
    **院校**：{{ site.author.university }}  
    **地址**：{{ site.author.address }}  
    **邮箱**：[{{ site.author.email }}](mailto:{{ site.author.email }})

    ## 🏅 荣誉奖励
    <div class="awards">
      <div class="card">
        <div class="card-body">
          <h6>奖学金</h6>
          <small>获奖时间/机构</small>
        </div>
      </div>
    </div>
  </div>

  <!-- 右侧主内容 -->
  <div class="col-md-8">
    ## 📢 最新动态
    <div class="alert alert-info">
      <strong>最新消息</strong><br>
      消息1xxx（可添加具体时间）
    </div>

    ## 🔬 研究方向
    <div class="research-areas">
      {% for area in site.author.research_areas %}
      <span class="badge badge-pill badge-primary">{{ area }}</span>
      {% endfor %}
    </div>

    ## 📚 学术成果
    <div class="publications">
      <!-- 示例文献条目 -->
      <div class="pub-item">
        <h5>论文标题</h5>
        <p>作者列表，会议/期刊名称，年份</p>
        <a href="#" class="btn btn-sm btn-outline-secondary">PDF</a>
      </div>
    </div>
  </div>
</div>

<style>
  .research-areas { margin: 20px 0; }
  .badge-primary { background: #007bff; margin: 3px; }
  .awards .card { margin-bottom: 10px; }
  .pub-item { 
    border-bottom: 1px solid #eee;
    padding: 15px 0;
  }
</style>
