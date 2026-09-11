# Cici AI Drama Storyboard Skill

逐镜分镜、三层生成提示词、连续性、声音与剪辑的唯一责任分支。

## 安装

`npx skills add wshicheng851-tech/cici-ai-drama-skill-family`

## 你可以直接这样说

“把锁定剧本和资产编译成时长闭合的逐镜表与三层生成提示词。”

## 验证

运行 `validate_skill.py` 并查看 `reports/trigger-eval.json`。

## Troubleshooting

P0 母资产未锁定时先停止批量，返回对应资产 Skill 补齐。
