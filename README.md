# Cici AI Drama Skill Family

> 把一个抖音 AI 短剧想法，稳定推进为可审批的剧本、视觉资产、逐镜提示词和试拍验收，而不是把所有规则塞进一个不断膨胀的提示词。

这是一个中文优先的模块化 Agent Skill 家族，包含 1 个总控和 7 个专业子 Skill。用户以投资人或甲方身份做关键决策；Agent 负责剧本统筹、资产拆解、连续性和生成生产规划。

## 安装

```bash
npx skills add wshicheng851-tech/cici-ai-drama-skill-family
```

查看仓库中可安装的 Skill：

```bash
npx skills add wshicheng851-tech/cici-ai-drama-skill-family --list
```

## 你可以这样说

- “把我当投资人，先给三个差异明确的抖音 AI 短剧方案，选定后再开发。”
- “检查这份 AI 短剧为什么逻辑出戏、信息点太少。”
- “基于锁定剧本建立角色、场景和道具母版。”
- “把锁定资产编译成精确时长的逐镜表和三层 AI 提示词。”
- “审核试拍镜头，找出角色变脸、空间漂移或道具失真的根因。”

## 包含的 Skill

| Skill | 职责 |
|---|---|
| `cici-ai-drama-director-skill` | 总控、审批门、资产矩阵、版本与路由 |
| `cici-ai-drama-script-skill` | 三案立项、钩子、情绪、剧本、血肉、逻辑与密度 |
| `cici-ai-drama-style-skill` | 视觉路线与 Style DNA |
| `cici-ai-drama-character-skill` | 角色母版、状态与一致性测试 |
| `cici-ai-drama-scene-skill` | 场景母版、空间动线和时段天气变体 |
| `cici-ai-drama-prop-skill` | 道具尺度、交互、多状态与测试 |
| `cici-ai-drama-storyboard-skill` | 逐镜分镜、三层提示词、连续性、声音与剪辑 |
| `cici-ai-drama-review-skill` | 试拍、漂移诊断、批量生成门与成片终检 |

## 工作方式

完整项目按以下顺序推进：

1. 明确受众、平台、时长、画幅、制作条件和权利边界。
2. 先给三个真正不同的故事方案，甲方选择后锁案。
3. 完成节拍、分场、逻辑链、信息点时间轴和剧本质检。
4. 按 Style、Character、Scene、Prop 建立母资产和状态。
5. 把锁定剧本与资产编译为逐镜分镜、提示词、声音和剪辑方案。
6. 先试拍高风险镜头；通过后才进入批量生成和终检。

所有跨分支信息通过资产 ID、固定项、变量、禁改项和 DIFF 传递，重复知识只在一个责任分支维护。

## 前置条件

- [ ] Node.js 与 npx：`node --version`、`npx --version`
- [ ] 支持 Agent Skills 或兼容 `SKILL.md` 的 Agent
- [ ] 实际生成图像/视频时，自行准备相应平台账号和授权素材

Skill 本身不要求 API Key，不直接登录或操作视频生成平台。

## 输出示例

```text
项目约束与授权清单
三案绿灯与锁案卡
精确节拍和分场剧本
逻辑链与信息点时间轴
Style / Character / Scene / Prop 母资产
逐镜表与三层生成提示词
试拍和最终验收报告
```

## 验证

v2.0.0 的 8 个包均通过本地结构校验和触发边界测试，合计 41/41 个触发、排除与相邻用例通过。仓库保留每个包的 `evals/` 和 `reports/trigger-eval.json`，便于复现静态测试。

这些结果不代表生成平台实测、人工盲评、播放量或商业回报；相应证据目前为 `missing evidence`。

## 边界

- 只面向抖音优先的 AI 短剧和 AI 剧情短片，不提供文学创作模式。
- 真人口播、Vlog、现场拍摄和收音不在本 Skill 家族范围内。
- 不模仿在世创作者，不处理未经授权的真人肖像或角色/IP。
- 不承诺“爆款”、平台推荐、播放量或商业收益。
- 音乐、字体、图片、角色、商标和训练参考的授权状态需由使用者核验。

## Troubleshooting

| 问题 | 可能原因 | 处理 |
|---|---|---|
| 只发现一个 Skill | 安装器只选择了单个包 | 先运行 `npx skills add wshicheng851-tech/cici-ai-drama-skill-family --list`，再选择全部 8 个 |
| 完整项目被某个子 Skill 单独接管 | 请求只描述了单一专业任务 | 明确说“从立项到试拍完整统筹”，触发总控 Skill |
| 逐镜提示词出现人物或场景漂移 | P0 母资产尚未锁定 | 返回角色、场景、道具分支完成固定项和标准测试 |
| 输出看起来像模板拼接 | 只写了标签，没有因果证据 | 要求提供逻辑链、信息点时间轴和血肉质检证据 |

## 目录

```text
skills/
  cici-ai-drama-director-skill/
  cici-ai-drama-script-skill/
  cici-ai-drama-style-skill/
  cici-ai-drama-character-skill/
  cici-ai-drama-scene-skill/
  cici-ai-drama-prop-skill/
  cici-ai-drama-storyboard-skill/
  cici-ai-drama-review-skill/
```

## 来源与致谢

- 使用 Qiaomu Meta Skill 的结构、验证与发布方法构建。
- 升级过程中参考了一套本地短剧课程资料的模块思路；来源未附可核验许可证。本仓库没有包含原始 DOCX、课程附件或逐段复制内容，只发布独立整理和改写后的工作流。

详见 [NOTICE.md](NOTICE.md)。

## License

[MIT](LICENSE)
