# AGNES Video 2.5 Prompt Skill

面向 AGNES AI 视频生成的提示词创作技能包。支持 **Text、Keyframe、Reference** 三种生成模式，帮助用户把创意和参考素材整理成清晰、连贯、可直接使用的视频提示词。

- 当前版本：**v1.0.0**
- 许可证：**MIT**
- 语言：中文提示词说明
- 适用方向：人物剧情、动物视频、产品展示、图片转视频、参考视频重构

## 核心能力

| 模式 | 用途 | 核心控制点 |
|---|---|---|
| Text | 文生视频 | 主体、场景、动作、镜头、风格、声音 |
| Keyframe | 首尾帧控制 | 起始状态、动作过程、结束状态、画面连续性 |
| Reference | 多模态参考 | 图片、音频、视频素材及其具体用途 |

Reference 模式素材数量约束：
- 图片最多 5 张
- 音频最多 3 段
- 视频最多 1 个

提示词必须说明每个参考素材的用途，不能只上传素材而不指定作用。

## 仓库结构

```text
agnes-video-2.5-prompt-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── CHANGELOG.md
└── examples/
    ├── text-to-video.md
    ├── keyframe.md
    └── reference.md
```

## 快速开始

1. 打开并阅读根目录的 [SKILL.md](./SKILL.md)。
2. 将 Skill 全文提供给兼容 Skill 的 AI 助手，或按该工具的 Skill 安装规范放入对应目录。
3. 描述你要生成的视频主题、时长、画幅和风格。
4. 如果使用 Reference 模式，上传素材并说明每份素材的用途。
5. 检查生成的完整提示词，再复制到 AGNES 使用。

本仓库提供的是提示词创作规范和案例，不包含 AGNES API 调用程序，也不代替 AGNES 平台自身的参数与内容限制。

## 示例

- [Text 文生视频示例](./examples/text-to-video.md)
- [Keyframe 首尾帧示例](./examples/keyframe.md)
- [Reference 多模态参考示例](./examples/reference.md)

## 提示词设计框架

Skill 采用六个核心维度组织复杂提示词：

1. 主体与场景
2. 动作与变化
3. 镜头语言
4. 视觉风格
5. 声音与节奏
6. 一致性要求

简单任务可以精简，复杂任务应明确动作顺序、镜头变化和主体连续性。

## 素材占位符

Reference 模式使用以下占位符，并逐一说明用途：

- 图片：`<Picture 1>` 至 `<Picture 5>`
- 音频：`<Audio 1>` 至 `<Audio 3>`
- 视频：`<Video 1>`

只使用用户实际提供的素材，不得虚构素材或编号。

## 版本记录

查看 [CHANGELOG.md](./CHANGELOG.md)。

## 参与改进

欢迎提交问题反馈、提示词案例和改进建议。提交案例时请说明生成模式、素材用途、目标时长及希望解决的问题；不要上传未经授权的第三方素材。

## License

本项目采用 [MIT License](./LICENSE)。
