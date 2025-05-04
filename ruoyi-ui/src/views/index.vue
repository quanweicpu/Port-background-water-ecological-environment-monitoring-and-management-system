<template>
  <div class="app-container home">
    <el-row :gutter="20">
      <el-col :sm="24" :lg="12" style="padding-left: 20px">
        <h2>港口本底水域生态环境监测管理系统</h2>
        <p>
           这个管理系统基于若依前后端分离系统开发，是本人在大连海事大学大二课程做的项目，我会尽全力把系统做的东西与实际相结合，开发更多的功能。
        </p>
        <p>
          <b>当前版本:</b> <span>v{{ version }}</span>
        </p>
        <p>
          <el-tag type="danger">&yen;免费开源</el-tag>
        </p>
        <p>
          <el-button
            type="primary"
            size="mini"
            icon="el-icon-cloudy"
            plain
            @click="goTarget('https://gitee.com/y_project/RuoYi-Vue')"
            >访问码云</el-button
          >
          <el-button
            size="mini"
            icon="el-icon-s-home"
            plain
            @click="goTarget('http://ruoyi.vip')"
            >访问主页</el-button
          >
        </p>
      </el-col>

      <el-col :sm="24" :lg="12" style="padding-left: 50px">
        <el-row>
          <el-col :span="12">
            <h2>中国“十四五”生态环境监测规划</h2>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="6">
            <h4>监测重点</h4>
            <ul>
              <li>港口水质监测</li>
              <li>底栖生物多样性监测</li>
              <li>污染物排放监测</li>
              <li>生态系统健康评估</li>
              <li>水文与气象数据采集</li>
              <li>...</li>
            </ul>
          </el-col>
          <el-col :span="6">
            <h4>技术手段</h4>
            <ul>
              <li>遥感监测技术</li>
              <li>无人船水质采样</li>
              <li>自动化监测站</li>
              <li>大数据分析与建模</li>
              <li>人工智能辅助决策</li>
              <li>...</li>
            </ul>
          </el-col>
        </el-row>
      </el-col>
    </el-row>
    <el-divider />
    <el-row :gutter="20">
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span>联系信息</span>
          </div>
          <div class="body">
            <p>
              <i class="el-icon-s-promotion"></i> Github地址：<el-link
                href="https://github.com/quanweicpu"
                target="_blank"
                >https://github.com/quanweicpu</el-link
              >
            </p>
            <p>
              <i class="el-icon-user-solid"></i> QQ娱乐群：
              <a href="http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=1k8gPoWg4U8OTWn7I1mtJjnXv_siHS4e&authKey=YKzMSGGTHD4uBA7e98hgFPHh0zLVc5L70R7MCE9tZqacjxe9009Aqbllx%2FhZHeoB&noverify=0&group_code=759687213" target="_blank">759687213</a>
            </p>
            <p>
              <i class="el-icon-chat-dot-round"></i> 微信号：<a
                href="javascript:;"
                >_qwamv</a
              >
            </p>
          </div>
        </el-card>
      </el-col>
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span>更新日志</span>
          </div>
          <el-collapse accordion>
            <el-collapse-item title="v1.0.0 - 2025-5-4">
              <ol>
                <li>基于若依的港口本底水域生态环境监测管理系统正式发布</li>
              </ol>
            </el-collapse-item>
          </el-collapse>
        </el-card>
      </el-col>
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span>捐赠支持</span>
          </div>
          <div class="body">
            <img
              src="@/assets/images/pay.png"
              alt="donate"
              width="100%"
            />
            <span style="display: inline-block; height: 30px; line-height: 30px"
              >你可以请作者喝杯咖啡表示鼓励</span
            >
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "Index",
  data() {
    return {
      // 版本号
      version: "1.0.0"
    }
  },
  methods: {
    goTarget(href) {
      window.open(href, "_blank")
    }
  }
}
</script>

<style scoped lang="scss">
.home {
  blockquote {
    padding: 10px 20px;
    margin: 0 0 20px;
    font-size: 17.5px;
    border-left: 5px solid #eee;
  }
  hr {
    margin-top: 20px;
    margin-bottom: 20px;
    border: 0;
    border-top: 1px solid #eee;
  }
  .col-item {
    margin-bottom: 20px;
  }

  ul {
    padding: 0;
    margin: 0;
  }

  font-family: "open sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #676a6c;
  overflow-x: hidden;

  ul {
    list-style-type: none;
  }

  h4 {
    margin-top: 0px;
  }

  h2 {
    margin-top: 10px;
    font-size: 26px;
    font-weight: 100;
  }

  p {
    margin-top: 10px;

    b {
      font-weight: 700;
    }
  }

  .update-log {
    ol {
      display: block;
      list-style-type: decimal;
      margin-block-start: 1em;
      margin-block-end: 1em;
      margin-inline-start: 0;
      margin-inline-end: 0;
      padding-inline-start: 40px;
    }
  }
}
</style>

