# SanJiuZhiWuAI
AI操控手机仅root
# 三玖之屋 · SanJiuZhiWuAI
Package Name：`com.sanjiuzhiwuai.lw`
> 🌏 Language Switch | [中文](#zh) | [English](#en)

<a id="zh"></a>
## 🇨🇳 中文介绍
✨ **项目简介**
三玖之屋 是一款 Android 开源客户端，基于 MIUIX 与 Material Design 开源组件开发。支持 Root 权限下 AI 解析指令自动操控手机执行任务；内置重力雪花、自定义图片雪花粒子特效；底部导航包含「权限」「AI」「聊天」「设置」四大页面；内置对接你之前的 PHP 聊天室接口。

> ⚠️ 重要警告
> 本程序**必须获取 Root 权限**才能执行自动化任务。AI 返回的 Shell 命令会直接通过 su 执行，存在误删文件、损坏系统的风险。仅用于技术学习研究，禁止任何恶意用途。
> 默认 GLM-4.6V-Flash Key 仅为演示使用，随时可能失效，正式使用请自行申请官方密钥。DeepSeek 系列模型需要你自行填入 API Key。

### 📱 页面功能说明
底部导航栏（MIUIX 风格）：权限｜AI｜聊天｜设置

#### 🔐 权限页
- Root 权限检测、SU 状态判断
- 读取展示设备信息：机型、Android版本、SDK、CPU、内存、屏幕分辨率

#### 🤖 AI 对话页
- 消息输入框
- 左侧：文件选择按钮，支持任意文件（图片、文档等，适配多模态模型）
- 右侧：发送按钮，提交内容到大模型 API
- 右上角汉堡菜单（☰）：API配置面板
- 默认模型：`GLM-4.6V-Flash`，默认密钥
- 预置可选模型：`deepseek-v4-pro` / `deepseek-flash`
- 支持自定义新增模型、自定义接口地址，填写密钥后右上角保存配置

> 逻辑约定：AI 输出可被程序识别的 Shell 指令，APP 拿到指令调用 Root 执行手机任务

#### 💬 聊天页
- 对接配套 PHP 聊天室 HTTP API（轮询简易聊天室）
- 右上角登录 / 注册弹窗，账号体系互通

#### ⚙️ 设置页（全部选项前置图标）
- 🔄 检测更新 开关
- 🎨 界面风格切换：MIUIX / Material
- 🌈 主题配色设置
- 🖼️ 自定义背景图片选择
- 🌫️ 背景模糊度调节滑块
- ❄️ 重力雪花特效 开关
- 🖼️ 图片重力雪花：选择雪花粒子图片
- ❄️ 图片重力雪花特效 开关
- ℹ️ 关于页面
  - 图标置顶居中
  - 项目名称：三玖之屋
  - 版本号
  - GitHub开源仓库链接
  - QQ交流群：https://qun.qq.com/universal-share/share?ac=1&authKey=bV12VcBJn%2BaaVvkPHbUY56YAAj98b8%2BjEtg1ttixgI%2B2MYbZ1bN9nzI9FxQJ%2F5Zg&busi_data=eyJncm91cENvZGUiOiIxMDU5NjcyMzkyIiwidG9rZW4iOiJMU2xBVStwZ3luNGZHVjB1VE12UjkyejdDcjVIMlkrbXdrMllveTB5dmUveGNRaW9hVkgzYXNQSW1UTWJYTkF6IiwidWluIjoiNjQxNTUwMzQyIn0%3D&data=BH9HPGxNgb7hcn-GKaleTHHv9msR3MeBNaGLAPI29yCV9GTvR_gAN5KPtBS83LwhHjB0BCLKjaZKE1MSm2JiVw&svctype=4&tempid=h5_group_info

### ✨ 粒子特效
1. 重力雪花：原生圆形粒子，重力下落物理动画
2. 图片重力雪花：使用用户自选图片作为雪花粒子

### 🧰 技术依赖
- MIUIX UI 开源库（底部导航、控件样式）
- Material Components Android
- AndroidX
- OkHttp3（网络请求，LLM & 聊天室API）
- Glide（图片加载、背景、雪花素材）
- libsu / RootShell（Root命令执行）
- 自定义粒子View（重力雪花）
- Gson JSON解析

### 📋 编译环境
- Android Studio
- MinSdk ≥ 24 (Android 7.0+)
- TargetSdk 34
- Gradle 8.x
- ApplicationId：`com.sanjiuzhiwuai.lw`

### 📦 配套后端
配套简易聊天室 PHP+MySQL API，放在仓库 `backend/`，上传虚拟主机即可使用，轮询模式。

### 📜 开源协议
MIT License

---

<a id="en"></a>
## 🇬🇧 English Introduction
# SanJiuZhiWuAI
Package Name: `com.sanjiuzhiwuai.lw`

✨ **Introduction**
SanJiuZhiWuAI is an open-source Android application built with MIUIX and Material Design components. It can receive AI-generated commands and control your phone automatically via Root permission. It includes gravity snowflake particle effects and custom image snowflake effects.
Bottom navigation tabs: **Permission | AI | Chat | Settings**. It connects to our simple PHP chatroom backend.

> ⚠️ WARNING
> This app **requires Root access** to run automation tasks. Shell commands returned by AI will be executed directly with `su`. Wrong commands may delete files or damage your system.
> This project is only for learning and research. Malicious usage is forbidden.
> The default API key for GLM-4.6V-Flash is for demo only and may expire anytime. You need to apply your own keys for DeepSeek models.

### 📱 Features by Page
#### 🔐 Permission Tab
- Check Root status & SU availability
- Show device info: model, Android version, SDK, CPU, RAM, screen resolution

#### 🤖 AI Tab
- Text input box
- Left button: file picker (supports all file types for multimodal models)
- Right button: send request to LLM API
- Top-right hamburger menu: API config panel
- Default model: `GLM-4.6V-Flash`
  Default key
- Predefined models: `deepseek-v4-pro`, `deepseek-flash`
- Support adding custom models & custom API endpoint. Save config after filling key.

> Rule: The AI outputs recognizable shell commands, and the app executes them via Root.

#### 💬 Chat Tab
- Connect to our PHP chatroom API (polling mode)
- Top-right button: login / register popup

#### ⚙️ Settings Tab (icon before every item)
- 🔄 Check update switch
- 🎨 UI Style switch: MIUIX / Material
- 🌈 Theme color setting
- 🖼️ Custom background image
- 🌫️ Background blur seekbar
- ❄️ Gravity snowflake toggle
- 🖼️ Select image for image snowflake
- ❄️ Image gravity snowflake toggle
- ℹ️ About page
  - App icon centered at top
  - App name: SanJiuZhiWu
  - Version text
  - GitHub repository link
  - QQ Group: https://qun.qq.com/universal-share/share?ac=1&authKey=bV12VcBJn%2BaaVvkPHbUY56YAAj98b8%2BjEtg1ttixgI%2B2MYbZ1bN9nzI9FxQJ%2F5Zg&busi_data=eyJncm91cENvZGUiOiIxMDU5NjcyMzkyIiwidG9rZW4iOiJMU2xBVStwZ3luNGZHVjB1VE12UjkyejdDcjVIMlkrbXdrMllveTB5dmUveGNRaW9hVkgzYXNQSW1UTWJYTkF6IiwidWluIjoiNjQxNTUwMzQyIn0%3D&data=BH9HPGxNgb7hcn-GKaleTHHv9msR3MeBNaGLAPI29yCV9GTvR_gAN5KPtBS83LwhHjB0BCLKjaZKE1MSm2JiVw&svctype=4&tempid=h5_group_info

### ✨ Particle Effects
1. Gravity snowflake: round particle with gravity physics simulation
2. Image gravity snowflake: use your selected picture as snow particle

### 🧰 Dependencies
- MIUIX UI Library
- Material Components Android
- AndroidX
- OkHttp3 (LLM & chat api request)
- Glide (image loader)
- libsu / RootShell (root command runner)
- Custom particle view for snow effect
- Gson for JSON

### 📋 Build Info
- Android Studio
- MinSdk ≥ 24 (Android 7.0+)
- TargetSdk 34
- Gradle 8.x
- ApplicationId: `com.sanjiuzhiwuai.lw`

### 📦 Backend
Simple PHP+MySQL chat api in `/backend` folder. Works on shared virtual host with polling.

### 📜 License
MIT License
