# AGNES Video 2.5 Prompt Skill

AGNES AI 视频生成提示词创作技能包，支持 **Text、Keyframe、Reference** 三种生成模式。

- 当前版本：**v1.0.1**
- 许可证：**MIT**
- 主要语言：中文
- 适用场景：人物剧情、动物视频、产品展示、图片转视频、参考视频重构

## 核心能力

| 模式 | 用途 | 核心控制点 |
|---|---|---|
| Text | 文生视频 | 主体、场景、动作、镜头、风格、声音 |
| Keyframe | 首尾帧控制 | 起始状态、动作过程、结束状态、连续性 |
| Reference | 多模态参考 | 图片、音频、视频及其具体用途 |

Reference 素材数量与模型兼容性：
- 图片最多 5 张（基础版与 Flash 版统一采用此上限）
- 音频最多 3 段
- `agnes-video-2.5`（基础版）最多支持 1 个视频参考
- `agnes-video-2.5-flash` 不支持视频参考

每份参考素材都必须在提示词中说明用途，不能只上传素材而不指定作用。使用 Flash 时，不得安排或引用 `<Video 1>`；如需表现视频中的动作，可改用图片关键帧参考或文字拆解动作。

## 仓库结构

```text
agnes-video-2.5-prompt-skill/
├── SKILL.md                         # 便于直接阅读的技能说明
├── README.md
├── LICENSE
├── CHANGELOG.md
├── examples/
│   ├── text-to-video.md
│   ├── keyframe.md
│   └── reference.md
└── skills/
    └── agnes-video-2-5-prompt-skill/
        └── SKILL.md                 # 标准 Agent Skill 入口
```

## 快速使用

### 方式一：直接使用提示词规范

打开根目录的 [SKILL.md](./SKILL.md)，复制完整内容，提供给支持自定义指令或 Skill 的 AI 助手。

### 方式二：按 Agent Skills 文件夹格式安装

标准 Skill 是一个包含 `SKILL.md` 的文件夹。本仓库已提供：

`skills/agnes-video-2-5-prompt-skill/`

将这个文件夹复制到你所使用的 AI 工具所支持的 Skills 目录。不同工具的安装目录和启用方式可能不同，请以该工具官方文档为准。安装后确认工具能够发现该 Skill，并在提出 AGNES 视频提示词创作任务时调用它。

> 本仓库不保证所有 AI 客户端都原生支持 Agent Skills；不支持该格式的工具可以使用方式一手动加载。

## 提示词设计框架

复杂任务采用六个核心维度：
1. 主体与场景
2. 动作与变化
3. 镜头语言
4. 视觉风格
5. 声音与节奏
6. 一致性要求

简单任务可以精简；复杂任务应明确动作顺序、镜头变化和主体连续性。

## 案例

- [Text 文生视频示例](./examples/text-to-video.md)
- [Keyframe 首尾帧示例](./examples/keyframe.md)
- [Reference 多模态参考示例（基础版）](./examples/reference.md)
- [Reference 多模态参考示例（Flash 版，无视频参考）](./examples/reference-flash.md)

## 版本与更新

查看 [CHANGELOG.md](./CHANGELOG.md)。正式版本请前往 GitHub Releases 页面。

## 反馈与贡献

欢迎通过 GitHub Issues 提交问题、改进建议和提示词案例。提交案例时请说明生成模式、素材用途、目标时长及希望解决的问题。请勿上传未经授权的第三方素材。

## License

本项目采用 [MIT License](./LICENSE)。
