---
title: "Part 6: Scheduled Automation — Routine Work That Runs Without Reminders"
date: 2026-11-12
slug: scheduled-automation-agent
lang: en
pair: otomasi-terjadwal
excerpt: "An agent wired to your data still waits to be told. This part installs the clock: routine jobs that run on their own every morning, every Friday, and at the end of each month."
tags: [tutorial, ai-agent, automation, productivity]
draft: false
series: setup-ai-agent
series_title: Setting Up Your Own AI Assistant, Step by Step
part: 6
---

In part five the agent learned to open files, read a calendar, and search the archive. Useful, with one flaw: it only moves when you speak first. Forget to ask and nothing happens. Disappear for three days and three days pass with no recap.

This part puts a clock inside it. No exotic new ability; every ingredient was built earlier. What changes is the trigger — no longer your message, but a schedule.

## Chat waits, a schedule doesn't

A conversation is reactive: you need something, you ask, it answers, done. Pleasant, but the whole list of what should get done stays in your head. Fill that head up and something slips.

A schedule moves part of the list into the machine. You decide once, the machine repeats it. For work with the same shape every week, that beats good intentions.

## What earns a slot

Simple test: repeated work, short answer, no big decision. If every run needs hard thinking, it isn't ready to be automated — keep doing it yourself.

Three that usually pay off right away:

- A morning brief: today's agenda, the next event coming up, the small items still open.
- A reminder before an event, two days ahead, while there is still time to fix the preparation.
- A Friday afternoon recap: what finished, what stalled, what is waiting on someone else.

## Five columns, that's all

Behind the name "cron" sit five columns: minute, hour, day of month, month, day of week. `0 5 * * *` means five in the morning, every day. `30 19 * * 5` means Friday at half past seven in the evening. An asterisk means "any".

You don't have to memorise it. One thing matters: the hour you write is the machine's hour, not your office wall clock. If the machine sits in another timezone, the morning brief lands at midnight. Fix the timezone first, then trust the schedule.

## A scheduled job remembers nothing

Here is where results usually disappoint. Every time the schedule fires, the agent starts from zero. It has no memory of yesterday's conversation, no idea the same report went out last week.

So write the brief in full: the context, where the material lives, the shape of the output, and what to do when there is no material. Picture instructions for someone who walked in five minutes ago. A line like "continue what we did yesterday" means nothing here.

## Silence beats noise

A job that messages you every time it runs gets ignored within a week. Alerts with nothing to act on teach people to stop reading alerts.

A healthier pattern: report only when something needs a look. When everything is normal, no message. But silence must be distinguishable from broken. Have the job record that it ran, and say so clearly when it fails — not go quiet because an error slipped past.

## Run it by hand first

Before handing work to a schedule, call it manually and check the result. Twice or three times, at different hours, with different material. Once the output looks right, attach the schedule.

For the first month, keep it to jobs that read and summarise. Jobs that message many people, change data, or delete something wait until you trust the pattern. Watch for collisions: two jobs firing in the same minute can step on each other.

At this point the agent moves on its own, and it still forgets. Part seven is about memory — getting the agent to record what it has already done, so tomorrow's brief doesn't repeat today's.
