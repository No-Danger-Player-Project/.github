# No Danger Player Project (NDP) - 多服务器联合封禁系统

## 项目概述
**No Danger Player Project (NDP)** 是一款由[EXE_autumnwind](https://github.com/EXE-autumnwind)的跨服务器封禁项目，旨在实时同步多个服务器之间的封禁名单，防止恶意玩家进入任何已连接的服务器。通过集中管理玩家封禁数据，显著提升服务器网络的安全性和管理效率。

---

## 核心功能
1. ​**实时封禁同步**
   - 当玩家在一个服务器被封禁时，该封禁会立即同步到所有安装了NDP插件/模组的服务器
   - 强制绑定**IP地址** **玩家名称** **UUID**(计划添加)，防止通过小号或代理逃避封禁

2. ​**多平台兼容性**
   - 稳定支持主流Java服务器平台(Vanilla/Fabric/Forge/Quilt/MCDR/Spigot/Paper/Folia)，其他平台正在适配中(见下方兼容性表格)
   - 未来计划包含代理层支持(BungeeCord/Velocity)

3. ​**轻量级与高性能**
   - 基于事件驱动的异步同步机制，最大限度降低性能影响
   - 可配置的本地缓存减少频繁数据请求的延迟

4. ​**管理工具**
   - 可自定义封禁原因、时长和审计日志

---

## 支持的服务器类型
| 服务器类型                  | 状态     | 备注            | 仓库地址                                                                 |
|------------------------|--------|---------------|----------------------------------------------------------------------|
| Bukkit / Spigot        | ✅ 支持 | 兼容Paper等衍生核心  | [NDP-Plugin](https://github.com/No-Danger-Player-Project/NDP-Plugin) |
| Folia                  | ✅ 支持 | 针对多线程优化       | [NDP-Plugin](https://github.com/No-Danger-Player-Project/NDP-Plugin) |
| Fabric                 | 🚧 开发中 | 计划支持1.16+版本   | NDP-Fabric                                                           |
| Forge                  | 🚧 开发中 | 计划支持1.16+版本   | NDP-Forge                                                            |
| Quilt                  | 🚧 开发中 | 计划支持1.16+版本   | NDP-Quilt                                                            |
| Velocity               | ✅ 支持 | 代理层封禁支持       | [NDP-Plugin](https://github.com/No-Danger-Player-Project/NDP-Plugin) |
| BungeeCord / Waterfall | ✅ 支持 | 与Velocity同步开发 | [NDP-Plugin](https://github.com/No-Danger-Player-Project/NDP-Plugin) |
| MCDReforged | ✅ 支持 | 支持MCDR 2.0+版本  | [NDP-MCDR](https://github.com/No-Danger-Player-Project/NDP-MCDR) |

---

## 工作原理
玩家加入服务器A → 插件检查本地/中央封禁名单 → 如果被封禁则拒绝访问 → 将封禁同步至服务器B/C/D...

## 快速开始
**安装**
   - 下载对应版本的JAR或mcdr文件到服务器的`plugins`或`mods`文件夹
   - 重启服务器生成`config.yml`配置文件

## 开发路线
   - 玩家行为分析系统，用于自动检测作弊行为

## 开源与贡献
   - GitHub仓库: [No-Danger-Player-Project](https://github.com/No-Danger-Player-Project)
   - 欢迎贡献: 接收新平台适配、性能优化或翻译的Issues/PR
   - 许可证: GPL-3.0
