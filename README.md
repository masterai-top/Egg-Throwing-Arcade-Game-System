[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 掼蛋游戏源码：C++ / Cocos2d-x 客户端与联网大厅模块

面向 **掼蛋源码、掼蛋游戏源码、掼蛋棋牌客户端、Guandan game source code** 检索的项目说明。仓库公开内容包含 C++/Cocos2d-x 客户端启动与生命周期、断线重连、用户资料、头像道具、兑换数据、特效及部分通信数据结构；产品截图展示大厅、四人牌桌和结算体验。

> 重要边界：这是可核验的客户端代码片段与产品资料，不等同于开箱即用的完整服务端、规则引擎或运营后台。上线前需补齐依赖、服务端、资源授权、安全与合规审查。

## 产品体验

| 模块 | 产品表现 | 仓库线索 |
|---|---|---|
| 游戏大厅 | 初级/中级/高级场、快速开始、帮助入口 | `AppDelegate.*`、客户端状态数据 |
| 四人牌桌 | 2 对 2 座位、手牌区、出牌/不出、局内提示 | `ClientData.*`、消息结构及截图 |
| 断线恢复 | 网络中断提示、重新连接游戏房间 | `BreakLineReconnectionHint.*` |
| 用户与头像 | 切换账号、购买/使用头像、资料状态 | `ChangeAccountPopupLayer.*`、`BuyHeadImage.*` |
| 视觉反馈 | 震动、涟漪和界面效果 | `CCShake.*`、`CCRippleSprite.*`、`Effects.*` |
| 基础工具 | Base64、MD5、兑换数据与银行消息结构 | `DataBase64.*`、`DataMd5.*`、`ExchangeDataManager.*` |

## 掼蛋玩法概览

掼蛋通常由四名玩家组成两队，对家为队友，使用两副扑克牌。玩家按牌型和点数轮流出牌，以一方两名成员的出牌名次决定升级结果。常见牌型包括单张、对子、三张、三带二、顺子、连对、钢板和炸弹；级牌、逢人配及具体升级规则应按采用的赛事规则配置和测试。

典型流程：**进入大厅 → 选择房间 → 匹配/入座 → 发牌 → 轮流出牌 → 一局结算 → 升级或开始下一局**。

## 产品截图

| 大厅与桌面 | 对局与结果 |
|---|---|
| ![丹阳掼蛋游戏大厅与房间入口](docs/assets/images/guandan-lobby.png) | ![掼蛋四人牌桌与手牌界面](docs/assets/images/guandan-table.png) |
| ![掼蛋产品品牌画面](docs/assets/images/guandan-brand.png) | ![掼蛋对局结算与排名界面](docs/assets/images/guandan-result.png) |

## 技术结构

- **语言与客户端：** C++、Objective-C++、Cocos2d-x 风格 API。
- **应用生命周期：** 场景启动、进入后台、恢复前台与网络关闭处理。
- **UI 层：** 弹窗、标签、按钮、头像选择与视觉动作。
- **网络衔接：** 重连参数、游戏服务器地址/端口和消息数据结构。
- **数据与工具：** 客户端状态、兑换数据、Base64、MD5。

## 二次开发建议

1. 先补齐缺失的引擎、UI 框架、场景、网络帮助类和美术资源。
2. 将公开客户端与经过测试的掼蛋规则服务、房间服务、匹配及结算服务对接。
3. 为牌型比较、逢人配、升级和异常重连建立自动化测试。
4. 移除示例中的生产地址、密钥、真实用户与支付信息，完成素材授权和当地法规审核。

## 在线图文文档

- [简体中文](https://masterai-top.github.io/Egg-Throwing-Arcade-Game-System/zh-cn/)
- [繁體中文](https://masterai-top.github.io/Egg-Throwing-Arcade-Game-System/zh-tw/)
- [English](https://masterai-top.github.io/Egg-Throwing-Arcade-Game-System/en/)

