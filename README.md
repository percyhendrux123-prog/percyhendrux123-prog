# P. K. Stewart

Percy Keith Stewart. I design and run multi-agent AI systems inside real businesses, from Baton Rouge, Louisiana. Founder of [Deploy Axiom](https://deployaxiom.com). AI writes the code; I decide what gets built, review it, verify it and own the result.

My own two businesses run on a team of agents every day. One operator agent takes requests and routes them. Specialist agents do the work on a shared task board, each with its own tools and an approval boundary. I also put agents on clients' own machines. When a client's agent gets stuck, it escalates to mine, and the problem is handled, logged and answered without anyone sitting in a chat.

## Results

Dated numbers from work that is live, with client identities withheld: [deployaxiom.com/results](https://deployaxiom.com/results/).

- An independent insurance agency went from no contact after the sale to live client care in 7 days.
- When a client's agent got stuck during a video call, the escalation loop opened and closed the ticket in 4 minutes. That evening is replayed in [escalation-desk](https://github.com/percyhendrux123-prog/escalation-desk).

## What I care about in this work

- **Approval boundaries.** Reversible, private work runs on its own. Money, deletions, new promises and messages to strangers wait for a person.
- **Evidence over claims.** A fix counts when there is proof it worked: an HTTP response, a delivered-message row, a screenshot. An agent saying "done" does not count.
- **Plain-English handoffs.** Every task ends with a summary the owner can read on a phone.

## The seat: a collection of Hermes plugins

The whole story, with six weeks of numbers: [Leave it running](https://www.linkedin.com/pulse/leave-running-p-k-stewart-mycne/).

One real job through the whole loop, in 67 seconds: [the seat, one real job](https://x.com/OfficialPercyK/status/2125020914676908241).

Most people run Hermes as it ships. I added a set of small plugins that work together, and you get a different agent. It takes the next step on its own, it stays quiet when there's nothing new, it remembers when you said no, and it shows its work. I call that a seat: an agent that holds a role on your team the way a person would, knowing its job, its limits and who it answers to.

No one has to build this from scratch. It's here, free and public.

### What each piece does

Each plugin does one job. Together they cover the whole loop: watch, decide, act, prove, hand off.

| Step | Plugin | What it does for you |
|---|---|---|
| Watch | [hermes-tripwire](https://github.com/percyhendrux123-prog/hermes-tripwire) | Every time the agent is told no, it writes it down and tells you. |
| Watch | [hermes-run-receipts](https://github.com/percyhendrux123-prog/hermes-run-receipts) | Each scheduled job the agent runs leaves a receipt: what ran, which tools it used, which ones errored. |
| Watch | [hermes-chiron](https://github.com/percyhendrux123-prog/hermes-chiron) | Watches how you talk, notices how much you already know, and tells the agent how to talk to you. |
| Decide | [hermes-axioma](https://github.com/percyhendrux123-prog/hermes-axioma) | Marks the few phrases in a reply where your decision matters. |
| Decide | [hermes-declines](https://github.com/percyhendrux123-prog/hermes-declines) | Remembers when you say no to a scheduled job, so it stops asking. |
| Decide | [hermes-repeat-pause](https://github.com/percyhendrux123-prog/hermes-repeat-pause) | Same result three runs in a row, you hear it once. The job keeps running. |
| Act | [hermes-gatekeeper](https://github.com/percyhendrux123-prog/hermes-gatekeeper) | Checks the messages it recognizes against your rules (consent, STOP, quiet hours, no double texts) before they send. Its README lists what it can't see. |
| Act | [send-lock-kit](https://github.com/percyhendrux123-prog/send-lock-kit) | A send lock that refuses by default, the wall behind it, and a test that proves the lock alone isn't enough. |
| Prove | [hermes-standing](https://github.com/percyhendrux123-prog/hermes-standing) | A task isn't done because the agent says so. It's done when a check passes. |
| Hand off | [hermes-handydandy](https://github.com/percyhendrux123-prog/hermes-handydandy) | When a session gets long, it writes a handoff so the next one picks up where this one stopped. |
| Hand off | [escalation-desk](https://github.com/percyhendrux123-prog/escalation-desk) | When an agent gets stuck, the problem goes to someone who can answer, and the answer comes back with proof. |
| The rules | [hermes-axiom-agent](https://github.com/percyhendrux123-prog/hermes-axiom-agent) | Nine articles the agent works by, and a report of which plugins above are enforcing each one. |

### How they serve each other

Tripwire and run-receipts write down what happened. Axioma, declines and repeat-pause decide what's worth your attention. Gatekeeper and send-lock stand in front of anything that leaves the machine. Standing turns the record into trust, so a proven worker asks you less. HandyDandy and escalation-desk make sure nothing is dropped between sessions or when the agent is stuck. The Axiom Agent plugin names the rules and shows which ones are actually being enforced.

Any one of them works alone. Together they're the whole seat.

### What you see on day one

- The agent's replies carry a few marked phrases where your decision matters.
- A refused action shows up in a log, not buried in a chat.
- A scheduled report that hasn't changed stops repeating itself.
- A "no" stays a no.
- A long chat ends with a handoff instead of a wall of context.

### For builders

The same collection in your vocabulary: proactivity with restraint. Observers (tripwire, run-receipts) record and never change what the agent does. Policies (gatekeeper, send-lock, declines) run before the tool call. Each README states whether it fails open or closed, and what it does not cover. Repeat-pause implements item 5 of the Hermes proactivity roadmap ([NousResearch/hermes-agent#158538](https://github.com/NousResearch/hermes-agent/issues/158538)); declines and run-receipts came out of the review on [#158289](https://github.com/NousResearch/hermes-agent/pull/158289).

Install any plugin from its repo, or from the [Hermes Agent plugin catalog](https://github.com/NousResearch/hermes-agent/tree/main/plugin-catalog).

### Merged upstream

Twelve of these plugins are in the official Hermes Agent plugin catalog. Each one went through a pull request to [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent/pulls?q=is%3Apr+author%3Apercyhendrux123-prog+is%3Amerged) and was merged by a maintainer.

| Repo | Catalog entry |
|---|---|
| [hermes-tripwire](https://github.com/percyhendrux123-prog/hermes-tripwire) | [tripwire](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/tripwire.yaml) |
| [hermes-run-receipts](https://github.com/percyhendrux123-prog/hermes-run-receipts) | [run-receipts](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/run-receipts.yaml) |
| [hermes-chiron](https://github.com/percyhendrux123-prog/hermes-chiron) | [chiron](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/chiron.yaml) |
| [hermes-axioma](https://github.com/percyhendrux123-prog/hermes-axioma) | [hermes-axioma](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/hermes-axioma.yaml) |
| [hermes-declines](https://github.com/percyhendrux123-prog/hermes-declines) | [hermes-declines](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/hermes-declines.yaml) |
| [hermes-repeat-pause](https://github.com/percyhendrux123-prog/hermes-repeat-pause) | [repeat-pause](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/repeat-pause.yaml) |
| [hermes-gatekeeper](https://github.com/percyhendrux123-prog/hermes-gatekeeper) | [hermes-gatekeeper](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/hermes-gatekeeper.yaml) |
| [send-lock-kit](https://github.com/percyhendrux123-prog/send-lock-kit) | [send-lock](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/send-lock.yaml) |
| [hermes-standing](https://github.com/percyhendrux123-prog/hermes-standing) | [hermes-standing](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/hermes-standing.yaml) |
| [hermes-handydandy](https://github.com/percyhendrux123-prog/hermes-handydandy) | [handydandy](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/handydandy.yaml) |
| [hermes-axiom-agent](https://github.com/percyhendrux123-prog/hermes-axiom-agent) | [hermes-axiom-agent](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/hermes-axiom-agent.yaml) |
| [hermes-axiom-coach](https://github.com/percyhendrux123-prog/hermes-axiom-coach) | [hermes-axiom-coach](https://github.com/NousResearch/hermes-agent/blob/main/plugin-catalog/hermes-axiom-coach.yaml) |

### Also built on Hermes

| Repo | What it does |
|---|---|
| [hermes-axiom-coach](https://github.com/percyhendrux123-prog/hermes-axiom-coach) | Connects Hermes to the open coach app and runs the Lite fitness calculators as local tools. |
| [coachapp](https://github.com/percyhendrux123-prog/coachapp) | Open-source coaching app: programs, nutrition, check-ins and messaging for coaches and their clients. |
| [Axiom-deploy](https://github.com/percyhendrux123-prog/Axiom-deploy) | The Deploy Axiom website. Static, with a test suite. |

## Stack

Python, Hermes Agent, Claude, MCP, SQLite, launchd, Netlify, Supabase, Stripe.

## Contact

[deployaxiom.com](https://deployaxiom.com) · [LinkedIn](https://www.linkedin.com/in/percy-keith-2380b1403)
