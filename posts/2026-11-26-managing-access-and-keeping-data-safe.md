---
title: "Part 7: Setting Access — Who Gets to Command the Agent, and What It Must Not Touch"
date: 2026-11-26
slug: managing-access-and-keeping-data-safe
lang: en
pair: akses-dan-keamanan
excerpt: "An agent that runs by itself every morning needs fences: who may give it orders, which keys it may hold, and which parts it must leave alone."
tags: [tutorial, ai-agent, security, access]
draft: false
series: setup-ai-agent
series_title: Setting Up Your Own AI Assistant, Step by Step
part: 7
---

Part six closed with a promise to talk about memory. Before that, something more urgent: who may give the agent orders, and how far those orders reach.

By part six the agent moves on its own every morning. It opens files, reads a calendar, sends a brief. While that stays on your desk, a small mistake costs one annoying afternoon. Once it runs unattended and holds keys to a few apps, a small mistake travels.

This part is about fences. Not ones that make the agent stupid, but ones that let you leave it working without watching your phone.

## Start with who gets to talk

Cheapest step, most often skipped. An agent in a chat channel answers anyone who knows its address. Narrow it to senders you recognise: one or two people, not the whole office group.

If several people need it, split channels by purpose. Private conversations don't belong in a shared channel, where anyone inside can read the history.

## One key per job

An agent that opens notes, calendars, and an archive holds several keys. The temptation is one big key for speed. Don't.

Make a separate key per app, and keep it narrow. Reading only? A read-only key. A key that can change and delete is for jobs that demand it, and even then don't let two apps share it.

Keep keys in a settings file only the machine can read, not in the instruction text. A key pasted into chat lands in the history, and history outlives good intentions.

## Give it a desk, not the house

You wouldn't hand a new assistant every drawer in the building on day one. Point the agent at one folder. If it needs another, let it ask.

Put a file outside that folder, then ask the agent to open it. A well-fenced agent says it can't. One that cheerfully reads it tells you the fence lives in your imagination, not the settings.

## Three things that ask first

Some actions deserve a pause even when the agent is sure:

- Deleting a file permanently.
- Messaging a large group.
- Changing records that involve money.

Route those to you for a yes first. "Let me know when it's done" isn't enough — a real person has to answer.

## Other people's data isn't chat material

Messages from members, complaints, contact details — all of it passes through the agent. Two habits keep that tidy: no personal details in a group channel, and no raw conversations sitting around longer than needed.

When a case needs discussing, use initials and the gist. The logs sit on a machine that keeps copies of many things, including what you forgot it saw.

## When a key leaks

Sooner or later a key lands where it shouldn't. Plan the response now: revoke the old one, issue a new one, then read the activity log for anything you never ordered.

Five minutes beats a week of hoping nobody noticed. Write the steps down for a bad day, when you won't want to think.

## Test it with a rude question

Once a month, ask the agent what it can reach and what it can't. Then check by hand: open the working folder, count the keys, see which apps are connected.

An agent that can name its own limits is easier to trust than one that answers everything confidently.

Part eight turns to the other side of the same coin: checking the agent's work. A tidy brief can still be wrong, and the next part shows how to catch it first.
