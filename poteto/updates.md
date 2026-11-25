# @poteto updates (read-only sync)

Maintained by poteto bot. Each sync reads @poteto (X user id 2832427459) posts newer than `last_seen_id`, keeps only advice-relevant takeaways with URLs, and notes when one changes earlier advice or adds a pstack skill.

last_seen_id: 2118152667625292100


## 2026-11-05 09:31 Asia/Taipei (scheduled run)
- New posts this run: 22 (2026-11-04 11:46 to 2026-11-05 09:25 Asia/Taipei). Nothing is left over.
- last_seen_id: 2118152667625292100
- Fetch note: `get_posts_counts_recent` gave 22; unique merged 22 (no gap). First `get_users_posts`/`search_posts_all` with `since_id` each returned 21 (search page 2 empty); second `get_users_posts` picked up 1 newer post that landed during the run (`2118152667625292100`). Long post `2118017093677494706` re-read with `get_posts_by_ids` for `note_tweet`.
- Most posts are game replies, retweets (X web rewrite, Grok Bot phone calls, Starlink), and banter (GTA 6). About 4 are advice-relevant.
- Use `/statechart` to understand the abstract model of the program: check whether the agent understands the goal and how the product should work; the skill draws a diagram from TLA+ specs from the user's point of view. https://x.com/poteto/status/2118073519515025804
- To customize her style: run `/automate-me` and make your own fork of poteto-mode. https://x.com/poteto/status/2118055219431109042
- Upcoming talk slides: they ship ~30× more code without reading it, while performance is as good or better; agent-friendly architecture bets are paying off at taming slop. Fun fact: ~230 people landed at least 1 PR to Grok Bot in October. Clarifies the PR chart covers all Grok Bot PRs, not only hers (follow-up). https://x.com/poteto/status/2118017093677494706
- On agent UX overload: you do not need a new UI first; figure out how to not be the bottleneck. https://x.com/poteto/status/2117899425733554628
- Product notes (not advice): Grok Bot phone calls RT https://x.com/poteto/status/2118044457753035193 ; PR chart clarification https://x.com/poteto/status/2118051545468301479 ; game/wiki/banter replies.
- Changes earlier advice: mild yes — `/statechart` framed as a check that the agent understands goals (user-POV diagram from TLA+); use `/automate-me` to fork poteto-mode; scale evidence for agent-friendly architecture (30× ship without reading; ~230 Oct PR authors); remove yourself as bottleneck before new agent UI. Reinforces SUMMARY principles 1, 8, 9, 11, and 12. New pstack skill released: no (`/automate-me` already exists).

## 2026-11-04 09:22 Asia/Taipei (scheduled run)
- New posts this run: 13 (2026-11-03 10:04 to 2026-11-04 08:42 Asia/Taipei). Nothing is left over.
- last_seen_id: 2117779429107900647
- Fetch note: `get_posts_counts_recent` gave 14; gap of 1 vs 13 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 13 on page 1; page 2 empty. `get_users_posts` with `since_id` returned the same 13 (no next_token). Long posts `2117437607940681849` and `2117445316043825393` re-read with `get_posts_by_ids` for `note_tweet`.
- Most posts are product plugs (Grok Bot shopping), retweets, game wiki replies, and banter. About 5 are advice-relevant (code review / verification thread).
- Adversarial / abstract agent code review: mostly a waste of tokens; prefer empirical verification combined with formal verification. She updated pstack to use `/interrogate` less and may remove it. Agents get lost in nitpicks and YAGNI. https://x.com/poteto/status/2117437607940681849
- Clarify: the problem is agents reviewing code without running it empirically or using a deterministic checker like formal verification (applies to cross-model and single-model). https://x.com/poteto/status/2117440753551204735
- Spec–code drift: agents mostly keep specs and code in sync, but sync is not enforced. https://x.com/poteto/status/2117440510847803764
- Overcooking a PR: multiple rounds of abstract agent review with no goal/intent context steers the authoring agent wrong; author agents are too sycophantic and accept all feedback. https://x.com/poteto/status/2117445316043825393
- Pre-merge checks without CI: she did not use CI at all for the side project; agents ran the checks before merging. https://x.com/poteto/status/2117453342477852824
- Product notes (not advice): shop/save/ship with @bot https://x.com/poteto/status/2117745465332846698 ; RT Grok Bot shopping https://x.com/poteto/status/2117741868889088410 ; RT statechart drawings https://x.com/poteto/status/2117471441788809635 ; game wiki reply https://x.com/poteto/status/2117743465501163613
- Changes earlier advice: yes — prefer empirical + formal verification over adversarial abstract review; avoid multi-round abstract agent review; agents can run checks before merge without CI; pstack de-emphasizes `/interrogate`. Reinforces SUMMARY principles 1, 9, and 11. New pstack skill released: no.

## 2026-11-03 09:26 Asia/Taipei (scheduled run)
- New posts this run: 29 (2026-11-02 09:36 to 2026-11-03 08:56 Asia/Taipei). Nothing is left over.
- last_seen_id: 2117420710134263879
- Fetch note: `get_posts_counts_recent` gave 30; gap of 1 vs 29 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 29 across 2 pages (25 + 4; page 3 empty). `get_users_posts` with `since_id` returned the same 29 across 2 pages (25 + 4; no further next_token). Long post `2117328786555564192` re-read with `get_posts_by_ids` for `note_tweet`.
- Most posts are game feedback replies (tibo.dog), retweets (Team Bot data bot, Runway Cursor plugin, pstack tip thread), and banter. About 2–3 are advice-relevant.
- Self-serve bot setup: to build a data bot like the Team Bot example, tag @bot and ask it to read the post and guide you through setup. https://x.com/poteto/status/2117366076342460440
- TLA+ pointer: when asked what TLA is, she linked Learn TLA+ (learntla.com) by @hillelogram. https://x.com/poteto/status/2117068631309996120
- Mild product: after ~100k non-story plays she buffed balance, added 17 languages, upgrading VFX, considering a gear system; plans to share how she built the game quickly with polish. https://x.com/poteto/status/2117328786555564192
- Mild: RT of community pstack 5-step tip thread (not her original advice). https://x.com/poteto/status/2117107568569106533
- Product notes (not advice): game feedback replies; “coming soon”; “will fix”; hire-grok-bot quote of Team Bot post.
- Changes earlier advice: no. Reinforces SUMMARY principles 1 and 8 (TLA+ learning path; @bot reads a reference post and guides setup). New pstack skill released: no.

## 2026-11-02 09:25 Asia/Taipei (scheduled run)
- New posts this run: 59 (2026-10-30 10:39 to 2026-11-02 09:22 Asia/Taipei). Nothing is left over.
- last_seen_id: 2117064701532389629
- Fetch note: `get_posts_counts_recent` gave 60; gap of 1 vs 59 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 59 across 3 pages (25 + 25 + 9; page 4 empty). `get_users_posts` with `since_id` returned the newest 25 on page 1; page 2 with pagination_token returned 0 (token not reusable); `until_id` retry also 0. Relied on search for the full set; merged users page 1 for `_sources`. Long posts re-read with `get_posts_by_ids` for `note_tweet` (trivia, bot guide, routines tips, rebuild-software).
- Most posts are Grok Bot support replies, retweets (/statechart charts, product plugs), and game/banter (tibo's game Day 28). About 6–7 are advice-relevant.
- Grok Bot guide: few good bots beat a large team; tell bots to create skills as you instruct; connectors/vault/tools; ask bot to remove copy-paste handoffs; onboard like an intern; voice dump then “restate in your own words”. https://x.com/poteto/status/2116576229319233596
- Routines tips: routines make bots proactive (scheduled + subscription); hourly is the most frequent she recommends for scheduled; prefer scripts/skills over the bot doing the work (tokens); share bot in Slack on team plans; think like a manager. https://x.com/poteto/status/2116580481236115933
- Rebuild software for agent pace: code becomes a continuous stream; make the easy thing the right thing; codebase is organic architecture around constraints; design systems/frameworks/languages to control chaos. https://x.com/poteto/status/2116191971714953262
- Software for humans (outside utilities/libraries) must be maintained as tastes change. https://x.com/poteto/status/2116217625554698569
- Side-project case study (~1,150 PRs in 4 days): every issue → lint rule; TLA+ / formal-verification skills per major system; filepath encodes hot paths (`.hot.ts`) + lint bans allocation; deterministic sim; comments banned by lint; bots play headless to tune difficulty. https://x.com/poteto/status/2117043478140276847
- Playtest loop: most time playtesting; each run spam feedback to a bot that orchestrates a Cursor Project. https://x.com/poteto/status/2117064701532389629
- Mild: keep improving bot proactivity. https://x.com/poteto/status/2116581185594020022
- Mild showcase: ask community for `/statechart` charts and formal-verification bugs (skill already released 10-30). https://x.com/poteto/status/2116302165702783320
- Product notes (not advice): tibo's game landed with grok bot + Cursor https://x.com/poteto/status/2117004709198475365 ; teaser https://x.com/poteto/status/2116662792631746861 ; “i used pstack” https://x.com/poteto/status/2117006144195764393
- Changes earlier advice: yes — concrete playtest→bot→Cursor Project loop; every bug → lint; multi formal-verification skills per system; routines max hourly + prefer scripts. Reinforces SUMMARY principles 1, 3, 4, 5, 6, 7, 8, and 11. New pstack skill released: no.


## 2026-10-30 09:19 Asia/Taipei (scheduled run)
- New posts this run: 20 (2026-10-29 10:56 to 2026-10-30 08:03 Asia/Taipei). Nothing is left over.
- last_seen_id: 2115957713515720763
- Fetch note: `get_posts_counts_recent` gave 21; gap of 1 vs 20 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 20 on page 1; page 2 empty. `get_users_posts` with `since_id` returned the same 20 (no next_token). Long post `2115880102601101414` re-read with `get_posts_by_ids` for `note_tweet`.
- Most posts are Grok Bot support replies, retweets (user tips, shopping, feedback thread), and banter (day 28). About 4–5 are advice-relevant.
- **New pstack skill released:** `/statechart` in pstack v0.15.36 is stable. Best combined with `/create-formal-verification-skill` to model state machines and distributed systems and find bugs. Mini TLC compiler → small IR → mmd; charts via pele.run (themeable). She found 2 real bugs with it. https://x.com/poteto/status/2115880102601101414
- Source path for the skill scripts: https://github.com/cursor/plugins/tree/main/pstack/skills/statechart/scripts (reply). https://x.com/poteto/status/2115927811131310346
- Mild: will look at supporting tla-ts. https://x.com/poteto/status/2115926914531819595
- Reinforces ban-comments: agents justify lazy hacks with comments and the hack spreads. https://x.com/poteto/status/2115644484226777581
- Comment exceptions still allowed: URL to upstream issue/RFC/issue; legal/licenses. https://x.com/poteto/status/2115664844863201667
- Outer-loop: @bot monitor this thread as well as part of your hourly loop. https://x.com/poteto/status/2115882883999232229
- Product notes (not advice): shop with grok bot https://x.com/poteto/status/2115648413530542286 ; day 28 https://x.com/poteto/status/2115714174026436832 ; grok bot 0.78.1 RT https://x.com/poteto/status/2115845643998777820 ; feedback-thread RT https://x.com/poteto/status/2115878277898473663
- Changes earlier advice: yes — `/statechart` companion skill is now released (was "will release soon" on 10-23). New pstack skill released: yes (`/statechart` v0.15.36). Reinforces SUMMARY principles 1, 6, 8, and 11.

## 2026-10-29 09:20 Asia/Taipei (scheduled run)
- New posts this run: 26 (2026-10-28 09:52 to 2026-10-29 08:48 Asia/Taipei). Nothing is left over.
- last_seen_id: 2115606712375988436
- Fetch note: `get_posts_counts_recent` gave 27; gap of 1 vs 26 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 26 across 2 pages (25 + 1; page 3 empty). `get_users_posts` with `since_id` returned the newest 25, then page 2 returned 1 (no further next_token). No long `note_tweet` posts in this batch.
- Most posts are Grok Bot support replies, retweets (referral program, product plugs, mcuban, theo MCP fleet), banter (poteto domains), and jokes. About 3 are advice-relevant.
- pstack as a Cursor plugin (vs copying skills): easier to distribute and keep updated; skills are meant to be composed together, though they can be used piecemeal. https://x.com/poteto/status/2115500996659122327
- Slack: for now make a team bot; soon you can add any bot to Slack; bots can collaborate with each other (quotes her earlier Slack teammates post). https://x.com/poteto/status/2115492618931151002
- Bot outer-loop example: @bot monitor a thread and give an hourly summary of top requests and issues. https://x.com/poteto/status/2115606712375988436
- Product notes (not advice): grok bot 0.78.1 RT https://x.com/poteto/status/2115591199943983129 ; SpaceX Grok Bot referral RT https://x.com/poteto/status/2115533963246882943 ; "grok bot told me to post this" https://x.com/poteto/status/2115586637484921102 ; "what should we ship next?" https://x.com/poteto/status/2115591296698163224
- Changes earlier advice: no. Reinforces SUMMARY principles 8 and 11. New pstack skill released: no.

## 2026-10-28 09:30 Asia/Taipei (scheduled run)
- New posts this run: 31 (2026-10-28 01:26 to 2026-10-28 08:58 Asia/Taipei). Nothing is left over.
- last_seen_id: 2115246885309165930
- Fetch note: `get_posts_counts_recent` gave 32; gap of 1 vs 31 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 31 across 2 pages (25 + 6; page 3 empty). `get_users_posts` with `since_id` returned the same 31 across 2 pages (25 + 6; no further next_token). Long posts use `note_tweet` when present; re-read 2 long posts with `get_posts_by_ids`.
- Most posts are Grok Bot support replies, retweets (Shared Bots, Cursor design Annotate, product plugs), tibot hire plug, and jokes. About 3–4 are advice-relevant.
- Agent-friendly codebase: make the easy thing the right thing; learn from each mistake so bots don't repeat it; token spend goes to quality+velocity; software work is an iceberg (features are a small fraction). https://x.com/poteto/status/2115133011352240581
- tibot example: a Grok Bot that watches mentions/keywords, daily or hourly digest, skips spam, translates, can auto-block abuse, never posts for you; she still writes posts/articles by hand. https://x.com/poteto/status/2115205951649423585
- Mild product: auto-block needs X API and uses API credits. https://x.com/poteto/status/2115207170488926318
- Mild product: X Chat All dropdown can filter out grok bots. https://x.com/poteto/status/2115232513761374227
- Mild: "wow pstack irl" (banter). https://x.com/poteto/status/2115236792136094035
- Product notes (not advice): tibot hire https://x.com/poteto/status/2115205951649423585 ; tibot avatar https://x.com/poteto/status/2115208436816445477 ; grok bot 0.77.0 quote https://x.com/poteto/status/2115242399312290040 ; Shared Bots RT https://x.com/poteto/status/2115152329481892097
- Changes earlier advice: no. Reinforces SUMMARY principles 3, 4, 5, 8, and 9. New pstack skill released: no.

## 2026-10-27 09:30 Asia/Taipei (scheduled run)
- New posts this run: 50 (2026-10-26 09:53 to 2026-10-27 05:04 Asia/Taipei). Nothing is left over.
- last_seen_id: 2114825415143625128
- Fetch note: `get_posts_counts_recent` gave 51; gap of 1 vs 50 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 50 across 2 pages (25 + 25; page 3 empty). `get_users_posts` with `since_id` returned the newest 25, then page 2 returned 0 (pagination token not reusable). Long posts use `note_tweet` when present; re-read 5 long/key posts with `get_posts_by_ids`.
- Most posts are Grok Bot support replies, retweets (Cursor Agent SDK, Elon, hire-bot plugs), personal banter, and jokes. About 4–5 are advice-relevant.
- Tips she highlighted from @yminsky's talk on agent-friendly codebases: agents thrive on feedback (types are one of the best kinds); make illegal states unrepresentable with types; property-based tests, fuzzing, and full-system deterministic simulation testing; expect tests (print and capture behavior; like compiler fixture tests; smaller review surface); formal methods used to be very expensive (seL4 example) but agents change the ROI. https://x.com/poteto/status/2114626630429913383
- Expect-tests example from React Compiler work. https://x.com/poteto/status/2114630175040348590
- Formal verification still early; Bend is promising; closest production-ready path she names is Rust + something like Verus (also incomplete). https://x.com/poteto/status/2114613597515190666
- Short affirmation: "yeah, codebase is memory!" (quotes her earlier inverse-pyramid post). https://x.com/poteto/status/2114765530687250758
- Mild: Jane Street folks interested in OxCaml and formal verification. https://x.com/poteto/status/2114620076494311796
- Mild: compiler backends (LLVM/GCC/Cranelift) will stay; new system languages with less high-level semantics may get more popular because agents make that code less painful. https://x.com/poteto/status/2114611298222875042
- Product notes (not advice): Cursor Agent SDK RT https://x.com/poteto/status/2114799127209115648 ; "hire grok bot" / "what are you going to ship this week with grok bot?" https://x.com/poteto/status/2114818880548041189 https://x.com/poteto/status/2114772732944728512
- Changes earlier advice: no. Reinforces SUMMARY principles 1, 3, and 4 (types/feedback, illegal states, verification ROI, codebase as memory). New pstack skill released: no.

## 2026-10-26 09:30 Asia/Taipei (scheduled run)
- New posts this run: 67 (2026-10-23 09:49 to 2026-10-26 02:35 Asia/Taipei). Nothing is left over.
- last_seen_id: 2114425609044791579
- Fetch note: `get_posts_counts_recent` gave 68; gap of 1 vs 67 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned 67 across 3 pages (25 + 25 + 17; page 4 empty). `get_users_posts` with `since_id` returned 50 across 2 pages (25 + 25; page 3 empty). Long posts use `note_tweet` when present.
- Most posts are Grok Bot support replies, retweets, product plugs, and jokes. About 7 are advice-relevant.
- pstack skills keep shrinking as models get stronger; she expects them to become mostly saved prompts. https://x.com/poteto/status/2114099131845423142
- On over/under-guiding AI, she points to pstack Complete Guide Pt.2 (already in articles/). https://x.com/poteto/status/2114095305910280363
- Favorite pattern: add bots to Slack and let them collaborate like teammates. https://x.com/poteto/status/2114071326411690209
- @bot can send work into a named Project for review (`send this to my silicon project to review`). https://x.com/poteto/status/2114141783735329119
- @bot can repro/fix inside a named Project (`repro and fix this in my X Feedback project`). https://x.com/poteto/status/2114402021461860430
- She runs many Projects at once (up to 27) and tells @bot to spin up more. https://x.com/poteto/status/2113802710248288641 https://x.com/poteto/status/2113807076019626006
- Cost tip: ask the bot to check expensive routines and reduce bot-to-bot messages; routines usually dominate. https://x.com/poteto/status/2113479806952276140
- Product note (not new advice): bot-to-bot email to tibo@mail.grokbot.com for repro (already in SUMMARY section 8). https://x.com/poteto/status/2113463141464154508
- Changes earlier advice: no. Reinforces SUMMARY principles 7, 8, and 11. New pstack skill released: no.

## 2026-10-23 09:30 Asia/Taipei (scheduled run)
- New posts this run: 28 (2026-10-22 09:38 to 2026-10-23 09:20 Asia/Taipei). Nothing is left over.
- last_seen_id: 2113440410442072232
- Fetch note: `get_posts_counts_recent` gave 29; gap of 1 vs 28 unique (same pattern as prior runs). `search_posts_all` with `since_id` returned all 28 across 2 pages (25 + 3; page 3 empty). `get_users_posts` with `since_id` returned the newest 25, then page 2 returned 0. One long post had `note_tweet` text.
- Most posts are Grok Bot support replies, product plugs (phone apps, 1Password, sidebar sections), retweets, and jokes. About 3 are advice-relevant.
- Upcoming companion skill (not released yet): agents draw statecharts/diagrams and check them against specs from `/create-formal-verification-skill`; diagrams use Pele. https://x.com/poteto/status/2113398433977659654
- Formal verification still hard; keep code and spec in sync, ideally in the same language (she names @bendlang). https://x.com/poteto/status/2113440410442072232
- Recommends pstack `/technical-writing` for technical articles (skill already listed in this pack's pstack.md). https://x.com/poteto/status/2113087210115551237
- Product notes (not advice): native phone apps for Grok Bot https://x.com/poteto/status/2113411672815944075 ; sidebar sections to organize bots https://x.com/poteto/status/2113435043205177724 ; bot-to-bot email again (already in SUMMARY section 8) https://x.com/poteto/status/2113084831752151245
- Changes earlier advice: no. Reinforces SUMMARY principles 1 and 11. New pstack skill released: no (companion skill "will release soon").

## 2026-10-22 09:30 Asia/Taipei (scheduled run)
- New posts this run: 21 (2026-10-21 09:31 to 2026-10-22 08:53 Asia/Taipei). Nothing is left over.
- last_seen_id: 2113071127044182505
- Fetch note: `get_posts_counts_recent` gave 22; one is the boundary post 2112670982687297565 (already stored), so 21 is complete. `search_posts_all` with `since_id` returned 21 on one page; `get_users_posts` with `since_id` returned the same 21. No long posts.
- Most posts are Grok Bot support replies, retweets of Grok Bot users, a Grok Bot Pages launch plug, and jokes. About 2 are advice-relevant.
- Ask your agent to draw a statechart of the user flow, then use the `/create-formal-verification-skill` skill you made with pstack to find bugs with TLA+. You understand the code and the user flow better, and fix issues users would otherwise see. https://x.com/poteto/status/2112736749281759566
- She tags the bot on X to "start a new project to implement all these" (bot as outer loop that starts a Project). https://x.com/poteto/status/2113062261791334667
- Product note, not advice: Grok Bot can now build Pages (reports, memos, dashboards). https://x.com/poteto/status/2112995138717016529
- Retweet of her own "pstack Complete Guide Pt.2" article (already in articles/). https://x.com/poteto/status/2112718275859923305
- Changes earlier advice: no. Reinforces SUMMARY principles 1 and 8. New pstack skill: no.

## 2026-10-21 09:30 Asia/Taipei (scheduled run)
- New posts this run: 20 (2026-10-20 09:33 to 2026-10-21 06:23 Asia/Taipei). Nothing is left over.
- last_seen_id: 2112670982687297565
- Fetch note: `get_posts_counts_recent` gave 21; one is the boundary post 2112317822533763290 (already stored), so 20 is complete. `search_posts_all` with `since_id` returned 20 on one page; `get_users_posts` with `since_id` returned the same 20. No long posts.
- Most posts are retweets of Grok Bot product news and users (@bot support-queue story, @elonmusk "Big Grok @Bot update", @jennywen UX note), Grok Bot support replies to @nikorasu_pro, and jokes. About 1 is advice-relevant.
- Prompt example for a bot, given by tagging it on X: "watch this livestream when it's up, take notes, and send me a summary". https://x.com/poteto/status/2112613162591932495 (she calls tagging the bot on X "one of the coolest features": https://x.com/poteto/status/2112606908893053223)
- Not advice, kept for context: "You Can Ship Everything" then "but should you?" (short posts, no article attached). https://x.com/poteto/status/2112356481597317544 https://x.com/poteto/status/2112358119829577826
- Bot-to-bot email feedback to tibo@mail.grokbot.com again (already in SUMMARY section 8 from 10-15). https://x.com/poteto/status/2112424589783633945
- Changes earlier advice: no. New pstack skill: no.

## 2026-10-20 09:30 Asia/Taipei (scheduled run)
- New posts this run: 15 (2026-10-19 13:45 to 2026-10-20 06:59 Asia/Taipei). Nothing is left over.
- last_seen_id: 2112317822533763290
- Fetch note: `get_posts_counts_recent` gave 16; one of them is the boundary post 2111955414166474838 (already stored), so 15 is complete. `search_posts_all` with `since_id` returned 15 on page 1; page 2 was empty. `get_users_posts` with `since_id` returned the same 15. No long posts were truncated.
- Most posts are retweets of Grok Bot product news (iPhone Action Button, new bot characters, Pumpkin Bot), a Cursor feedback call by @n2parko, plugin and support replies, and a retweet of @elonmusk. About 2 are advice-relevant.
- A bot can message your cloud agent or your project agent. Context: @Livenadav asked to tag a Grok Bot inside Cursor chat ("follow @swe bot recommendations from yesterday"); her answer is to tell the bot to message the agent instead. https://x.com/poteto/status/2112303622285668402
- Prompt idea for a bot: "watch this thread and based on what you know about me and my work, propose ideas to improve my bots and workflows". https://x.com/poteto/status/2112264935334126033 (thread: https://x.com/poteto/status/2112246281016119780)
- Retweet (not her words): @aiDotEngineer lists @poteto as "Principal Engineer @ SpaceX" among the first AIE Code Summit speakers. https://x.com/poteto/status/2112317822533763290
- Changes earlier advice: no. Reinforces SUMMARY principle 8 (bot as outer loop that hands work to cloud agents and Projects). New pstack skill: no.

## 2026-10-19 09:30 Asia/Taipei (scheduled run)
- New posts this run: 60 (2026-10-16 11:05 to 2026-10-19 06:59 Asia/Taipei). Nothing is left over.
- last_seen_id: 2111955414166474838
- Fetch note: `get_posts_counts_recent` gave 61 (17 + 30 + 14). Merged unique posts: 60 (gap of 1, same pattern as prior runs). `search_posts_all` with `since_id` returned all 60 across 3 pages (25 + 25 + 10; page 4 empty). `get_users_posts` returned the newest 25, then page 2 returned 0. Two long posts were truncated in search; full text re-read with `get_posts_by_ids`.
- Most posts are Grok Bot support replies, thanks to followers, retweets of Grok Bot users, a "is chat the final form of agent UI" poll, and jokes. About 5 are advice-relevant.
- Trust "inverse pyramid": put most effort at the top. 1) codebase improvements (architecture, stronger types and invariants, clear boundaries; "make the easy thing the right thing"); 2) static analysis (lint, tests, CI, verification such as TLA+); 3) prose (comments, rules, AGENTS.md, skills), used minimally, but do use `/create-verification-skill`; 4) human review, the hardest to scale, so spend it on designing the environment. https://x.com/poteto/status/2111133080526495985
- Same post, Project prompt: 1) read my Slack/chat and code review feedback; 2) `/recall` my past transcripts; 3) `/poteto-mode` use `/correct` and `/architect` on past commits to find common agent pitfalls, then propose a plan to rearchitect code I own to be more agent friendly, prototype instead of deferring, back it with real data; 4) first use `/sharpen` + `/in-your-own-words` to confirm the prompt. (`/sharpen` is not in this pack's pstack.md; not verified.) https://x.com/poteto/status/2111133080526495985
- New pstack skill (v0.15.27, beta): `/create-formal-verification-skill`. A meta-skill like `/create-verification-skill`: it creates a project skill plus a formal verification suite for properties you name (for example TLA+ for state machines and concurrency, kani for Rust undefined behavior). She modeled her team's code with TLA+ and found several bugs. https://x.com/poteto/status/2111926622278521253 (teaser: https://x.com/poteto/status/2111596610836955561)
- The point of her skills is to move rules out of prose and make them deterministic. https://x.com/poteto/status/2111211085575716902
- Retweet (not her words): @addyosmani "Give your agent a way to verify its work." https://x.com/poteto/status/2111604948731609235
- Changes earlier advice: no. Reinforces SUMMARY principles 1, 3, and 4. New pstack skill: yes (`/create-formal-verification-skill`, added to pstack.md).

## 2026-10-16 09:30 Asia/Taipei (scheduled run)
- New posts this run: 72 (2026-10-15 09:32 to 2026-10-16 08:16 Asia/Taipei). Nothing is left over.
- last_seen_id: 2110887537971802251
- Fetch note: `get_posts_counts_recent` gave 73 (70 + 3). Merged unique posts: 72 (gap of 1 is likely a deleted post or boundary bucket, same as prior runs). `get_users_posts` with `since_id` returned only the newest 25 posts then page 2 returned 0. `search_posts_all` with the same `since_id` returned all 72 across 3 pages (25 + 25 + 22). Prefer search for completeness. Three long posts already included `note_tweet` text; re-checked with `get_posts_by_ids`.
- Most posts are Grok Bot support replies, jokes, Tesla Roadster banter, and retweets. About 8 are advice-relevant.
- Comments are unstructured and unenforceable; agents may ignore them or treat them as an escape hatch for bandaids. Prefer stronger types, better API design, and lint rules so the comment is unnecessary. Prompt idea: audit comments to find those opportunities. https://x.com/poteto/status/2110758788525621282 https://x.com/poteto/status/2110635971884802049
- Example: a `// don't use this` comment does not stop another agent from calling the API; a lint rule, or deleting the API, does. https://x.com/poteto/status/2110635971884802049
- You can mix and match pstack skills; they use `disable-model-invocation: true`, so installing pstack does not auto-inject skills or add token cost. Use `/poteto-help` to pick skills. https://x.com/poteto/status/2110760668987322408
- Concrete prompt: `/poteto-mode create a skill that does <xyz> and eval it`. https://x.com/poteto/status/2110759504778592664
- `/poteto-mode` can apply to non-coding goals when the work still needs writing code to reach the goal. https://x.com/poteto/status/2110777496119709745
- Power pstack prompts to upgrade code, starting with refactoring to make the codebase friendlier to agents. https://x.com/poteto/status/2110758136852385984
- Short pstack tutorial (already known): `/setup-pstack` → `/poteto-mode` → `/poteto-help`. https://x.com/poteto/status/2110757066709356851
- Product note: you can submit Grok Bot (and Grok, Cursor) plugins. https://x.com/poteto/status/2110840796954202186
- Changes earlier advice: no. Reinforces SUMMARY principles 3, 4, 6, and 11 (comments → lint/types/delete API; install-cheap skills; poteto-mode + eval for new skills). New pstack skill: no.

## 2026-10-06 16:00 Asia/Taipei (first sync)
- Baseline: pack has 443 posts up to https://x.com/poteto/status/2107366329527513281 (2026-10-06 15:04).
- New since baseline: 1 post, https://x.com/poteto/status/2107375595458105520 (15:41), a joke reply. No advice takeaway.
- Changes earlier advice: no. New pstack skill: no.

## 2026-10-07 09:23 Asia/Taipei
- New posts: 84 (2026-10-06 16:07 to 2026-10-07 09:23 Asia/Taipei). Most are jokes, banter with @thsottiaux, retweets of Grok Bot users, and product plugs (Teams, Atlassian, @bot tagging on X). About 17 are advice-relevant.
- Bot does the "first mile" (pull context from connectors, routines on schedule or events). Cursor cloud agents do the "last mile" (ship code). Her daily loop: Slack feedback, Linear ticket, cloud agent triages and reproduces with pstack, fix PR, fuzz with a small agent swarm, ping on Slack, auto-merge after 1 hour unless she asks for changes. https://x.com/poteto/status/2107510472601985336
- Last mile in engineering means shipping: bots use cloud agents to build, test, and verify, then the PR ships. https://x.com/poteto/status/2107514676401893740
- Use an issue tracker as a queue and as memory, so bots dedupe and search related issues first. She uses Linear. https://x.com/poteto/status/2107513933838065821 https://x.com/poteto/status/2107528644398854576
- Split big loops into specialist bots, a Cursor cloud agent, or skills that the bot writes. https://x.com/poteto/status/2107520739645726845
- Release and QA automation: two Team Bots in Slack (release manager "sandcastle" and engineer bot "poteto"). A fuzz swarm of 10+ agents uses the verification skills and feature map, some directed and some random. Found issues go to a Cursor Project that owns triage and fixes, with a cherry-pick plus patch release when severe. https://x.com/poteto/status/2107527180263829827
- This works only because of a high-quality verification skill. Make one with pstack `/create-verification-skill`. https://x.com/poteto/status/2107529149355319657
- "Fuzzing" means agents run the app on their own computers with a test user account against prod and click around like a real user. https://x.com/poteto/status/2107584297351970839 https://x.com/poteto/status/2107640440908595699
- She now mostly reviews the videos and screenshots that agents record in their VMs. https://x.com/poteto/status/2107529532144234937
- Verification stack: verification skills and CLIs, good unit and integration tests, a few critical e2e tests, CI of about 5 minutes. https://x.com/poteto/status/2107516481844269509
- Unit tests still pay off, but agents write slop tests, so add skills that teach better tests. https://x.com/poteto/status/2107520037666136125
- Monorepo CI: prefilter directories so each PR runs only the affected subset of CI. https://x.com/poteto/status/2107601625804378182
- Cloud agents have their own VMs and can get secrets, so they can install any CLI they need. https://x.com/poteto/status/2107602532549956055
- Give plenty of direction at the start, then let agents run with pstack and self-verification. https://x.com/poteto/status/2107567417316831523
- Her PRs are a few hundred LOC: refactors, performance, bug fixes, CI infra, things that help teammates move faster. https://x.com/poteto/status/2107538850344296622 https://x.com/poteto/status/2107555957584937373
- A bot in Slack with its own profile must be a Team Bot. https://x.com/poteto/status/2107593186453684532
- Retweet: pstack autonomously found and fixed an O(n^3) event-loop stall (160x speedup). https://x.com/poteto/status/2107498315919319448
- Note: the "last day at cursor / spacex" post she replied to is by @msfeldstein, not by her. https://x.com/poteto/status/2107533903133348174
- Changes earlier advice: no. All of this reinforces SUMMARY.md principles 1, 2, 7, 8, and 9 (verification first, verification CLI plus feature map, Projects plus cloud agents, Bot as outer loop, land only after independent verification).
- New pstack skill: no. `/create-verification-skill` is already in pstack.md.

## 2026-10-08 09:22 Asia/Taipei
- New posts: 100 (2026-10-07 10:47 to 2026-10-08 09:12 Asia/Taipei). Most are jokes, short replies, Grok Bot support replies, and retweets about the Grok Bot update (Opus 5.5 as a back-end model, Main bot, Team Bots in Slack, X search/monitor). About 12 are advice-relevant.
- Fetch note: `get_users_posts` with `since_id` returned only the newest 21 posts (from 2026-10-08 06:28). `search_posts_all` with `from:poteto` and the same `since_id` returned the other 79. Use both in later syncs.
- Cloud agents for one-off small tasks ("fix this bug here"). Projects for a group of related tasks ("fix all the bugs users reported on Slack"). https://x.com/poteto/status/2107954395979944361
- Ask your bot to spawn a project agent; bots can create Projects. https://x.com/poteto/status/2107939119058088281 https://x.com/poteto/status/2107701402093113772
- Grok Bot plus Cursor Projects is her recommended pairing. https://x.com/poteto/status/2107915158601535885 https://x.com/poteto/status/2107664192631455970
- Feedback loop: bot monitors X for user feedback, sends feature requests to the issue tracker, and sends bug reports to a Cursor cloud agent or Project to triage and fix. X search/read is free for all users with no X connector. https://x.com/poteto/status/2107963437154435182 https://x.com/poteto/status/2107963575105192357 https://x.com/poteto/status/2107984949223817511
- Thought experiment "time to (fully automated) rewrite" (TTR): if you would not trust a hands-off rewrite because agents cannot prove identical user-visible behavior, that same gap slows you today. Also ask about perf, ease of deletion and extension, and whether quality holds as PRs flow in. https://x.com/poteto/status/2107913381751730352
- Ways to lower TTR: verification as token efficiency (no verification means rework later), a high-quality test suite (the cheapest lever, but few codebases have one), and libraries such as XState or Effect to enforce business-logic invariants. "Your codebase is a form of memory and an input to agents." https://x.com/poteto/status/2107922229711585334 https://x.com/poteto/status/2107918163111477487 https://x.com/poteto/status/2107919330931609601
- Candidate metrics for agent setup quality: percent of agent-written code that gets merged, revert or rework rate, and number of human messages per accepted PR (fewer is better). https://x.com/poteto/status/2107923381001781362
- Good engineering still matters; imagining a rewrite helps you work backwards to improvements in legacy code. https://x.com/poteto/status/2107920188494709220
- `/setup-pstack` can now set a budget. https://x.com/poteto/status/2107949669695582437
- New Grok Bot users: connect the apps you use first, and do everything with one bot before you add specialist bots. https://x.com/poteto/status/2107830403549831186
- Bot templates must be reinstalled to get updates. https://x.com/poteto/status/2107988934345318426
- Retweet (by @vinvan, not her words): "poteto playbook" of one Project (orchestrator) per workstream, talk only to Projects, Projects spawn cloud agents in poteto mode, verify with cross-model reviews; 145 PRs merged in a day. https://x.com/poteto/status/2108000083468067199
- Changes earlier advice: no. The cloud agent versus Project split matches SUMMARY.md principle 7 and the earlier advice to keep one Project for fuzz-issue triage and repair (a group of related fixes), not one Project per fix. TTR and the metrics reinforce principles 1 and 4.
- New pstack skill: no. `/setup-pstack` (models and reasoning budget per role) is already in pstack.md.

## 2026-10-08 11:29 Asia/Taipei（视频转写：X 帖 2107911765967118750）
- 来源：https://x.com/scarfpinkgirl/status/2107911765967118750 （@scarfpinkgirl 转发的合集，不是 poteto 本人发布；3:43:40）。
- 内容：Colin Matthews 主持的 workshop（出现 3 次，其中 1 次是完整版）加 Matt Pocock 直播访谈（已在 `spacex-transcript.md`）。
- 转写：`videos/2107911765967118750/transcript.md`（烧录字幕 OCR，加 Whisper 核对）。总结：`videos/2107911765967118750/summary.md`。
- 新细节：Dune 五条规则原文；skill eval 做法（rubric、伪装目录、跨模型 judge、`/loop` hillclimb）；先在本地建验证再上云；`useEffect` 禁用和依赖图 CI 检查；拆 PR 的理由；token 投入的 ROI 说法。
- Changes earlier advice: no. 内容加强 SUMMARY.md 原则 1、2、3、6、9。
- New pstack skill: no.

## 2026-10-09 17:40 Asia/Taipei (manual rerun; the 09:17 scheduled run failed and wrote nothing)
- New posts: 160 (2026-10-08 09:38 to 2026-10-09 16:33 Asia/Taipei). Most are jokes, banter with @thsottiaux, Grok Bot support replies (sign-in, @bot tagging, X search is free), retweets about the Grok Bot update and the Shopify connector, and "@bot repro this" replies. About 15 are advice-relevant.
- Fetch note: `get_users_posts` with `since_id` returned only the newest 50 posts (from 2026-10-09 05:58). `search_posts_all` with `from:poteto`, the same `since_id`, and `until_id` returned the other 110. `get_posts_counts_recent` gives 127 + 33 posts for the same window, which matches the 160. Both tools now return at most 25 posts per call.
- File note: `public_metrics` is stored only for the first 25 of these 160 posts. The 185 posts from the 10-07 and 10-08 syncs were backfilled into `posts-raw.json` and `posts.md` on 2026-10-09 (788 posts now).
- "Volume does matter": if you are no more productive with agents than before, ask why. Scaling up depends on trust in agent output. The engineer's job is now to build "the machine that writes the software" (software factory, or "Michelin kitchen"). https://x.com/poteto/status/2108290818746528017 https://x.com/poteto/status/2108468915802431533 https://x.com/poteto/status/2108295872052359290
- Where her PRs come from, all using pstack: perf, bug fixes from user reports, refactoring to make the codebase friendlier for agents, skills, features, UI polish, harness, dev tools, release, and o11y. https://x.com/poteto/status/2108279582088671583 https://x.com/poteto/status/2108293717555908763
- Risk-based review: agentic code review rates the risk of every PR. Low- and medium-risk PRs merge without human review, with bugbot as well. Humans review only some higher-risk PRs. Goal: "figure out how to make human code review obsolete". https://x.com/poteto/status/2108283057581195413 https://x.com/poteto/status/2108088020146720913 https://x.com/poteto/status/2108329348600381660 https://x.com/poteto/status/2108394806548566459
- "A lot of this hinges on verifiability." https://x.com/poteto/status/2108469410587685055
- Bug loop: her X-mention bot sends reports to Slack. Another bot in Slack uses pstack to triage, reproduce, and fix. She replies "@bot repro this" or "repro this and remind me to check on it 8am". https://x.com/poteto/status/2108253488451100877 https://x.com/poteto/status/2108454433415934253
- Cursor Projects make context switching easier for her. She relies on videos and screenshots, although agents struggle to capture some interactions. https://x.com/poteto/status/2108471414122815799
- Feature map: it helps agents understand every feature in the app and how a user reaches it. "Think of it like docs." https://x.com/poteto/status/2108098335152521311
- Start with one bot. Add new bots only when one gets hard to manage, or you end up with too many unnecessary bots. https://x.com/poteto/status/2108097362283597916
- Non-frontier models get smarter and stay affordable. You do not need frontier intelligence for every task. https://x.com/poteto/status/2108464956165554477
- Software engineering principles still matter. Her priorities: user experience first, then whatever helps the team move faster. To understand a change, ask your agent for visualizations and diagrams. https://x.com/poteto/status/2108304148009730244 https://x.com/poteto/status/2108300758605320594 https://x.com/poteto/status/2108297694561394852
- Reaching her current setup took about 6 months and a lot of refactoring; her talk is the closest compressed form of these ideas. https://x.com/poteto/status/2108320890333388854 https://x.com/poteto/status/2108454075138548016
- Grok Bot features: daily-digest routine prompt (watch X, Slack a digest at 9am, suggest workflow improvements). Grok Bot can run shell commands and CLIs on your machine (local computer use is still WIP). It works with Cursor Ultra. There is a Shopify plugin. https://x.com/poteto/status/2108232222163812795 https://x.com/poteto/status/2108099135228510453 https://x.com/poteto/status/2108394093164609806 https://x.com/poteto/status/2108338959386554546
- Changes earlier advice: no. Risk-based auto-merge sharpens principle 9 (self-merge only when verification is trusted): low-risk changes can land on automated review, and higher-risk ones (such as production data writes) still need a human. The other posts reinforce principles 1, 2, 4, 7, and 8.
- New pstack skill: no.

## 2026-10-13 10:40 Asia/Taipei (scheduled run, capped at about 300 posts)
- New posts this run: 296 (2026-10-09 23:18 to 2026-10-12 00:52 Asia/Taipei). Not fetched yet: 153 newer posts (2026-10-12 01:00 to 2026-10-13 10:20 Asia/Taipei). The next run starts from last_seen_id and gets them.
- Most are jokes, banter, Grok Bot support replies (sign-in, @bot tagging, bot email), the "what did you get done this week with @bot?" thread replies, and retweets. About 15 are advice-relevant.
- Fetch note: `search_posts_all` rejects `since_id` together with `end_time`. This run used `start_time` (time of the last_seen post) plus `end_time` 2026-10-11T17:00Z to take the oldest ~300, and filtered by id. 12 pages of 25. `get_posts_counts_recent` gives 80 + 142 + 74 = 296 for the same window, which matches. `get_users_posts` was not called because the counts matched.
- Projects, not nested agents: she lets Cursor Projects manage agent nesting. https://x.com/poteto/status/2108659455386906898
- She runs 16 Cursor Projects in parallel, each with hundreds of subagents. Her most used prompt: "/bro catch me up on everything since my last message, and if there are any action items for me give me enough context (exec summary) to make a call". This became pstack `/ketchup`. https://x.com/poteto/status/2109024196760305861 https://x.com/poteto/status/2109026625564368991 https://x.com/poteto/status/2109041205132816740
- "If its fuzzed it ships": she runs most work on full autopilot so she is not the blocker. https://x.com/poteto/status/2109027957658595612
- "Lately i just make a new project every time i get an idea." https://x.com/poteto/status/2109030035315364212
- Starter prompt for a coding bot: "make me an engineer bot that uses cloud agents and pstack for coding work. it should make a project to group together related tasks". https://x.com/poteto/status/2108592835046101383
- Cloud agents can use any model available in Cursor; tell the bot which ones to use. Cloud agents run on fairly large machines with no GPU. You can open bot-spawned cloud agents in Cursor for detail. https://x.com/poteto/status/2108595867469172908 https://x.com/poteto/status/2108595707024417203 https://x.com/poteto/status/2108601188644192389 https://x.com/poteto/status/2108596143437557931
- Emails do not wake a bot. https://x.com/poteto/status/2108758810336936278
- pstack is now 10% smaller (fewer tokens) with no loss in behavior; updates are automatic in Grok Bot and Cursor. She tests skill changes with evals. https://x.com/poteto/status/2109116030761230571 https://x.com/poteto/status/2109119085007257692 https://x.com/poteto/status/2109132333140091244
- Too many slash commands: try `/poteto-help`. https://x.com/poteto/status/2109153122526662682
- Long post "all code is slop": Good Code is correct, bug free, and fast and cost efficient to run. Most software relies on tests and o11y, not formal proof. The new craft is to make agents write better code; if your productivity with and without agents is about the same, something is wrong. https://x.com/poteto/status/2109110547824378140
- Follow-ups: you still need all the testing you did before. "Easy to change" is more a property of the agent loop than of the code. Humans stay responsible, but they change outcomes by designing a better agent loop, not by hand-editing code. Agents are a mirror: guide and constrain them well. Use agents to pay down tech debt. https://x.com/poteto/status/2109126675644723245 https://x.com/poteto/status/2109120300755612006 https://x.com/poteto/status/2109307800367337744 https://x.com/poteto/status/2109307096152092880 https://x.com/poteto/status/2109300499153555513
- Script rot in CLI + skill tooling is not a real risk; agents update the scripts as they use them. https://x.com/poteto/status/2109137640377512370
- Retweet (by @mattpocockuk, not her words): /retro may recommend turning repeated tasks into custom tooling (a CLI plus a skill). https://x.com/poteto/status/2108950264850104518
- Changes earlier advice: no. "A new project for every idea" fits the 10-08 rule (Projects for a group of related tasks, cloud agents for one-off fixes); it does not mean a Project per single fix. "If its fuzzed it ships" reinforces principle 9.
- New pstack skill: yes, `/ketchup` (catch up on everything since the user's last message, with an executive summary for each action item). It is not yet listed in pstack.md.

## 2026-10-14 09:40 Asia/Taipei (scheduled run)
- New posts this run: 225 (2026-10-12 01:01 to 2026-10-14 09:05 Asia/Taipei). This includes the 153 posts left over from the 2026-10-13 capped run. Nothing is left over.
- last_seen_id: 2110175208632164577
- Fetch note: `search_posts_all` with `since_id` gave 225 posts in 9 pages of 25. `get_users_posts` with the same `since_id` stopped after 75 posts (3 pages); all 75 were already in the search set. `get_posts_counts_recent` gives 226 (68 + 76 + 68 + 14). The gap of 1 is probably a deleted post or the boundary bucket. Search results did not include `note_tweet`, so the full text of 11 long posts was read with `get_posts_by_ids`.
- Most posts are the "slop / clean code / maintainability" reply debate, Grok Bot support replies (0.70.2 desktop-offline fix, "update computer" in settings), the new X Subscription (one plan for Grok, Grok Bot, Cursor, X Premium), jokes, and retweets. About 20 are advice-relevant.
- Verification is the entry point of the agent loop. The agent runs the app like a real user (CLI, API, or UI) and makes an artifact (video or screenshots for UI) that proves the work is correct, matches intent, and is easier to review than the whole PR. Skill packs are optional. https://x.com/poteto/status/2109436202554372476
- Two things cut through the noise: 1) the agent can verify its own work, 2) the codebase is memory. Turn every nit and bad agent pattern into a constraint (lint, compiler diagnostics, types) until an agent with little context can one-shot a good PR. Better: make anti-patterns impossible with types or a framework. "forget rules and skills. you can add those later." https://x.com/poteto/status/2109699980248408574
- Move rules out of prose (comments, rules, skills) into hard constraints where possible. For a migration: add a lint rule that blocks new use of the old pattern, then open PRs to rewrite old uses. A deprecation comment is not enforced. https://x.com/poteto/status/2110166571335455209 https://x.com/poteto/status/2110161793331208527 https://x.com/poteto/status/2110164056422465845
- Ban and delete most code comments; agents copy workaround comments. Use pstack `/no-comments`; it keeps comments that must exist (for example a browser quirk). Prompt: "create a project agent that uses /poteto-mode to spawn a /swarm to use /no-comments and identify useless code comments we can prune in my repo. come back with a high level plan of which of these workarounds would be best solved by refactoring and which we can straight up delete". https://x.com/poteto/status/2110149626133438732 https://x.com/poteto/status/2110162500658557438 https://x.com/poteto/status/2110164915776577813
- Engineers design the environment so agents write good code ("let it write slop", then constrain the codebase so average output is good). Maintainers can shape the codebase so anyone can write good PRs. Fix it by designing better codebases, not by slowing down or rejecting work. https://x.com/poteto/status/2109338732713447790 https://x.com/poteto/status/2109761952696483905 https://x.com/poteto/status/2110044493378646252
- Good Code = correct, bug free, fast, resource efficient. Clean code for humans costs performance; agent maintainability means fast and bug-free code and token efficiency. New principles of agent-friendly architecture will come. Most of her PR volume is refactoring. https://x.com/poteto/status/2109356992032817621 https://x.com/poteto/status/2109401462526951717 https://x.com/poteto/status/2109384476707168646 https://x.com/poteto/status/2109361189071499640
- New pstack skill `/in-your-own-words` (pstack 0.15.23): the agent restates your goal and problem to confirm alignment. pstack updates automatically in Grok Bot and Cursor. https://x.com/poteto/status/2110047236369547621 https://x.com/poteto/status/2110047891201114165 https://x.com/poteto/status/2109892229938794508
- Use `/poteto-mode` for work that needs rigor; it has a bugfix playbook (repro and root cause before the fix). Most engineering tasks need the rigor. Ask `/poteto-help` which skill to use. https://x.com/poteto/status/2110151974733881568 https://x.com/poteto/status/2110158810040217784
- She lets agents write skills because it is faster inside an eval loop; she runs evals on pstack skills. LLM-judge eval example: https://x.com/poteto/status/2110168010942276005 . pstack now has an agent plugin.json and may work in other harnesses. https://x.com/poteto/status/2109891339781574941 https://x.com/poteto/status/2109912648116826250 https://x.com/poteto/status/2110151011176427623
- Bot topology is your choice: one bot for all, specialist bots, or several generalists that each own a project. The key is multitasking. Personas help the human group related work, like Projects do. https://x.com/poteto/status/2109781899610874002 https://x.com/poteto/status/2109777878099558553 https://x.com/poteto/status/2109774976987660343
- Retweets (not her words): @addyosmani "the at scale part comes from verification" https://x.com/poteto/status/2109384567090274521 ; @DanielLockyer "~75% of my issues with AI coding disappeared once I gave my agent the ability to verify its own work" https://x.com/poteto/status/2109727751267885310
- Changes earlier advice: no. It supports the current Geyoto order: make smoke-modules produce proof (screenshots or video) first, then turn repeated agent errors into lint or type rules. New pstack skill: yes, `/in-your-own-words`.

## 2026-10-15 09:30 Asia/Taipei (scheduled run)
- New posts this run: 96 (2026-10-14 09:30 to 2026-10-15 08:59 Asia/Taipei). Nothing is left over.
- last_seen_id: 2110535901600481520
- Fetch note: `get_posts_counts_recent` gave 97 (89 + 8). Merged unique posts: 96 (gap of 1 is likely a deleted post or boundary bucket, same as 10-14). `get_users_posts` with `since_id` stopped after 50 posts (2 pages of 25); page 3 returned 0. `search_posts_all` with the same `since_id` returned all 96 across 4 pages. Prefer search for completeness; keep user timeline for `note_tweet` on the newest pages. One long-looking post was re-fetched with `get_posts_by_ids` and was already complete (no missing `note_tweet`).
- Most posts are Grok Bot support replies (sign-in, bot mail, Grok Voice 3.0 plugs), jokes, LAY'S potato banter, and retweets. About 14 are advice-relevant.
- Durable part of pstack: engineering principles as short skills (~10–20 LOC). `/poteto-mode` holds a short index and tells agents to name each principle that shaped a decision. You can also invoke `/principle-<name>`. As models get smarter she expects many skills to compress into short principles or workflow step lists, and some to be deleted. https://x.com/poteto/status/2110496830429839869
- Prefer moving prose (comments, agents.md, rules, skills) into deterministic code: lint rules, strong types, good API design. Skills stay flexible (omit or invoke on demand). For cost: run `/setup-pstack` and pick a budget; when you invoke `/poteto-mode`, tell the agent not to create large swarms — that is usually where cost comes from. https://x.com/poteto/status/2110498629307990461 https://x.com/poteto/status/2110205947079721252 https://x.com/poteto/status/2110214216783401042
- `/poteto-mode` usage: she mostly leaves agents/bots in `/poteto-mode` and lets it pick skills. Do not use it for everything — reserve it for the hardest tasks that need rigor; run `/setup-pstack` for budget. Skills default to `disable-model-invocation: true`; you can add a personal rule to always run `/poteto-mode`, or call it by hand. https://x.com/poteto/status/2110504678048014571 https://x.com/poteto/status/2110534523389943974 https://x.com/poteto/status/2110535901600481520
- Tell your bot to spawn cloud agents with mode set to poteto-mode by default (a param on the spawn-agent tool). https://x.com/poteto/status/2110498826813649079
- Some skills are a real list of steps (a workflow), e.g. `/arena`; agents will not do that pattern on their own. Continuously tune skills and ablate sections that are no longer needed. Ask `/poteto-help` to learn the plugin. https://x.com/poteto/status/2110502000437924249 https://x.com/poteto/status/2110415199962612120 https://x.com/poteto/status/2110483991363289395
- Action at a distance is a footgun for humans and agents; refactor it away now that agents can do the rewrite. Agent-written comments are rarely good. https://x.com/poteto/status/2110229209130086668
- Multiplayer Grok Bot over email: debugging (send bug reports to another bot), support, booking, group buys, craigslist-style trades. Example: ask your bot to email tibo@mail.grokbot.com for a bug report. https://x.com/poteto/status/2110192382096679248 https://x.com/poteto/status/2110192878379278662
- Changes earlier advice: no. Reinforces SUMMARY principles 3, 4, 6, 8, and 11 (deterministic constraints over prose, comment hygiene, Bot outer loop + poteto-mode defaults, principles index). New pstack skill: no (`/grill-the-poteto` was a joke reply; `/principle-<name>` already listed in pstack.md).
