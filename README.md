# AI 小说写作仓库

这个仓库用于把小说创作过程拆成一组可版本管理的 Markdown 文件：从脑洞、设定、人物、小纲到正文，都可以用 Git 记录每一次增删改查。

## 推荐工作流

1. **收集脑洞**：把一句话灵感、冲突、场景写到 `story/ideas/inbox.md`。
2. **沉淀设定**：把稳定下来的世界观、规则、地点写到 `story/worldbuilding/`。
3. **建立角色档案**：每个重要角色一个 Markdown 文件，放在 `story/characters/`。
4. **拆分章节**：每章一个文件，放在 `story/volumes/`，文件名使用 `001-章节名.md` 这种格式。
5. **AI 协作修改**：让 AI 针对具体文件执行“新增、改写、润色、续写、查找矛盾、生成摘要”等任务。
6. **提交版本**：每次完成一批改动后用 Git commit 保存创作版本。

## Markdown 管理小说内容的方式

Markdown 很适合小说项目，因为它：

- 纯文本，方便 Git 对比差异。
- 标题层级清晰，适合章节、小节、设定卡。
- 支持列表、引用、表格，适合人物表、时间线和伏笔清单。
- 不绑定任何写作软件，后续可导出为网页、PDF、电子书或继续交给 AI 处理。

## 目录说明

```text
story/
  ideas/           # 灵感池、脑洞、待整理素材
  characters/      # 人物卡、人物弧光、关系网
  worldbuilding/   # 世界观、地点、组织、规则、时间线
  volumes/         # 正文章节，每章一个 Markdown 文件
templates/         # 可复制使用的写作模板
docs/              # 写作规范、AI 协作提示词、流程说明
```

## 常用 AI 指令示例

- “请读取 `story/volumes/001-开篇.md`，把节奏改得更紧张，但不要改变剧情结果。”
- “请根据 `story/characters/protagonist.md` 检查第 1 章中角色行为是否一致。”
- “请在 `story/ideas/inbox.md` 中新增 10 个适合本书风格的反转点。”
- “请把 `story/worldbuilding/timeline.md` 整理成按时间排序的年表。”
- “请列出当前章节里的伏笔，并建议后续回收方式。”

## 起步建议

先复制模板：

```bash
cp templates/chapter.md story/volumes/001-开篇.md
cp templates/character.md story/characters/protagonist.md
```

然后把你的核心脑洞写进 `story/ideas/inbox.md`，我就可以继续帮你扩展人物、世界观和章节正文。
