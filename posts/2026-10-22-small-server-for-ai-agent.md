---
title: "Part 3: Setting Up a Place to Run Your Agent (a Small Server)"
date: 2026-10-22
slug: small-server-for-ai-agent
lang: en
pair: tempat-ngajalankeun-agen
excerpt: "An agent that only lives while your laptop is open will not help much. This part is about where it lives: how small a server is enough, and how to keep it from dying."
tags: [tutorial, server, ai-agent]
draft: false
series: setup-ai-agent
series_title: Setting Up Your Own AI Assistant, Step by Step
part: 3
---

In part one we mapped the five pieces that make up an assistant, and in part two we picked the thinking engine. Now comes the step most people postpone: where the thing actually lives.

The reason is plain. An agent that only runs while your laptop is open will never be reliable for the jobs that matter most — answering a message at five in the morning, preparing notes before a meeting, or sending a reminder about tonight's schedule while you are on the road.

## It has to stay awake

An assistant works because it waits. A message arrives and it has to be there to read it. A job is scheduled for early morning and the machine has to be running at that hour. So what you are shopping for is not speed. It is a computer that hardly ever dies.

## You do not need an expensive machine

The language model runs somewhere else, rented from a provider, so your server is mostly a courier: it receives messages, assembles the material, calls the model, and sends the reply back. Two processor cores and a couple of gigabytes of memory are enough for that. A graphics card is not part of the picture.

The choices are ordinary: an old laptop nobody uses anymore, a small computer at home, a single-board computer, or the smallest monthly cloud server. The last one is the least fuss — no cables, no worry when the power drops, reachable from anywhere. The trade-off is that you rent instead of own, and you still have to watch it.

## Start smaller than you think

Take the cheapest plan for a month or two. If it turns out to be enough, you can grow later. Plenty of people overbuy at the start because they imagine a workload that never shows up.

What matters more than size: run Linux, since nearly every guide assumes it; get in with an SSH key rather than a phrase you type from memory; and let the system install its security updates on a routine.

## Keep it alive on its own

Anything started by hand dies the moment the terminal closes, or the moment the machine restarts. The fix is one small thing: register the agent as a system service, so it comes back up with the server and gets restarted when it stops.

Add a simple check as well — a test message every morning, or an alert when nothing is heard for a whole day. A quiet assistant is usually not busy. It has probably been dead since yesterday.

## Two things people forget

First, backups. Keep notes, rules, and task lists somewhere you can restore from. A small server can fail, and the annoying part is not the hardware, it is the habits you lose along with it.

Second, the small monthly costs: the server rent, electricity if it sits at home, and model usage. None of them is large, but writing them down early spares you a surprise later.

A small server is not about hardware that looks impressive. It is about the promise that the assistant is there when you call.

Next part: wiring up the working tools — so the agent can read files, search the web, and send messages.
