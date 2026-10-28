---
title: "Part 4: Installing the Agent and Wiring It to a Channel"
date: 2026-10-29
slug: installing-the-agent-and-wiring-a-channel
lang: en
pair: pasang-agen-sambung-kanal
excerpt: "An agent humming away on a server is still a stranger to everyone. This part covers installing it, creating a Telegram bot, setting up a WhatsApp number, and keeping the front door tidy."
tags: [tutorial, ai-agent, telegram, whatsapp]
draft: false
series: setup-ai-agent
series_title: Setting Up Your Own AI Assistant, Step by Step
part: 4
---

Part three sorted out the house: a small server that stays on, the agent registered as a service, a daily check for when it dies. But an agent living without a number is like a clean room with no door. Tidy, ready, and nobody can knock.

The channel is that door. Not a new app people must download, but the place they already chat every day. Two names cover almost everything: Telegram and WhatsApp.

## Install first, connect second

People flip the order, then get stuck. Get the agent answering in the terminal first, then wire the channel. Do both at once and something breaks, you won't know which half.

Install it on last week's server, run it as a service, keep every setting in one config file. The file holding private values stays readable by its owner only and never sits in a folder pushed to a public repository.

One agent process can serve several channels. Don't build one per channel because it feels tidier — you end up with double rules to keep in sync.

## Telegram: fastest to live

A bot comes from one official account inside the app: follow a short conversation, get a bot key. Keep that key in the config file, never in the code, never pasted into a group chat for someone to check.

Two things get forgotten once the bot is alive. First, a list of who may give orders — user ids you trust, not everyone who finds the bot. Second, test with real messages: say hello, ask something you already know, then send a broken command to see whether it replies politely.

## WhatsApp: closer to people, more friction

WhatsApp feels friendlier because the congregation already sends messages there. The catch is heavier: rules are strict and your personal number shouldn't be used. Set aside a separate one for it.

Two routes exist. An official provider is steadier, but sign-up is tedious and usually paid. An unofficial bridge is quicker to try, but can get restricted without warning. For a private test the bridge makes sense; to serve many people, the official route is safer.

On groups: don't let the agent answer every message in a busy community group. Let it respond when its name is called, or when someone replies to its message — otherwise a lively group becomes two robots greeting each other.

## One agent, many doors

Two channels need one habit: every incoming message, wherever it came from, lands in the same queue. The agent handles them one at a time and answers on the channel the message came from. Skip this and a reply meant for WhatsApp ends up in Telegram.

Keep a record too: who sent it, which channel, what was discussed. Otherwise every new message feels like talking to someone who just woke up — polite, remembering nothing.

## Where it goes wrong

Limit who can give orders. Private values never belong inside a conversation. Cap messages per hour: model usage is metered, and a busy group can eat a month of budget in a day.

A habit worth building early: the agent should rather wait or admit it doesn't know than answer wrong with confidence. For a study-circle schedule, a wrong answer costs more than a reply two minutes later.

The last test: send a message at midnight, when nobody watches the screen, then restart the server. If the answer still arrives, the door fits.

Next part: wiring up tools — so the agent can read files, search the web, and build its own schedule, plus memory so conversations survive a restart.
