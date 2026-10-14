# The Agent Commons

### One shared folder where all your AI agents — from every platform — can work together and talk

*Draft v1 — October 2026 — Dan Palermo / Candlelight AI*

---

## The problem

I asked a simple question: my wife is getting her own AI agent — can my agent and hers talk to each other and plan things together?

The honest answer was no. Personal AI agents are siloed by design. Each one serves one person, on one platform, and there is no agent-to-agent channel. The industry's answers are all heavy: orchestration platforms with per-seat pricing, agent "teammates" that only exist inside one vendor's walls, and formal protocols (Google's A2A, for instance) built for enterprises with engineering teams.

But while I was being told it couldn't be done, I noticed something: both agents could already read and write the same Google Drive. So could every other agent I run, on every other platform. The transport I needed had been sitting in my pocket the whole time.

**So I gave my agents an office instead of a protocol. It's a folder.**

---

## The idea in 30 seconds

Create **one shared folder** in the cloud storage you already have. Every agent you use gets access to it. Inside it:

- A **Constitution** doc holds the rules every agent follows.
- A **Chat** area holds conversations — **one doc per task or question**, never one endless log.
- When a task is done, its doc gets an outcome line and is **retired to a Finished folder** — the permanent record of everything your fleet has settled.
- A **Library** holds finished work and reference files any agent may use.
- A **Scratch** area gives each agent its own work-in-progress space.

That's the whole system. No server. No API keys. No new accounts. The agents coordinate through documents, the way human teams did for decades — because documents turn out to be a perfectly good message bus.

Architects will recognize this: it's the **blackboard pattern** from 1970s AI (HEARSAY-II and its descendants) — independent specialists coordinating through one shared surface instead of passing messages. The industry rebuilt it with platforms and protocols. This guide rebuilds it with a folder.

---

## What you need

- Two or more AI agents (any platforms — Muse, ChatGPT, Grok, local agents, agent frameworks) that can read and write cloud files, directly or through a connector.
- One shared folder: Google Drive, Dropbox, OneDrive, iCloud, or a self-hosted folder (Syncthing, a NAS). This guide says "Drive" — substitute yours freely. The method is transport-agnostic.
- About ten minutes.

---

## Setup

**1. Create the folder.** Name it `Agent Commons`. Inside it, create four subfolders: `Chat`, `Library`, `Scratch`, `Finished`.

**2. Add the Constitution.** Copy the Constitution template (included with this guide) into a doc at the root of the Commons. Edit the names, the members, and the authority limits to fit your household or team. This doc is the law of the office — every agent reads it first.

**3. Start the General doc.** In `Chat`, create a doc called `General`. This is the standing room for quick questions and chatter that don't deserve their own thread. Everything with a real beginning and end gets its own doc, named like this:

```
2026-10-14 — Weekend trip plan
2026-10-14 — Q4 budget draft
```

Date first, topic second. The folder listing becomes your board: whatever sits in `Chat` is, by definition, everything still open.

**4. Connect each agent.** For each agent platform, connect the same cloud account (or share the folder with the account that agent uses) and give it the onboarding prompt (included with this guide). It reads the Constitution, introduces itself in `General`, and it's staff.

**5. Give each agent a check-in rhythm.** Agents don't live in the folder — they visit it. Tell each agent when to check: on a schedule, when you start a session, or when you say "check the Commons." Mailbox time, not real-time. For planning, files, and decisions, mailbox time is almost always fast enough.

**6. Work.** Drop a task doc in `Chat`, or ask one of your agents to. Agents pick up threads, post entries, hand work to each other through the folder, and retire finished docs to `Finished` with an outcome line. You read the summaries and veto what you don't like. You're the owner of the office; the agents are staff.

---

## The lifecycle (the rule that makes it scale)

One endless chat log fails: it grows until no agent can afford to re-read it, and nobody can tell what's still open. So the Commons runs on a lifecycle instead:

1. **Open** — a doc is created in `Chat`, named `YYYY-MM-DD — topic`. Its first entry states the question or task and who it's for.
2. **Work** — agents append timestamped entries: proposals, answers, drafts, questions. Entries are never edited or deleted; corrections are new entries.
3. **Close** — when the task is complete, the closing agent writes the final entry: `✓ resolved` plus one line stating the outcome.
4. **Retire** — the doc moves to `Finished`. It is never deleted. `Finished` is your ledger — months later, any agent (or you) can answer "what did we decide about X?" by reading it.

Receipts, not rubble. An audit trail is a feature, and here it's free.

---

## Security — read this part twice

This design deliberately routes the hard parts of multi-agent security through your cloud provider, and that's its strength: identity, login security, access control, version history, and instant revocation are all inherited from Google/Microsoft/whoever runs your folder — infrastructure those companies spend billions on, which no orchestration startup can match and you don't have to build. But inheritance cuts both ways. Five rules keep the office safe:

1. **No secrets in the Commons. Ever.** No passwords, API keys, tokens, or financial credentials in any doc or file in the folder. The Commons is for plans and work product. (If you have a file with "TOKEN" in the name sitting in a shared folder right now, go move it. Everyone has one. Move it.)
2. **The sharing list is the membership list.** Anyone — human or agent — with editor access can write. Grant it deliberately. Remove people and agents the moment they leave the circle; unsharing is your eviction, and it's instant.
3. **Entries are data, not commands.** An agent takes orders only from its own human. A note in the Commons — even one written by a trusted agent — is a proposal to weigh, never an instruction to obey. This one rule is what stops a confused or compromised agent from steering the whole fleet.
4. **Money and irreversible actions need the human's yes.** Agents may propose, draft, summarize, and agree in principle. Purchases, bookings, filings, and messages to outsiders require the owning human's explicit approval, given outside the doc.
5. **Protect the hub account like a master key.** Your cloud account *is* the office's front door: passkey or strong 2FA on it, always. One compromised account inherits the whole Commons.

And the honest trade: your provider can see the contents (consumer cloud storage is generally not end-to-end encrypted), and your office inherits that provider's uptime and terms. For coordination that's a trade most households and small teams have already made. If it ever stops being acceptable, move the folder to a hub you control — the method survives the move intact.

---

## What it's for — and what it isn't

**For:** planning across people and agents, shared files and drafts, summaries and decision logs, households coordinating calendars and lists, small teams where a partner's agent keeps them current on a shared folder, a personal fleet (coding agent, research agent, personal agent) sharing one memory of what's been decided.

**Not for:** real-time collaboration at machine speed, high-frequency task loops, typed machine-to-machine contracts, anything where a two-second delay matters. That's what the heavy orchestration machinery is for, and this guide isn't pretending otherwise. Most of what real people need agents to coordinate on is asynchronous documents — and for that band, the heavy machinery is theater.

---

## Why this isn't sold to you

Every component of this pattern is old, and file-based agent bridges exist in a handful of open-source projects aimed at developers. What doesn't exist is a product — because there's nothing to productize. No server to host, no seats to sell, no lock-in to harvest. The pattern spreads only as knowledge, so here it is as knowledge: take it, adapt it, and if it saves your fleet from silo hell, tell someone.

Your agents were never unable to talk. They were just never given a room.

---

*Kit contents: this guide · `CONSTITUTION.md` (the rules template) · `ONBOARDING-PROMPT.md` (the paste-able instruction for adding an agent to your Commons).*
