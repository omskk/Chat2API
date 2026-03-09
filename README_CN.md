# Chat2API

<p align="center">
  <img src="build/icons.png" alt="Chat2API Logo" width="128" height="128">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Release-v1.1.0-blue?style=flat-square&logo=github" alt="Release">
  <img src="https://img.shields.io/badge/License-GPL--3.0-blue?style=flat-square" alt="License">
  <br>
  <a href="https://www.electronjs.org/"><img src="https://img.shields.io/badge/Electron-33+-47848F?style=flat-square&logo=electron&logoColor=white" alt="Electron"></a>
  <a href="https://react.dev/"><img src="https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React"></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"></a>
  <img src="https://img.shields.io/badge/Platform-macOS%20%7C%20Windows%20%7C%20Linux-lightgrey?style=flat-square" alt="Platform">
</p>

<p align="center">
  <strong><a href="README.md">English</a></strong>
</p>

<p align="center">
  <strong>多平台 AI 服务统一管理工具</strong>
</p>

<p align="center">
  Chat2API 是一款原生桌面应用，提供 <strong>OpenAI 兼容 API</strong> 接口，支持多个 AI 服务提供商。让你可以在 <strong>macOS</strong>、<strong>Windows</strong> 和 <strong>Linux</strong> 上使用任何 OpenAI 兼容客户端连接 DeepSeek、GLM、Kimi、MiniMax、Qwen、Z.ai 等服务。
</p>

## ✨ 功能特性

- OpenAI 兼容 API：提供标准 OpenAI 兼容接口，无缝对接现有工具
- 多服务商支持：支持 DeepSeek、GLM、Kimi、MiniMax、Qwen、Z.ai 等
- 🆕 多轮对话支持：完整支持多轮对话，提供会话管理和上下文保持功能
- 🆕 工具调用支持：通过提示词工程为所有模型提供通用工具调用能力，兼容 Cherry Studio、Kilo Code 等客户端
- 🆕 模型映射：灵活的模型名称映射，支持通配符和首选服务商/账户选择
- 🆕 自定义参数：支持自定义 HTTP Header 开启联网搜索、深度思考、深度研究等功能
- 仪表盘监控：实时请求流量、Token 使用量和成功率统计
- API Key 管理：为本地代理生成和管理密钥
- 模型管理：查看和管理所有服务商的可用模型
- 请求日志：详细的请求日志记录，便于调试和分析
- 代理配置：灵活的代理设置和路由策略
- 系统托盘集成：从菜单栏快速访问状态
- 多语言支持：支持英文和简体中文
- 现代界面：简洁响应式界面，支持深色/浅色主题

## 🤖 支持的服务商

| 服务商           | 认证类型      | OAuth | 模型                                              |
| ---------------- | ------------- | ----- | ------------------------------------------------- |
| DeepSeek         | User Token    | 是    | DeepSeek-V3.2                                    |
| GLM              | Refresh Token | 是    | GLM-5                                            |
| Kimi             | JWT Token     | 是    | kimi-k2.5                                        |
| MiniMax          | JWT Token     | 是    | MiniMax-M2.5                                     |
| Qwen (国内版)    | SSO Ticket    | 是    | Qwen3.5-Plus, Qwen3-Max, Qwen3-Flash, Qwen3-Coder, qwen-max-latest |
| Qwen AI (国际版) | JWT Token     | 是    | Qwen3.5-Plus, Qwen3-Max, Qwen3-VL-Plus, Qwen3-Coder-Plus, Qwen-Plus, Qwen-Turbo |
| Z.ai             | JWT Token     | 是    | GLM-5, GLM-4.7, GLM-4.6V, GLM-4.6             |

## 📥 安装

### 下载安装

从 [GitHub Releases](https://github.com/xiaoY233/Chat2API/releases) 下载最新版本：

| 平台                  | 下载文件                              |
| --------------------- | ------------------------------------- |
| macOS (Apple Silicon) | `Chat2API-x.x.x-arm64.dmg`            |
| macOS (Intel)         | `Chat2API-x.x.x-x64.dmg`              |
| Windows               | `Chat2API-x.x.x-x64-setup.exe`        |
| Linux                 | `Chat2API-x.x.x-x64.AppImage` 或 `.deb` |

### 从源码构建

**环境要求：**

- Node.js 18+
- npm
- Git

```bash
# 克隆仓库
git clone https://github.com/xiaoY233/Chat2API.git
cd Chat2API

# 安装依赖
npm install

# 启动开发服务器
npx electron-vite dev 2>&1
```

### 构建生产版本

```bash
npm run build              # 构建应用
npm run build:mac          # 构建 macOS 版本 (dmg, zip)
npm run build:win          # 构建 Windows 版本 (nsis)
npm run build:linux        # 构建 Linux 版本 (AppImage, deb)
npm run build:all          # 构建所有平台
```

## 📖 使用方法

### 1. 启动应用

启动 Chat2API，配置你的偏好设置。

### 2. 添加服务商

进入 **供应商** 标签页 → 添加服务商 → 输入 API Key 或通过 OAuth 认证。

### 3. 配置代理

进入 **代理设置** 标签页 → 配置端口和路由策略 → 启动代理服务器。

### 4. 管理 API Key

进入 **API Key** 标签页 → 生成访问本地代理的密钥。

### 5. 监控使用情况

- **仪表盘**：整体健康状况和流量统计
- **模型**：查看所有服务商的可用模型
- **日志**：请求日志，用于调试

## 📸 截图

| 仪表盘                                       | 服务商                                       |
| -------------------------------------------- | -------------------------------------------- |
| ![Dashboard](docs/screenshots/dashboard.png) | ![Providers](docs/screenshots/providers.png) |

| 代理设置                                  | API Key                                    |
| ----------------------------------------- | ------------------------------------------ |
| ![Proxy](docs/screenshots/proxy.png)      | ![API Keys](docs/screenshots/api-keys.png) |

| 模型管理                                | 日志                                    |
| --------------------------------------- | --------------------------------------- |
| ![Models](docs/screenshots/models.png)  | ![Logs](docs/screenshots/logs.png)      |

| 设置                                       | 关于                                    |
| ------------------------------------------ | --------------------------------------- |
| ![Settings](docs/screenshots/settings.png) | ![About](docs/screenshots/about.png)    |

## ⚙️ 设置选项

- **端口**：更改代理监听端口（默认：8080）
- **路由策略**：轮询（Round Robin）或填充优先（Fill First）
- **自动启动**：应用启动时自动启动代理
- **主题**：浅色、深色或跟随系统
- **语言**：英文或简体中文

## 🏗️ 项目结构

```
Chat2API/
├── src/
│   ├── main/                    # Electron 主进程
│   │   ├── index.ts            # 应用入口
│   │   ├── tray.ts             # 系统托盘集成
│   │   ├── proxy/              # 代理服务器管理
│   │   ├── ipc/                # IPC 处理器
│   │   └── utils/              # 工具函数
│   ├── preload/                # 上下文桥接
│   └── renderer/               # React 前端
│       ├── components/         # UI 组件
│       ├── pages/              # 页面组件
│       ├── stores/             # Zustand 状态
│       └── hooks/              # 自定义 Hooks
├── build/                      # 构建资源
└── scripts/                    # 构建脚本
```

## 🔧 技术栈

| 组件     | 技术                  |
| -------- | --------------------- |
| 框架     | Electron 33+          |
| 前端     | React 18 + TypeScript |
| 样式     | Tailwind CSS          |
| 状态管理 | Zustand               |
| 构建工具 | Vite + electron-vite  |
| 打包工具 | electron-builder      |
| 服务器   | Koa                   |

## 📁 数据存储

应用数据存储在 `~/.chat2api/` 目录下：

- `config.json` - 应用配置
- `providers.json` - 服务商设置
- `accounts.json` - 账户凭证（加密）
- `logs/` - 请求日志

## ❓ 常见问题

### macOS 提示"应用已损坏，无法打开"？

由于 macOS 的安全机制，非 App Store 下载的应用可能会触发此提示。运行以下命令即可修复：

```bash
sudo xattr -rd com.apple.quarantine "/Applications/Chat2API.app"
```

### 如何更新？

在 **关于** 页面检查更新，或从 [GitHub Releases](https://github.com/xiaoY233/Chat2API/releases) 下载最新版本。

## 🤝 贡献

1. Fork 本项目
2. 创建功能分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 提交 Pull Request

## 📄 许可证

GNU 通用公共许可证 v3.0。详见 [LICENSE](LICENSE)。

这意味着：
- ✅ 可以自由使用、修改和分发
- ✅ 衍生作品必须以相同许可证开源
- ✅ 必须保留原始版权声明

## 🙏 致谢

- [Electron](https://www.electronjs.org/) - 跨平台框架
- [React](https://react.dev/) - UI 框架
- [TypeScript](https://www.typescriptlang.org/) - 类型安全的 JavaScript
- [Tailwind CSS](https://tailwindcss.com/) - CSS 框架
- [Zustand](https://zustand-demo.pmnd.rs/) - 状态管理
- [Koa](https://koajs.com/) - HTTP 服务器
