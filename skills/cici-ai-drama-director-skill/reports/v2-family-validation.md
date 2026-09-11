# v2.0.0 家族验证报告

日期：2026-09-11

## 安装结构

- 1 个总控 Skill：`cici-ai-drama-director-skill`
- 7 个同级子 Skill：script、style、character、scene、prop、storyboard、review
- 每个目录只有一个根 `SKILL.md`，文件夹名与 frontmatter `name` 一致，版本均为 2.0.0。

## 格式与触发

| Skill | 格式校验 | 触发用例 |
|---|---:|---:|
| director | 通过 | 6/6 |
| script | 通过 | 5/5 |
| style | 通过 | 5/5 |
| character | 通过 | 5/5 |
| scene | 通过 | 5/5 |
| prop | 通过 | 5/5 |
| storyboard | 通过 | 5/5 |
| review | 通过 | 5/5 |

合计 41/41；无假阳性、无假阴性。每个包均已生成 `reports/skill-ir.json` 与 `reports/trigger-eval.json`。

## 家族回归结论

1. 完整项目由总控接单，并明确“先三案、后锁案、再剧本→资产→分镜→试拍”。
2. 单项剧本、风格、角色、场景、道具、分镜与质检请求分别由对应子 Skill 接单。
3. 上游变化通过 DIFF 和资产状态只影响必要分支，锁定项不得静默覆盖。
4. 活跃版无文艺创作工作流和模式开关；仅保留一条“已移除/不支持”的边界说明与回归语义。
5. 真人口播和现场拍摄明确转交 `cici-short-video-director-skill`。
6. P0 资产未锁定或关键试拍未通过时，不允许盲目批量生成。

## 来源与证据边界

大鹏老师包的 6 个有效 DOCX 已用于架构与方法提炼，3 个零字节副本未纳入。来源包未附可核验许可证，因此不逐段复制、不对外发布。历史 v1.4.0 已保留完整备份。
