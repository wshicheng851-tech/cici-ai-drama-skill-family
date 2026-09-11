# Cici AI 短剧 Skill Family v2.0.0

本包是抖音优先的 AI 短剧模块化工作流。`cici-ai-drama-director-skill` 负责总控，七个兄弟 Skill 分别负责剧本、风格、角色、场景、道具、分镜和质检。不要把子 Skill 嵌套到总控目录，否则部分 Agent 无法独立发现它们。

活跃版本不包含文艺作者模式。历史版本可从备份恢复。

## 安装

`npx skills add wshicheng851-tech/cici-ai-drama-skill-family`

## 你可以直接这样说

“把我当投资人，从三个方案开始，统筹一部抖音 AI 短剧到试拍验收。”

## 验证

运行乔木工具的 `validate_skill.py`，并查看 `reports/trigger-eval.json`。

## Troubleshooting

若只需单项任务，请直接调用相应的剧本、风格、角色、场景、道具、分镜或质检子 Skill。
