# Changelog

本文件记录 AGNES Video 2.5 Prompt Skill 的重要变更。

## [1.0.0] - 2026-11-13

### Added
- 建立 AGNES Video 2.5 提示词创作 Skill。
- 支持 Text、Keyframe、Reference 三种生成模式。
- 定义主体与场景、动作与变化、镜头语言、视觉风格、声音与节奏、一致性要求六大提示词维度。
- 规定 Reference 模式素材上限：5 张图片、3 段音频、1 个视频。
- 增加图片、音频、视频参考占位符及用途说明规范。
- 增加时间轴设计、画幅选择、专项创作规则和输出前质量检查。
- 增加三种生成模式的独立提示词示例。
- 完善 README 项目说明和快速开始流程。

## [1.0.1] - 2026-11-13

### Changed
- 明确区分 `agnes-video-2.5` 基础版与 `agnes-video-2.5-flash` 的视频参考兼容性。
- 基础版允许最多 1 个视频参考；Flash 版禁止视频参考。
- 图片最多 5 张、音频最多 3 段的 Skill 统一素材上限保持不变。
- 同步更新根目录与标准 Agent Skills 入口的 Skill 文档。
- README 增加模型兼容性说明，并新增 Flash Reference 示例。
