# Crypto 一键启动脚本

> 加密货币研究工具箱的一键启动脚本，支持前后端同时启动、自动检测端口占用、日志输出。

![Shell](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnu-bash)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 功能特性

- ✅ **一键启动** — 同时启动后端 + 前端
- ✅ **智能检测** — 端口被占用时跳过启动，显示运行状态
- ✅ **健康检查** — 启动后自动验证 API 是否正常响应
- ✅ **统一管理** — 启动 / 停止 / 状态查看 一个脚本搞定
- ✅ **他人可用** — 只需修改顶部配置就能给任何人用

---

## 使用方法

### 1. 下载脚本

```bash
# 克隆仓库
git clone https://github.com/endlessroadddd/crypto-start-script.git
cd crypto-start-script
chmod +x start.sh
```

### 2. 修改配置

用文本编辑器打开 `start.sh`，修改顶部配置区域：

```bash
# ========== 配置 (其他用户修改这里) ==========
PROXY_URL="http://127.0.0.1:7897"   # 改成你的代理地址
BACKEND_PORT=3000                    # 后端端口
FRONTEND_PORT=5173                   # 前端端口
PROJECT_DIR="/path/to/你的/crypto项目"  # 改成你的项目路径
# =============================================
```

### 3. 运行

```bash
# 启动前后端（默认命令）
./start.sh

# 查看运行状态
./start.sh status

# 停止所有服务
./start.sh stop

# 显示帮助
./start.sh help
```

---

## 命令说明

| 命令 | 作用 |
|------|------|
| `./start.sh` (不加参数) | 启动前后端 |
| `status` | 查看哪个端口在使用、PID、API 是否正常 |
| `stop` | 停止前后端所有服务 |
| `help` | 显示帮助信息 |

---

## 前置要求

- **macOS / Linux**（Bash 环境）
- **Node.js 20+**
- **pnpm**
- **Clash 代理**（或任意 HTTP 代理）

---

## 常见问题

**Q: 提示"端口被占用"？**
> 说明服务已经在运行了，不用管它，直接打开浏览器访问就行。

**Q: 启动后 API 无响应？**
> 检查 Clash 代理是否开启、端口是否正确（默认 `7897`）。

**Q: 想修改端口？**
> 改 `start.sh` 顶部的 `BACKEND_PORT` 和 `FRONTEND_PORT` 即可。

---

## License

MIT — 随便用，改成自己的项目也行。
