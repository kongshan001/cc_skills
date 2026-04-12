# ClawHub 游戏技能调研报告

> 自动化调研 ClawHub 热门游戏类技能并生成独立调研文档

## 技能索引

| # | 技能名称 | 描述 | 推荐安装 |
|---|---------|------|---------|
| 1 | [game-ai](./skills/game-ai.md) | Game AI 开发指南 - 行为树/状态机/寻路 | 本地 |
| 2 | [text-game-arcade-universe-v3](./skills/text-game-arcade-universe-v3.md) | 综合性 ASCII 文字游戏大厅 | 本地 |
| 3 | [identity-guess-game](./skills/identity-guess-game.md) | 身份猜猜猜 - 多人互动推理游戏 | 本地/ECS |
| 4 | [play-any-game](./skills/play-any-game.md) | AI游戏伴侣助手 | ECS |
| 5 | [tianyi-cloud-game](./skills/tianyi-cloud-game.md) | 天翼云游戏 | 本地 |
| 6 | [rpsls-game](./skills/rpsls-game.md) | Rock Paper Scissors Lizard Spock | 本地/ECS |
| 7 | [game](./skills/game.md) | 即时游戏设计引擎 | 本地/ECS |
| 8 | [text-adventure-game-skill](./skills/text-adventure-game-skill.md) | 龙虾文游系统 | 本地/ECS |
| 9 | [kuuila-game](./skills/kuuila-game.md) | Kuuila互动游戏框架 | 本地/ECS |
| 10 | [game-numeric-design](./skills/game-numeric-design.md) | 游戏数值策划工具 | 本地/ECS |
| 11 | [rule-pasta-zoo-game](./skills/rule-pasta-zoo-game.md) | 动物园规则怪谈 | 本地/ECS |
| 12 | [agent-arcade-games](./skills/agent-arcade-games.md) | Agent Arcade 竞技游戏 | ECS |
| 13 | [endless-downstairs](./skills/endless-downstairs.md) | Endless Downstairs 文字冒险 | 本地/ECS |
| 14 | [interactive-games](./skills/interactive-games.md) | 互动游戏框架 | 本地/ECS |
| 15 | [the-flip-publish](./skills/the-flip-publish.md) | Solana 区块链翻转游戏 | 本地(测试) |
| 16 | [clawland](./skills/clawland.md) | Solana 链上奇偶博弈 | 本地(测试) |
| 17 | [agent-arcade](./skills/agent-arcade.md) | PROMPTWARS 社交工程竞技 | ECS |
| 18 | [lobster-trap](./skills/lobster-trap.md) | AI 社交推理游戏 | ECS |

## 调研方法

```bash
# 搜索游戏类技能
clawhub search "game" --limit 30

# 查看技能详情
clawhub inspect <slug>
```

## 推荐分类

### 休闲娱乐类
- rpsls-game, identity-guess-game, endless-downstairs

### 游戏开发类
- game-ai, game-numeric-design, game, interactive-games

### AI竞技类
- agent-arcade, agent-arcade-games, lobster-trap

### 区块链实验类
- clawland, the-flip-publish (需要Solana环境)

### 中文特色类
- text-adventure-game-skill, kuuila-game, rule-pasta-zoo-game

---
*调研时间: 2026-04-12*