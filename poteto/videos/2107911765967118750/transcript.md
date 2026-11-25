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


## 段 A：Colin Matthews workshop 剪辑版（0:00:00–0:52:26；字幕 OCR）

**[0:00:00]** Personally, I think that the a - - = = © really like someone you're pair programming with, and nota tool to just replace the _ act of writing code. or worse, outsourcing your thinking. And think there's a tendency, because AI is so exciting, you want to put AI everywhere and be seen as someone who Is very, what do you call it, on the ball, I guess, with

**[0:00:31]** AI. [hat you feel this PIicosoure Vi, i ve Sut tu increase my productivity, I've got to ship like 100 PRs this week and barely understand what I'm doing and vibe a - ae a * “ I on code my way toa LUUE ITly Way LU a code my way toa 3 million ARR or whatever. But think, you know, one of the things that I've personally seen Is that although save some time, you know, writing the code, I actually find myself spending more time reviewing what the AI did and like correcting it. So

**[0:01:02]** you know, like I've tried the thing that a lot of people say like, you know, you instead of prompting an AI to tust build the feature outright, you sort of get it to build a spec for you first, then you review that spec, and then you do that whole thing then it's like, okay, so I assume you can see my screen. Yes. Yeah. So yeah, today. Yeah, i think I think the big theme for me as I've been using agents to write code, and I'm sure a lot of you have had the same experience as well is how do you trust it? You know, especially

**[0:01:32]** if you are an engineer that's been writing code for a very long time, you have a lot of opinions and lessons that you've learned about doing good engineering. And when you see agents just, you know, winging it and, you know, guessing, hallucinating, you know, confidently stating that they found the smoking gun for the hundredth time, but it's actually not the real problem. You lose a lot of trust. And when you lose, when you don't have much trust in your agents, feel like you really can't get the most out

**[0:02:02]** of them. And for me, the parallel is like with management. So if I'm an engineer manager of a team, and I have a bunch of, you know, I have a team of engineers on my team, and I don't trust them, then the mode of operation I'm going to be in is going to be like micromanagement, right? I'll have to spend a lot of time looking over my report's shoulders and checking that they're doing their work well. You know, that they're not shipping bugs to production. And so I drew this chart because It's

**[0:02:33]** not, it's not a verv scientific chart, but like, this is how I imagine myself and my journey through using agents. So, you know, like fast forward or back forward or fast back, fast backwards, like a year or so when, you know, nobody was, or not many people were using agents to code. So think you, you know, get into this mode where you are in very heavily in the loop with one or several, like a handful

**[0:03:04]** of agents. And you find yourself just constantly, you know, trying to understand what your agents are doing. And you're very, very in the loop. You're watching every single output. You are sitting there prompting. And you really can't parallelize beyond that because you don't, again, you don't have that trust, right? You can't go to a hundred agents, like spawn a hundred agents when you don't even trust the output of one agent. So over the past five months, I feel like I've really been able to, like,

**[0:03:34]** ascend this trust curve. And now I'm at the point where I actually have, this sounds kind of scary to say this, and it makes me sound like a slop artist, but I promise I'm not. But I actually have my agents now auto-merging PRs for me, which ts like a wild thing to say. But like I woke up today and there were like 20 PRs landed and I just reviewed them on main, like they were already landed and they were good. So how did I get to that point? It's basically

**[0:04:04]** what I wanted to talk about today. And again, like, yeah, feel free to jump in if you have questions, Colin. But, oh yeah, of course I got to show this chart where... No, do not trust... Someone requested to control my computer. Probably won't do that. But yeah, so this chart, think... I'm sharing this chart not to kind of like flex, but to kind of show like the journey.

**[0:04:35]** Like, so you can see like the curve, like it sort of like inversely matches the contributions I've been able to land at Cursor. So I joined five months ago. And five months ago, like I, you know, my first month, I was like. not very productive because I was, you know, I was learning the code base. I was going on. And as. got more confident in mv agents, I've really been able to kind of ramp up my productivity. And again, like, yeah, like last month I shipped a. thousand PRs, which is ridiculous.

**[0:05:05]** And then this month, we're only on the 12th. I'm already at like almost 800 PRs landed. So the velocity is definitely high. And you, I'm sure. a lot of you will. definitely be questioning like how, how much of this code is actually good. And I think, yeah, that's definitely fair to question. But yeah, I think, I think if you set uD your agents well, you can definitely get to a very similar level. I

**[0:05:35]** talk about how we do that. So for me, I think I'm curious, like, I guess, calling your experience as well. But for me, I think the most important skill that you should have in your toolbox when you work with agents Is verification. And by verification, I mean the ability for an agent to actually run the code or take CPU traces or heap snapshots or, you know, open an iOS simulator,

**[0:06:08]** whatever, you know, however your application is exposed to your users, it can do the same thing and run it for real and actually test and verify it don't work. Because that's the thing that really closes the loop. It doesn't guarantee your agent writes good code, but it allows them to at least write correct code, which is a big, a really big step forward for being able to trust your agent. will, I can share one example that we have

**[0:06:38]** within cursor. So for the cursor agent window, so this Is actually an interesting story. But when I joined cursor five months ago, they're actually, well, I

**[0:07:10]** was supposed to joina different team. I was supposed to join like the cloud agents team. But then since I have a lot of experience working on React and agents window is a React application, was asked to basically help out with the agent window work. But there wasn't really a lot of like skills to help me. So I just found myself that, okay, agents window Is going to launch in like a week. Right. We have a really tight deadline. And there was, you

**[0:07:42]** know, I was just sitting there like, okay, I'm going to open up the performance, the Chrome Dev tools and look at it myself and try to make sense of this flame graph. And keep in mind, I was just like in my first week. So I had no idea what I was looking at. No idea what, you know, mean, I had some idea, but you know, the code base was completely fresh to me. And I realized like my agent had no idea either, you know, like I would take a screenshot of the trail, download trace, I would send it to it and it'd be like, yeah, it kind of looks like this, you know, and it would like confidently state like it's

**[0:08:12]** this thing. And then I try to fix that. And turns out that's not the actual thing. So this was a very, very slow process. And if you've ever done any like know, Just even development with an agent where you don't have a verification skill, you are the verifier, right? You're the bottleneck. You tell your agent to do something, and then it goes off and write some code. Then you open up your, you know, local dev build. And then you start to say, oh, you know, it doesn't work. Then you have to copy paste screen, you know, screenshots or console errors or

**[0:08:42]** whatever. And then your agent like slowly kind of like, you know, works with that, and then tries to understand it and fix the thing. But then you're constantly just in the loop and being a bottleneck. So there's really no way to parallelize. So the control glass skills are like one of the first skills I built for cursor. And glass, by the way, is the code name for agents window that we use internally, but it's just cursor, I guess. And so this skill is, guess, the code itself

**[0:09:12]** is not super interesting. Your agent can very easily make one for you. Where if you're building an electron app or a web app, or even iOS applications, you can teach your agent how to use like the Chrome DevTools protocol, or through. Apple has some utilities as well for running the simulator I and taking traces and controlling programmatic control as well. So that's really useful. But one thing |! actually want to talk about

**[0:09:43]** is the this thing. Where is the read me? So this skill comes with this very unique feature called, or not feature, a unique file called a feature map. And so the story then is like, I built this skill. And so now the agent was able to actually run the agent window and take traces and whatnot. But it had no idea what the agent's window was. So,

**[0:10:13]** you know, like, someone would say like, oh, the left sidebar is like, laggy or something like that. Or, you know, the right side, the PR tab is not working. And the agent I would just be like kind of flailing around. It would spend a lot of time trying to like look up the code. And, you know, where Is this feature? How do I actually get to iton the UI? Which made it basically completely useless? You know, like, you know, like, I would run the skill locally. And, you know, it would spawn a dev build. But then it just be churning. Like, I just try to click here.

**[0:10:43]** It wouldn't know how to get to things. And it was just an awful experience. So, Wu is putting arrows ont my screen. So, yeah, this feature n map has been really useful because it teaches the agent how. to get to all of. the features th at you have. And in Pstack, the plugin that I've made, if you search for Pstack cursor on Google, you'll find it. But there is a create verification skill in that plugin where it actually helps you

**[0:11:14]** set up something like this for yourself, including the feature map. So, it will actually explore the code and build up this initial feature map that tells your agent how to get to all of the different features that you have. And this IS extremely powerful because now that you have these user repo rts that come in, you can actually map even likea vasue report or even a screenshot. So, we have this internally at Cursor where we have a Slack channel with, you know, lots of people giving us feedback on the agents

**[0:11:45]** window and Rockbott and whatnot. And. oftentimes the report Is bad, like very low quality. Like someone will just put very often we get like a screenshot and then someone just says question mark, question mark, question mark. Like, what is this? And, you know, like without this, your agent is like, Ihave. no clue. Right. But with at featu re map like this, it has a lot more context and understanding of how get to all of the different features. So, like, you know, example, like, I guess, like the sidebar, like what Is the

**[0:12:15]** . sidebar? You know, like all the different sub features that are present in It. Like from the user point of view, here's how to get to it. All the . different keyboard shortcuts. Even like the the what do you call it? The DOM elements or like the attributes that you use for selecting things through the CDP are all there. So again, yeah, this Is agents. : And Pstack ships that create

**[0:12:46]** verification skill, but also a maintain verification skill. So you can keep this up to date. Cool. Yeah. was just going to ask how you created that. So do you mind sharing a little bit more about that process in the context of Pstack and maybe just what Pstack ts for the folks who aren't familiar? Yeah. So Pstack is pretty interesting because, well, first of all, the name Is kind of goofy. Like the P, the P in Pstack is like potato, potato snack because I, so there's a pretty

**[0:13:16]** famous person, Gary Tan, who is the CEO of Y Combinator. And he's come up with this plugin called Gstack, Garystack. And funnily enough, we share the last name. We have no relations, but ! thought It would be funny to kind of, you know, poke fun at Gary and make Pstack. My version of his plugin, but kind of just tailor it to mv own set of engineering practices. But I honestly actually never set out to build Pstack.

**[0:13:47]** it just started witha bunch of skills, right? Like started with that control glass skill and then I started with another skill like called how, which I| also noticed through like observing agents. So like, you know, in the early days of me, this ladder, I was like super in the loop. And was basically nitpicking my agents to an extreme degree. was like, I would tell it, you know, this a bug report. Like, why isn't it working? And very often the agent would just

**[0:14:17]** like confidently state like, oh, it has to be this, right? It has to be this thing. And I noticed like when I looked at the actual tool calls, I noticed it wasn't actually reading the code that I thought should be affected. And that made me just extremely suspicious. And at that point I was like, I'm not going to, I can't trust any, this agent anymore because it's And I think, I think it's very easy to just, you know, like build up that distrust and not, and kind of feel helpless. Like,

**[0:14:47]** you know, you don't know how to help your agents succeed. But like, again, I think the management analogy is super helpful because like, imagine if you were a manager of an engineering team and you had an engineer on your team who was a really good coder, no business context whatsoever. You know, they and they onboarded, you know, like five seconds ago. And so how do you actually teach that person to be effective? is through a skill, a skill being just, you know, just markdown, right. But, you

**[0:15:17]** know, it encodes a lot of information instructions, a lot of, you can really draw out a lot of intelligence from an agent by, well, some people on Twitter call it like, you know, pull the agent to a different latent space, which Is kind of like a fancy way of just saying, like, since, you know, LLMs are sort of like, they predict the next token. When you give it some high quality tokens to begin with, then, you know, it can kind of pattern match on like a higher space that's, you know, smarter.

**[0:15:49]** interesting model there. But yeah, built P-Stack very, very incrementally. So started with just really observing how agents, you know, all the different failure modes of that agents were having. And every time I saw that, I just, okay, I'm just going to make that a skill. All right. Like stop hallucinating. Actually go and search up, look up the code. Use a lot of sub-agents. And yeah, stop guessing. Yeah, that makes sense. One kind of follow-up question here,

**[0:16:19]** both from myself and from a bunch of people in the chat. So I guess it's two parts. So one is like, how do you maintain these skills? So like the product changes over time. Obviously, there's a lot of the code base. So how do these skills get maintained? And then second to that is like, how do you know when your verification Is good enough? Like, you know, you can trust that the verification loops that you've built are going to, I Suess you trust that the outputs when they're done. Yeah, maybe I'tl talk about, think that's somewhat related.

**[0:16:49]** Maybe I'll start with this one first. So like, how do I maintain these skills? So if you're not familiar with this concept, an eval is essentially like a way well, I think the mental model I have is like, it's like a unit test for an agent. And you can actually make your own evals. You don't need like a special framework for them. You can build, you can, you can build one depending on like, you know, how scientific and how rigorous vou want to be.

**[0:17:19]** My screen Is red. Yeah, there's a little button. Sorry. Oh, do you mind like disabling the drawing or something? I can't see my screen. Yeah, sorry. If you guys could not draw on the screen, that'd be great. But there's a little button in the... Is thata troll? Yeah, the little drop down. How do I clear? Yeah. Okay. Yeah, you got it. Perfect. Good to hear. Yeah, so evals area way to unit test your skills basically. And actually in Pstack, we ship under potato

**[0:17:51]** mode, there's a playbook if you search for it called eval playbook. And it's like not... It's actually pretty rigorous the way it's done. But essentially what I do is I spawn a lot of different sub-agents. I have my main coordinator agent come up with a rubric for what I want the skill to do. these sub-agents and it creates individual directories for them which are cleverly named to

**[0:18:22]** not let the sub-agents know that it's being evaluated. Because agents can actually tell and when they do, they change their behavior. of stuff like that to essentially... Yeah, like test whether or not the skill I'm making or changing ts actually doing what I| think it does. And one of the really nice things about Cursor is that we support so many different models. So you can actually eval your skill across all sorts of different models and get

**[0:18:53]** a sense of how well it performs across that different matrix, especially for the models that you use. lot. Every time I modify a skill, I will run one of these, like the email playbook and make sure that it's actually leading to a result |! want. But I will say like maintaining skills is actually pretty hard. It requires, I think, a lot of taste and observation. So you kind of need to be very good at being a backseat driver. You

**[0:19:26]** if you've ever done pair programming, for example, and you watch a co-worker code and you just like... you could probably do this better. You know, vou could do... vou know, like why did you not do this, right? You ask a lot of questions to your co-worker. And it's kind of a similar thing here. You like... you don't want to just bea passive observer of the agent. You want to be very in the driver's seat in the initial stages when you're building up your own set of skills. You know, obviously you can use something like PSAC, but if you're building your own set of skills, it's very... I think, you know, opening up all the tool calls and like reading the code

**[0:19:58]** reading all the agent behavior and their thinking blocks is a really great way to see where they fail, right? Like what... you know, where are they being done? And then you can go and build a skill for that. And then with verification, how you trust It Is... It's... think it's alsoa very similar iteration loop, where, you know, like I actually did the same process for verifying the verification skill, where I actually get... So one thing that's interesting about evals is that you can sort of hill climb

**[0:20:28]** them, meaning that your eval can produce a score, right? A score that you can get your coordinator to produce, but also vou can have a judge agent of a different model to kind of cross-reference and make sure that the first model is not being biased, right? The model that's judging all of the sub-agents that are running the thing. But you can also like hill climb. So meaning that you can use like slash loop in cursor and you can say, okay, keep looping on this eval, right? Until

**[0:20:59]** everything is 10 out of 10, as an example. And I did the same... basically the same approach with the control skill. And so i kind of... it was very... it was very hands-off actually. So, you know, l... I that skill that way, like the CLI in that skill. And over time, it's gotten really good. But yeah, it was definitely not super smooth at the beginning. It required a lot of iteration. And I think there's an analogy here for me, which IS... Well, I make this analogy later in a different slide

**[0:21:31]** on my drawing here. But I think of it You know, as a... as a engineer now, you're sort of more like... Like maybe a manager or... The analogy I like is like you're like a chef ina restaurant. You're the head chef. You're not cooking all the food yourself anymore. You have a team of cooks, right? You have line cooks, you have a sous chef, you have all these different stations. really design the environment. You know, you're in charge of setting up the kitchen. You're

**[0:22:01]** in charge of, you know, like giving tasks to different people. Yeah, it's a very interesting way of working. But yeah, that's how I basically built these verification skills. Yeah. Just one fault there. I'm like... Mm-hmm. I'm like, I'm going to try to go one layer deeper. So are you... Let's say we wanted to build an eval ora skill for something and we wanted to kind of get better on its own, which is what I think you're suggesting. Are you doing that in like a

**[0:22:31]** work tree, kind of isolated with like the sub-agents and then the reviewer agent and all that? Is it happening like in some type of cloud-hosted environment? Like what's the practical steps? If I wanted to so do this and like set up a verification system for something, what would do or where would start? I think that the best place to start is local because you can observe. You can definitely observe what your agents are doing. So if you're building a verification skill for yourself, I would definitely start local and just

**[0:23:02]** have your agent bring up the application, whether it's like a CLI or a desktop app or whatever. And so you can actually observe, right? You can see how the agent is interacting with the application. You can see it, you know, how it calls like the different APIs that allow it to interact with the application. But for me personally, I have basically been kind of all in, mostly all in on cloud agents because they're extremely powerful.

**[0:23:33]** And the really powerful thing about cursor is the cloud agents actually, where if you spend a little bit of time setting up your environment, these control skills, these verification skills pay a huge amount of dividends because it's not just something that makes you as a single engineer better. It actually levels up your whole team and even your whole company, because you can actually start thinking about cloud agents. You can start thinking about automations that automatically do things like I'll get to. kind of talk about I

**[0:24:04]** this a bit later, but. I'll just kind of get Tt just kind of get [| into it where, you know, for example, like I talk a lot about this agent. we have called Benny, right? Who, you know, who takes all of the bug reports that we get and automatically goes off in the cloud, opens upa cloud. It's desktop. It runs cursor in its own computer and it uses the same control skills to interact with the application and try to reproduce the bug or the user report. Right. And this Is so, so powerful because at once

**[0:24:35]** Ican immediately, I set. so much information from this automatically. Like here in this example, you can see that. the Benny actually reproduced the bug, but it's already fixed on main. So it actually confirms that we fixed this. problem already. And allt need to do Is just release another build of of cursor. So that's like huge. information there that I didn't have to go off and sit with an agent, you I know, and spend an hour. trying to fit like, is this fixed? Is this not fixed? So you you vou . gain back so much time. But, you know, everybody on

**[0:25:05]** my team benefits from this. Everybody in the company benefits from this. So definitely think that, you know, keeping these using cloud agents Is super powerful. But, yeah, it’s like a journey. You have to © trust it first. Right. Before you you get to this point. And that's it goes back to what I was saying here where, you know, it's very hard. It's almost. impossible. And I would definitely encourage you not to try to jump from, you know, like if you're still in this zone, you don't want to jump to like I'm going to spawna hundred

**[0:25:35]** or thousands of cloud agents right now because you're just. going to waste a lot of tokens and it's soins to be extremely expensive. Yeah. So just to kind of recap so far, basically, if we wanted to go on the journey that you've kind of gone on, It would be to start with verification, building some some skills and some some ways of determining that the agents are producing at least like correct code. Whether like you said, whether it's good code or not is maybe a separate question. But like it's it's technically solving the problem by looking at, you know, stack traces, looking at, you know, the actual behavior in the

**[0:26:05]** app. And so on. And then once we trust it locally, then we can start to think about scaling into the cloud and running more agents that are picking up signals, I guess, on their own. Right. So whether that's like a bug report that comes in or something, they can go and pick it up and solve the problem and give us back a PR. And then maybe the last step is like auto merging the PRs, which is where you're at. Maybe not where everyone is at. Yeah. Yeah. Maybe not where you're

**[0:27:06]** at. You're at the same time. Maybe not where you're

**[0:28:15]** at. One of the most controversial topics in the industry, I think, is like, should you rewrite your app or not? Because I think engineers are very prone to this where, especially when you join a company, you come in and you see like the code base and you're like, oh man, this ts shit. Like who wrote this code? You know, it's terrible. I want to rewrite the whole thing. There is a very common inclination. I think a lot of, you know, before agents and I guess arguably even now, people will definitely discourage you from rewriting stuff. But I'm actually here to

**[0:28:45]** make a case for why you might want to consider it. Because I think it really depends. You know, brownfield applications, I think, are actually in a pretty good spot, especially if they're set up well already. And like recently I've been talking to some people, but, you know, I was just observing, I just noticed this parallel, which is that a lot of big tech company problems are now everybody's problems. And the big tech company problem, you know,

**[0:29:16]** like when I was working at Meta, like we had this giant monorepo. We had like, I don't know, tens of thousands of engineers just, you know, like banging on their keyboards and shipping code. And a lot of really great engineers at Meta. But I'll say like, you know, you'll be surprised that the code quality is actually not that good. And so I often joke that like, you know, before AI sloth, we had human sloth. And so, you know, I think a lot of big tech info, like what Meta has or

**[0:29:46]** Goosle, you know, really big tech companies are actually designed for that, where you're sort of like you're catering to the, you know, like, this sounds so bad to say, but like the least capable engineer on your team. Right. You build frameworks, you build conventions, you build guardrails, you know, you restrict credentials so that, you know, your intern doesn't wipe your production database. There's, you know, if you have that level of infra already, I think your agents can actually already doa very solid job. Right. Right.

**[0:30:18]** Because they have the guardrails are already in place for agents to not cause havoc or not cause too much havoc in your code base. And you can always add more, you know, guardrails. But think like Greenfield applications, especially are, you know, like the brand new applications are like the biggest risk in my opinion, and also the greatest opportunity. Because, you know, if you vibe code a project, a prototype, like we did for Grokbot, you know, Grokbot was spun up very, very, very quickly. And if you

**[0:30:49]** haven't heard of Grokbot, it's like our new application we just launched yesterday. It's really cool. Let's you orchestrate your, create like individual agents that have their own identity and you can kind of orchestrate them. It's super cool. Definitely check it out. But yeah, it was like a very, it was a very Greenfield application, like most prototypes are. So it was like vibe coded very quickly. Humans were not reading the code at all. And I had this tweet recently where I said something about organic architecture. Maybe

**[0:31:21]** rll find it. But the idea is that when you have a completely vibe coded application, you essentially have no guardrails whatsoever. So your agents, when you give thema task, they will just solve it in whatever method is the most convenient. And over time you get into this situation where you have a code base that is spiraling out of control. Because you don't understand it. Because you don't understand it. Your agents understand it, I guess, in

**[0:31:51]** a way. But like they've built something that Is, you know, optimized for short, for shortcuts. And you know, it will, you will suffer. You have a lot of issues with that application. So I think starting your code base with like very strong constraints is very much needed. Because like when you have a code base that you can trust, right? When you have guardrails that actually help you, help your agents write good code, you can get into

**[0:32:22]** the, you know, like into this part of the curve where I, where I, like said, you know, I woke up today and I had like 20 PRs merged by my agents. And that's because I invested a lot of time, over 600 PRs. calculated yesterday when I refactored all of GropBot to this new architecture that I've been building. And yeah, I've gotten to a point where don't really look, I really don't look at the that not just, you know,

**[0:32:53]** to sell you tokens, but because I, you know, it took a lot of work to get to that point. I spent a lot of tokens to get the code base to this point where Ino longer have to look at it. Uh, but I'm very excited because. You know, the potential where, you know, it's not just, this doesn't just benefit me. It benefits everyone contributing to GropBot. I And it also empowers, you know, designers and product managers and, you know, people, even GTM people to add features to GropBot. And I don't have to worry, you know, don't have to wake

**[0:33:23]** up at night in the middle of the night and worry about, oh shit, someone's Right. I have a ton of constraints and Cl. I was like, it's actually very annoying to write code in, in GropBot, but like agents absorb all of that annoyance. Um, but yeah, I'm happy to talk about what exactly : that is. Um, yeah, I think one question, um, before we get into the, this part here is just around that element of like what your, your, your Cl looks like, or maybe some of the constraints, and then also like the average PR size.

**[0:33:53]** Tsaw a question about that earlier, just to give of a glance. It doesn't have to be like mathematically average, but just, uh, you know, like what generally the size of the PRis, um, if it's onlya couple of lines of code or, you know, um, yeah. um, i think it depends me. I'm trying to do thisina way where I'm not gonna like, you, yeah, you don't have to share the actual number of you, like the actual average. Uh, I think this is fine. Benchmark. Benchmark. But like we have, so, okay, this is not that interesting,

**[0:34:23]** but, uh, well, fun fact is that virtualization in GrokBot and in, uh, cursor is actually powered by, uh, Pretext, uh, which is a sort of new library that someone's built. Um, that's really interesting. You should, you should check it out, but that's not really that important. Uh, I think the average PR size, actually don't know. I don't know if I want to click on these. Uh, probably can, but I would say like they can range anywhere from a few hundred lines or 50 lines to like a thousand, depending

**[0:34:55]** on what the thing is doing. Uh, so like here I'm not here like deleting a bunch of files. So expect that it's just, but veah, it, it kind of varies. There's no like, yeah. There's no like hard cap or hard limit. They're all like 50 line PRs. There's no hard cap. There's definitely no hard cap, but do encourage my agents to split up their work into multiple PRs. Uh, I do that mostly because, uh, like, I like the idea of the, I guess maybe this ts much harder to do now as in the world of agents and you have like so many

**[0:35:25]** commits, but I like the idea that, you know, the Git history Is a very rich source of context. Uh, and I like the, I like each PR to sort of atomically describe what that small piece of thing is doing, which also makes it easier for me to revert changes and like figure out, you know, oh, I shipped a bug and it's just, it's here. Right. It's not in this 40,000 line PR where who knows what landed in there. Uh, but |, don't have a hard cap on PR size. Cool. And then, um, yeah, also

**[0:35:56]** quick question on like Cl. So again, you don't have to go into like, uh, the screen share of like your Cl does, but just generally would you describe what the Cl kind of looks tike, uh, or how strict it is? Uh, yeah. So, uh, well specifically for Grokbot. So Dune is the, it's the sort of cheeky code, code I name for the architecture that we've built for Grokbot. Um, the Cl looks pretty annoying because there's checks for everything. So like literally I have, um, uh, well, if you've written any react, for

**[0:36:27]** example, you know, you know that one of the biggest foot guns in React is use effect. Uh, so in, uh, Dune and in Grokbot, we've banned use effect. So Dune Is just the, the mental model of what Dune is. Uh, you can kind of think of it as like next JS for, uh, electron apps and it's designed for agents to write. Uh, and it's like custom for, you know, our agent powered applications. Um, so the Cl checks are very like specific to that. Like, you know, don't use use effect. It's,

**[0:36:57]** it's, it's banned. Like Cl will fail, uh, and yell at you. We have like some of the more interesting ones that people might raise eyebrows Is like, I actually ban code comments as well. Uh, which is very interesting. Um, but I've noticed that 99% of the time agents just write code comments that kind of describe some historical thing that is actually totally irrelevant to the code. Um, like it will often say like, you know, oh, Lauren said you should never do this. And it's now in the, in a code comment. Like what? Like why? What? That was, I didn't say

**[0:37:28]** that as like a durable, you know, global rule. I PR sucks and you should change that part. Uh, agents don't really understand us that well, surprisingly. Uh, and, or they kind of assume too much and they kind of do things in like very stupid ways. So like, yeah, we just ban everything. Everything you can imagine like the agents are bad at, we ban. Uh, so one example that we actually suffer a lot in the agents window is we have, uh, you know, if you've used agents

**[0:37:59]** window, you've definitely seen performance I issues and you know, we're constantly trying to fix them. Uh, but it's like a, it's a never ending struggle because there's so many pull requests that get merged. Any one of them could just regress performance or stability or reliability. Uh, you know, the agents window doesn't have this architecture yet. I plan to do bring this learning back there and kind of refactor everything there. Uh, but, uh, it just regresses super often, uh, because, uh, there's just one example is like, we have very poor, um, isolation

**[0:38:30]** between processes. So like on, you know, on, on electron, you have a renderer thread that renders your UI, but you also have like a run other code that, you know, doesn't need to block the renderer. Um, but we do a poor job of separating those things. And so oftentimes you just accidentally have code that gets pulled into running on the renderer thread. And then all of a sudden you're competing with the, the renderer that, you know, that has a very, if you want like 60 FPS, you have to, every frame that gets drawn has to be done in 16 milliseconds.

**[0:39:02]** So very, very small, you know, deadline per frame. Uh, if you want, you know, a very smooth product. Uh, and when you start building, bringing in, accidentally bringing in, you know, things that are like very computationally heavy, or they have a lot of lO, uh, then you just get into like a lot your FPS really drops. You start, uh, you know, losing frames. You get long tasks that take more than 16 milliseconds. And then you just get this really choppy experience. So all of those patterns that we've learned basically building electron apps, we've encoded into

**[0:39:33]** this framework and it becomes like a hard failure. So literally, in, in GrokBot, we literally have a directory called electron main, electron renderer. And we have, uh, import, uh, Cl, I Suess, where we actually check the dependency graph to make sure you're not accidentally importing code from one directory to another. Uh, so that's enforced by Cl, um, as well as bug bots, uh, which is our, which cursor's, um, like code review tool that runs on Cl, uh, you know, in

**[0:40:04]** our agents MD, it's everywhere. Like, so J, I, |, um, I have this thing here where I talk about like, um, you know, like there are multiple layers, I think for building a good code base. Uh, obviously the code base is one where, uh, if you have an architectu re like this, where it's extremely strict, uh, you know, the, the, the way to build features is very conventional. That's like the strongest, strongest level of enforcement because agents just love to copy existing patterns. So, uh, one example of this in GrokBot is

**[0:40:35]** like, we have this, these concepts called like a feature and we have entry points and transcript cards. Like, oh, you know, the cards that you see in the chat. Like, these are all like, like nouns, I guess, In, in the framework. And so there's a very conventional way of creating them. And so like a feature is allin a, in a single directory as an example. And so all of the code that contributes to that feature lives in one directory. So it's all co-located in one place. Makes it super easy. You know, agents don't have to like, uh, grab around and try to figure out like where all

**[0:41:06]** the things are. It just looks at the feature and like, oh, okay, I'm working on the onboarding feature in GrokBot. Uh, I'm just going to work in this directory. And for 80% of the work, it's mostly just very encapsulated there. But, uh, like, it's like very, it's like design again for, you know, like the dumbest agent. Like you don't have to think, right? The, the, the, one of the key principles I have for this framework is like the shortest, the shortest path is the best path. So, uh, because that plays

**[0:41:36]** exactly to how agents love. to write goals. Like they like to take shortcuts really, you know, they'tl find the quickest way to solve the. problem. So why not make I that the best way to solve the problem? Uh, so_ get into all the specific. details. Um, and, uh, the, the, this framework's really more of a collection of ideas and principles rather than something that will open source. Uh, you can, you can, you know, screenshot this, I guess, if you want and, uh, tell your agent to, uh, do some, build, build something like this for you too.

**[0:42:08]** um, yeah, but it's really. all about the layers. Uh, you know, like the, the code base is one part with features, uh, and directories and, you know, import, uh, blocking import dependencies, uh, that shouldn't be imported. Uh, but, and, and it all enforces that and static analysis. So like, uh, uh, there's Cl checks. We have a lot of lints for bad patterns that we observe, uh, compiler diagnostics. Uh, there's also rules and bug bot, which are, um, I think like three, four, five are more soft,

**[0:42:39]** right? These two actually make, make Cl read, right? So that, you know, there's a hard constraint where the agent can just write crappy code. For rules and skills and bug bot, your agents can still forget, right? You can still, or it may not always consistently apply them. So but I don't, I don't like to rely on them as the only source of enforcement because it's very, very soft, right? And if you, if you only have rules

**[0:43:09]** and bug bot and skills and a style suide for your code, you will, it's only a matter of time : before your code base looks like complete trash. I'm sorry to say that, but, uh, I definitely recommend, yeah, like, you know, investing in, you know, things that can be hard and forced, right? And this is why, you know, maybe, uh, the choice of tech stack that you use is also very important. Um, like, I think for example, Rust is sort of making, vou know, it's like getting super popular again, uh, because the compiler is so strict, right? The compiler enforces

**[0:43:41]** n so many different things. You know, there's a borrow checker that you have to appease. And if, as long as you make sure your agents don't write unsafe code blocks, uh, you can more or less feel somewhat confident that if the code compiles, it's probably works and it's good. Uh, but you'll see, it gives you that level of r trust and confidence that you as a human engineer no longer need to go and check it yourself. You know, you, you rely on code and static analysis to actually make that, uh, a lot smoother.

**[0:44:12]** Um, and I guess the worst part, the worst place to be in is if you are stuck in code review land where you actually the invariance in your code base by literally the human person saying, you know, reading the code and like, okay, you should not do this. Right. Every time you have to that as a code smell, like a, uh, anti pattern. And you should say, okay, instead of me commenting on the PR, how do I . turn this into a hard rule? Right. How do I turn this into a lint rule? How do I turn

**[0:44:42]** this into a Cl failure? Or how do I even categorically eliminate this problem, uh, entirely? about another migration I've done, but rt probably pause here. Yeah. I feel like that's, that's where I am. Um, to be honest is, is what you're describing right now, which ts that like, I don't have all of these rules. Uh, so I have some things to go do after this session, uh, in terms of being able to scale my agents. I'm, I'm definitely on like the, uh, you know, maybe a couple like two to three locally. And I'm sure most people here are on the same.

**[0:45:13]** So, uh, yeah, I know we only have a couple minutes left. Uh, Lauren, was there anything else that you wanted to, to highlight? I obviously there's lots of questions so I can grab more, but I want to give you a few minutes. Uh, if there's anything else you want to talk about. Weil, think I've been yapping for quite a lot. So I'm maybe let's just do questions. Okay, cool. Uh, one question that had a couple of, uh, came up a couple of times was just around like token usage. So the question is like, Is, Is what you're describing a realistic thing for people who are on, you know, uh, a normal set of token usage. They don't have, you know, basically unlimited tokens, uh, to

**[0:45:44]** work with. think that's a really good point. I mean, like, obviously, you know, I work at an AI lab where we have unlimited tokens. So, uh, I definitely cannot say that, vou know, this is something everyone should do in the exact same way that I did it. I think this point without, you know, breaking the bank. you know, you're, you're, you have a startup that you lead. Um, I think to me it's a question of ROI. Um, and it's like, uh, yes, you spenda

**[0:46:16]** lot of money on tokens in the upfront stage. You base is going to take a lot of tokens. Uh, adding all these things, uh, is going to take a bunch of tokens. But if we're heading to a world where agents are writing all the code and, you know, you want to be very lean, right? You don't want to have to hire. You don't want to become like meta, right? Like, mean, like in terms of, you don't want to become a 10,000 person engineering org, because, I mean, that's a cool problem to have. But also, you know, you have so much overhead. There's

**[0:46:47]** like planning, you know, like it's, it's, uh, personally, I wouldn't, uh, it's not super fun. But, um, I think you want to stay very nimble, right? And you want to, you want to be like agents are all about allowing you to do things that you couldn't do before. That's really to me, like the value of agents. You tokens on every single little thing. But, um, to me, like the thing I couldn't do before is like enforce this level of constraints in a code base by myself. Right? Like I'm justa

**[0:47:17]** single person. You know, uh, it would have taken me uh, and do all the refactoring and test everything myself and verify, you know, like run. Imagine if there, it was just me, right? No, in, in pre-agent era, just like running, you know, it would take me so long. Right? And my salary Is you know, the, the question might have is just then, you know, like what is, there's a trade-off of, do you hire someone to do

**[0:47:47]** this? Or do you spend the tokens to set up a code base so that even the, the most naive, do a good job? And when you actually get to this point, like even agents that are not, you know, fable size do an excellent job of writing code. And this pays a lot of dividends as well for me personally, where I've empowered not just myself, but again, like PMs, designers, engineers who to just contribute ina way that is sustainable.

**[0:48:19]** definitely like a trade-off for sure. You know, like nothing is like free for sure. And tokens are pretty expensive. But, oh, actually, I don't know how many of you have seen this, but we So, yeah, Grok 4.6 would be like a great, it was very, very smart. It's really good on the, on the benchmarks. And it's the same, the tokens, well, I hopefully I'm believe the cost per token is the same as

**[0:48:53]** more intelligence for the same cost. think this is an area that cursor tries to, cursor and SpaceX AI try that pareto frontier of, you know, cost versus intelligence. You know, we don't necessarily want to build the biggest model ever because that is extremely expensive to run. It's really about, like, how do you find that sweet spot, right? You don't needa giant model, but it's just super smart, right? And it's not very expensive for inference. But, yeah, I think to

**[0:49:23]** kind of round it up, think it's like a, it's, it's, there's a, if you do your own analysis, feel like it's pretty positive. It'll be pretty positive that the ROI you get from investing in stuff like this but your whole team to be so much more productive. Right, like imagine if you have an army of engineers like me who are shipping so much improvements and bug fixes, you know, every day, right? Like that Is pretty exciting.

**[0:49:53]** Cool. One last question before we wrap up. This one is for the people in product on the, on the call. So let's say we do have an army of engineers who are shipping like Lauren. I'm just curious, like, how ts the product team or other functions of your company keeping up given that, like, if you're shipping so quickly, have, are they using AI more to do their you can speak to that, know, obviously, you don't have, like, you're not in that role, but just curious about how that works. GroffBot has been actually exceedingly powerful. Where, so before GroffBot, like,

**[0:50:24]** you know, obviously cursor only had cursor, like we only had agents window. We had a CLI, we had an IDE, and these are really like power user tools, right? They're designed for developers. So it's very, very developer centric. You can do knowledge work in them, but like the Ul is not really optimized for that. So we actually didn't really have, well, I think like a lot of people in like, you know, GTM product, like they might have used cursor. So they're not really, like, they're not really, really, really excited for that. So

**[0:50:55]** they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. You can have you can kind of do orchestration in a very, like, natural way where you can sort of, you know, each agent is like a person. And now you've got

**[0:51:25]** a team of agents like working on. You have one one agent per account that you manage, as an example. Or if you're a PM, you have, you know, you can have an agent that summarizes all the work that Lauren did last night. And then now you know what did. Right. So I think our PMs are leveraging that a lot and they're shipping code too. So, you know, oftentimes they will just say, oh, here's a bug. fixed it. Can you look at it? And then I'll go review it. And actually it's just perfect. I'm like, okay, stamp. So I think that shows that, you know, the Dune architecture is holding up. Right. The all

**[0:51:55]** 7 the really strict constraints allow people who are not experts in engineering to contribute at a high level. So |! feel like I'm already seeing that pay off a lot : where, you know, designers and PMs are just able to ship features directly. And that just makes the GrokBot team super fast. Right. Where we can ship so quickly. And we have a lot planned. So I'm very excited to, you know, to ship more

## 段 B：Matt Pocock 直播访谈（0:52:26–1:54:20；Whisper small.en，字幕 OCR 失败）

[0:52:20] We have a lot planned, so I'm very excited to ship more stuff.
[0:52:26] Potato, welcome. Thank you so much for joining.
[0:52:29] Thanks for having me. Very excited to be here. Big fan of yours.
[0:52:33] And a huge fan of yours. I think people have been talking about this like it's like the meeting of
[0:52:38] the skill minds. The skill Mount Olympus or something. Because both of us have very popular skill libraries.
[0:52:44] As I was saying before we started, I've not used a ton of yours. And like I want to get
[0:52:49] all of the juice, out of your brain, so that I can go and use it better. I think where I want
[0:52:55] to start with this is you gave a talk pretty recently, like about 10 days ago and post it on
[0:53:01] X, which went absolutely nuts as about how I shipped 2500 P hours last month to production,
[0:53:07] got about 3 million views or something on X. And I watched it and I loved it and I recommended it.
[0:53:13] And I kind of want to run this as almost like a Q&A of that talk, basically of giving you
[0:53:18] I just had tons of questions about it and I wanted to dive into it.
[0:53:23] And I think where I want to start is you talk about a trust ladder with agents where you
[0:53:29] as you trust agents more, you
[0:53:30] you can get them to do better and better things and or scale up to use more and more agents.
[0:53:38] So what is your story of how you climbed the trust ladder and how did that work when
[0:53:43] like you got SpaceX and started climbing more and more?
[0:53:47] So I think the journey sort of began even before I joined Cursor, which is now SpaceX AI.
[0:53:55] So the story is after meta, so I used to work at meta on the React team, I took a month off
[0:54:03] because I was feeling kind of burnt out.
[0:54:06] And of course, what do you do when you're burnt out?
[0:54:08] You go and start a new project.
[0:54:11] And so I started a side project, you know, I was, of course, using AI to write code.
[0:54:16] But then I started to realize, spending so many hours just
[0:54:20] micromanaging one agent.
[0:54:46] Of course, I was a bit nerd sniped by that.
[0:54:49] And as I was building my toy project,
[0:54:53] I got nerd sniped by, oh, how do I make my AI coding
[0:54:55] setup more efficient?
[0:54:57] And so I kind of started the journey there
[0:55:00] where I just took a step back and realized
[0:55:04] I was spending all this time micro-managing a single agent.
[0:55:08] I was creating skills, and I was finding it quite difficult
[0:55:11] to measure the output or the results, the impact
[0:55:15] of the skill as well.
[0:55:16] So I was kind of flying blind,
[0:55:18] but I was iterating really fast.
[0:55:23] So that project eventually sort of became the basis
[0:55:27] of P-stack, even though at the time.
[0:55:30] And a lot of some tricks I had learned
[0:55:33] like building that early set of skills.
[0:55:35] Actually, it's still open source if you wanna,
[0:55:37] if anybody wants to take a look,
[0:55:38] it's on my GitHub, like potato slash noodle, N-O-O-D-L-E.
[0:55:45] And in there you will see some skills and a brain directory.
[0:55:48] And so I was really interested in this idea of,
[0:55:50] how do I extract my own ability, if that makes sense,
[0:55:55] and agent, right, because I realized that,
[0:55:59] all I was trying to do was trying to teach the agent
[0:56:01] to write code more like me,
[0:56:03] do workflows more like me.
[0:56:06] So, you know, like an entry point to doing that.
[0:56:10] And then, after I joined cursor,
[0:56:14] I was starting to work on the agents window
[0:56:16] and it had a lot of performance issues.
[0:56:20] It was pretty laggy.
[0:56:21] And so since I had experience working on React,
[0:56:24] I was asked like,
[0:56:25] hey, do you wanna come and help out with the agents window?
[0:56:28] And so the beginning of the cursor journey was very manual.
[0:56:36] I was deep in like looking at like flame grass
[0:56:39] and he, heaps snapshots and trying to see like,
[0:56:41] why exactly is the app so slow?
[0:56:44] But then coming back to the same realization that I was sort of the bottleneck. I was doing
[0:56:49] everything manually. I was sort of the meet proxy in a way. I was the meet proxy between my agent
[0:56:54] and Chrome DevTools. And I was like really in it. And what month of the year is that,
[0:56:59] let's say? Where are we in the timeline? So I joined cursor in March. So this is like early,
[0:57:05] early April, probably early April is when, you know, I joined and I didn't have any skills.
[0:57:11] I sort of abandoned my personal skills because I didn
[0:57:20] working on Grokbot, I sort of realized that a lot of the lessons I had learned from those
[0:57:26] skills, time building the initial set of skills, were very relevant, especially around things like
[0:57:31] verification, you know, being very rigorous in your work. Because I think agents from my experience,
[0:57:40] even the frontier ones, tend to tend to take shortcuts. They tend to do the easy thing.
[0:57:50] So a lot of the skills that
[0:58:20] What do you think about that, just as a sort of vibe check before we start talking?
[0:58:25] I actually feel like domain expertise is more important than ever.
[0:58:30] I think I wrote this on my ex at some point, but at times I sometimes think of AI the models get smarter and smarter and more of the front-tier models are getting so good.
[0:58:45] Like I love Opus 5.5, by the way.
[0:58:49] As the models get really, really, really good,
[0:58:52] it almost becomes like the bottleneck is no longer
[0:58:54] the agent.
[0:58:56] It becomes your ability to express your intent
[0:58:59] and your goals in a clear way that the agent can
[0:59:05] carry out.
[0:59:06] And that's why I think people with a lot of domain expertise
[0:59:09] are extremely have a huge advantage, in my opinion,
[0:59:13] you're a little bit like techno curious.
[0:59:18] So I think of people like a doctor or a lawyer
[0:59:22] or someone who has a deep expertise
[0:59:25] in a particular non-engineering domain,
[0:59:28] and if they're actually just a little bit tech savvy
[0:59:30] and they can figure out how to use agents,
[0:59:32] they can actually build really, really great products.
[0:59:36] If they have a clear enough vision in their head
[0:59:39] and they can articulate it in a way
[0:59:40] that the agent can build it,
[0:59:43] think that that is really the bottleneck these days is like the transfer of your intent, right,
[0:59:51] and your vision to the agent. Yeah, I've been obsessed with language basically since
[1:00:05] what might
[1:00:35] and
[1:01:05] all of the useless tests that they write.
[1:01:08] And so that was one thing where, you know,
[1:01:35] and
[1:01:37] how they came to be and.
[1:01:39] It's so interesting that now with agents it's like this meeting of
[1:01:43] natural language with programming language but
[1:01:45] but it
[1:01:50] it's all language.
[1:01:51] It's all communication.
[1:01:55] I a long time.
[1:02:20] to people who don't understand how this works.
[1:02:22] So where I wanna get to is sort of from people
[1:02:24] who are doing kind of like one to five agents today
[1:02:27] up to, you know, hundreds of agents running once
[1:02:30] and how that sort of functions.
[1:02:32] And so I'd love to hear about your metaphor
[1:02:34] of the Michelin kitchen
[1:02:36] instead of the software factory.
[1:02:37] So I think that says a bit about
[1:02:39] the way you think about this stuff.
[1:02:40] Yes.
[1:02:42] Yeah, I've never really liked the term software factory,
[1:02:46] not because, you know, it's not accurate,
[1:02:48] But I think a lot of people, when they think factory,
[1:02:52] they don't necessarily create that with quality or craft.
[1:02:57] Things which are very important to me and a lot of people
[1:03:00] and technologists who work building products,
[1:03:03] we care about the user experience.
[1:03:05] We care about the things we're building.
[1:03:08] So while I do think software factory is an apt term,
[1:03:12] it also, I guess, maybe conjures up negative,
[1:03:15] maybe sometimes negative connotations.
[1:03:17] So Michelin kitchen is the thing that I've sort of landed on where it's much more,
[1:03:22] I feel like it's much more aspirational and I like the metaphor a lot cause you
[1:03:26] know, I like food. I'm called potato of course, and I like cooking.
[1:03:30] And I see a lot of parallels, right? Like with food, right?
[1:03:34] When you're cooking a meal for yourself, for example, it's both utilitarian.
[1:03:38] Like you're trying to just feed yourself, right? And, and survive.
[1:03:42] But it can actually be transformed into art, right?
[1:03:45] And that's what a Michelin-starred chef, or even just a chef or a cook, food, is take
[1:03:51] something very ordinary and turn it into a delicious meal that takes you back to your
[1:03:56] childhood days or something like that.
[1:04:00] And so it almost mirrors that trust letter that I talk about, where you can sort of
[1:04:05] imagine your own journey as a home cook, right?
[1:04:08] As a home cook, you are doing all of the food, the cooking yourself.
[1:04:12] You cut all the vegetables, you do all the prep work,
[1:04:15] you do all the cleanup.
[1:04:17] You are the one man or a one woman show, really.
[1:04:23] And it's an interesting thought experiment.
[1:04:26] If you were to cook a meal, and then you add people,
[1:04:30] your partner, your brother, your sister.
[1:04:33] And now I have your whole family in the kitchen.
[1:04:35] I think most people would get very stressed by that.
[1:04:38] The thought of, oh, so many people are just
[1:04:39] mucking around in my kitchen.
[1:04:41] If no idea where all the utensils are, they're making a decision.
[1:04:43] I have a max capacity of one person.
[1:04:45] Yeah, absolutely
[1:04:46] So I feel, like that that's really out because when you ask yourself that question of how do I go from being a solo cook, right?
[1:04:53] To having an army or even not even an army but a few sous chefs right there helping me in the kitchen.
[1:05:00] How do I think about dividing the work in a way that makes sense?
[1:05:05] I'm not dividing work just for the sake of it.
[1:05:07] But in a way, that actually makes the sum the better
[1:05:11] than the total of its parts.
[1:05:14] And so the Michelin kitchen metaphor to me
[1:05:17] works really well in that regard.
[1:05:19] Because as a chef, if you're in a position
[1:05:24] where you're not necessarily cooking all the food yourself
[1:05:27] anymore, but you are thinking, you're
[1:05:30] almost like the tech lead for the kitchen, where
[1:05:34] chefs have to think about not just cooking,
[1:05:36] but they have to basically organize the whole kitchen.
[1:05:38] And they're like the CEO of the kitchen.
[1:05:40] They have to think about when do you order ingredients, how
[1:05:43] do you store them, how do you prepare them,
[1:05:45] when do they have to be prepared.
[1:05:47] It's a whole job that's not just cooking.
[1:05:51] And I think that, again, it mirrors so much of how
[1:05:54] engineers write code today, where you are not
[1:05:57] writing the code yourself anymore.
[1:05:58] You have agents.
[1:05:59] But you, as a human, are still responsible for the final
[1:06:03] outcome.
[1:06:04] your name still is associated
[1:06:06] with the work that you do, your reputation.
[1:06:08] And so how you set up your kitchen
[1:06:12] and how you set up your skills, your environment,
[1:06:15] your code base, I think are ultimately
[1:06:18] the new ingredients that go into building product.
[1:06:23] Yeah, I think what I love about your approach
[1:06:26] is the amount of focus that you put into the environment
[1:06:28] that the agent operates in.
[1:06:30] Because I think a lot of people, they think the agent is good.
[1:06:34] I'm probably not going to be able to make it better.
[1:06:36] Let's just trust what these magic model people have
[1:06:39] put in the harness and the model combination.
[1:06:42] There's nothing I can really do, like I
[1:06:44] can't mess about with Cloud Codes internals or something
[1:06:46] or whatever you're using.
[1:06:49] But what I love about your approach,
[1:06:51] and it's something I advocate for too,
[1:06:53] is that you can change the environment
[1:06:55] the agent operates in.
[1:06:56] You can make changes in the code base
[1:06:59] and also give it tools for verification as well
[1:07:02] and allow it to verify its own work. So the thing I loved about watching that talk is
[1:07:07] the amount of photo and verification and like that is the lever that you can start to generate
[1:07:13] trust. Can you talk about that and what that concretely looks like? Let's start like looking
[1:07:17] at practical people can improve their own process.
[1:07:20] systems, their implications.
[1:07:22] Yeah, I've said this a lot, actually,
[1:07:24] that even if you don't use PSAC or your skills,
[1:07:29] I think that the single most important skill that
[1:07:32] should be in your toolkit is verification.
[1:07:36] Because without verification, and for those watching
[1:07:40] don't know what that means, it's this idea
[1:07:42] that you can give your agent hands and eyes in a way.
[1:07:47] That's the analogy I like, where the agent is able to run the code
[1:07:53] and actually interact with it like a normal human user would,
[1:07:58] and also do things like debug it, take traces and snapshots.
[1:08:04] And funnily enough, that was actually the first skill
[1:08:07] I built when I joined Cursor.
[1:08:09] That was the thing that actually started
[1:08:12] to let me ascend the trust ladder a little bit in a way
[1:08:14] that some of the other skills I had looked at
[1:08:17] or belts had not really let me through.
[1:08:20] Because no matter how good some of the other skills
[1:08:23] were, like the how skill, the why skill, the unslob skill
[1:08:27] were, I was still relying on me as the proxy
[1:08:31] between my agent and the output so that if the agent can actually
[1:08:35] see the result of its work, there's no way
[1:08:38] it can actually iterate.
[1:08:39] And so this is where people start to talk about loops,
[1:08:42] this idea of a loop.
[1:08:43] And really, I think the term loop seems almost abstract.
[1:08:49] People are like, what is a loop?
[1:08:51] What is an agent loop?
[1:08:52] But really, to me, the most important part
[1:08:54] of a loop that allows it to be a loop
[1:08:57] is the verification part, because the agent is
[1:09:00] able to verify its own work. a And that takes you out
[1:09:05] of the equation, where now I can actually do something
[1:09:08] like, so one of the very first use cases I had for verification
[1:09:12] was the performance work that I was doing on Cursors agent
[1:09:15] window.
[1:09:16] And I wanted to get to where I could do something called
[1:09:18] hill climbing, which is a term that I think the labs talk
[1:09:23] about a lot, which is this idea that you have some kind
[1:09:26] of rubric or a way to judge or score something.
[1:09:30] And now, because you have a loop,
[1:09:32] you can have an agent continually
[1:09:33] try to make improvements to that.
[1:09:36] I think Andre Carpathy also famously released something
[1:09:41] called auto-research that has a lot of these ideas.
[1:09:45] But yeah, verification, I would say,
[1:09:46] is probably the most important skill in PSAC
[1:09:50] and many other tool sets.
[1:09:54] And I think, think it's the most important thing to focus on.
[1:09:58] So a lot of the, I spent a lot of time actually,
[1:10:01] tuning the verification, the creative verification skill,
[1:10:06] And also internally, we have so many verification skills now.
[1:10:11] Every app that Cursor has or SpaceX AI has
[1:10:14] has a verification skill that is auto-maintained as well.
[1:10:19] And it's become critical infrastructure for our team
[1:10:21] because everybody uses it.
[1:10:24] And you went pretty far with that too, right?
[1:10:25] You had a, in your talk, I saw that you actually
[1:10:28] built a custom CLI for that too.
[1:10:30] So what does that CLI do?
[1:10:31] How does it execute things?
[1:10:32] And why did you,
[1:10:33] I mean, that's proof of how deep you're going,
[1:10:36] of how much you pushing that?
[1:10:38] Yeah, so this is actually a tip I learned early on,
[1:10:42] where, I guess back in January,
[1:10:47] or late last year, the thing that people were very
[1:10:50] concerned about was context window, right?
[1:10:52] That was the big topic at the time was.
[1:10:55] How do I manage the context window?
[1:10:57] Because compaction summarization
[1:10:59] wasn't really that good yet.
[1:11:01] And people were always people have this.
[1:11:03] There was almost this meme in the community
[1:11:05] that once your agent summarized or compacted once,
[1:11:10] it would become sort of stupid for the rest of your session.
[1:11:14] So there was a lot of thinking around being very efficient
[1:11:18] with your context usage.
[1:11:20] And so that was actually the inspiration
[1:11:22] for some of the CLI work inside of the verification skills.
[1:11:28] I guess now it's less so about context
[1:11:31] because agents are much better or harnesses
[1:11:35] gotten a lot of summarization. I still have a clean context window. So the CLI is more
[1:12:05] and skills and sort of like, is like a gradient.
[1:12:09] You have some parts of the work that are entirely judgment-based, right?
[1:12:14] You know, it's something that requires thought, you know, putting together multiple pieces of context, thinking.
[1:12:20] And then you have the more deterministic parts.
[1:12:21] Like, I don't know, if you wanted
[1:12:23] to refactor some code from one pattern to another,
[1:12:28] that's very mechanical.
[1:12:29] You don't need an agent to think about it
[1:12:32] and come up with it in a novel way each time.
[1:12:36] And so that was really the inspiration for the CLI.
[1:12:39] And you'll see this in a lot of the other skills that I built,
[1:12:41] is like I try to extract out the deterministic parts
[1:12:45] and turn that into code, and just leave only the parts that
[1:12:48] actually require judgment through the agent.
[1:12:51] So in a way, I think of the skill as kind of like a wrapper.
[1:12:54] It's a wrapper with some light instructions
[1:12:56] around how to use these custom tools that
[1:12:58] are inside of the skill.
[1:13:01] Yeah, I don't think the skill is really that interesting
[1:13:03] in its own, really.
[1:13:04] It's not like a novel piece of software.
[1:13:07] It's just something that interacts with Playwright,
[1:13:09] and the Chrome DevTools protocol,
[1:13:11] and calls a bunch of APIs.
[1:13:13] It's just a bunch of glue.
[1:13:14] is fascinating because it's a way of hiding information from the skill, right? It's a way
[1:13:18] of conserving the skill, keeping the skill quite small, I imagine, and then you're
[1:13:22] able to get more of the complicated deterministic stuff into a script within the skill. So it's
[1:13:27] almost you're compressing information and making the agent do more consistent things more
[1:13:34] consistently. Yeah, that's fascinating. Yeah, it also helps, I guess, if you care about context
[1:13:39] window, it does help because now the agent doesn't need to reinvent things. Because one
[1:13:47] thing I had noticed early on when we didn't have a CLI was that while the agent would try to verify
[1:13:55] it's work, it would basically rebuild the world each time and then every agent did it differently.
[1:13:59] And I was starting to notice that's very inefficient. I was wasting. It wasn't actually not just about
[1:14:04] context usage, but also speed. Because now I had to actually go off and write the scripts
[1:14:08] or the CLI and test it and it doesn't work.
[1:14:12] And the last agent did it and it worked, but it discarded it.
[1:14:15] So it was just very obvious at that point,
[1:14:17] like I should just turn this into a CLI
[1:14:19] and put that inside of the skill
[1:14:21] so that every agent that uses it now,
[1:14:24] benefits from that same piece.
[1:14:27] But I also think it's a good push for people to think about
[1:14:31] is how much of your skills and rules
[1:14:34] could actually be deterministic?
[1:14:37] That's another core thing, or one of my core principles
[1:14:41] that I like to think about is how
[1:14:43] do I make very efficient use of determinism and non-determinism
[1:14:49] and let agents shine at the non-deterministic parts,
[1:14:54] because that's what they're trained to do.
[1:14:57] And the other parts, which are much more mechanical
[1:15:00] or straightforward, can be just pure determinism.
[1:15:04] And you see this as well for things like doing migrations,
[1:15:08] which is another big thing that I've talked about is, you know,
[1:15:13] going from one technology to another, especially one that is better for agents.
[1:15:19] And a lot of how you can do that migration is I think through things like scripts and CLI is like the deterministic parts like code mods, you know like crawling the AST, the abstract syntax tree and transforming code literally mechanically like a script does it for you instead of that agent.
[1:15:34] Totally makes sense. I mean, I think what there's another thing there, which is you're taking
[1:15:43] stuff away from the agent, and you're kind of putting it in the environment to a little
[1:15:48] bit, which is, let's say you have a thing that you notice the agent always gets wrong,
[1:15:53] you want to make that impossible within the environment. And that sort of comes down to
[1:15:59] code quality as well. I mean, I's talk about a lot like having a what a good code base means, right?
[1:16:06] what is a good code base. And there's a definition I like which is a good code base is a R code base
[1:16:11] that's easy to make changes in, right? Easy to change stuff without things screwing up. And that
[1:16:18] means that you have a lot of guardrails that you have a lot of the agent or the human is constrained
[1:16:23] to very narrow paths. And that's, again, something you talk about in your talk. And you
[1:16:28] talk about this not only on the kind of automated checks side of things, so linting and time
[1:16:33] checking, but also in the way you design abstractions and you guys even, even I think, built a
[1:16:39] framework for your agent to work into. I think what I'd love to hear is you obviously think of
[1:16:45] that as very important, right? And that's how important is that compared to other things you
[1:16:50] could be doing, like building features or shipping work?
[1:16:52] Yeah, I think that's, I almost feel like the new job of the engineer is really to spend
[1:16:59] time on the environment. I must actually wrote a tweet about this yesterday, but I didn't.
[1:17:05] But I think that, I think that, you know, if you haven't really spent time, you know,
[1:17:12] building trust in your agents and building skills and tools, you can get stuck in this
[1:17:16] mode where you're very low on that truss ladder, right? You don
[1:17:20] have a lot of trust in your agent's work.
[1:17:22] And so the only way to cope when you're in that situation
[1:17:26] is just to kind of lock in and micromanage your agents.
[1:17:29] And that's very time consuming.
[1:17:31] And when you're stuck in that mode,
[1:17:32] you don't really have the luxury
[1:17:34] to think about higher level things,
[1:17:39] like making yourself more productive, in the same way
[1:17:43] that I guess analogy would be like if you've never
[1:17:47] taking the time to learn your tools as a developer
[1:17:50] when you're writing code yourself.
[1:17:52] And you've never heard of VS Code,
[1:17:54] you've never heard of VIM, you only knew about Notepad,
[1:17:58] and you hadn't even heard about Git.
[1:18:00] That's sort of the analogy.
[1:18:01] It's like you haven't spent the time
[1:18:03] sharpening your own knives, right?
[1:18:05] And so of course, if you have a dull knife,
[1:18:08] then everything can take a long time.
[1:18:13] And especially if the deadlines are looming the you don't
[1:18:16] have the now you're stuck in this rut, right? Where you don't have sharp knives, you don't
[1:18:22] , but you're under all this pressure to ship, right? And so all you can do is just
[1:18:27] focus on that. But I do think that, you know, if you can find yourself the time to actually
[1:18:33] spend time thinking about your setup, it's again, going back to the cooking analogy.
[1:18:39] It's like, you know, if you, for example, if cutting the garlic is like super slow,
[1:18:45] There are garlic and matchaurs, right?
[1:18:47] You can buy it and you put it in the thing
[1:18:49] and you squeeze it out, right?
[1:18:50] It's super fast.
[1:18:52] MACHINES and tools were invented for a reason, right?
[1:18:55] And so if you were operating a Michelin kitchen kitchen
[1:18:58] and your cooks had no tools,
[1:19:01] then of course everything's gonna be extremely inefficient.
[1:19:04] Very, very, every cook is gonna make something
[1:19:07] up of their own.
[1:19:08] So I think the tools and the determinism to me
[1:19:11] are taking that part away.
[1:19:14] And just like you said about constraints as well,
[1:19:17] the constraints are to me as well.
[1:19:21] Actually, a slight tangent on that
[1:19:22] is I think we should talk about TypeScript.
[1:19:26] Because we actually both share a background in TypeScript
[1:19:29] where you obviously have done a lot of work with TypeScript
[1:19:31] and total TypeScript, and you're a leader in that space.
[1:19:35] And I had adopted R-TypeScript pretty early,
[1:19:38] and I had given a talk or two at TypeScript Conf
[1:19:41] many years ago.
[1:19:43] And so one of the talk that I did actually
[1:19:45] was about type systems and constraining types.
[1:19:50] One of my most favorite things about type strips
[1:19:52] is actually type narrowing, this idea
[1:19:54] that you this idea that you go from a very broad type,
[1:19:57] that could be anything.
[1:19:58] And then you, through type guards and type narrowing
[1:20:03] and runtime checks, you can actually narrow the space
[1:20:06] and say, oh, this isn't just a string.
[1:20:08] This is a very special type of string.
[1:20:10] It's a constant.
[1:20:11] Like I determined that through the type system.
[1:20:14] And in a way, it's like, there's a lot of parallels,
[1:20:17] I think, to that with constraints in your code base,
[1:20:21] where is it you're constraining the space, right?
[1:20:25] If you think about category theory as well,
[1:20:27] you're constraining the number of possible types, right?
[1:20:31] That can exist.
[1:20:34] And you're saying there's only one type, right?
[1:20:36] And for us, like that framework that I'm building
[1:20:39] called Dune.
[1:20:41] It's not an open-sourcing work.
[1:20:43] The way I describe it to people, it's
[1:20:45] kind of like our internal Next.js for our Electron apps.
[1:20:50] But it comes with a lot of really, really restrictive
[1:20:53] lit rules.
[1:20:54] And the code base is designed in a way
[1:20:56] that there's really only one way to.
[1:20:58] So we make use of a lot of conventional patterns.
[1:21:03] So features all go into a specific directory.
[1:21:07] Well, every feature has its own directory as an example.
[1:21:10] There's a thing that discovers features through a registry
[1:21:14] and crawling the code base and stuff like that.
[1:21:17] But this conventional pattern and the lint rules
[1:21:22] make for an environment where it's actually
[1:21:24] very hard to write bad code.
[1:21:27] And that sort of frees out the, it both frees up
[1:21:31] your own mental capacity as well as the agent
[1:21:37] sort of doesn't have to think about that anymore.
[1:21:39] Or it's just like, oh, there's only,
[1:21:41] I should just, if I want to add a new feature,
[1:21:43] it just goes into the new feature directory
[1:21:45] and all the code goes in there
[1:21:46] and I'm not gonna append to a God file, right?
[1:21:50] That was really actually the inspiration
[1:21:51] for those feature directories
[1:21:52] is the very first couple of versions of Grokbot
[1:21:56] or composed of like eight God files,
[1:22:00] which for like at least 10,000 lines long, if not longer.
[1:22:04] And so I kind of had to break it up into smaller pieces.
[1:22:07] But I was just observing, you know that's another important part is observing how agents fail.
[1:22:13] And then every time you see a mistake, every time you see something that could be done better, you think, you step back and think...
[1:22:20] How do I turn this into a literal?
[1:22:21] How do I make it so that the code base makes this impossible?
[1:22:26] And it comes back to me for my background.
[1:22:28] learning TypeScript and types systems
[1:22:32] is how do I constrain the space so that I know precisely
[1:22:37] what I'm working with.
[1:22:38] And I think, yeah, there's a lot of parallels there.
[1:22:40] Totally makes sense.
[1:22:41] And I mean, it's funny that you mentioned TypeScript
[1:22:44] and code files in the same sentence.
[1:22:46] Because TypeScript famously has a 25,000 line type file.
[1:22:49] Yeah, I realized that I already is bad.
[1:22:52] Well, I don't know if they've rewritten that and go.
[1:22:53] They probably have, haven't they?
[1:22:56] OK, so the environment is important.
[1:22:59] You should watch your agent like a hawk
[1:23:01] to make sure that any mistakes it makes,
[1:23:03] you turn
[1:23:05] them
[1:23:06] into things in the environment.
[1:23:07] And the benefit of the environment is you're not
[1:23:08] overloading your agent, right, in terms of rules,
[1:23:10] in terms of things it has to remember.
[1:23:12] It's just in the environment.
[1:23:13] And so it stumbles into the rules and, you know,
[1:23:17] bounces off them and hits them at the right moment.
[1:23:19] So, okay, we, we know about the 2,500 PRs,
[1:23:23] where do those come from?
[1:23:24] Like, how do you, you've built your trust ladder,
[1:23:26] you've worked on your environment and you understand,
[1:23:29] okay, I now want to scale up.
[1:23:32] What are the mechanics of that scaling?
[1:23:35] Are you initiating 2,500 like chats per month?
[1:23:40] That can't be right.
[1:23:41] So there must be, are there any kind of automated triggers
[1:23:44] that trigger
[1:24:14] So in a way, I think of this as I've spent the time building one kitchen and one restaurant.
[1:24:21] And now I'm in a position where I?
[1:24:24] Actually have to be there anymore because the environment, you know, the same analogy,
[1:24:29] right?
[1:24:30] It works really well.
[1:24:31] You know, exactly.
[1:24:32] Yeah, exactly.
[1:24:33] Yeah, exactly.
[1:24:34] It's like you're Gordon Ramsey and you know, you've taught your executive chef like
[1:24:40] all the tricks of coming up with a great menu, and the kitchen is set up really well, everything
[1:24:45] is just perfect. And you're now in a position where you can open your second, your third
[1:24:49] restaurant. I guess I sort of see each project that I work on, each big chat, is sort of like
[1:24:57] a restaurant. And I have multiple of them operating at the same time. And I'm sort of like helicoptering
[1:25:04] R between prospective people, sometimes some more than others, depending on how in the
[1:25:08] loop I am. But yeah, definitely I think there are external triggers and context that those
[1:25:16] projects don't have that for a long time I was the proxy for that. So the best example I have
[1:25:24] is you have a project that's working on a feature or you're trying to fix a bug and you're getting
[1:25:30] bug reports but the bug reports are going to things like Slack or linear or X, right? And these
[1:25:37] are external systems that aren't connected to your inner loop.
[1:25:41] So I like to talk about this outer loop and the inner loop.
[1:25:45] I don't know if I'm using I'm using the definition correctly,
[1:25:47] but, but to me, my inner loop is like basically my engineers,
[1:25:51] my agent to engineers working on the code,
[1:25:55] building towards an intent or snapshot of my intent.
[1:26:00] And the thing about that is that the snapshot can go stale.
[1:26:03] New information comes to light that I then
[1:26:06] have to be the proxy of and transfer that context to my agent.
[1:26:10] So if you don't have these triggers pulling information
[1:26:14] back into the interlude, then you have
[1:26:17] to play that role where you're off in Slack
[1:26:21] or X or whatever, and you're gathering context, right?
[1:26:25] You're getting context about bug reports,
[1:26:27] about feature requests, about something,
[1:26:30] someone said about our back in infrastructure
[1:26:32] has some limitation, all that information.
[1:26:36] You have to ferry that across to your agent.
[1:26:39] So that's where I think like tools like Grokbot
[1:26:41] are really good because you automate
[1:26:44] the outer loop as well.
[1:26:46] And when you connect those two loops,
[1:26:48] it's very, very powerful because now all of a sudden,
[1:26:51] your agents have the ability ability to get context for themselves.
[1:26:55] If, for example, either through, just as a simple example,
[1:27:01] like maybe you have the Slack MCP, or you have your own harness
[1:27:06] that you've built a Slack subscription into for a particular Slack channel.
[1:27:11] Now, all of a sudden, you can tell your agents, okay, subscribe to the Slack channel.
[1:27:15] every time there's a bug report about something...
[1:27:20] and then go off and challenge that thing, right.
[1:27:22] Go reproduce the issue, right.
[1:27:24] Using the verification skills
[1:27:25] that we've already spent time building
[1:27:28] and all of those other skills that we've set up
[1:27:30] so that I have a lot of trust, right.
[1:27:32] I have a lot of trust that these agents
[1:27:33] can actually go off and understand the bug, you know,
[1:27:37] verify that the bug actually still exists on main
[1:27:41] and it wasn't something about, you know,
[1:27:44] maybe the user's setup or their data or maybe, I don't know,
[1:27:48] they didn't install a dependency or something
[1:27:49] like that, like basically I think creating that,
[1:27:56] yeah, creating those two loops and connecting them
[1:27:58] is really a very important part of the job these days,
[1:28:01] especially if you are thinking about how to scale yourself.
[1:28:05] So a big theme here is really just like,
[1:28:07] always thinking about like,
[1:28:09] what, where am I the bottleneck in this process?
[1:28:12] Why do my agents need me, you know,
[1:28:14] to answer this question?
[1:28:15] I always like to think about that.
[1:28:17] And so I try to think about how do I actually
[1:28:19] get the agent to answer its own question,
[1:28:22] but not by hallucinating, not by guessing,
[1:28:24] but actually real data.
[1:28:26] And a lot of people talk about this idea of a company
[1:28:29] brain or a context graph.
[1:28:31] I feel like those terms aren't necessarily complex
[1:28:36] or even abstract.
[1:28:37] To me, it's just about how do I take information
[1:28:41] that my agent means that I would otherwise
[1:28:44] have to go and pass it myself and just teach it
[1:28:47] to do it. And that removes me from the equation. And so how I arrive at 2000 or however many PRs
[1:28:55] is the fact that I have all these loops set up. And so it allows me to open chain restaurants.
[1:29:04] I can really parallelize myself. So yeah, I'm not sitting there creating 2500 chats, of course.
[1:29:09] It's really like these projects are actually cursor has a new feature called projects,
[1:29:15] which are these like coordinator agents.
[1:29:19] And so the coordinator agents are really good at sort of delegating and not doing work of their own,
[1:29:24] but they manage and supervise like almost a list of tasks and re-sponsor agents to go and do them.
[1:29:30] And so I'm just constantly feeding context or teaching the, the agents how to get their own
[1:29:34] contacts and then they. They're going off and doing the work for me.
[1:29:38] And really the big the last thing I
[1:31:09] agents, but they're a connector to things like, and they are a great
[1:31:39] which funnily enough
[1:31:41] I know, has so much.
[1:31:44] carry over to the agent's world of, you.
[1:31:48] You of course can drive to an outcome you want by, control
[1:32:20] constantly watching and I have I'll tell them things like you know a watch for issues with bugs in
[1:32:27] the grokrbot desktop as an example and whenever you find that send it to my cursor so one of
[1:32:34] the really cool things about grokrbot is it connects to cursor so cursor has like I just
[1:32:40] mentioned this new feature called projects and a project is really a again like a that you get
[1:32:46] You get a coordinator agent that's in the cloud.
[1:32:48] It has its own computer.
[1:32:50] And all it really does is it's a manager of agents.
[1:32:52] It's like your executive chef, your chief of staff.
[1:32:56] It doesn't do the work itself.
[1:32:57] It delegates and orchestrates and manages
[1:33:01] the work of other sub-agents that report
[1:33:05] to your chief of staff.
[1:33:09] And it basically is responsible for driving the work forward
[1:33:13] and managing things and passing context to them.
[1:33:17] So if you get a sudden burst of issues,
[1:33:19] let's say you get 30 issues at once in one payload
[1:33:21] or something, or very quickly, the coordinator agent
[1:33:23] can figure it out and delegate.
[1:33:25] Yeah, exactly.
[1:33:25] It gets like 30 or so payloads and spawns a sub-agent
[1:33:29] or a single coordinator agent.
[1:33:31] It can actually do a bunch of different topologies of agents.
[1:33:38] And it will sort of figure out the best way
[1:33:40] your team of agents.
[1:33:45] So I use cursor projects a lot.
[1:33:48] And I also use Grotbot a lot.
[1:33:50] And cursor projects are my inner loop,
[1:33:52] and Grotbot is my outer loop.
[1:33:54] Grotbot takes all the context, external context,
[1:33:58] gives it to the projects, because it can actually just
[1:34:00] send messages to those projects.
[1:34:02] You don't even have to open cursor.
[1:34:04] You can just tell your Grotbot, OK, create a project
[1:34:06] for these series of tasks.
[1:34:09] They're all related.
[1:34:10] Maybe, as an example, you've had a big burst of issues
[1:34:16] that are all about performance.
[1:34:17] your app is slow, and they're all connected.
[1:34:21] Maybe some of them even have a a similar fix.
[1:34:25] And you can certainly go off and just
[1:34:26] on one agent per task, but then you've
[1:34:29] lost that thread between them.
[1:34:32] And you may duplicate work, or you may not really
[1:34:34] think about the higher-level problem.
[1:34:36] Sometimes when you solve bugs, it
[1:34:39] helps to have multiple bug reports that
[1:34:41] are slightly different, because it helps you really zoom out
[1:34:44] and see, actually, the problem, when
[1:34:46] I thought the bug was here, but actually when I see the other multitude of bugs, it R is
[1:34:51] actually up here.
[1:34:52] Yeah, got you.
[1:34:54] That's why you have so many agents in that loop then, right?
[1:34:57] Because it's not just you have a bug report comes in, you spawn a single agent to look
[1:35:01] at that bug report.
[1:35:03] That single agent will be duplicating work with other agents, right?
[1:35:07] Because if there are multiple bug reports coming in through the same thing, that can
[1:35:10] be duplicated work.
[1:35:11] Yeah, exactly.
[1:35:12] Fascinating.
[1:35:13] That's really fascinating.
[1:35:14] Okay. R is just this end-to-end.
[1:35:16] endless series of triggers coming from real users reporting real reports, builds up this
[1:35:23] sort of and accelerates the factory sort of adds more orders in other than bug reports.
[1:35:27] Are there any other sources that you use for like accelerating for pushing these PRs?
[1:35:33] Well, finally enough, it's some of it comes from reading the code too. So I guess I have
[1:35:41] sort
[1:35:43] To clarify, the 2500 PRS, they're not obviously like 2500 features.
[1:35:49] A lot of the work actually is spent on gardening,
[1:35:54] another term that I really love.
[1:36:00] So I guess this is more important when you have a big team of engineers,
[1:36:03] human engineers that you work with.
[1:36:07] And this goes back a little bit to what I was talking about with the environment.
[1:36:09] setting up a really good environment that doesn't just help you and your agents, but everybody on
[1:36:13] your team, right? Think of a new hire who doesn't
[1:36:20] And if you have a really good environment, they can be productive, from day one, right?
[1:36:24] They don't have to like, you know, open a bunch of low R's,
[1:36:29] They can start, you know, they can start just training out really good code.
[1:36:32] code. And, yeah, I think I sort of lost my train of thought.
[1:36:39] I've got a follow-up, which is what are the mechanics of triggering? When do you
[1:36:46] have an agent to go and look at the code? Some people might say let's just do that every
[1:36:52] hour or something or on a cron job or what's...
[1:36:56] Oh, yeah. I saw some of your recent tweets as well about some of the tweets you've been
[1:37:02] are great for San Andreas routines.
[1:37:06] I have some routines like that as well.
[1:37:09] So one of them is looking through just another simple example
[1:37:17] is React has a lot of f-ing.
[1:37:20] foot guns. So as I'm sure you're aware, and so I have an agent that's just constantly
[1:37:25] looking for patterns. And the interesting thing about that one is I don't actually tell
[1:37:30] it to fix the issue first, I tell it to append it to a document. And then every couple of
[1:37:36] days I look at it and I see actually these are all the same thing, you know, and so
[1:37:40] that gives me, you know, you almost want like a buffer, a bfer, a queue, sometimes that's
[1:37:44] actually more effective than just spawning off a couple of like a lot of sub-agents
[1:37:48] to fix every single thing.
[1:37:50] Because when you are in kind of pure execution mode
[1:37:53] and just trying to execute on the orders that
[1:37:58] are coming in very fast, you sometimes miss the big picture.
[1:38:01] So sometimes having a buffer forces
[1:38:03] you to think about the big picture
[1:38:05] because you have these artifacts and things
[1:38:08] that you can look at as a human and sort of use
[1:38:12] your own human judgment to, or I
[1:38:14] guess you can use an agent to do that as well,
[1:38:17] But you give the agent and yourself a way to identify patterns that you might otherwise miss if you're just only solving each bug at a time.
[1:38:27] And that's also really the benefit of having something like a chief of staff agent is it can see the forest in addition to actually.
[1:38:36] Actually doing the execution.
[1:38:39] Fascinating.
[1:38:40] I mean, my brain is exploding a bit there with the sort of chief of staff as the software factory.
[1:38:45] I. Might have to change some of the course that I'm filming next week.
[1:38:47] That's all right.
[1:38:50] Let's talk about let's talk about review, right?
[1:38:51] Because this is the reply that you get.
[1:38:53] Yes. Is did you read?
[1:38:55] Did you taste all 2500 of those dishes as they swept past you?
[1:39:00] And I assume the answer is a variety is a version of no.
[1:39:07] Yeah, I think you don't want to be in a position where you're in a food ever.
[1:39:11] again. But you also scale, you cannot be tasting every single dish that comes out of your kitchen,
[1:39:17] especially if you have multiple restaurants. So it becomes more about sampling and thinking about
[1:39:23] the processes. In the same way that if, I guess maybe this is where the factory analogy is a bit
[1:39:30] more apt, is as a quality supervisor on a factory, you can't look at every single item. You sample,
[1:39:37] you go, you go in there every day and you look at the quality of the pull requests,
[1:39:43] you look at the agents are writing, and you scrutinize it very rigorously and you think
[1:39:50] about all the inefficiencies, the bad patterns that the agents are doing.
[1:39:54] And then you think about how to course correct the environment, right?
[1:39:58] Not that single agent.
[1:40:00] Because if maybe if it was a one-off incident, it's fine, you know, that maybe there's nothing
[1:40:06] to fix there.
[1:40:08] But if you actually notice that multiple Asians are
[1:40:11] having the same issue, they're taking the same shortcut,
[1:40:14] they're propagating the same work around everywhere,
[1:40:18] that's a sign that you should
[1:40:28] type systems and adjusting it so that problem doesn't happen
[1:40:34] again.
[1:40:35] And when you do that enough times,
[1:40:36] then you get to a place where the code
[1:40:38] base's environment is so constrained.
[1:40:41] And so it guides you so well that you can just step away.
[1:40:47] That's the dream.
[1:40:48] And I'll definitely say it's very hard to get to this point.
[1:40:53] I don't want to sell this as something
[1:40:55] that you can just do easily by using PSAC.
[1:40:58] It takes a lot of time and effort
[1:41:00] to think about your code and where
[1:41:02] you see your agents failing.
[1:41:04] and thinking very thoughtfully, intentionally, and setting up guardrails and constraints
[1:41:10] so that they do the right thing by default.
[1:41:14] And you're not like, if to go back to the software factory analogy, this isn't a dark
[1:41:19] factory, right?
[1:41:20] This, the lights are on.
[1:41:21] It kind of is actually.
[1:41:23] Is it?
[1:41:24] Yeah, well, it's dark in the sense that so it's dark in the sense that, well, a thing of
[1:41:28] agents are merging their own pull requests, it's sort of become dark where I go to sleep
[1:41:34] by my agents and now work 24 seven. I have, I have the equivalent of like more than 10
[1:41:40] chiefs of staff, right? Each working on a different area. Like for example, I have one
[1:41:45] that's working on performance of the Grokbot desktop app. I have one that's working on
[1:41:50] fixing bugs that users report. I have one that's exploring, rewriting it in a different
[1:41:55] language just for fun.
[1:41:57] You know, like, what if, you know, just re-imagining what it would be if it was like a native app,
[1:42:01] it's just
[1:42:13] a toy.
[1:42:14] full autopilot is something that you do in PSAC.
[1:42:18] And that will trigger off.
[1:42:20] tense, rigorous verification loop where it will spawn a bunch of
[1:42:24] verifier agents for every pull request and fuzzing, meaning that it will
[1:42:29] actually run the application, it's going to click around and try to use it like a
[1:42:33] real... look for regressions, look for bugs in your implementation, and it will
[1:42:39] try to find issues with the thing and then it will fix it itself, it'll do
[1:42:43] that again and eventually get the PR to a state where it can land. So it
[1:42:49] It is quite token intensive.
[1:42:52] You can this, of course.
[1:42:54] So instead of 10 verifier agents,
[1:42:57] you might do one, or just tell the agent to verify it's
[1:43:01] unworked.
[1:43:02] But yeah, the key thing is the verification part
[1:43:05] is really the key piece.
[1:43:06] That gives me a lot of confidence.
[1:43:09] I guess verification plus the environment.
[1:43:11] The combination of these two things
[1:43:13] that allow me to step away and say,
[1:43:15] agents, go up and merge your thing.
[1:43:16] I'll review it in the morning by looking at my commit
[1:43:19] history. And if I see problems, I go in course correct. Right. And I'll go in revert or modify
[1:43:26] add new lint rules and whatever. So it does it does take time to get to that point. But
[1:43:32] once you get it, oh, it's so it feels so magical. I tell people like I'm sleeping so much better
[1:43:38] now. Because, you know, it took it the very first day I turned on this sort of dark factory
[1:43:49] And it took a lot of bravery, I think, to do that.
[1:43:55] But somehow I did it.
[1:43:56] And now I'm in a place where my agents are merging their own code.
[1:44:01] Well, I think it's dark in that sense.
[1:44:04] Yes, it's dark sometimes, right?
[1:44:06] You do sometimes.
[1:44:06] That's true.
[1:44:07] That's true.
[1:44:07] Because I think of a dark factory is like almost like if you take the original definition of Carpathi's vibe coding, right?
[1:44:14] Which is the code almost doesn't exist.
[1:44:16] You forget the code might be a thing.
[1:44:17] I think your approach is totally different from that, which is that code and the environment is
[1:44:23] Essential and if the code and on the environment are bad, then you will get bad outputs garbage in garbage out
[1:44:28] I see why yeah, I think this is a this is a different thing. It's like
[1:44:33] You know
[1:44:35] The I don't know I don't know switch or something, right?
[1:44:37] I can get some parts of that through dark some parts where this is why that maybe the the kitchen is a better analogy
[1:44:43] the restaurant because you know you have a
[1:44:47] As a restaurant, you still might go to your restaurants every now and then to take a
[1:44:53] peek in, taste the food, right?
[1:44:55] Yeah, I think the idea of sampling instead of blocking, I think is really important.
[1:45:00] I think what would you say to people who are in, I guess you're obviously in a pretty security
[1:45:05] conscious environment where you're working very security conscious.
[1:45:10] Maybe there are folks working in like medical applications or law or finance or something.
[1:45:17] I think that some PRs are kind of like two-way doors,
[1:45:20] which is you can merge it and then revert it, right?
[1:45:23] It's cheap to go back through.
[1:45:24] But there are some PRs that are one-way doors, right,
[1:45:26] that will cause data loss of some kind.
[1:45:28] That will do something that can't be easily walked back.
[1:45:33] How do you deal with situations where most of your PRs,
[1:45:36] let's say, are one-way doors?
[1:45:38] Like, is this something you just wouldn't recommend?
[1:45:40] Or like, what do you think?
[1:45:42] Yeah, I think that's a really good question.
[1:45:43] think that it all comes back to me
[1:45:46] to the quality of the verification
[1:45:48] that you're able to get out of your agents.
[1:45:54] And I think for domains where the work is verifiable,
[1:45:58] this is easier, right?
[1:46:00] And the one-way doors become two-way doors in a sense.
[1:46:05] But I guess, I don't know, if you're
[1:46:06] working on something that is extremely,
[1:46:09] is very hard to verify programmatically,
[1:46:12] then I think, yeah, you're definitely in a position
[1:46:14] where it's very hard to get to that point.
[1:46:18] So I do think like, yeah, verifiability of the domain
[1:46:20] is an important aspect to be able to do this.
[1:46:24] And software engineering is just one of those things
[1:46:26] where it's quite verifiable in a lot of cases,
[1:46:30] maybe not, you know, like other domains, like mathematics,
[1:46:34] I think are another example of, not all of it, of course,
[1:46:37] but some of mathematics can be verifiable.
[1:46:42] for example. So, yeah, I think it's a great question that I don't really have the answer
[1:46:49] to and I think that this is something the industry and us as engineers will have to figure out
[1:46:54] is my sort of hope and prediction for the future is that we'll see more and more interesting
[1:47:01] new agent-oriented programming languages. And one of the most fascinating ones that I've
[1:47:07] seen so far
[1:47:20] used to be a time where you actually had to write your proofs in a different language.
[1:47:25] And proofs, by the way, for those who aren't familiar, is this idea that you can formally
[1:47:31] verify that some code is correct mathematically, especially if you've written your code in
[1:47:38] a very functional programming way. But for the longest time, you had to do that in
[1:47:44] separate language like Lean or TLA Plus or I'm blanking on some of the other other examples, but
[1:47:51] languages like that where you would construct the mathematical proof and then use a solver
[1:47:56] essentially to check that you've covered all the cases, you don't have like a race condition or
[1:48:02] whatever. So yeah, I think trying to sum up the question, I think if you are in a position,
[1:48:10] you can actually have the PRs merge
[1:48:17] merge. Because if it compiles, if the proofs show you that it's correct, then why wouldn't you just merge it?
[1:48:25] But of course, yeah, not all the means are verifiable.
[1:48:30] means are verifiable. Yeah, it's a tough one. Okay, I think we've got to think
[1:48:38] about wrapping up nearly on the hour. Have you got something after this?
[1:48:41] I mean, I've got some, I get my son dinner, but I can go a bit longer up to you. Okay,
[1:48:46] let's go. I think I just want to have one more question, which is
[1:48:51] is I think I want to ask how you see PStack
[1:48:58] and how you see skills in general,
[1:49:01] like in terms of,
[1:49:03] we talked about this before we went on air,
[1:49:04] which is like, people think of it as like my skills
[1:49:07] versus your skills.
[1:49:08] And how do you combine frameworks together?
[1:49:12] How do you use PStack with my stuff?
[1:49:14] Like what should you take from each one?
[1:49:17] And, because I think I see skills as sort of
[1:49:20] just derived from process, basically.
[1:49:23] They're just processes turned into words.
[1:49:26] And I would love to know how you recommend people
[1:49:30] take PStack and take my stuff as well
[1:49:32] and turn it into their own processes.
[1:49:36] I think you shared a tip actually
[1:49:38] to tell you that I thought it was actually very relevant,
[1:49:40] which is this idea that you go off
[1:49:42] and look at your previous transcripts, right?
[1:49:44] And you sort of mine for information of your own,
[1:49:48] look through your own prompts, right, to the agents where you correct them,
[1:49:53] where you have to constantly intervene, and, you know, take that higher level learning and turn that into a reusable skill, right, so that agents stop repeating that mistake.
[1:50:04] I think that PSAC and your skills are very complementary. I totally agree with you that they're like a skill is really much just process.
[1:50:13] I mean, it's just at the end of the day, skill is just English or language. It's just
[1:50:17] Markdown. And I think you can definitely weave them, combine them in a way that makes sense
[1:50:24] to you. bBut I do think that everyone should have their own set of knives. I keep going
[1:50:33] back to the cooking, the cooking analogy, but it's so apt because, you know, every chef,
[1:50:38] when they go to a different job, right? When they go to a different restaurant, they carry,
[1:50:41] bring their knives with them. The tools go with them. And so trust to me, it's really about trust
[1:50:45] in your own tools. And when you spend the time sharpening them and understanding them really,
[1:50:50] really well, you can do great things. And everybody's skills and toolset is going to look
[1:50:55] different. Someone might find a lot of success combining, you know, like your grill with docs
[1:51:02] or weight finder skill with some of the execution skills in PStack as an example.
[1:51:06] Some people might use more of your skills. Some people might use more of my skills.
[1:51:10] I think at the end of the day, it really just comes back to how much do you trust, you know, me and Matt, right?
[1:51:16] Like, trust us both, of course, use our skills, but I also encourage you to, you know, look at your trips.
[1:51:22] Tell the agent to look through, you know, some of the, all of the patterns that you've used, the times you've had to intervene, you know, suggest turning them into lit rules or new skills, right?
[1:51:36] the, the past chance I often say is like a treasure trove of context because that, you know, it's,
[1:51:43] it's like the process materialized, right? Like it's the real process, not an abstract idea in your
[1:51:50] head. It's the actual thing, right? And you can actually happen in practice and extract so much
[1:51:55] information from that. And there's so much show that I actually turn, I have a skill in PeaceNet
[1:51:59] called Recall, which is exactly that. Where this was a pattern where, you know, I was working in
[1:52:06] I was working on a similar problem.
[1:52:08] So I was working on virtualization
[1:52:10] for the cursor application.
[1:52:12] And there were a lot of bugs.
[1:52:13] And so every time I started a new chat,
[1:52:15] I was like, oh, there's so much good context
[1:52:17] from the last one, though.
[1:52:18] And I want to bring you over to the new chat.
[1:52:20] chat. How do I do that? And that's where the transcript, you know, looking at the past transcript came about.
[1:52:25] And then recall was just a way for me to collapse and compress that workflow into a skill so that I didn't have to just say I
[1:52:50] exact script commands you should use.
[1:52:53] I think with the latest models, you can just delete those parts and just really focus
[1:52:58] on the workflow.
[1:53:00] The skill becomes more like a series of steps, a series of your process.
[1:53:07] I think over time, we'll see that skills get smaller and smaller, more compact.
[1:53:12] They're very compatible.
[1:53:17] If you want, why not read our skills and combine them of your own, right?
[1:53:22] Combine Wayfinder with Potato Mode and make your own custom mode, right?
[1:53:27] Like skills are, the thing I love about skills are that they're so malleable.
[1:53:32] You can do anything you want, it's just language.
[1:53:34] Absolutely.
[1:53:35] There's nothing magical in them, right?
[1:53:36] They're just words.
[1:53:37] Yes, exactly.
[1:53:38] If there is any magic in them, it's just, the words chosen and the phrases and the
[1:53:44] the thinking that's been done to turn those like take abstract process and turn them into
[1:54:14] Fire too.
[1:54:15] Well, thanks so much.
[1:54:16] I'm going to close the stream here.
[1:54:18] Lauren and I will chat a little bit and stay here.
[1:54:20] But thank you guys so much for watching.
[1:54:22] I'm glorious.
[1:54:23] Hello everyone.
[1:54:24] I'm Lauren, Lauren Tan.
[1:54:25] I guess not many people know my last name.
[1:54:28] I am Potato.

## 段 C：Colin Matthews workshop 完整版（1:54:20–2:51:07；字幕 OCR）

**[1:54:01]** : fami vaalh: vsaalhs antnuad . nm oe ® 1 « a a uf oo I oe ee L. om ae mo. 0 8. . a2 . oe ® 1 « a oo ug , oe I , ee ee I ee ee oe 22m : *. _ °* *, a lag a «, - e - as a i i, a Sn [| i] *,. ue a I . . ! ft awaunm aheanlitatis arem aaah we'llcheckininuh- e a om. Of - : yeah yeah yeah monday let's 2 -= = oe. - - lat's da it nart tun ae en ne Se Sa neem on a8 a I i'm going to close the _ = a i #° @uaa a Ci - ac. own a Le a - a os - hit and etaw hava hist I a a - a tHhanhl wan “fmanse eM much for watching Hello everyone, I'm Lauren Tan. I suess not many people know my last name. __ am potato on Twitter, potato with spelled with an

**[1:54:33]** E. And I have been Cursor for about five months. Previously, I was at Meta where I worked on the React team, specifically working on the React compiler, which was a whole lot of fun. I'm still on the core team and contributing to open source here and there. So that's really nice that they still let me do that. : And before Meta, I was I at Netflix, where I was both a tech lead and transitioned to be an

**[1:55:05]** engineering manager for about two years. So I've hada lot of experience going between EG >. Oe a eel engineering management and being an individual contributor. And I think something I've noticed actually, which Is quite interesting, Is that there are so many parallels with, you know, management skills and how to like manage agents. And that's actually a big part about what I wanted to chat with you and everybody else about today. But yeah, that's, that's me. do have some like

**[1:55:37]** very light slides, but It's not going to be just rambling. So let me just share my screen and hana that I dan't leak anything. don't know. I need to allow permissions. No worries. Take your time. There's always tech, tech, tech, tech trouble. Give me one second to rejoin. Yeah, go for it. see many of you already know Lauren from the

**[1:56:07]** looks of the chat here. So yeah, it's exciting to get a chance to chat with her and go through some of her recent work. As you guys heard, you know, a lot of recent experience from Netflix to Meta and then now over at We're going to chata little bit about GrokBot as well. So that'll be exciting. don't know if you suys saw that was a recent release. I think literally maybe yesterday or the day before from the Cursor team, which I ° e* r woes . Pa] is kind of like. let's call it like agents for everyone. You can go check °. » Of - and learn a little bit QAnhU LOA aA LILLEC WIL and learn a little bit more about the product. But

**[1:56:38]** yeah, we'll explore that a little bit today as well. Alrighty. Welcome back. And Lauren, you're just on mute there if you want to hop off of mute or you're chatting. Yeah, sorry. No worries. It's 2026 and still don't know how to use Zoom. That's all good. Okay. So l assume you can see my screen.

**[1:57:08]** Yes. Yeah, we're good. So yeah, today, yeah, I think the big theme for me as I've been using agents to write code, and I'm sure a lot of you have had the same experience as well, is how do you trust it? Especially if you are an engineer that's been writing code for a very long time, you have a lot of opinions and lessons that you've learned about doing good engineering. And when you see agents just winging it and guessing, hallucinating,

**[1:57:39]** confidently stating that they found the smoking gun for the hundredth time, but it's actually not the real problem. You lose a lot of trust. And when you lose, when you don't have much trust in your can't get the most out of them. And for me, the parallel is like with management. So if I'm an engineer manager of a team and I have a bunch of, you know, I have a team of engineers on my team and I don't trust them, then the mode of operation I'm going

**[1:58:10]** to be in is going to be like micromanagement, right? I'll have to spend a lot of time looking over my reports' shoulders and checking that they're doing their work well, you know, that they're not shipping bugs to production. And so I drew this chart because, uh, it's not, it's not a very scientific chart, but like, this is how I imagine myself and my Journey through using agents. So, you know, like fast forward or back forward, uh, or fast back, uh, fast

**[1:58:42]** backwards, like a year or so when, you know, nobody was, or not many people were using agents to code. Uh, I think you, uh, you get into this mode where you are in very heavily in the loop with one or several, like a handful of agents and you find yourself just constantly figure, uh, you know, trying to understand what your agents are doing. Uh, and you're very, very in the loop. You're watching every single output you are sitting there prompting. Um, and you really can't parallelize

**[1:59:13]** beyond that because you don't, again, you don't have that trust, right? You can't go to a hundred agents, uh, like spawn a hundred agents when you don't even trust the output of one agent. So over the past five months, I feel like I've really been able to, uh, like ascend this trust curve. And now I'm at the point where, uh, I actually have, this sounds kind of scary to say this and it makes me sound like a slop artist, but I promise I'm not, but I actually have my agents now,

**[1:59:43]** um, auto-merging PRs for me, uh, which is like a wild thing to say. But, um, like I woke up today and there were like 20 PRs landed and I just reviewed them on main, like they were already landed and they were good. Uh, so how did get to that point? It's basically what I wanted to talk about today. Uh, and again, like, yeah, feel free to jump in if you have questions, Colin. Um, but, uh, oh yeah, of course I gotta show this, this chart, uh, where,

**[2:00:15]** uh, no, do not trust to re someone requested to control my computer. Uh, probably won't do that. Uh, but yeah, so this chart, I think I, I I'm sharing this chart, not to kind of like flex, but to kind of show like the journey, like, so you can see like the curve, like it's sort of like inversely matches the contributions I've been able to land at cursor. So I joined five months ago and five months ago, like I, you know, my first month I was like not very productive

**[2:00:46]** because I was, you know, was learning the code base. I didn't know what the heck was going on. And as I got more confident in my agents, uh, I've really been able to kind of ramp up my productivity Uh, and again, like, yeah, like last month I shipped a thousand PRs, which ts ridiculous. Uh, and then this month we're only on the 12th. I'm already at like almost 800 PRs landed. Uh, so the velocity is definitely high and you, you, I, I'm sure a lot

**[2:01:16]** of you will definitely be questioning like how, how much of this code is actually good. Um, and I think, yeah, like that's definitely fair to question. Um, but, uh, yeah, I think, I think if you set up your agents well, you can definitely get to a very similar level. Um, and so I'm going to talk about how we do that. Uh, so for me, I think I'm curious, like, I well, but, uh, for me,

**[2:01:47]** I think the most important skill that you should have in your toolbox when you work with agents is verification. Uh, and by verification, I mean the ability for an agent to actually run the code, uh, or take CPU traces or heap snapshots or, uh, you know, open an 10S simulator, whatever, you know, however your application is exposed to your users, it can do the same thing and, uh, run it for

**[2:02:18]** real and actually test and verify it don't work because that's the thing that really closes the loop. Uh, it doesn't guarantee your agent writes good code, uh, but it allows them to at least write correct code, uh, which is a big, a really big step forward for being able to trust your agent. Um, I will, I can share one example that we have, uh, within cursor. Uh, oops, where, let me open this.

**[2:02:54]** Let me just make this, uh, make me full screen. There you go. Uh, so for the, for cursors agent window, uh, so this is actually an interesting story, but, uh, when I joined cursor five months ago, uh, they're actually, uh, well, was supposed to join a different team. I was supposed to join, like, the cloud agents team. Uh, but then since |havea lot of experience working on react and agents window Is

**[2:03:24]** a react application, uh, I was, uh, I was asked to basically help out with, uh, the agent window work. Uh, but, um, there wasn't really a lot of, like, skills to help me. So I just found myself, like, okay, uh, agents, which is going to launch in like a week, right? We have a really tight deadline. And, um, there was, uh, you know, I was just sitting there like, okay, I'm going to open up the performance, the, the Chrome dev tools and just like take a trace, look

**[2:03:54]** at it myself and try to make sense of this flame graph. And keep in mind, I was just like in my first week. So had no idea what was looking at. No idea where, you know, I mean, I had some idea, but you know, the, the code base was completely fresh to me. Uh, and I realized like my agent had no idea either. You know, like I would take a screenshot of the trail, download trace, I would send it to it and it'd be like, yeah, it kind of looks like this, you know, uh, and it would like confidently state like it's this thing. And then I try to fix that. And turns out that's not the actual thing. So this was a

**[2:04:25]** very, very slow process. And if you've ever done any like performance work yourself or, you know, just even development with an agent where you don't have a verification skill, you are the verifier, right? You, you're the bottleneck. You, you, you tell your agent to do something and then it goes off and write some code. Then you open up your, you know, local dev build and then you start to say, oh, you know, it doesn't work. Then you got to copy paste screen, uh, you know, screenshots or console errors or whatever. Uh, and then your agent like slowly kind of like, uh, you know, works with

**[2:04:55]** that and then tries to understand it and, um, uh, fix the thing, but then you're constantly just in the loop and being a bottleneck. So there's really no way to parallelize. So the control glass skills are like one of the first skills I built, uh, for cursor. Uh, and glass by the way is the code name for agents window that we use internally, but it's just cursor, I suess. Um, and so this skill, uh, is, I guess the, the code itself is not super interesting. Your

**[2:05:25]** agent can very easily make one for you, uh, where if, if you're building an electron app or a web app or even 108, uh, applications, uh, you can teach your agent how to use like the Chrome DevTools protocol or through, uh, Apple has some utilities as well for running the simulator and taking traces and controlling programmatic control , as well. Uh, so that's really useful. Uh, but one thing I actually want to talk about is, uh, the, this thing,

**[2:05:57]** uh, where has to read Uh, so this skill comes with this very unique feature called, or not feature, a unique file called a feature map. And so the story then is like, I built this skill and so now the agent was able to, uh, actually run the agent window and take traces and whatnot. Uh, but it had no idea what, what the agent's window was. So, um, you know, like someone would say like, oh, the, the

**[2:06:27]** left sidebar is like lagey or something like that. Or, you know, the right side, the PR tab is not working and the agent would just be like kind of flailing around. It would spend a lot of time trying to like look up the code and you know, where is this feature? How do! actually get to it on the Ul? Which made it basically completely useless. Uh, you know, like we would, I would run the skill locally and you know, it would spawn a dev build, uh, but then it It wouldn't know how to

**[2:06:57]** get to things. Um, and it was just an awful experience. Uh, so who was putting arrows on my screen? Um, so, uh, yeah, this, this feature map has been really useful, uh, because it teaches the agent how to get to all of the features that you have. Um, and in pstack, the plugin that I I've made, uh, search for pstack cursor on Google, you'll, you'll find it. Uh, but there is a create verification skill in that

**[2:07:27]** plugin where it actually helps you set up something like this for yourself. Um, including the feature map. So it will actually explore the code and build up this initial feature map that tells your agent how to get to all of the different features that you have. Uh, and this is extremely powerful because now that you have these user reports that come in, uh, you can actually map even like a vague report or even a screenshot. So we have this, uh, internally at cursor where, uh, we have a Slack channel where,

**[2:07:58]** you know, lots of people giving us feedback on the agents window and rock bot and whatnot. Uh, and oftentimes the report is very bad, like very low quality. Like someone will just put very often we get like a screenshot, like, and then someone just says question mark, question mark, question mark, like, what is this? And you know, like without this, your agent is less like, I have no clue. Right. But with a feature map like this, it has a lot more context and understanding of how to actually navigate, how to get to all of the different features. Uh, so like,

**[2:08:29]** you know, example, like, I guess like the sidebar, like what is the sidebar? Uh, you know, like all the different sub features that are present in it. Um, like from the user point of view, which is where to, how do I get to it? All the different keyboard shortcuts, uh, even like the, the, what do you call it? The dom elements or yeah, like the attributes that you use for selecting things through the CDP, uh, are all there. So, uh, again, yeah, this is like really, really powerful,

**[2:08:59]** uh, for, for agents. Uh, and at P stack ships, uh, that create verification skill, but also a maintain verification skill. Uh, so you can keep this up to date. Cool. Yeah. I was just going to ask how you created that. So do you mind sharing a little bit more about, um, that, that process in the context of P stack and maybe just what P stack is for the folks who aren't familiar? Yeah. So P stack is pretty interesting because, uh, well, first of all the name is kind of goofy, like the P, the P and P stack is like potato

**[2:09:29]** potato stack, because I, um, so, uh, uh, there is a pretty, uh, famous person, Gary Tan, who is the CEO of Y Combinator. And he's come up with this plugin called G stack, uh, Gary stack. And, uh, funnily enough, we share the last name. We have no relations. Uh, but I thought it'd be funny to kind of, you know, poke fun at Gary and make P stack my version of, of, of, of his plugin. Uh, but kind of just tailor it

**[2:10:00]** to my own set of engineering practices. Uh, but I honestly actually never set out to build P stack. Uh, it just started witha bunch of skills, right? Like started with that control glass skill. And then I started with another skill like called how, which I also noticed through like observing agents. Um, so like, you know, in the early days of me, you know, trying to climb this ladder, I was like super in the loop. And I was basically nitpicking my agents to an extreme degree. I was like, I would tell it, um,

**[2:10:32]** you know, this feature has stopped working. Here's a bug report. Like, why isn't it working? And very often the agent would just like confidently state like, oh, it has to be this, right? It has to be this thing. And I noticed like, when looked at the actual tool calls, I noticed it wasn't actually reading the code that I thought should be affected. And that made me just extremely suspicious. And at that point I was, I'm not gonna, I can't trust any, this agent anymore because it's And I think,

**[2:11:06]** build up that distrust and not, and kind of feel helpless. Like, you know, you don't know how to help your agents succeed, but like, again, I think the, the, the management analogy is super helpful because like, imagine if you were a manager of an engineering team and you had an engineer on your team who was a really good coder, no business context whatsoever. You know, they, they and they, they onboarded, you know, like five seconds ago. Uh, and so how do you actually teach that person to be effective?

**[2:11:37]** So how you do that is through a skill, a skill being just, you know, it's just markdown, right. But you know, it encodes a lot of information instructions, a lot of, uh, you can really draw out a lot of intelligence from an agent by, well, some people on Twitter call it like, you know, pull the agent to a different latent space, which is kind of likea fancy way of just saying like, since, uh, you know, LLMs are sort of like, they predict the next token, uh, when you give it some high quality tokens, uh, to begin with, then, you

**[2:12:07]** know, It, it can kind of pattern match on like a higher space that's, you know, smarter. Um, so that's like a very interesting model there, but yeah, I built P stack very, very incrementally. Uh, so, uh, started with you know, all the fail, different failure modes of, of that agents were having. And every time I saw that I just, okay, I'm just going to make that a skill, right. Like stop hallucinating. So I actually go and search up, look up the code, use a lot of

**[2:12:37]** side agents, uh, and yeah, stop guessing. Yeah, that makes sense. One, one kind of follow-up question here, uh, both for myself and from a bunch of people in the chat. So I guess It's two, two parts. So one Is like, how do you maintain these skills? So like the product changes over time, obviously there's a lot of people who are shipping against the code base. So how did these skills get maintained? Uh, and then second to that is like, how do you know when your verification Is, is good enough? Uh, like, and you know, you can trust that the verification, verification loops that you've built are gonna,

**[2:13:08]** I suess you trust that the outputs, uh, when, when they're done. Uh, yeah, maybe I'll talk about, um, I think that's somewhat related. Maybe I'll start with this one first. So like, how do maintain these skills? So, um, if you're not familiar with this concept and eval is essentially like a way to, uh, well, I think the mental model I have is like, it's like a unit test for an agent. Um, and, uh, you can actually make your own evals.

**[2:13:39]** You don't need like a special framework for them. You can build, you can, you can build one depending on like, you know, how scientific and how rigorous you want to be. Uh, my screen is red. Yeah. There's a little button. Um, sorry. Oh, if you mind like disabling the drawing or something, I can't see my screen. Yeah. Sorry. If you guys could not draw on the screen, that'd be great. But, um, there's a little button in the control. Yeah. The, the little drop down. Um, how did I clear? Yeah. Okay.

**[2:14:09]** Yeah. You got it. Perfect. Um, yeah. So evals are a way to unit test your skills basically. And actually in P stack, we ship, uh, under potato mode, there's a playbook. If you search for it, it's called eval playbook. Um, and it's, uh, uh, it's like not, it's actually pretty, pretty rigorous the way it's done. Uh, but, um, essentially what dois I spawn a lot of different sub agents. I have like my main coordinator agent, uh, come

**[2:14:40]** up with a rubric for, uh, what I want the skill to do. Um, and then it spawns all these sub agents and it, it creates individual directories for them which are cleverly named to not let the sub agent know that it's being evaluated because, uh, agents can actually tell. And when they do, they change their behavior. Uh, but it does a bunch of stuff like that to, um, essentially, yeah, like test whether or not the skill

**[2:15:10]** I'm making or changing ts actually doing what I think it does. Um, and one of the really nice things about cursor is that we are, we, we support so many different models. So you can actually eval your skill across all sorts of different models. Um, and you know, get a sense of how well it performs across that different matrix. Um, especially for the models that you use. Uh, so I do this a lot. Every time |, modify a skill, I will run one of these, uh, like the email playbook,

**[2:15:41]** uh, and make sure that, you know, it's actually leading to a result I want. Uh, but I will say like maintaining skills is actually pretty hard. Uh, it requires, think a lot of taste and observation. So you kind of need to be very good at being a backseat driver. You know what mean? Like If you do pair, if you've ever done pair programming, for example, uh, and you watcha coworker code and you just like, you could probably do could do, you know, like, why did you not do this? Right. You, you ask

**[2:16:11]** a lot of questions to your coworker and It's kind of a similar thing here. You like, you don't want to just be a passive observer of the agent. You want to be very in the driver's seat in the initial stages when you're building up your own set of skills. Uh, you know, obviously you can use something like PSAC, but if you're building your own set of skills, it's very, I think, you know, opening up the, all the tool calls and like reading the code and reading all the, uh, the agent behavior and their thinking blocks is a really great way to see where they, they fail, right? Like what, what,

**[2:16:43]** you know, where are they being done? And then you can go and build a skill for that. And then with verification, how you trust It is it's, think it's alsoa very similar iteration loop, uh, where, you know, like I actually did the same process for verifying the verification skill where I actually get, um, so one thing that's interesting about evals is that you can sort of hill climb them, meaning that, uh, your eval can produce a score, right? A score that you can get your coordinator to produce, uh, but also comp,

**[2:17:14]** uh, you can have a judge agent of a different to, uh, kind of cross-reference and make sure that the first model is not being biased, right? The model that's judging all of the sub-agents that are running the thing. Uh, but you can also like hill climb. So meaning that you can, you can use like slash loop in cursor and you can say, okay, keep looping on this eval, right? Until everything is 10 out of 10 as an example. Uh, and I did the same, the basically the same approach with the control skill. And so I kind of, it was very,

**[2:17:45]** it was very hands-off actually. Uh, so, you know, I, uh, I kind of built, built that skill that way, like the CLI and that skill. Um, and over time it's gotten really good. Uh, but yeah, it was definitely not super smooth at the beginning. It required a lot of iteration. And I think there's an analogy here for me, which is, um, well, I make this analogy later in a different slide on my drawing here. Uh, but I think of it like, uh, you know, as a, aS a engineer now,

**[2:18:17]** you're sort of more like, you, uh, like maybe a manager or the analogy I like is like, you're like a chef in a restaurant. Uh, you know, you're the head chef. Uh, you're not cooking all the food yourself anymore. You have a team of cooks, right? You have line cooks, you have a sous chef, you know, you Um, and It's your job to really design the environment. You know, you, you're in charge of setting up the kitchen. You're in charge of, you know, like giving tasks to different people. So, um,

**[2:18:48]** yeah, it's a very interesting way of working. Uh, but yeah, that's, that's how I've basically built, uh, these verification skills. Yeah. Just, just one ball there on like, I had to go, try to go one layer deeper. So are you, let's say we wanted to build, um, uh, an eval ora skill for, for something. And we wanted to kind of get better on its own, which ts, is what think you're suggesting. Uh, are you doing that in like a work tree, kind of isolated with like the sub agents and then the reviewer agents and all that?

**[2:19:19]** Is it happening like in some type of cloud hosted environment? Like what's the, the more, the practical steps if wanted to go do this, uh, and like set up a verification system for something, what would I, what would I do or where would I start? Um, I think that, uh, the best place to start is local because you can observe, you can definitely observe what your agents are doing. So, uh, if you're building a verification skill for yourself, uh, would definitely start local and just have your agent bring up the application, whether it's like a CLI or

**[2:19:50]** a desktop app or whatever. And so you can actually observe, right. You can see how the agent is interacting with the, the application. You can see it, you know, how it calls like the different APIs that allow it to interact with the, uh, the application. Um, but, uh, for me personally, uh, I have basically been kind of all in, mostly all in cloud agents because they're extremely powerful. Uh, and the really powerful thing about cursor is the, the

**[2:20:21]** cloud agents actually, where if you spend a little bit of time setting up your environment, these control skills, these verification skills pay a huge amount of dividends because it's not just something that makes you. as a single engineer better. It actually levels up your whole team. Uh, and even your whole company, because, uh, you can actually start thinking about cloud agents, you can start thinking about automations that automatically do things like, uh, I'll, I get to, I kind of talk about this a bit later, but rit

**[2:20:51]** just kind of get into it. Uh, where, where, you know, for example, like 1 talk a lot about this agent we have called Benny, right. Who, who, uh, you. know, takes all of the bug reports that we get and it automatically goes off in the cloud, opens up a cloud. Uh, it's, you know, it's desktop. It runs. cursor in its own computer and it uses the same control skills to interact with the application and try to reproduce the bug, uh, or. the user report. Right. And. this is so, so powerful

**[2:21:21]** because at once I can immediately, I get So much information from this automatically. Like here in this example, you can see that, uh, the Benny actually reproduced the bug, uh, but it's already fixed. on main. So it actually confirms that we fixed this. problem already. And all ' need to do Is just release another build of. of cursor. Uh, so that's like huge information there that I didn't have to go off and sit with an agent, you know, and spend an hour trying to feel like, is this fixed? Is this not fixed? So you, you, . you gain back so much

**[2:21:51]** time. Uh, but you know, everybody on my team benefits from this. Everybody in the. company benefits from this. Uh, so definitely think that, uh, you know, keeping these, uh, I using cloud agents Is super } powerful. Uh, but yeah, it's, like a journey. You have to trust it first, right? Before you, you get to this point. And that's, it goes back to what I was saying here where, you know, it's very hard. It's almost impossible. And I would definitely encourage you not to know, like if you're still in this zone, you don't

**[2:22:22]** want to jump to like, I'm going to spawna hundred of thousand or thousands of cloud agents right now, because you're just going to waste a lot of tokens. um, and it's going to be extremely expensive. Yeah. So just to kind of recap so far, basically the, if the journey that you've kind of gone on, it would be to start with verification, um, building some, some skills and some, some ways of determining that the agents are producing at least like correct code, whether, like you said, whether it's good code or not, it's maybe a separate question, but like, it's, it's technically solving the problem by

**[2:22:52]** looking at, you know, stack traces, looking at, you know, the actual behavior in the app and so on. Um, and then once we trust it locally, then we can start to think about scaling into the cloud and running more agents that are on their own, right? So whether that's like a bug report that comes in or something, they can go and pick it up and solve the problem and give us back a PR. And then maybe the last step is like auto-merging the PRs, which, uh, is where you're at. And maybe not where everyone is at. Yeah. Yeah. Um, and then reviewing them on main, but, um, is that, is that about right? Yeah, exactly. I think, yeah,

**[2:23:23]** that's why I drew this, this, uh, this, this curve, right? Because that, this, this basically describes my journey of, you know, when I started, barely could use a couple of agents and I was just observing every single thing. I think there's really no shortcut for going from here to there because this is really about your personal level of trust in agents, right? Um, obviously, you know, as, as an engineer, you don't want to So how do you actually build up that trust? Takes, um, a lot of, uh, suess, taste and judgment.

**[2:23:53]** Um, but, uh, you know, like I think plugins like Pstack definitely can help you, uh, get up to speed much quicker. Uh, and so suess It's like, if you trust me and you trust Pstack, then in by extension, you can maybe trust your agents. But if you don't trust me and I definitely would not encourage people to blindly trust me. Uh, uh, you know, if you build up your own set of skills that you can obviously, you know, take a look at Pstack and kind of fork it, make it your own, improve the skills,

**[2:24:24]** definitely encourage that. Uh, but for me, it's really all about, it just keeps coming back to trust. You know, every one of us here in this chat have a different standard for engineering. Uh, and there are different things that are important for us in our code base. And, uh, when you are able to encode all of that into skills and you can verify that your agent is actually doing them, that allows you to really kind of ascend this curve and, um, uh, you know, start automating things. Uh, there's another piece wanted to talk about.

**[2:24:56]** Um, if there's. Yeah, go for it. I'll pick up more questions as I go, but yeah. Yeah. I think there's a third part to this, which I haven't talked about yet, which is kind of an interesting one, which is like refactoring and rewriting. Like one of the, uh, Suess most controversial, one of the most controversial topics in the industry, I think is like, should you rewrite your app or not? Um, because I think engineers are very prone to this where, especially when you joina company, you come in and you see like the code base and you're like, oh man, this Is shit. Like

**[2:25:27]** who wrote this code? You know, it's, it's terrible. I want to rewrite the whole thing. There Is a very common inclination. And I think a lot of, you know, before agents, um, and I guess arguably even now people will definitely discourage you from rewriting stuff, but I'm actually here to make a case for why you might want to consider it. Um, because I think it really depends. Uh, you know, uh, brownfield applications, I think are actually in a pretty sood spot, especially if they're set up

**[2:25:57]** well already. Uh, and like recently I've been talking to some people, but, uh, you know, I, I was just observing, I just noticed this parallel, which is that a lot of big tech company problems are now everybody's problems. Um, and the big tech company problem, you know, like when I was working at Meta, like we had this don't know, tens of thousands of engineers, Just, you know, like banging on their keyboards and shipping code and engineers at Meta. Uh, but,

**[2:26:29]** uh, I'll say like, you the code quality is actually not that good. Um, and so I often joke that like, you know, before AI sloth, we had human sloth. Um, and so, uh, you know, I think a lot of big tech info, like, uh, like what Meta has or Google, you know, you know, really big tech companies are actually designed for that, where you're sort of like, you're catering to the, the, you know, like, uh, sound, that sounds so bad to say, but like the, the least capable engineer on your team, right? You build, you

**[2:27:00]** build frameworks, you build conventions, you build guardrails, you know, you restrict credentials so that, you know, your intern doesn't wipe your production database. Um, there's, uh, you know, if you have that level of infra already, I think your agents can actually already do a very solid job, right? Because they have, the, the guardrails are already in place for agents to not cause havoc or not cause too much havoc, uh, in your code base. Um, and you can always add more, you know, guardrails. Uh,

**[2:27:31]** but I think like Greenfield applications especially are, you know, like the brand new applications are like the biggest risk in my opinion, uh, and also the greatest opportunity because, y you know, if you vibe code a project, uh, a prototype, um, like we did for Grokbot, you know, Grokbot was spun up very, very, very quickly. Um, and if you, uh, if you haven't heard of, of Grokbot, it's like our, a new application we just launched yesterday. Uh, it's, it's really cool. Uh, lets you orchestrate your, create like individual agents that have

**[2:28:02]** their own identity and you can kind of orchestrate them. It's super cool. Definitely check it out. Uh, but yeah, that was, it's like a very, it was a very Greenfield application like most prototypes are. So it was like vibe coded very quickly. Humans were not reading the code at all. And, uh, I had this tweet recently, uh, where I said something about organic architecture. Um, maybe I'll find it. Uh, but the idea is that, uh, when you have a completely vibe coded application, you

**[2:28:34]** essentially have no guardrails whatsoever. So, uh, your agents, when you give them a task, they will just solve it in whatever method is the most convenient. And over time you get into this, uh, situation where you have a code base that Is spiraling out of control, because you don't understand it. Uh, your agents understand it, I guess in a way, but like they've built something that is, you know, optimized for short, for shortcuts. Uh, and, uh, you know, it will, you will suffer, you have

**[2:29:05]** a lot of issues with that application. Uh, so I think starting your code base with, uh, like very strong constraints is very much needed. Uh, because like when you have a code base that you can trust, right. When you have guardrails that actually help you, uh, uh, help your agents, right. Good code. You can get into the, you know, like into this part of the curve where I, , where I, like I said, you know, I woke up today and I had like 20 PRs merged, uh,

**[2:29:36]** by my agents. And that's because I invested a lot, a lot of time, uh, over 600 PRs. I, I, calculated yesterday, uh, when refactored all of GrokBot to this new architecture that I've been building. Um, and yeah, I've gotten toa point where I, I don't really look, I really don't look at the code anymore. And, um, I say that not just, you know, to sell you tokens, but because I, you know, it, it took a lot of work to get to that point. I spent a lot of

**[2:30:06]** tokens to get the code base to this point where no longer have to look at it. Uh, but I'm very excited because, you know, of the potential where, you know, it's not just, it, this doesn't just benefit me. It benefits everyone contributing to GrokBot. And it also empowers, you know, designers and product managers and, you know, people, even GTM people to add features to GrokBot. And don't have to worry, you know, I don't have to wake up at night in, in the middle of the night and worry like, oh shit, someone's just merged a perf regression. Right. I

**[2:30:37]** have a ton of constraints and Cl Is like, it's actually very annoying to write code in, in GrokBot, but like agents absorb all of that annoyance. Um, but yeah, I'm happy to talk about what exactly that Is. um, yeah, I think one question, um, before we get into the, this part here is just around that element of like what your, your, your Cl looks like, or maybe some of the constraints and then also like the average PR size. |sawa question about that earlier, just to give people a, you know, kind of a glance,

**[2:31:07]** it doesn't have to be like mathematically average, but just, uh, you know, like what generally the size of the PR is, um, if it's only a couple lines of code or, you know, um, yeah. Um, I think it depends on me. I'm trying to dothisina way where I'm not gonna like. Yeah. You don't have to share the actual number of you, like the actual average. Uh, I think this is fine. Benchmark. But like we have, so, okay, this is not that interesting, but, uh, well, fun fact is that virtualization in GrokBot and

**[2:31:39]** in, uh, cursor ts actually powered by, uh, Pretext, uh, which is a sort of new library that someone's built. Um, that's really interesting. You should, you should check it out, but that's not really that important. Uh, I think the average PR size, I actually don't know if I want to click on these. Uh, I probably can, but I would say like they can range anywhere from a few hundred lines or 50 lines to like a thousand, depending on what the thing is doing. Uh, so like here, I'm not here

**[2:32:10]** like deleting a bunch of files. So I expect that it's just as like mostly deletion. Uh, but yeah, it, it kind of varies. There's no like, yeah. There's no like hard cap or are the middle? They're all like 50 line. There's no hard cap. There's definitely no hard cap, but I do encourage my agents to split up their work into multiple PRs. Uh, I do that mostly because, uh, I like, I like the idea of the, guess maybe this Is much harder to do now as in the world of agents and you have like sO many commits, but I like the idea that, you

**[2:32:41]** know, the Git history Is a very rich source of context. Uh, and I like the, I like each PR to sort of atomically describe what that small piece of thing is doing, which also makes it easier for me to revert changes and like figure out, you know, oh, shipped a bug and it's just, it's here. It's not in this 40,000 line PR where who knows what landed in there. Uh, but , I don't havea hard cap on PR size. Cool. And then, um, yeah, also quick question on like

**[2:33:12]** Cl. So again, you don't have to go into like, uh, the screen share of like your, your CI does, but just generally would you describe what the Cl kind of looks like, uh, or how strict it is? Uh, yeah. So, uh, well, specifically for Grokbot. So Dune is the, is the sort of cheeky code, code name for the architecture that we've built Grokbot. Um, the Cl looks pretty annoying because there's checks for everything. So like literally have, um, uh, well,

**[2:33:42]** if you've written any react, for example, you know, you know that one of the biggest foot suns in react is use effect. Uh, so in, uh, Dune and in Grokbot, we've banned use effect. So Dune Is just the, the, the mental model of what Dune Is, uh, you can kind of think of it as like next.js for, uh, electron apps and it's designed for agents to write. Uh, and it's like custom for, you know, our agent powered applications. Um, so the Cl checks are very like specific to that. Like, you

**[2:34:13]** know, don't use use effect. It's, it's, it's banned. Like Cl will fail, uh, and yell at you. We have like, some of the more interesting ones that people might raise eyebrows is like, I actually banned code comments as well. Uh, which is very interesting. Um, but I've noticed that 99% of the time agents just write code comments that kind of describe some historical thing that is actually totally irrelevant to the code. Um, like it will often say like, you know, oh, Lauren said you should never

**[2:34:43]** do this and it's now in the, in a code comment. Like what? Like why, what that was, I didn't say that as likea durable, you know, global rule. just meant like your, this PR sucks and you should change that part. Uh, agents don't really understand us that well, surprisingly. Uh, and, or they kind of assume too much and they kind of do things in like very stupid ways. So like, yeah, we just ban everything, everything you can imagine, like the agents are bad at, we ban. Uh, so one example that we actually suffer

**[2:35:14]** a lot in the agents window is we have, uh, you know, you know, If you've used agents, we do, you've definitely seen performance issues and you know, we're constantly trying to fix them. Uh, but it's like a, it's a never ending struggle because there's so many pull requests that get merged. Every, any one of them could just resress performance or stability or reliability. Uh, you know, the agents window doesn't have this architecture yet. I plan to do, bring this learning back there and kind of refactor everything there. Uh, but, uh, it just regresses super often,

**[2:35:46]** uh, because, uh, there's just one example is like, we have very poor, um, isolation between processes. So like on, you know, on, on Electron, you have a renderer thread that renders your UI, but you also have like a main thread that you can run other code that, you know, doesn't need to block the renderer. poor job of separating those things. And so oftentimes you just accidentally have code that gets pulled into running on the renderer thread, right? And then all of a sudden you're competing with the, the renderer that, you know, that

**[2:36:17]** has a very, If you want like 60 FPS, you have to, every frame that gets drawn has to be done in 16 milliseconds. So very, very small, you know, deadline per frame, uh, if you want, you know, a very smooth product. Uh, and when you start building, bringing in, accidentally bringing in, you know, things that are like very computationally heavy, or they have a lot of IO, uh, then you just get into like a lot of jank and your, your FPS really drops. You start, uh, you know, losing frames. You get long tasks that take

**[2:36:47]** more than 16 milliseconds. And then you just get this really choppy experience. So all of those patterns that we've learned, basically building Electron apps, we've encoded into this framework and it becomes like a hard failure. So I literally, in, in GrokBot, we literally have a directory called electron main, electron renderer, and we have, uh, import, uh, Cl, I guess, where we actually check the dependency graph to make sure you're not accidentally importing code from one directory to another. Uh, so that's

**[2:37:19]** enforced by Cl, um, as well as bug bots, uh, which is our, which cursor's, um, like code review tool that runs on Cl. Uh, you know, in our agents MD, it's everywhere. Like, so have this thing here where I talk about like, um, you know, like there are multiple layers, I think for building a good code base. Uh, obviously the code base is one where, uh, if you have an architecture like this, where it's extremely strict, uh, you know, the, the,

**[2:37:50]** the way to build features Is very conventional. That's like the strongest, strongest level of enforcement because agents just love to copy existing patterns. So, uh, one example of this in GrokBot is like, we have this, these concepts called like a feature and we have entry points and transcript cards. Like, oh, you know, the cards that you see in the chat, these are all like, like nouns, I guess, In, in the framework. And so there's a very conventional way of creating them. And so like a feature is all in

**[2:38:20]** a single directory as an example. And so all of the code that contributes to that feature lives in one directory. So it's all co-located in one place, makes it super easy. You know, agents don't have to like, uh, srab around and try to the things are. It just looks at the feature and like, oh, okay, I'm working on the onboarding feature in GrokBot. Uh, I'm just going to work in this directory and for 80% of the work, it's mostly just very encapsulated there. But, uh, like it's like very, it's like

**[2:38:50]** design again for, you know, like the dumbest agent, like you don't have to think, right? The, the, the, one of the key principles I have for this framework is like the shortest, the shortest path is the best path. So, uh, because that plays exactly to how agents love to write goals. Like they like to take shortcuts really, you know, they'll find the quickest way to solve the problem. So why not make that the best way to solve the problem? Uh, so I, I probably won't get into all the specific details. Um, and, uh,

**[2:39:22]** the, the, this framework is really more of a collection of ideas and principles rather than something that will open source. Uh, you can, you can, you know, screenshot this, I suess, if you want and, uh, tell your agent to, uh, do some, build, build something like this for you too. Um, yeah, but it's really all about the layers. Uh, you know, like the, the code base Is one part { with features, uh, and directories and, you know, import or blocking import dependencies, uh, that © shouldn't be imported. Uh, but,

**[2:39:52]** and, and it all enforces that ; and static analysis. So like, uh, there's ci checks. We have a lot of lints for bad patterns that we observe, uh, compiler diagnostics. Uh, there's also rules and bug bot, which are, um, Ith ink like three, four, five are more soft, right? o These two actually make, make ciread, right? So that, you know, there's a hard He constraint where the agent can just write crappy code for rules and skills and bug

**[2:40:23]** bot. You rt agents can still forget, right? You can still, or it may not always a consistently apply them. So I like to layer them, but Idon't, I don't like to rely on them as the only source of enforcement because it's very, very soft, right? And if you, if you only have rules and bug bot and skills and astyle guide for your code, you will, it's onlya matter of time before your 7 code base looks like complete trash. I'm sorry to say that, but, uh, I definitely recommend, yeah, like, you know,

**[2:40:54]** ves investing in, you know, things that can be hard and forced, right? And this is why, you know, maybe, uh, the choice of tech stack that you use Is also very important. Um, like I think for example, Rust is sort of making, you know, #m it's like getting super popular * again, uh, because the compiler is so strict, right? The 4 compiler enforces so many different things. You know, there's a * borrow checker that you have to appease. And if, as long as you make su re your agents don't write unsafe code blocks, uh, you can more or

**[2:41:24]** less { feel somewhat confident that if the code compiles, it's € probably works and it's good. Uh, but you'll see, it gives you that level of om trust and confidence that you asa human engineer, no longer need to go and check it youn rself. You know, you, you rely on code om and static analysis to actually make that, uh, a lot smoother. Um, and I guess the worst part, the worst place to be in is if you are stuck in code review land where you

**[2:41:54]** actually enforce all of the constraints, the invariance in your code base by literally the human person saying, you know, i reading the code and like, okay, you should not do this. Right. Every time you have to do that, you should consider that as a code smell, like a, uh, anti-pattern. And you should say, okay, instead of me commenting on the PR, how do I turn this into a hard rule? Right. How do I turn this into a lint rule? How do I turn this into a Cl failure? Or how do I even categorically eliminate this problem, uh, entirely? Uh,

**[2:42:26]** I, I can talk about another migration I've done, but I'll probably pause here. Sure. Yeah. I feel like that's, that's where I am to be honest is, is it what you're describing right now, which is that like, I don't have all of these rules. Uh, so I have some things to go do after this session, uh, in terms of being able to scale my agents. I'm, I'm definitely on like the, uh, you know, maybe a couple of parallel ones locally stage, like two to three locally. And I'm sure most people here are on the same. So, uh, yeah, I know we only have a couple minutes left. Uh, Lauren, was there anything else that you wanted to, to highlight? I obviously there's lots of questions

**[2:42:57]** so I can grab more, but I want to give you a few minutes, uh, if there's anything else you want to talk about. Well, think I've been yapping for quite a lot, so i'm, maybe let's just do questions. Okay, cool. Uh, one question that had, uh, a couple of, uh, came up a couple of times was just arou nd, like, token usage. So the question is like, is, is what you're describing a realistic thing for people who are on, you know, uh, a normal set of token usage? They don't have, you know, basically unlimited tokens, uh, to work with. I think that's a really good point. 1 mean, like, obviously, you

**[2:43:27]** know, I work at an AI lab where we have unlimited tokens. So, uh, I definitely cannot say that, you know, this is something everyone should do in the exact same way that I did it. I think it's possible to get to this point without, you know, breaking the bank. But, you know, if or, you know, you're, you're, you have a startup that you lead, um, I think to me, it's a question of ROI. Um, and it's like, uh, yes, you spend a lot of money on tokens in

**[2:43:57]** the upfront stage. You know, like refactoring your code base is going to take a lot of tokens. Uh, adding all these things, uh, is going to take a bunch of tokens. But if we're heading to a world where agents are writing all the code and, you know, you want to be very lean, right? You don't want to have to hire, you don't want to be, you don't want to become like meta, right? Like, I mean, like in terms of, you don't want to become a 10,000 person engineering org because I mean, that's a cool problem to have, but also, you know, you, you have so much overhead. There's like planning,

**[2:44:29]** you know, like it's, it's, it’s, uh, personally, I wouldn't, uh, it's not super fun, but, um, I think you want to stay very nimble, right? And you want to, you want to be like, agents are all about allowing you to do things that you couldn't do before. That's really to me, like the value of agents, you know, it's not just storing tokens on every single little thing. But, um, to me, like the thing I couldn't do before is like, enforce this level of constraints ina code base by myself, right? Like I'm just

**[2:44:59]** asingle person, you know, uh, it would have taken me years to build this framework, uh, and do all [ the refactoring and J test everything myself and verify, 3 you know, like run, imagine if there, it was just me right now in, in pre-agent era, just like running, me so long, right? And my salary Is pretty high, right? Like, so, you know, the, the question I| think dan engineering leader might have is just then, you know, like what is, there's a trade-off of, do you hire

**[2:45:30]** someone to do this? Or do you spend the tokens to setupa code base so that even the, the most naive, right? an The dumbest agents can do a good job. And when you actually get to this are not, you know, fable size do an excellent job of writing code. And this pays a lot of dividends as well for me personally, where I've empowered not just = myself, but again, like PMs, d designers, engineers who are not © familiar with GrokBot to just

**[2:46:00]** contribute in a way that is sustainable. So I think, yeah, it's definitely like a. like nothing Is like free for sure. And tokens are pretty expensive. But, oh, actually, I don't know how many of you have seen this, but we actually announced Grok 4.6 today. a SO very exciting, finally out. So yeah, Grok 4.6 would be like a great, it's very, very smart. It's really good on the, the same, the tokens, well,

**[2:46:31]** [hopefully I'm not saying T this incorrectly, but I believe the cost per token is the same as 4.5. So you're actually setting more intelligence for the same cost. I think this is an area that Cursor tries to, Cursor and SpaceX AI try to really optimize for oF like that Pareto frontier of, a know, cost versus intelligence. You know, we don't necessarily want to build the biggest extremely expensive to run. It's really about like, how do you find that sweet spot,

**[2:47:01]** right? You don't, you don't need a giant model, but mH it's just super smart. Right. wy And it's not very expensive for inference. Uh, but, um, yeah, I think to kind of round it up, um, I think it's like a, it's, it's, there's a, if you do your own analysis, I feel like it's pretty positive. It will be pretty positive that the ROI you get from investing and stuff like this, uh, just empowers not just yourself, but your whole team to be so much more productive, right? Like imagine if you have an army of

**[2:47:32]** engineers like me who are shipping so much improvements and bug fixes, uh, you know, every day, right? Like that is pretty exciting. Cool. Uh, one last question before we wrap up, this one is for the people in product on the, on the call. So let's say we do have an army of engineers who are shipping like Lauren. I'm just curious, like how is the product team or other functions of your company keeping up given that like, if you're shipping so quickly, have, have, are they using AI more to do their jobs? Like as much as you can speak

**[2:48:03]** to that, I obviously, you don't have like, you're not in that role, but just curious about how that works. Um, I think this is where Grokbot has been actually exceedingly powerful, uh, where, so before Grokbot like, you know, uh, obviously cursor only had cursor, like we only had agents window. We had a CLI, we had an IDE and these are really like power user tools, right? They're designed for developers. So it's very, very developer centric. You can do knowledge work in them, but it like the Ul is not really optimized for that. So we

**[2:48:33]** actually didn't really have, uh, well, I think like a lot of people in like, you know, GTM product, like they might have used cursor, uh, to do their work, but it definitely wasn't like a delightful experience for them. Um, I think now with Grokbot, uh, it's become, Grokbot is basically like the cursor moment for people who are not in tech. In my opinion, like it's like, it's like a very, very accessible way to use agents in a very comfortable, very familiar interface. It looks like iMessage.

**[2:49:05]** Um, and it's very fun too. You know, you can give your agent a fun name. Uh, you can have, you can kind of do orchestration with, in a very like natural way where you can sort of, you know, each agent's like a person and now you've gota team of agents like working on, you have one, one agent per account that you manage as an example. Or if you're a PM, you have, you know, you can have an agent that summarizes all the work that Lauren did last night. And then now you know what I did, right? are leveraging that a lot and they're shipping code too. Uh, so, you know, oftentimes

**[2:49:36]** they will just say, oh, here's a bug. I fixed it. Can you look at it? And then I'll go review it and actually it's just perfect. I'm like, okay, stamp. Uh, so, uh, that think that shows that, you know, the, the Dune architecture is holding up, right? The, all the, the really strict constraints allow people who are not experts in engineering to contribute at a high level. Uh, so I'm, I feel like I'm already seeing that pay off a lot where, uh, you know, designers and PMs are just able to, to, to ship features directly. Um, and that just

**[2:50:07]** makes the GrokBot team super fast, right? Where we can ship so quickly. Um, and we have a lot planned, so I'm very excited, uh, to, you know, uh, to, to ship more, ship more stuff. Yeah, that's awesome. Uh, we are at time. So, uh, I guess Lauren, if, if folks want to support you, maybe go try out GrokBot and try out, uh, four, six and, uh, you know, get, get, provide some feedback, but yeah, this was awesome. Really appreciate you taking the time. Uh, thanks everyone for all the messages

**[2:50:37]** in the chat. Uh, lots of good questions. I know we didn't get through everything, but, uh, as I kind of said at the top, way more questions than, than we could get through, but, uh, yeah, really, really thanks. Thanks for, for joining. Thanks everyone for joining and, uh, hopefully you, you enjoyed the session. Yep. All right. Yeah. I see you. Thanks for having me. And, uh, if you have any more questions, yeah, just DM me on Twitter. Uh, rll, I'll open them up, I guess. I'tl let the flood. You're gonna get, you're gonna get a lot of DMs. Yeah. I'tl open the floodgates. So, yeah, DM me. Maybe I'll do like a Twitter space at some point as well for more questions, but really appreciate everyone for showing

## 段 D：与段 A 重复（2:51:07–3:43:40；字幕 OCR，保留备查）

**[2:51:07]** up, uh, you know, taking an hour out of your day. Yeah. All right. Thanks all Ileana wan tha all. I'll see you the next one. Okay. Thanks everyone. = wyt. roi SUTICALLY, B UCREREUIN CHTGAL Bye. Personally, I think that ey A ie a en a Tl iba really like someone you're pair programming with, and nota tool to just replace the _ act of writing code, or worse, outsourcing your thinking. And think there's a tendency, because AI is so exciting, you want to put AI everywhere and be seen as

**[2:51:37]** someone who is very, what do you call it, on the ball, I guess, with AI. [hat you feel this AI. [Nat YOU TeeL UNMIS pressure of, I've got to _ increase my productivity, I've got to ship like 100 PRs this week and barely understand what I'm doing and vibe a - oF I Lad “ I on LUUC IIly way lu a code my way toa million ARR or whatever. But think, you know, one of the things that I've personally seen is that although when I use AI, I save some time, you know,

**[2:52:07]** writing the code, I actually find myself spending more time reviewing what the AI did and like correcting it. So you know, like I've tried the thing that a lot of people say like, you know, you instead of prompting an AI to iust build the feature outright, you sort of get it to build a spec for you first, then you review that spec, and then you do that whole thing then it's like, okay, so I assume you can see my screen. Yes. Yeah. So yeah, today. Yeah, I think I think the bic theme for me as I've been using agents to

**[2:52:38]** write code, and I'm sure a lot of you have had the same experience as well is how do you trust it? You know, especially if you are an engineer that's been writing code for a very long time, you have a lot of opinions and lessons that you've learned about doing good engineering. And when you see agents just, you know, winging it and, you know, guessing, hallucinating, you know, confidently stating that they found the smoking gun for the hundredth time, but it's actually not the real problem. You lose a lot

**[2:53:08]** of trust. And when you lose, when you don't have much trust in your agents, feel like you really can't get the most out of them. And for me, the parallel is like with management. So if I'm an engineer manager of a team, and I have a bunch of, you know, I have a team of engineers on my team, and I don't trust them, then the mode of operation I'm going to be in is going to be like micromanagement, right? I'll have to spend a lot of time looking over my report's shoulders and checking that they're doing

**[2:53:39]** their work well. You know, that they're not shipping bugs to production. And so I drew this chart because It's not, it's not a very scientific chart, but like, this is how I imagine myself and my journey through using agents. So, you know, like fast forward or back forward or fast back, fast backwards, like a year or so when, you know, nobody was, or not many people were using agents to code. So think you, you know,

**[2:54:09]** get into this mode where you are in very heavily in the loop with one or several, like a handful of agents. And you find yourself just constantly, you know, trying to understand what your agents are doing. And you're very, very in the loop. You're watching every single output. You are sitting there prompting. And you really can't parallelize beyond that because you don't, again, you don't have that trust, right? You can't go to a hundred agents, like spawn a hundred agents when

**[2:54:39]** you don't even trust the output of one agent. So over the past five months, I feel like I've really been able to, like, ascend this trust curve. And now I'm at the point ! where I actually have, this sounds kind of scary to say this, and it makes me sound like a slop artist, but I promise I'm not. But I actually have my agents now auto-merging PRs for me, which ts like a wild thing to say. But like I woke up today and there were like 20 PRs landed and I just

**[2:55:09]** reviewed them on main, like they were already landed and they were good. So how did I get to that point? It's basically what I wanted to talk about today. And again, like, yeah, feel free to Jump in if you have questions, Colin. But, oh yeah, of course got to show this chart where... No, do not trust... Someone requested to control my computer. Probably won't do that.

**[2:55:40]** But yeah, so this chart, think... I'm sharing this chart not to kind of like flex, but to kind of show like the journey. Like, so you can see like the curve, like it sort of like inversely matches the contributions I've been able to land at Cursor. So I joined five months ago. And five months ago, like I, you know, my first month, I was like not very productive because I was, you know, I was learning the code base. I was going on. And as. got more confident in my agents, I've really been able to kind of ramp

**[2:56:10]** up my productivity. And again, like, yeah, like last month I shipped a. thousand PRs, which is ridiculous. And then this month, we're only on the 12th. I'm already at like almost 800 PRs landed. So the velocity is definitely high. And you, I'm sure. a lot of you will. definitely be questioning like how, how much of this code is actually good. And I think, yeah, that's definitely fair to question. But yeah, I think, |. think if you set uD

**[2:56:42]** your agents well, you can definitely get to a very similar level. I talk about how we do that. So for me, I think I'm curious, like, I guess, calling your experience as well. But for me, I think the most important skill that you should have in your toolbox when you work with agents is verification. And by verification, I mean the ability for an agent to actually run the

**[2:57:12]** code or take CPU traces or heap snapshots or, you know, open an 10S simulator, whatever, you know, however your application is exposed to your users, it can do the same thing and run it for real and actually test and verify it don't work. Because that's the thing that really closes the loop. It doesn't guarantee your agent writes good code, but it allows them to at least write correct code,

**[2:57:42]** which is a big, a really big step forward for being able to trust your agent. will, I can share one example that we have within cursor. So for the cursor agent

**[2:58:14]** window, so this is actually an interesting story. But when I joined cursor five months ago, they're actually, well, I was supposed to joina different team. I was supposed to join like the cloud agents team. But then since I have a lot of experience working on React and agents window is a React application, was asked to basically help out with the agent window work. But there wasn't really a lot of like skills to

**[2:58:46]** help me. So I just found myself that, okay, agents window Is going to launch in like a week. Right. We have a really tight deadline. And there was, you know, I was just sitting there like, okay, I'm going to open up the performance, the Chrome Dev tools and just like take a trace, look at it myself and try to make sense of this flame graph. And keep in mind, I was just like in my first week. So I had no idea what I was looking at. No idea what, you know, mean, I had some idea, but you know, the code base was completely fresh to me. And I realized like my agent had no idea either,

**[2:59:17]** you know, like I would take a screenshot of the trail, download trace, I would send it to it and it'd be like, yeah, it kind of looks like this, you know, and it would like confidently state like It's this thing. And then I try to fix that. And turns out that's not the actual thing. So this was a very, very slow process. And if you've ever done any like performance work yourself, or, a know, just even development with an agent where you don't have a verification skill, you are the verifier, right? You're the bottleneck. You tell your agent to do something, and then it goes off and write some code. Then

**[2:59:47]** you open up your, you know, local dev build. And then you start to say, oh, you know, it doesn't work. Then you have to copy paste screen, you know, screenshots or console errors or whatever. And then your agent like slowly kind of like, you know, works with that, and then tries to understand it and fix the thing. But then you're constantly just in the loop and being a bottleneck. So there's really no way to parallelize. So the control glass skills are like one of the first slalls I built for cursor. And glass, by the way, Is the code name

**[3:00:17]** for agents window that we use internally, but it's just cursor, I guess. And so this skill is, guess, the code itself is not super interesting. Your agent can very easily make one for you. Where if you're building an electron app or a web app, or even iOS applications, you can teach your agent how to use like the Chrome DevTools protocol, or through Apple has some utilities as well for running the simulator I and taking traces and controlling.

**[3:00:48]** programmatic control as well. So that's really useful. But one thing |! actually want to talk about is the this thing. Where ts the read me? So this skill comes with this very unique feature called, or not feature, a unique file called a feature map. And so the story then is like, I built this skill. And so. now the agent was able to actually run the agent window and

**[3:01:18]** take traces and whatnot. But it had no idea what the agent's window was. So, you know, like, someone would say like, oh, the left sidebar is like, laggy or something like that. Or, you know, the right side, the PR tab is not working. And the agent I would just be like kind of flailing around. It would spend a lot of time trying to like look up the code. And, you know, where is this feature? How do I actually get to iton the UI? Which made it basically completely useless? You know, like, you know, like, I would run

**[3:01:48]** the skill locally. And, you know, it would spawn a dev build. But then it just be churning. Like, I just try to click here. It wouldn't know how to get to things. And it was just an awful experience. So, Wu Is putting arrows ont my screen. So, yeah, this feature r map i has been really useful because it teaches the agent how: to get to all of the features that you have. And in Pstack, the plugin that I've made, if you

**[3:02:18]** search for Pstack cursor on i Google, you'll find it. But there is a create verification skill in that plugin where it actually helps you set up something like this for yourself, including the feature map. So, it will actually explore the code and build up this initial feature map that tells your agent how to get to all of the different features that you have. And this IS extremely powerful because now that you have these user repo rts that come in, you can actually map even like a vague report or even a screenshot.

**[3:02:50]** So, we have this internally at Cursor where we have a Slack channel with, you know, lots of people giving us feedback on the agents window and Rockbott and whatnot. And. oftentimes the report Is very bad, like very low quality. Like someone will just put very often we get like a screenshot and then someone just says question mark, question mark, question mark. Like, what is this? And, you know, like without this, your agent is like, Ihave. no clue. Right. But with at featu re map like this, it has a lot more context and understanding of how

**[3:03:22]** get to all of the different features. So, like, you know, example, like, I suess, like the sidebar, like what ts the . sidebar? You know, like all the different sub features that are present in It. i: Like from the user point of view, here's how to get to it. All the different keyboard shortcuts. Even like the the what do you call it? The DOM elements or like the attributes that you use for selecting things through the CDP are all there. So again, yeah, this Is

**[3:03:55]** agents. : And Pstack ships that create verification skill, but also a maintain verification skill. So you can keep this up to date. Cool. Yeah. was just going to ask how you created that. So do you mind sharing a little bit more about that process in the context of Pstack and maybe just what Pstack ts for the folks who aren't familiar? Yeah. So Pstack is pretty interesting because, well, first of all, the name Is kind of goofy. Like the P, the P in Pstack is like potato, potato snack because

**[3:04:25]** I, so there's a pretty famous person, Gary Tan, who is the CEO of Y Combinator. And he's come up with this plugin called Gstack, Garystack. And funnily enough, we share the last name. We have no relations, but I thought it would be funny to kind of, you know, poke fun at Gary and make Pstack. My version of his plugin, but kind of just tailor it to my own set of engineering practices.

**[3:04:57]** But I honestly actually never set out to build Pstack. It just started witha bunch of skills, right? Like started with that control glass skill and then I started with another skill like called how, which I also noticed through like observing agents. So like, you know, in the early days of me, this ladder, I was like super in the loop. And was basically nitpicking my agents to an extreme degree. was like, I would & tell it, you know, this a bug report. Like, whv isn't it working? And very

**[3:05:28]** often the agent would just like confidently state like, oh, it has to be this, ricsht? It has to be this thing. And I noticed like when I looked at the actual tool calls, I noticed it wasn't actually reading the code that I thought should be affected. And that made me just extremely suspicious. And at that point I was like, I'm not going to, I can't trust any, this agent anymore because it's And I think, I think it's very easy to just, you know, like build up that distrust and not, and

**[3:05:59]** kind of feel helpless. Like, you know, you don't know how to help your agents succeed. But like, again, I think the management analogy is super helpful because like, imagine if you were a manager of an engineering team and you had an engineer on your team who was a really good coder, no business context whatsoever. You know, they and they onboarded, you know, like five seconds ago. And so how do you actually teach that person to be effective? is through a skill, a skill being just, you know,

**[3:06:29]** just markdown, right. But, you know, It encodes a lot of information instructions, a lot of, you can really draw out a lot of intelligence from an agent by, well, some people on Twitter call it like, you know, pull the agent to a different latent space, which is kind of like a fancy way of just saying, like, since, you know, LLMs are sort of like, they predict the next token. When you give it some high quality tokens to begin with, then, you know, it can kind of pattern match on like a higher space

**[3:06:59]** that's, you know, smarter. interesting model there. But yeah, built P-Stack very, very incrementally. So started with just really observing how agents, you know, all the different failure modes of that agents were having. And every time I saw that, I just, okay, I'm just going to make that a skill. All right. Like stop hallucinating. Actually go and search up, look up the code. Use a lot of sub-agents. And yeah, stop guessing.

**[3:07:30]** Yeah, that makes sense. One kind of follow-up question here, both from myself and from a bunch of people in the chat. So I guess it's two parts. So one is like, how do you maintain these skills? So like the product changes over time. Obviously, there's a lot of the code base. So how do these skills get maintained? And then second to that is like, how do you know when your verification Is good enough? Like, you know, you can trust that the verification loops that you've built are going to, I guess you trust that the outputs when they're done. Yeah, maybe I'll talk about, think that's somewhat related.

**[3:08:02]** Maybe I'll start with this one first. So like, how do I maintain these skills? So if you're not familiar with this concept, an eval is essentially like a way well, I think the mental model I have is like, it's like a unit test for an agent. And you can actually make your own evals. You don't need like a special framework for them. You can build, you can, you can build one depending on like, you know, how scientific and how rigorous vou want to be.

**[3:08:32]** My screen Is red. Yeah, there's a little button. Sorry. Oh, do you mind like disabling the drawing or something? I can't see my screen. Yeah, sorry. If you guys could not draw on the screen, that'd be great. But there's a little button in the... Is thata troll? Yeah, the little drop down. How do |! clear? Yeah. Okay. Yeah, you got it. Perfect. Good to hear. Yeah, so evals area way to unit test your skills basically. And actually in Pstack, we ship under potato

**[3:09:04]** mode, there's a playbook if you search for it called eval playbook. And it's like not... It's actually pretty rigorous the way it's done. But essentially what I do is I spawn a lot of different sub-agents. I have my main coordinator agent come up with a rubric for what I want the skill to do. these sub-agents and it creates individual directories for them which are cleverly named to

**[3:09:35]** not let the sub-agents know that it's being evaluated. Because agents can actually tell and when they do, they change their behavior. of stuff like that to essentially... Yeah, like test whether or not the skill I'm making or changing is actually doing what I think it does. And one of the really nice things about Cursor is that we support so many different models. So you can actually eval your skill across all sorts of different models and get

**[3:10:06]** a sense of how well it performs across that different matrix, especially for the models that you use. lot. Every time I modify a skill, I will run one of these, like the email playbook and make sure that it's actually leading to a result |! want. But I will say like maintaining skills is actually pretty hard. It requires, I think, a lot of taste and observation. So you kind of need to be very good at being a backseat driver. You

**[3:10:39]** if you've ever done pair programming, for example, and you watch a co-worker code and you just like... you could probably do this better. You know, you could do... you know, like why did you not do this, right? You ask a lot of questions to your co-worker. And it's kind of a similar thing here. You like... you don't want to just bea passive observer of the agent. You want to be very in the driver's seat in the initial stages when you're building up your own set of skills. You know, obviously you can use something like PSAC, but if you're building your own set of skills, it's very... I think, you know, opening up all the tool calls and like reading the code

**[3:11:11]** reading all the agent behavior and their thinking blocks is a really great way to see where they fail, right? Like what... you know, where are they being done? And then you can go and build a skill for that. And then with verification, how you trust It Is... It's... think it's alsoa very similar iteration loop, where, you know, like I actually did the same process for verifying the verification skill, where I actually get... So one thing that's interesting about evals is that you can sort of hill climb

**[3:11:41]** them, meaning that your eval can produce a score, right? A score that you can get your coordinator to produce, but also you can have a judge agent of a different model to kind of cross-reference and make sure that the first model is not being biased, right? The model that's judging all of the sub-agents that are running the thing. But you can also like hill climb. So meaning that you can use like slash loop in cursor and you can say, okay, keep looping on this eval, right? Until

**[3:12:12]** everything is 10 out of 10, as an example. And I did the same... basically the same approach with the control skill. And so i kind of... it was very... it was very hands-off actually. So, you know, l... I that skill that way, like the CLI in that skill. And over time, it's gotten really good. But yeah, it was definitely not super smooth at the beginning. It required a lot of iteration. And I think there's an analogy here for me, which IS... Well, I make this analogy later in a different slide

**[3:12:44]** on my drawing here. But I think of it You know, as a... as a engineer now, you're sort of more like... Like maybe a manager or... The analogy I like is like you're like a chef ina restaurant. You're the head chef. You're not cooking all the food yourself anymore. You have a team of cooks, right? You have line cooks, you have a sous chef, you have all these different stations. really design the environment. You know, you're in charge of setting up the kitchen. You're

**[3:13:14]** in charge of, you know, like giving tasks to different people. Yeah, it's a very interesting way of working. But yeah, that's how I basically built these verification skills. Yeah. Just one fault there. I'm like... Mm-hmm. I'm like, I'm going to try to go one layer deeper. So are you... Let's say we wanted to build an eval ora skill for something and we wanted to kind of get better on its own, which is what I think you're suggesting. Are you doing that in like a

**[3:13:44]** work tree, kind of isolated with like the sub-agents and then the reviewer agent and all that? Is it happening like in some type of cloud-hosted environment? Like what's the practical steps? If I wanted to go do this and like set up a verification system for something, what would do or where would start? I think that the best place to start is local because you can observe. You can definitely observe what your agents are doing. So if you're building a verification skill for yourself, I would definitely start local and just

**[3:14:15]** have your agent bring up the application, whether it's like a CLI or a desktop app or whatever. And so you can actually observe, right? You can see how the agent is interacting with the application. You can see it, you know, how it calls like the different APIs that allow it to interact with the application. But for me personally, I have basically been kind of all in, mostly alt in on cloud agents because they're extremely powerful.

**[3:14:46]** And the really powerful thing about cursor Is the cloud agents actually, where if you spend a little bit of time setting up your environment, these control skills, these verification skills pay a huge amount of dividends because it's not just something that makes you as a single engineer better. It actually levels up your whole team and even your whole company, because you can actually start thinking about cloud agents. You can start thinking about automations that automatically do things like I'll get to. kind of talk about

**[3:15:17]** this a bit later, but I'l just kind of get into it where, you know, for example, like I talk a lot about this agent. we have called Benny, right? Who, you know, who takes all of the bug reports that we get and automatically goes Off in the cloud, opens upa cloud. It's desktop. It runs cursor in its own computer and it uses the same control skills to interact with the application and try to reproduce the bug or the user report. Right. And this Is so, so powerful because at once

**[3:15:48]** Ican immediately, I set. so much information from this automatically. Like here in this example, you can see that. the Benny actually reproduced the bug, but it's already fixed on main. So it actually confirms that we fixed this. problem already. And allt need to do is just release another build of of cursor. So that's like huge. information there that I didn't have to go off and sit with an agent, you know, and spend an hour. trying to fit like, is this fixed? Is this not fixed? So you you _ . gain back so much time. But, you know, everybody on

**[3:16:18]** my team benefits from this. Everybody in the company benefits from this. So definitely think that, you know, keeping these using cloud agents is super powerful. But, yeah, it’s like a journey. You have to © trust it first. Right. Before you you get to this point. And that's it goes back to what I was saying here where, you know, it's very hard. It's almost. impossible. And I would definitely encourage you not to try to jump from, you know, like if you're still in this zone, you don't want to jump to like I'm going to spawna hundred

**[3:16:48]** or thousands of cloud agents right now because you're just. going to waste a lot of tokens and it's going to be extremely expensive. Yeah. So just to kind of recap so far, basically, if we wanted to go on the journey that you've kind of gone on, It would be to start with verification, building some some skills and some some ways of determining that the agents are producing at least like correct code. Whether like you said, whether it's good code or not is maybe a separate question. But like It's It's technically solving the problem by looking at, you know, stack traces, looking at, you know, the actual behavior in the

**[3:17:18]** app. And so on. And then once we trust it locally, then we can start to think about scaling into the cloud and running more agents that are picking up signals, I guess, on their own. Right. So whether that's like a bug report that comes in or something, they can go and pick it up and solve the problem and give us back a PR. And then maybe the last step is like auto merging the PRs, which Is where you're at. Maybe not where everyone is at. Yeah. Yeah. Maybe not where you're

**[3:18:19]** at. You're at the same time. Maybe not where you're

**[3:19:28]** at. One of the most controversial topics in the industry, I think, is like, should you rewrite your app or not? Because I think engineers are very prone to this where, especially when you join a company, you come in and you see like the code base and you're like, oh man, this ts shit. Like who wrote this code? You know, it's terrible. I want to rewrite the whole thing. There is a very common inclination. I think a lot of, you know, before agents and I guess arguably even now, people will definitely discourage you from rewriting stuff. But I'm actually here to

**[3:19:58]** make a case for why you might want to consider it. Because I think it really depends. You know, brownfield applications, I think, are actually in a pretty good spot, especially if they're set up well already. And like recently I've been talking to some people, but, you know, I was just observing, I just noticed this parallel, which is that a lot of big tech company problems are now everybody's problems. And the big tech company problem, you know,

**[3:20:29]** like when I was working at Meta, like we had this giant monorepo. We had like, I don't know, tens of thousands of engineers just, you know, like banging on their keyboards and shipping code. And a lot of really great engineers at Meta. But I'll say like, you know, you'll be surprised that the code quality is actually not that good. And so! often joke that like, you know, before AI sloth, we had human sloth. And so, you know, I think a lot of big tech info, like what Meta has or

**[3:20:59]** Google, you know, really big tech companies are actually designed for that, where you're sort of like you're catering to the, you know, like, this sounds so bad to say, but like the least capable engineer on your team. Right. You build frameworks, you build conventions, you build guardrails, you know, you restrict credentials so that, you know, your intern doesn't wipe your production database. There's, you know, if you have that level of infra already, I think your agents can actually already doa very solid job. Right. Right.

**[3:21:31]** Because they have the guardrails are already in place for agents to not cause havoc or not cause too much havoc in your code base. And you can always add more, you know, guardrails. But think like Greenfield applications, especially are, you know, like the brand new applications are like the biggest risk in my opinion, and also the greatest opportunity. Because, you know, if you vibe code a project, a prototype, like we did for Grokbot, you know, Grokbot was spun up very, very, very quickly. And if you

**[3:22:02]** haven't heard of Grokbot, it's like our new application we just launched yesterday. It's really cool. Let's you orchestrate your, create like individual agents that have their own identity and you can kind of orchestrate them. It's super cool. Definitely check it out. But yeah, it was like a very, it was a very Greenfield application, like most prototypes are. So it was like vibe coded very quickly. Humans were not reading the code at all. And I had this tweet recently where I said something about organic architecture. Maybe

**[3:22:34]** rll find it. But the idea is that when you have a completely vibe coded application, you essentially have no guardrails whatsoever. So your agents, when you give thema task, they will just solve it in whatever method is the most convenient. And over time you get into this situation where you have a code base that Is spiraling out of control. Because you don't understand it. Because you don't understand it. Your agents understand it, I guess, in

**[3:23:04]** a way. But like they've built something that is, vou know, optimized for short, for shortcuts. And vou know, it will, you will suffer. You have a lot of issues with that application. So I think starting your code base with like very strong constraints is very much needed. Because like when you have a code base that you can trust, right? When you have guardrails that actually help you, help your agents write good code, you can get into

**[3:23:35]** the, you know, like into this part of the curve where I, where I, like said, you know, I woke up today and I had like 20 PRs merged by my agents. And that's because I invested a lot of time, over 600 PRs. calculated yesterday when I refactored all of GropBot to this new architecture that I've been building. And yeah, I've gotten to a point where don't really look, I really don't look at the that not just, you know,

**[3:24:06]** to sell you tokens, but because I, you know, it took a lot of work to get to that point. I spent a lot of tokens to get the code base to this point where I no longer have to look at it. Uh, but I'm very excited because. You know, the potential where, you know, it's not just, this doesn't just benefit me. It benefits everyone contributing to GropBot. : And it also empowers, you know, designers and product managers and, you know, people, even GTM people to add features to GropBot. And I don't have to worry, you know, don't have to wake

**[3:24:36]** up at night in the middle of the night and worry about, oh shit, someone's Richt. I have a ton of constraints and Cl. I was like, it's actually very annoying to write code in, in GropBot, but like agents absorb all of that annoyance. Um, but yeah, I'm happy to talk about what exactly : that is. Um, yeah, I think one question, um, before we get into the, this part here is just around that element of like what your, your, your Cl looks like, or maybe some of the constraints, and then also like the average PR size.

**[3:25:06]** Tsaw a question about that earlier, just to give of a glance. It doesn't have to be like mathematically average, but just, uh, you know, like what generally the size of the PRis, um, if it's only a couple of lines of code or, you know, um, yeah. um, i think it depends ion me. I'm trying to do thisina way where I'm not gonna like, you, yeah, you don't have to share the actual number of you, like the actual average. Uh, I think this is fine. Benchmark. Benchmark. But like we have, so, okay, this is not that interesting,

**[3:25:36]** but, uh, well, fun fact is that virtualization in GrokBot and in, uh, cursor is actually powered by, uh, Pretext, uh, which is a sort of new library that someone's built. Um, that's really interesting. You should, you should check it out, but that's not really that important. Uh, I think the average PR size, actually don't know. I don't know if I want to click on these. Uh, probably can, but I would say like they can range anywhere from a few hundred lines or 50 lines to like a thousand, depending

**[3:26:08]** on what the thing is doing. Uh, so like here I'm not here like deleting a bunch of files. So expect that it's just, but veah, it, it kind of varies. There's no like, yeah. There's no like hard cap or hard limit. They're all like 50 line PRs. There's no hard cap. There's definitely no hard cap, but do encourage my agents to split up their work into multiple PRs. Uh, I do that mostly because, uh, like, I like the idea of the, I guess maybe this is much harder to do now as in the world of agents and you have like so many

**[3:26:38]** commits, but I like the idea that, you know, the Git history is a very rich source of context. Uh, and I like the, I like each PR to sort of atomically describe what that small piece of thing is doing, which also makes it easier for me to revert changes and like figure out, you know, oh, I shipped a bug and it's just, it's here. Right. It's not in this 40,000 line PR where who knows what landed in there. Uh, but |, don't have a hard cap on PR size. Cool. And then, um, yeah, also

**[3:27:09]** quick question on like Cl. So again, you don't have to go into like, uh, the screen share of like your Cl does, but just generally would you describe what the Cl kind of looks tike, uh, or how strict it is? Uh, yeah. So, uh, well specifically for Grokbot. So Dune is the, it's the sort of cheeky code, code I name for the architecture that we've built for Grokbot. Um, the CI looks pretty annoying because there's checks for everything. So like literally I have, um, uh, well, if you've written any react, for

**[3:27:40]** example, you know, you know that one of the biggest foot guns in React is use effect. Uh, so in, uh, Dune and in Grokbot, we've banned use effect. So Dune Is just the, the mental model of what Dune is. Uh, you can kind of think of it as like next JS for, uh, electron apps and it's designed for agents to write. Uh, and it's like custom for, you know, our agent powered applications. Um, so the Cl checks are very like specific to that. Like, you know, don't use use effect. It's,

**[3:28:10]** it's, it's banned. Like Cl will fail, uh, and yell at you. We have like some of the more interesting ones that people might raise eyebrows Is like, I actually ban code comments as well. Uh, which is very interesting. Um, but I've noticed that 99% of the time agents just write code comments that kind of describe some historical thing that is actually totally irrelevant to the code. Um, like it will often say like, you know, oh, Lauren said you should never do this. And it's now in the, in a code comment. Like what? Like why? What? That was, I didn't say

**[3:28:41]** that as like a durable, you know, global rule. I PR sucks and you should change that part. Uh, agents don't really understand us that ! well, surprisingly. Uh, and, or they kind of assume too much and they kind of do things in like very stupid ways. So like, yeah, we just ban everything. Everything you can imagine like the agents are bad at, we ban. Uh, so one example that we actually suffer a lot in the agents window is we have, uh, you know, if you've used agents

**[3:29:12]** window, you've definitely seen performance I issues and you know, we're constantly trying to fix them. Uh, but it's like a, it's a never ending struggle because there's so many pull requests that get merged. Any one of them could just regress performance or stability or reliability. Uh, you know, the agents window doesn't have this architecture yet. I plan to do bring this learning back there and kind of refactor everything there. Uh, but, uh, it just regresses super often, uh, because, uh, there's just one example is like, we have very poor, um, isolation

**[3:29:43]** between processes. So like on, you know, on, on electron, you have a renderer thread that renders your UI, but you also have like a run other code that, you know, doesn't need to block the renderer. Um, but we do a poor job of separating those things. And so oftentimes you just accidentally have code that gets pulled into running on the renderer thread. And then all of a sudden you're competing with the, the renderer that, you know, that has a very, if you want like 60 FPS, you have to, every frame that gets drawn has to be done in 16 milliseconds.

**[3:30:15]** So verv, verv small, vou know, deadline per frame. Uh, if you want, you know, a very smooth product. Uh, and when you start building, bringing in, accidentally bringing in, you know, things that are ! like very computationally heavy, or they have a lot of 10, uh, then you just get into like a lot your FPS really drops. You start, uh, you know, losing frames. You get long tasks that take more than 16 milliseconds. And then you just get this really choppy experience. So all of those patterns that we've learned basically building electron apps, we've encoded into

**[3:30:46]** this framework and it becomes like a hard failure. So literally, in, in GrokBot, we literally have a directory called electron main, electron renderer. And we have, uh, import, uh, Cl, I Suess, where we actually check the dependency graph to make sure you're not accidentally importing code from one directory to another. Uh, so that's enforced by Cl, um, as well as bug bots, uh, which is our, which cursor's, um, like code review tool that runs on Cl, uh, you know, in

**[3:31:17]** our agents MD, it's everywhere. Like, so I, I, I, um, I have this thing here where I talk about like, um, you know, like there are multiple layers, I think for building a good code base. Uh, obviously the code base Is one where, uh, if you have an architecture like this, where it's extremely strict, uh, you know, the, the, the way to build features is very conventional. That's like the strongest, strongest level of enforcement because agents patterns. So, uh, one example of this in GrokBot is

**[3:31:48]** like, we have this, these concepts called like a feature and we have entry points and transcript cards. Like, oh, you know, the cards that you see in the chat. Like, these are all like, like nouns, I guess, in, in the framework. And so there's a very conventional way of creating them. And so like a feature is allin a, in a single directory as an example. And so all of the code that contributes to that feature lives in one directory. So it's all co-located in one place. Makes it super easy. You know, agents don't have to like, uh, grab around and try to figure out like where all

**[3:32:19]** the things are. It just looks at the feature and like, oh, okay, I'm working on the onboarding feature in GrokBot. Uh, I'm just going to work in this directory. And for 80% of the work, it's mostly just very encapsulated there. But, uh, like, it's like very, it's like design again for, you know, like the dumbest agent. Like you don't have to think, right? The, the, the, one of the key principles I have for this framework ts like the shortest, the shortest path is the best path. So, uh, because that plays

**[3:32:49]** exactly to how agents love. to write goals. Like they like to take shortcuts really, vou know, they'tl find the quickest wav to solve the problem. So why not make I that the best way to solve the problem? Uh, so. get into all the specific details. Um, and, uh, the, the, this framework's really more of a collection of ideas and principles rather than something that will open source. Uh, you can, you can, you know, screenshot this, I guess, tell your agent to, uh, do some, build, build something ; like this for you too.

**[3:33:21]** um, yeah, but it's really. all about the layers. Uh, you know, like the, the code base is one part with features, uh, and directories and, you know, import, uh, blocking import dependencies, uh, that shouldn't be imported. Uh, but, and, and it all enforces that and static analysis. So like, uh, uh, there's Cl checks. We have a lot of lints for bad patterns that we observe, uh, compiler diagnostics. Uh, there's also rules and bug bot, which are, um, I think like three, four, five are more soft,

**[3:33:52]** right? These two actually make, make Cl read, right? So that, you know, there's a hard constraint where the agent can just write crappy code. For rules and skills and bug bot, your agents can still forget, right? You can still, or it may not always consistently apply them. So but I don't, I don't like to rely on them as the only source of enforcement because it's very, very soft, right? And if you, if you only have rules

**[3:34:22]** and bug bot and skills and a style suide for your code, you will, it's only a matter of time 4 before your code base looks like complete trash. I'm sorry to say that, but, uh, I definitely recommend, veah, like, you know, investing in, you know, things that can be hard and forced, right? And this is why, you know, maybe, uh, the choice of tech stack that you use Is also very important. Um, like, I think for example, Rust is sort of making, you know, it's like getting super popular again, uh, because the compiler is so strict, right? The compiler enforces

**[3:34:54]** so manv different things. You know, there's a borrow checker that you have to appease. And if, as long as you make sure your agents ! don't write unsafe code blocks, uh, you can more or less feel somewhat confident that if the code compiles, it's probably works and it's good. Uh, but you'll see, it gives you that level of trust and confidence that you as a human engineer no longer need to go and check it yourself. You know, you, you rely on code and static analysis to actually make that, uh, a lot smoother.

**[3:35:25]** Um, and I guess the worst part, the worst place to be in is if a are stuck in code review land where you actually the invariance in your code base by literally the human person saying, you know, reading B the code and like, okay, you should not do this. Right. Every time you have to that as a code smell, like a, uh, anti pattern. And vou should say, okay, instead of me commenting on the PR, how do I . turn this into a hard rule? Right. How do I turn this into a lint rule? How do I turn

**[3:35:55]** this into a Cl failure? Or how do I even categorically eliminate this problem, uh, entirely? about another migration I've done, but rll probably pause here. Yeah. I feel like that's, that's where I am. Um, to be honest is, is what you're describing right now, which Is that like, I don't have all of these rules. Uh, so I have some things to go do after this session, uh, in terms of being able to scale my agents. I'm, I'm definitely on like the, uh, you know, maybe a couple of parallel ones locally stage, like two to three locally. And I'm sure most people here are on the same.

**[3:36:26]** So, uh, yeah, I know we only have a couple minutes left. Uh, Lauren, was there anything else that you wanted to, to highlight? I obviously there's lots of questions so I can grab more, but I want to give you a few minutes. Uh, if there's anything else you want to talk about. Weil, think I've been yapping for quite a lot. So I'm maybe let's just do questions. Okay, cool. Uh, one question that had a couple of, uh, came up a couple of times was just around like token usage. So the question Is like, Is, Is what you're describing a realistic thing for people who are on, you know, uh, a normal set of token usage. They don't have, you know, basically unlimited tokens, uh, to

**[3:36:57]** work with. think that's a really good point. I mean, like, obviously, you know, I work at an AI lab where we have unlimited tokens. So, uh, I definitely cannot say that, you know, this is something everyone should do in the exact same way that I did it. I think this point without, you know, breaking the bank. you know, you're, you're, you have a startup that you lead. Um, I think to me it's a question of ROL. Um, and it's like, uh,

**[3:37:28]** yes, you spend a lot of money on tokens in the upfront stage. You know, like refactoring your code base is going to takea lot of tokens. Uh, adding all these things, uh, is going to take a bunch of tokens. But if we're heading to a world where agents are writing all the code and, you know, you want to be very lean, right? You don't want to have to hire. You don't want to become like meta, right? Like, mean, like in terms of, you don't want to become a 10,000 person engineering org, because, I mean, that's a cool problem to have. But also, you know, you

**[3:37:58]** have so much overhead. There's like planning, you know, like it's, It's, uh, personally, I wouldn't, uh, it's not super fun. But, um, I think you want to stay very nimble, right? And you want to, you want to be like agents are all about allowing you to do things that you couldn't do before. That's really to me, like the value of agents. You tokens on every single little thing. But, um, to me, like the thing I couldn't do before is like enforce this level of constraints in a code base by myself.

**[3:38:29]** Right? Like I'm just a single person. You know, uh, it would have taken me years to build this framework, uh, and do all the refactoring and test everything myself and verify, you know, like run. Imagine if there, it was just me, right? No, in, in pre-agent era, just like running, you know, it would take me so long. Right? And my salary Is misht have is iust then. you know, like what is, there's a trade-off of, do you hire someone to do

**[3:38:59]** this? Or do you spend the tokens to set up a code base so that even the, the most naive, right, the dumbest agents can do a good job? And when you actually get to this point, like even agents that are not, you know, fable size do an excellent job of writing code. And this pays a lot of dividends as well for me personally, where I've empowered not just mvself, but again, like PMs, designers, engineers who to just contribute ina way that is sustainable.

**[3:39:34]** sure. You know, like nothing is like free for sure. And tokens are pretty expensive. But, oh, actually, I don't know how many of you have seen this, but we So, yeah, Grok 4.6 would be like a great, it was very, very smart. It’s really good on the, on the benchmarks. And it's the same, the tokens, well, I hopefully I'm believe the cost per token is the same as

**[3:40:06]** more intelligence for the same cost. think this is an area that cursor tries to, cursor and SpaceX AI try that pareto frontier of, you know, cost versus intelligence. You know, we don't necessarily want to build the biggest model ever because that Is extremely expensive to run. It's really about, like, how do you find that sweet spot, right? You don't needa giant model, but it's just super smart, right? And it's not very expensive for inference. But, yeah, I think to kind of round it up,

**[3:40:37]** think it's like a, it's, it's, there's a, if you do your own analysis, feel like it's pretty positive. It'll be pretty positive that the ROI you get from investing in stuff like this but your whole team to be so much more productive. Right, like imagine if you have an army of engineers like me who are shipping so much improvements and bug fixes, you know, every day, right? Like that is pretty exciting. Cool. One last question before

**[3:41:08]** we wrap up. This one is for the people in product on the, on the call. So let's say we do have an army of engineers who are shipping like Lauren. I'm just curious, like, how Is the product team or other functions of your company keeping up given that, like, if you're shipping so quickly, have, are they using AI more to do their jobs? Like, as much as you can speak to that, know, obviously, you don't have, like, you're not in that role, but just curious about how that works. GroffBot has been actually exceedingly powerful. Where, so before GroffBot, like, you know, obviously cursor only

**[3:41:39]** had cursor, like we onlv had agents window. We had a CLI, we had an IDE, and these are really like power user tools, right? They're designed for developers. So it's very, very developer centric. You can do knowledge work in them, but like the Ul is not really optimized for that. So we actually didn't really have, well, I think like a lot of people in like, you know, GTM product, like they might have used cursor. So they're not really, like, they're not really, really, really excited for that. So they're not really excited for

**[3:42:09]** that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So they're not really excited for that. So thev're not really excited for that. So they're not really excited for that. So they're not really excited for that. You can have you can kind of do orchestration in a very, like, natural way where you can sort of, you know, each agent is like a person. And now you've got a team of agents like

**[3:42:39]** working on. You have one one agent per account that you manage, as an example. Or if you're a PM, you have, you know, you can have an agent that summarizes all the work that Lauren did last night. And then now you know what did. Right. So I think our PMs are leveraging that a lot and they're shipping code too. So, you know, oftentimes they will just say, oh, here's a bug. fixed it. Can you look at it? And then I'll go review it. And actually it's just perfect. I'm like, okay, stamp. So I think that shows that, you know, the Dune architecture is holding up. Right. The all ; the really strict constraints allow

**[3:43:11]** people who are not experts in engineering to contribute at a high level. So I feel like I'm already seeing that pay off a lot : where, you know, designers and PMs are just able to ship features directly. And that just makes the GrokBot team super fast. Right. Where we can ship so quickly. And we have a lot planned. So I'm very excited to, you know, to ship more stuff.
