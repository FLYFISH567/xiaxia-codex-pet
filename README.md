# 夏夏（Xiaxia）虚拟宠物制作档案

这是 ChatGPT Work / Codex 自定义虚拟宠物“夏夏”的完整 v2 制作档案。档案保留了最终精灵图、动作预览、生成提示词、源动作条、拆帧结果和质量验证报告，既可用于创建同款宠物，也可作为制作其他宠物的参考样本。

## 最快使用方式

如果只想在自己的账号中创建同款“夏夏”，请上传：

`final/spritesheet-extended.png`

并告诉 Codex：

> 请验证这张 v2 精灵图，创建名为“夏夏（Xiaxia）”的自定义宠物并启用。描述：温柔陪伴的兽耳少女夏夏。

宠物记录绑定各自账号。接收者上传后会创建新的宠物 ID，不会继承原账号中的宠物记录。

## 关键文件

| 路径 | 用途 |
| --- | --- |
| `final/spritesheet-extended.png` | 最终可上传的 v2 精灵图，1536×2288，RGBA |
| `final/validation-extended.json` | 最终精灵图结构验证报告 |
| `qa/pet-quality.json` | 综合质量检查结果 |
| `final/contact-sheet-extended.png` | 所有动作帧总览 |
| `final/direction-qa.png` | 16 个注视方向检查图 |
| `final/previews/all-states.gif` | 全部动作快速预览 |
| `final/previews/look-loop.gif` | 16 方向循环预览 |
| `pet_request.json` | 宠物规格、动作行与画布定义 |
| `prompts/` | 基础形象和各动作行的生成提示词 |
| `decoded/` | 生成并选定的源图与动作条 |
| `qa/` | 拆帧、检查、连续性与质量验证材料 |
| `MANIFEST.sha256` | 所有文件的 SHA-256 校验值 |

## 动作表结构

最终精灵图采用 8 列 × 11 行、单元格 192×208 的 v2 布局：

1. idle（6 帧）
2. running-right（8 帧）
3. running-left（8 帧）
4. waving（4 帧）
5. jumping（5 帧）
6. failed（8 帧）
7. waiting（6 帧）
8. running（6 帧）
9. review（6 帧）
10. 000°–157.5° 注视方向（8 帧）
11. 180°–337.5° 注视方向（8 帧）

## 验证状态

- 最终结构验证：通过，无错误、无警告。
- 综合质量验证：通过。
- 16 个注视方向语义检查：完整。
- 综合报告记录了少量相邻方向像素变化和中心位移提示，但未达到阻止创建的失败条件；原始报告已完整保留。
- 最终上传文件 SHA-256：`7c6611ef04525711b8e4a8c0981165a103e386abd9231cd003b278bd37fdf1fb`

## 档案完整性

`final/spritesheet-extended-raw.png` 是最终清理前版本，`final/spritesheet-extended.png` 是实际验证和上传使用的版本。不要用 raw 文件替代最终文件。

本档案未删除任何原始制作或 QA 文件。新增说明与校验清单只用于改善分享、复用和版本核验体验。

## 分享与再利用

你可以分享整个档案，也可以只分享最终精灵图和预览。若公开发布或用于再创作，请自行选择并明确仓库许可证；本档案本身不自动授予第三方额外的商业使用许可。
