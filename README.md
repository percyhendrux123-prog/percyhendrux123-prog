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

## Open source

| Repo | What it does |
|---|---|
| [escalation-desk](https://github.com/percyhendrux123-prog/escalation-desk) | The loop that answers when an agent gets stuck: watcher, leased dispatcher, fail-closed approval gate, evidence trail. |
| [send-lock-kit](https://github.com/percyhendrux123-prog/send-lock-kit) | A default-deny send plugin, the container wall behind it, and the test that shows why the plugin alone is not enough. |
| [hermes-gatekeeper](https://github.com/percyhendrux123-prog/hermes-gatekeeper) | Owner-configured policy checks on recognized outbound messaging calls. It does not inspect connector, MCP, browser or script sends. |
| [hermes-tripwire](https://github.com/percyhendrux123-prog/hermes-tripwire) | Logs every action an agent is refused and alerts the owner. It records what happened instead of asking the agent. |
| [hermes-axioma](https://github.com/percyhendrux123-prog/hermes-axioma) | Inline signal color: the agent marks the few phrases that deserve a second look. An advisor, not a gate. |
| [hermes-standing](https://github.com/percyhendrux123-prog/hermes-standing) | Earned trust for Hermes workers: independent proof checks, a local record, and level-based approval gates. |
| [hermes-handydandy](https://github.com/percyhendrux123-prog/hermes-handydandy) | Session-size notices and structured handoffs, so long agent sessions end cleanly. |
| [hermes-axiom-agent](https://github.com/percyhendrux123-prog/hermes-axiom-agent) | Adds the nine-article Axiom Doctrine and reports which enforcer plugins are enabled. It enforces nothing itself. |
| [hermes-chiron](https://github.com/percyhendrux123-prog/hermes-chiron) | Reads how much you know about the topic in front of you from your own words, with no model call, and tells the agent how to talk to you. |
| [coachapp](https://github.com/percyhendrux123-prog/coachapp) | Open-source coaching app: programs, nutrition, check-ins and messaging for coaches and their clients. |
| [Axiom-deploy](https://github.com/percyhendrux123-prog/Axiom-deploy) | The Deploy Axiom website. Static, with a test suite. |

Several of the plugins above are listed in the [Hermes Agent plugin catalog](https://github.com/NousResearch/hermes-agent/tree/main/plugin-catalog), each merged by a maintainer.

## Training

Anthropic Academy: Claude 101, Claude Code 101, Introduction to Claude Cowork.

## Stack

Python, Hermes Agent, Claude, MCP, SQLite, launchd, Netlify, Supabase, Stripe.

## Contact

[deployaxiom.com](https://deployaxiom.com) · [LinkedIn](https://www.linkedin.com/in/percy-keith-2380b1403)
