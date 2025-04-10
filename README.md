# 🐱 懒惰猫 (LazyCat) - 语音控制浏览器扩展

![Swiper](https://bu.dusays.com/2025/03/30/67e89cbdcaa2c.gif)

"懒惰猫"是一款智能语音控制浏览器扩展，让您通过中文语音命令轻松操控Microsoft Edge浏览器。所有语音处理均在本地完成，保障您的隐私安全。

[![Edge扩展商店](https://img.shields.io/badge/Edge-微软扩展商店-green)](https://microsoftedge.microsoft.com/addons)
[![稀土掘金](https://img.shields.io/badge/稀土-CHESSUNYAN-blue)](https://juejin.cn/user/2461172964265243)
[![BiliBili](https://img.shields.io/badge/BiliBili-ChessunYan开心盐-pink)](https://space.bilibili.com/3493257422047481)
![js](https://img.shields.io/badge/开发语言-javascript-blue?logo=javascript)
![GitHub top language](https://img.shields.io/github/languages/top/laomoz404/lazycat)
![GitHub Repo stars](https://img.shields.io/github/stars/laomoz404/lazycat)

## 🌟 功能特性

### 🎙️ 语音控制
- 中文语音指令操作浏览器
- 支持自然语言表达
- 快速响应(<300ms)

### 🛠️ 主要功能(后续支持自定义指令)
- **导航控制**："打开B站"、"访问知乎"
- **页面操作**："刷新页面"、"关闭标签页"
- **滚动控制**："向下滚动"、"滚动到底部"
- **显示模式**："夜间模式"、"恢复正常亮度"

### 🔒 隐私保护
- 100%本地语音处理
- 不上传任何语音数据
- 无痕浏览模式支持

## 🚀 快速开始

![Study](https://bu.dusays.com/2025/03/30/67e8e418c0265.gif)

### 安装要求
- Microsoft Edge v89+ (Chromium内核)
- 麦克风设备
- 网络连接(仅用于扩展更新)

### 安装步骤
1. 从仓库中拉取扩展包，在本地解压缩
2. 在Edge浏览器管理扩展中心，打开开发者模式
3. 点击加载解压缩的扩展，选择lazyCat的根目录
4. 检查是否存在于扩展列表中

### 使用步骤
1. 点击浏览器工具栏中的懒惰猫图标，启动状态为ON，默认OFF
2. 点击侧边栏"开始聆听"或使用快捷键(默认为Ctrl+Shift+L)
3. 说出您的指令，如："打开百度"

## ⚙️ 技术架构

graph TD
    A[语音输入] --> B[Web Speech API]
    B --> C[命令解析引擎]
    C --> D[浏览器操作执行]
    D --> E[结果反馈]

### 核心技术
- Web Speech API实现语音识别
- Edge扩展API集成
- 响应式设计架构

## 📦 项目结构

```
lazy-cat-extension/
├── public/                 # 静态资源
│   └── icon.jpg            # 扩展图标
├── sidepanel/              # 侧边栏资源
│   ├── sidepanel.html      # 侧边栏界面
│   └── sidepanel.js        # 侧边栏逻辑
├── background.js           # 后台服务
├── content.js              # 内容脚本
└── manifest.json           # 扩展清单
```

## 📜 命令参考

| 命令类别 | 示例命令 | 功能说明 |
|---------|----------|----------|
| 导航 | "打开B站" | 跳转到指定网站 |
| 搜索 | "搜索XX" | 百度搜索指定内容 |
| 页面 | "刷新" | 重新加载页面 |
| 滚动 | "向下滚动" | 页面向下滚动 |
| 模式 | "夜间模式" | 切换深色主题 |
| 自定义指令 | "下一页/暂停/播放等" | 用户自定义功能 |

## 🛠️ 开发指南

### 构建步骤
1. 克隆仓库
   ```bash
   git clone https://github.com/laomoz404/lazycat.git
   ```
2. 在Edge浏览器中加载解压的扩展
   - 打开 `edge://extensions`
   - 启用"开发者模式"
   - 点击"加载解压缩的扩展"
   - 右键扩展权限，允许扩展使用麦克风

### 测试建议
- 测试不同网站上的兼容性
- 验证语音识别准确率
- 检查内存占用情况

## 🤝 贡献指南

欢迎提交Issue和Pull Request！请确保：
1. 代码符合ESLint规范
2. 新功能附带测试用例
3. 更新相关文档


---

> **温馨提示**：使用前请确保授予麦克风权限。所有语音处理均在本地浏览器中完成，不会上传任何数据。
```
