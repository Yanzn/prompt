# 转写：X 视频 2107911765967118750

- 帖子：https://x.com/scarfpinkgirl/status/2107911765967118750 （@scarfpinkgirl "pinky girl"；2026-10-08 03:11:42 Asia/Taipei；不是 poteto 本人发布）
- 媒体：amplify_video 2107897040931876864；时长 3:43:40（13420 s）；本地文件 `video720.mp4`（1280x720）
- 转写时间：2026-10-08 Asia/Taipei，poteto bot
- 总结：`summary.md`

## 结构

| 段 | 时间 | 内容 | 方法 |
|---|---|---|---|
| A | 0:00:00–0:52:26 | Colin Matthews 主持的 workshop（剪辑版）。0:00:00–0:01:02 是插入的开场：画面为 Lauren 在 SpaceX 舞台拿麦讲话，来源活动未确认 | 烧录字幕 OCR |
| B | 0:52:26–1:54:20 | Matt Pocock 直播访谈。与 `../../spacex-transcript.md` 同一场 | Whisper small.en（字幕样式不同，OCR 失败） |
| C | 1:54:20–2:51:07 | 同一场 workshop 的完整版，带 Lauren 自我介绍和主持人开场 | 烧录字幕 OCR |
| D | 2:51:07–3:43:40 | 与段 A 重复 | 烧录字幕 OCR |

## 说话人

- Lauren Tan（@poteto）：1:54:22 自我介绍 "I'm Lauren Tan … potato on Twitter … at Cursor for about five months"。
- Colin Matthews（段 A/C/D 主持人）：Lauren 在 0:04:04 称 "Colin"；画面有他的摄像头和名字。
- Matt Pocock（段 B 主持人）：画面标注 "Matt"。
- 0:00:00–0:01:02 开场的说话人：画面是 Lauren；音频不属于 workshop 原始录音；无法确认是不是她本人的观点。

## 方法与质量

- OCR：ffmpeg 3 fps，裁剪字幕框（crop=1080:90:100:580），只保留框内白字，tesseract 5.5（eng，psm 7），相邻相似行（相似度 > 0.8）合并。按约 30 秒分段，时间戳是该段第一行字幕出现的时间。
- 质量：段 A/C/D 好。与 Whisper 抽样（1:02–9:50）词级一致率 92.4%。字幕原文的错别字（"GroffBot"、"SpaxeXAI"、"Pstack"）保留不改。0:50:55 和 3:42:09 附近的重复句是原字幕错误。段 C 开头（1:54:01）有少量 OCR 噪声。
- Whisper：faster-whisper 1.2.1，small.en，int8，CPU。段 B 的时间戳已换算成整段视频的时间。
