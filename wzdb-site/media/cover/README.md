# media/cover — 封面图放这里

视频 poster、作品卡片封面、音乐封面（可选）都从这个目录读。

## 现在的示例条目对应文件名

| 用在哪 | works.js 字段 | 现在写的路径 |
| --- | --- | --- |
| `VID-001` 视频封面 | `videos[].poster` | `media/cover/vid-001.jpg` |
| `VID-002` 视频封面 | `videos[].poster` | `media/cover/vid-002.jpg` |
| `WRK-001` 作品封面 | `works[].cover` | `media/cover/wrk-001.jpg` |
| `WRK-002` 作品封面 | `works[].cover` | `media/cover/wrk-002.jpg` |
| `WRK-003` 作品封面 | `works[].cover` | `media/cover/wrk-003.jpg` |
| `WRK-004` 作品封面 | `works[].cover` | `media/cover/wrk-004.jpg` |

照抄文件名放进来即可，或者去 `assets/js/works.js` 里把这些 `poster` / `cover` 字段改成你自己的路径。

## 尺寸建议

- 视频封面（poster）：**16:9**，建议 1280×720 或 1920×1080。
- 作品卡片封面：**16:9**，建议至少 800×450（卡片区按 16:9 裁切）。
- 音乐封面（可选字段 `cover`）：**1:1**，建议 600×600 以上。

## 格式

`jpg` 优先（体积小、兼容性最好），需要透明通道时用 `png`，`webp` 现代浏览器都支持。
文件名建议英文 + 短横线，例如 `wrk-001.jpg`。

## 图片缺失时

页面会显示一个等宽字体的占位块（例如 `NO COVER` / `POSTER MISSING`）并标出编号，不会出现破图图标。
