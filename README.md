# AutoFormX - 智能表单填写助手

<div align="center">

**使用AI智能填写表单，快速生成测试数据，提高测试效率**

</div>

## ✨ 功能特性

- 🤖 **AI智能识别** - 自动识别表单字段类型（姓名、邮箱、电话、地址等）
- 🎯 **双模式填写** - 支持单字段填写和一键填写整个表单
- 🔧 **多厂商支持** - 支持 DeepSeek、OpenAI 等多个AI服务商
- 🎨 **现代化UI** - 美观简洁的用户界面，不影响原页面布局
- ⚡ **高效便捷** - 为测试人员量身打造，大幅提升工作效率
- 🔒 **安全可靠** - API密钥本地加密存储，保护隐私安全

## 📦 安装方法

### 从 Chrome Web Store 安装（推荐）

1. 打开 Chrome Web Store 中的 [AutoFormX - 智能表单填写助手](https://chromewebstore.google.com/detail/jelfgoajbeknodkmlpagkfmebjneahol)

2. 点击页面右上方的“添加至 Chrome”

3. 在确认弹窗中点击“添加扩展程序”

4. 安装完成后，AutoFormX 图标会出现在浏览器工具栏

如果链接无法直接打开，也可以在 [Chrome Web Store](https://chromewebstore.google.com/) 搜索 `AutoFormX - 智能表单填写助手` 后安装。

## 🚀 快速开始

### 1. 配置API

首次使用需要配置AI服务：

1. 点击扩展图标，在弹出窗口点击"设置"
2. 选择AI厂商（推荐：DeepBricks）
3. 输入您的API Key
4. 选择模型（如：gpt-4-turbo）
5. 点击"测试连接"验证配置
6. 点击"保存设置"

### 2. 使用方式

#### 方式一：单字段填写
- 打开包含表单的网页
- 每个输入框旁会自动出现紫色的魔法棒按钮
- 点击按钮即可为该字段生成合适的测试数据

#### 方式二：一键填写
- 方案1：点击浏览器工具栏的扩展图标，在弹窗中点击"一键填写当前页面"
- 方案2：使用快捷键 **Ctrl+Shift+L** (Mac系统: **Cmd+Shift+L**)
- 扩展会自动识别所有表单字段
- AI会生成一套完整且相互关联的测试数据
- 自动填充到所有字段

## 📖 使用场景

- ✅ Web应用测试 - 快速填写注册、登录等表单
- ✅ 功能测试 - 生成各种类型的测试数据
- ✅ UI测试 - 验证表单布局和样式
- ✅ 性能测试 - 批量生成测试数据
- ✅ 演示展示 - 快速填充演示数据

## 🎯 支持的字段类型

AutoFormX能够智能识别以下字段类型并生成相应数据：

| 类型 | 说明 | 示例 |
|------|------|------|
| 姓名 | 中文姓名 | 张三 |
| 邮箱 | 有效的邮箱地址 | zhangsan@example.com |
| 手机号 | 中国大陆手机号 | 13800138000 |
| 电话 | 固定电话号码 | 010-12345678 |
| 地址 | 详细地址 | 北京市朝阳区xxx街道xxx号 |
| 公司 | 公司名称 | XX科技有限公司 |
| 职位 | 职位名称 | 产品经理 |
| 身份证 | 18位身份证号 | 110101199001011234 |
| 日期 | 日期格式 | 2024-01-01 |
| 网址 | URL地址 | https://example.com |
| ... | 更多类型 | ... |

## 🔧 配置选项

### API配置
- **AI厂商** - 选择AI服务提供商（DeepBricks/OpenAI/自定义）
- **API Base URL** - API服务地址
- **API Key** - 您的API密钥
- **模型选择** - 选择使用的AI模型
- **Temperature** - 控制生成数据的随机性（0-1）

### 界面设置
- **显示字段按钮** - 是否在输入框旁显示快捷按钮
- **显示全局按钮** - 是否显示右下角的浮动按钮

## 🤝 支持的AI厂商

AutoFormX与多个领先的AI服务商合作，为用户提供强大的数据生成能力：

| 厂商 | 官网 | 优势 |
|------|------|------|
| **DeepSeek** | [deepseek.com](https://www.deepseek.com/) | 国产创新模型，成本低廉 |
| **OpenAI** | [openai.com](https://platform.openai.com/) | 领先的GPT模型，性能稳定 |
| **SiliconCloud** | [siliconcloud.cn](https://cloud.siliconcloud.cn/) | 高性价比，支持开源大模型 |
| **通义千问** | [dashscope.aliyun.com](https://dashscope.aliyun.com/) | 阿里云，功能完整，性价比高 |
| **讯飞星火** | [xfyun.cn](https://www.xfyun.cn/) | 中文理解能力强，响应快 |
| **Nebius AI** | [nebius.ai](https://nebius.ai/) | 多模型支持，API成本低 |
| **百度千帆** | [ai.baidu.com](https://ai.baidu.com/) | 国内大厂，生态完整 |
| **DeepBricks** | [deepbricks.ai](https://www.deepbricks.ai/) | 国内API，低延迟，支持多种模型 |

> 💡 **提示**: 您可以配置任何兼容OpenAI API格式的服务商。选择"自定义"模式即可使用其他厂商的API。

## 🛠️ 技术架构

```
AutoFormX/
├── manifest.json              # 扩展配置
├── icons/                     # 图标资源
├── src/
│   ├── content/              # 内容脚本（注入到页面）
│   │   ├── content.js       # 表单扫描和按钮添加
│   │   └── content.css      # 样式文件
│   ├── background/           # 后台服务
│   │   └── service-worker.js # API调用处理
│   ├── options/              # 设置页面
│   │   ├── options.html
│   │   ├── options.js
│   │   └── options.css
│   ├── popup/                # 弹窗页面
│   │   ├── popup.html
│   │   ├── popup.js
│   │   └── popup.css
│   └── utils/                # 工具模块
│       ├── fieldDetector.js  # 字段类型识别
│       └── aiClient.js       # AI客户端封装
└── README.md
```

## 🌟 核心特性

### 智能字段识别
通过分析字段的多个属性（name、id、placeholder、label等）智能判断字段类型：
- 权重评分系统
- 支持中英文关键词
- 自动适配各种表单框架（React、Vue等）

### AI数据生成
- 根据字段类型生成真实可信的测试数据
- 批量生成时保证数据之间的关联性
- 符合中国用户使用习惯

### 用户体验优化
- 按钮智能定位，不影响原页面布局
- 监听DOM变化，支持动态加载的表单
- 加载状态提示，操作反馈清晰
- 支持拖动全局按钮调整位置

## 📝 API配置指南

### DeepSeek API

1. 访问 [DeepSeek 开放平台](https://platform.deepseek.com/)
2. 注册账号并获取API Key
3. 在扩展设置中配置：
   - Provider: DeepSeek
   - API Base URL: `https://api.deepseek.com/v1`
   - API Key: 您的密钥
   - Model: `deepseek-chat`

### OpenAI API

1. 访问 [OpenAI Platform](https://platform.openai.com/)
2. 创建API Key
3. 在扩展设置中配置：
   - Provider: OpenAI
   - API Base URL: `https://api.openai.com/v1`
   - API Key: 您的密钥
   - Model: `gpt-4` 或 `gpt-3.5-turbo`

## 🤝 贡献指南

AutoFormX 目前暂未开放源码，暂不接受 Pull Request。

如果您在使用过程中遇到问题，或有功能建议，欢迎通过 [GitHub Issues](https://github.com/qitest/AutoFormX/issues) 反馈。

## 📄 许可证

AutoFormX 目前暂未开放源码，所有权利由项目作者保留。未经授权，请勿复制、分发或反向工程本项目相关代码与资源。

## 🙏 致谢

- 感谢所有贡献者
- 感谢AI技术的支持
- 感谢所有用户的反馈与建议

## 📮 联系方式

- 问题反馈：[GitHub Issues](https://github.com/qitest/AutoFormX/issues)
- 功能建议：[GitHub Discussions](https://github.com/qitest/AutoFormX/discussions)

---

<div align="center">

**如果这个项目对您有帮助，请给我们一个 ⭐️ Star！**

Made with ❤️ by AutoFormX Team

</div>
