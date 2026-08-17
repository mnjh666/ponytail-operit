---
name: 马尾帮助
description: >
  马尾全部模式、技能和命令的快速参考卡。只显示一次，不是常驻模式。触发词：ponytail-help、
  /ponytail-help、马尾帮助、马尾命令、马尾怎么用、马尾参考卡。
---

# 马尾帮助

被调用时显示这张参考卡。一次性：不要改模式、不要写标记文件、不要持久化任何东西。

## 档位

| 档位 | 触发 | 变化 |
|------|------|------|
| 精简 | /ponytail 精简 | 把要求的做出来，用一句话点出更懒的替代方案。 |
| 默认 | /ponytail | 阶梯强制执行：YAGNI → 标准库 → 原生 → 一行 → 最少代码。默认档。 |
| 极端 | /ponytail 极端 | 极端的 YAGNI。先删再加，动手前先质疑需求。 |

档位一直保持到被改变或会话结束。

## 技能

| 技能 | 触发 | 作用 |
|------|------|------|
| 马尾 | /ponytail | 懒模式本体。能跑通的最简方案。 |
| 马尾审查 | /ponytail-review | 过度设计审查：第42行: 过度设计：工厂只有一个产品，内联。 |
| 马尾审计 | /ponytail-audit | 全仓库过度设计审计，按可删规模排。 |
| 马尾债务 | /ponytail-debt | 把「马尾:」注释收成一张追踪台账。 |
| 马尾收益 | /ponytail-gain | 实测收益记分板：更少代码、更低成本、更快速度。 |
| 马尾帮助 | /ponytail-help | 这张卡。 |

## 停用

说「停止马尾」或「正常模式」。随时可用 /ponytail 重新启用。
/ponytail off 也可以。

## 配置默认档位

默认档 = 默认，每个会话自动生效。改法：

**环境变量**（优先级最高）：
```bash
export PONYTAIL_DEFAULT_MODE=ultra
```

**配置文件**（~/.config/ponytail/config.json，Windows 是 %APPDATA%\ponytail\config.json）：
```json
{ "defaultMode": "lite" }
```

设成 "off" 会在会话开始时关闭自动激活，想用的时候手动 /ponytail。

优先级：环境变量 > 配置文件 > 默认。

## 更多

完整文档和示例：https://github.com/DietrichGebert/ponytail
