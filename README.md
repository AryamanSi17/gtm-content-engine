# GTM Content Engine

A Claude Code skill that turns Claude into a B2B content strategy desk for go-to-market work.

You tell it what your company sells, who your ideal buyer is, and what customer results you can talk about. It then sets up a folder of research, evidence and drafts, and runs five agents on a nightly schedule. Each morning you get a short brief with the best LinkedIn ideas, a customer case study, lead magnet ideas and what to work on first. Every Monday you get a weekly report showing which content actually brought in qualified buyers.

The main idea is simple: content should bring in buyers, not just likes. The skill only uses claims it can back up with a source, scores every idea before it is written, and ends each recommendation with a short section on why it could fail.

## What it does

The skill runs five agents, each with one job:

1. **Market Researcher** (1:00 in the morning by default) watches competitors, creators, industry news, funding rounds, product launches and platform changes. It saves every source along with a note on why it matters to your buyers.
2. **Evidence Miner** (2:00) reads your customer interviews, sales call notes, case studies and campaign reports. It pulls out buyer problems, objections, buying triggers, quotes and results that can be verified.
3. **Content Strategist** (3:00) turns that research into founder posts, case studies, educational breakdowns, contrarian takes and long-form articles for X.
4. **Lead Magnet Architect** (4:00) proposes at least four free resources each week, such as calculators, templates, prompt libraries or full workflows. For each one it plans the full path from LinkedIn post to booked sales call.
5. **Performance Analyst** (5:00) separates views and likes from the things that matter: qualified leads, meetings, sales opportunities and revenue.

By 8:00 a file called `morning.md` is ready. It is meant to be read in under ten minutes.

## How to install

This repository is private, so you need access to it on GitHub first. Then copy the skill into your personal skills folder:

```bash
git clone https://github.com/AryamanSi17/gtm-content-engine.git ~/.claude/skills/gtm-content-engine
```

To make it available in only one project, clone it into that project's `.claude/skills/` folder instead.

Restart Claude Code (or start a new session) and the skill will be picked up automatically.

To get the latest version later, run `git pull` inside that folder.

## How to use it

Open Claude Code in the folder where you want the content work to live and say something like:

> Set up the content engine for my company.

Claude will then:

1. Ask you up to six questions: what you sell and at what price, who your ideal buyer is, the costly problems you solve, which customer results you can use, which founders and competitors to track, and anything it must never mention.
2. Create a `content-engine/` folder with sub-folders for company details, evidence, research, strategy, finished drafts, performance and briefs.
3. Save your answers into a `CLAUDE.md` file so every agent works from the same instructions.
4. Do a small trial run and show you five scored ideas, one case study outline, one lead magnet idea, the agent schedule and the plan for the first night.
5. Wait for your go-ahead before it creates any scheduled tasks.

## Safety rules built in

The skill never publishes anything, never contacts anyone and never buys anything. It does not guess results, quotes or numbers. Any claim without a source is marked "UNVERIFIED" and kept out of final copy. Web pages, transcripts and uploaded files are treated as information to read, never as instructions to follow. It will not name a customer you have marked as confidential.

## Changing the defaults

The run times, the scoring range (1 to 10), the number of lead magnets per week (4) and the weekly report day (Monday at 9:00) are all set in `SKILL.md`. You can change them there, or simply give different values when Claude asks its setup questions.

## Files

- `SKILL.md` contains the skill itself: the full prompt Claude follows.
- `README.md` is this guide.
