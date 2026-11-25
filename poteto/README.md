# poteto

Lauren Tan（[@poteto](https://x.com/poteto)）公开资料的整理包。

这里放她的原则摘要、pstack 说明、X 帖子、长文和演讲转写。以后所有 poteto 资料都放到本目录，不再上传到 `Yanzn/my-private-notes`。

## 规模与时间

统计均来自本目录实文件，时间按 Asia/Taipei（UTC+8）。

| 项目 | 数量 / 范围 |
| --- | --- |
| 原则摘要 | 13 节，见 [SUMMARY.md](SUMMARY.md)。日期增补从〔10-09〕到〔11-05〕。 |
| X 帖 | 1938 条。时间范围：2026-02-28 08:00 至 2026-11-05 09:25。 |
| X 长文 | 5 篇，见 [articles/](articles/)。 |
| 演讲 / 视频转写 | 4 场，见 [transcripts/TRANSCRIPTS.md](transcripts/TRANSCRIPTS.md) 和 [videos/](videos/)。 |
| 最近一次同步 | 2026-11-05 09:30。`posts-raw.json` 的 `updated_at_taipei` 与此一致。最新帖 id：`2118152667625292100`。 |

每日 X 同步目前已暂停。本目录没有 2026-11-05 之后的新帖。

## 阅读顺序

1. [SUMMARY.md](SUMMARY.md)：提炼后的原则摘要。先读这个。
2. [pstack/pstack.md](pstack/pstack.md)：pstack 命令和纠正顺序。完整说明见 [pstack/pstack-README.md](pstack/pstack-README.md)。
3. [posts.md](posts.md) 和 [articles/](articles/)：原帖和长文。
4. [transcripts/TRANSCRIPTS.md](transcripts/TRANSCRIPTS.md)：演讲转写索引。
5. [updates.md](updates.md)：每次 X 同步的记录。

## 目录

| 路径 | 大小 | 说明 |
| --- | ---: | --- |
| [SUMMARY.md](SUMMARY.md) | 37.3 KB | 13 条原则摘要，带出处。 |
| [posts.md](posts.md) | 382.0 KB | 1938 条去重原帖，按时间从新到旧。有长文时优先用 `note_tweet` 全文。 |
| [posts-raw.json](posts-raw.json) | 1.88 MB | 同期原始 API 数据，便于程序处理。阅读请用 `posts.md`。 |
| [updates.md](updates.md) | 56.0 KB | 每次同步的增量记录。 |
| [articles/](articles/) | 5 个文件 | X Article 全文。 |
| [transcripts/](transcripts/) | 4 个转写 + 索引 | 演讲转写。 |
| [pstack/](pstack/) | 3 个文件 | 公共插件说明和 skill 元数据。 |
| [videos/2107911765967118750/](videos/2107911765967118750/) | 转写和总结 | workshop + 访谈合集。不含视频文件。 |

## 文章

| 文件 | 标题 | 发布时间（Asia/Taipei） |
| --- | --- | --- |
| [articles/2058975157503570132.md](articles/2058975157503570132.md) | How I Use Cursor | 2026-05-26 02:15 |
| [articles/2069824386283319343.md](articles/2069824386283319343.md) | Loops You Can Trust | 2026-06-25 00:46 |
| [articles/2094457600259842065.md](articles/2094457600259842065.md) | The Complete Guide to pstack Pt. 1 | 2026-09-01 00:09 |
| [articles/2097732320606507506.md](articles/2097732320606507506.md) | The Complete Guide to pstack Pt. 2 | 2026-09-10 01:02 |
| [articles/2103571281014861957.md](articles/2103571281014861957.md) | Coding is dead, long live Coding | 2026-09-26 03:44 |

## 转写

详见 [transcripts/TRANSCRIPTS.md](transcripts/TRANSCRIPTS.md)。

1. `transcripts/talk2500.txt`：[How I shipped 2,500 PRs last month](https://x.com/poteto/status/2102050467505430555)。约 38 分钟。08:20–09:20 和 27:30–29:30 识别较差。引用这两段时要标明。
2. `transcripts/salary.txt`：较长的一场谈话（约 43 分钟）。来源：[x.com/0xfuckpoverty/status/2107162560214548994](https://x.com/0xfuckpoverty/status/2107162560214548994)。
3. `transcripts/spacex-transcript.md`：[LIVE: Poteto on shipping 1000s of PRs](https://www.youtube.com/watch?v=MN9dGgmLyso)（pstack / SpaceX / Matt Pocock）。
4. `videos/2107911765967118750/`：Colin Matthews workshop + Matt Pocock 直播合集。转写在 `transcript.md`，总结在 `summary.md`。来源：[x.com/scarfpinkgirl/status/2107911765967118750](https://x.com/scarfpinkgirl/status/2107911765967118750)。

## 来源

- X 账号 [@poteto](https://x.com/poteto)（Lauren Tan）。
- 官方 pstack 插件：[cursor/plugins 的 pstack 目录](https://github.com/cursor/plugins/tree/main/pstack)。
- 演讲转写：本地 Whisper 或字幕 OCR，细节见转写索引。
- 工作底稿来自共用电脑 `/workspace/poteto-pack/`，截至 2026-11-05。

## 未收入的文件

| 未收入项 | 原因 |
| --- | --- |
| `pages/` | 原始抓取分页 JSON，内容已被 `posts.md` / `posts-raw.json` 覆盖。 |
| `backups/`、`.bak*`、`.sync-*`、`.backfill-*`、`.summary-backup-*` | 备份和临时文件。 |
| `videos/*/video720.mp4`（约 848 MB） | 视频二进制，体积过大。 |
| `videos/*/` 下的 OCR 中间文件、`probe/` 截图、`*.py`、`*.log`、`*.json` | 处理中间产物。结果已在 `transcript.md` 和 `summary.md`。 |
| 源目录里的 `README.md` | 内容已并入本文件。 |

`posts-raw.json` 约 1.88 MB，小于 20 MB，且扫描后未发现密钥，因此一并收入。

提交前已扫描密钥。一条转发帖里有玩笑用的 PEM 头尾，已改成「PEM 头/尾已省略」。原帖：https://x.com/poteto/status/2112968754531594422 。
