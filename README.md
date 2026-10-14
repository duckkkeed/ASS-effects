# ASS-effects

一组 ASS 字幕特效脚本模板：卡拉OK逐字特效、矢量绘图变形、抖动与残影。

## ⚠️ 必须安装 Yutils 和 VSFilterMod

**两个依赖缺一不可，否则脚本无法正常渲染：**

| 依赖 | 缺了会怎样 |
| --- | --- |
| **Yutils** | 报 `attempt to index nil value (field 'Yutils')`，文字无法转矢量绘图，`2.ass` / `4.ass` / `6.ass` 失效 |
| **VSFilterMod** | `3.ass` 的 `\jitter` 被忽略（VSFilterMod 独有标签，libass / 原版 VSFilter 不支持） |

- **Yutils**：<https://github.com/Youka/Yutils> — 把 `Yutils.lua` 放进 Aegisub 的 `automation\include\`（`自动化 → 打开脚本目录` 可定位），重启后确认 `自动化` 菜单里有 `Yutils`
- **VSFilterMod**：<https://github.com/sorayuki/VSFilterMod> — 播放器下重命名为 `VSFilter.dll` 覆盖，或 AviSynth 下 `LoadPlugin` + `TextSubMod()`
- Aegisub 预览用的是 libass，**看不到 `\jitter` 真实效果**，以实际播放 / 压制结果为准

## 文件说明

| 文件 | 效果 |
| --- | --- |
| [`ass/1.ass`](ass/1.ass) | 逐层裁切 + `\move`，文字分条向上推出 |
| [`ass/2.ass`](ass/2.ass) | 逐字随机矩形遮罩 + `\clip` 逐帧模糊闪烁 |
| [`ass/3.ass`](ass/3.ass) | 逐层裁切擦除 + `\jitter` 抖动（**需要 VSFilterMod**） |
| [`ass/4.ass`](ass/4.ass) | 逐字矢量绘图 + `shape.filter` 正弦波纹扭曲 |
| [`ass/5.ass`](ass/5.ass) | 用 Layer 1–120 叠出多层残影拖尾 |
| [`ass/6.ass`](ass/6.ass) | 文字转轮廓后沿贝塞尔曲线飞散 |

## 使用

脚本由 **Aegisub 3.4.2** 生成。用 Aegisub 打开 `.ass`，再 `自动化 → 应用卡拉OK模板`。

`Comment` 行中的 `code` / `template` / `karaoke` 是模板控制行，不要删除或改成 `Dialogue`。

**字体**：需安装 微软雅黑、楷体、Arial，以及 **极影毁片和圆**（`Default` 样式用），否则排版错位。

## 许可

[MIT](LICENSE)
