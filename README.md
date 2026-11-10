# P. K. Stewart

Forward-deployed AI engineer in Baton Rouge, Louisiana. I design and run multi-agent systems that do real work inside real businesses. Founder of [Deploy Axiom](https://deployaxiom.com). Anthropic certified.

My own two businesses run on a team of agents, every day. An operator agent takes requests and routes them. Specialist agents do the work on a shared task board. Each one has a lane, a set of tools and an approval boundary. I also deploy agents onto clients' own machines. When a client's agent gets stuck, it escalates to mine and the problem gets handled, logged and answered without anyone sitting in a chat.

What I care about in this work:

- **Approval boundaries.** Reversible, private work runs on its own. Money, deletions, new promises and messages to strangers wait for a person.
- **Evidence over claims.** A fix counts when there's proof it worked: an HTTP response, a delivered-message row, a screenshot. An agent saying "done" doesn't count.
- **Plain-English handoffs.** Every task ends with a summary the owner can read on a phone.

## Open source

| Repo | What it does |
|---|---|
| [escalation-desk](https://github.com/percyhendrux123-prog/escalation-desk) | The loop that answers when an agent gets stuck: watcher, leased dispatcher, fail-closed approval gate, evidence trail. |
| [hermes-tripwire](https://github.com/percyhendrux123-prog/hermes-tripwire) | Logs every action an agent is refused and alerts the owner. It records what happened instead of asking the agent. |
| [hermes-handydandy](https://github.com/percyhendrux123-prog/hermes-handydandy) | Session-size notices and structured handoffs, so long agent sessions end cleanly instead of degrading. |
| [hermes-axioma](https://github.com/percyhendrux123-prog/hermes-axioma) | Inline signal color: the agent marks the few phrases that deserve a second look. An advisor, not a gate. |
| [hermes-standing](https://github.com/percyhendrux123-prog/hermes-standing) | Earned trust for Hermes workers: independent proof checks, a local record, and level-based approval gates. |
| [hermes-gatekeeper](https://github.com/percyhendrux123-prog/hermes-gatekeeper) | Owner-configured policy checks on recognized outbound messaging calls. It does not inspect connector, MCP, browser or script sends. |
| [hermes-axiom-agent](https://github.com/percyhendrux123-prog/hermes-axiom-agent) | Adds the nine-article Axiom Doctrine and reports which enforcer plugins are enabled. It enforces nothing itself. |
| [hermes-chiron](https://github.com/percyhendrux123-prog/hermes-chiron) | Reads how much you know about the topic in front of you from your own words, with no model call, and tells the agent how to talk to you. Anything risky still waits for a yes. |
| [Axiom-deploy](https://github.com/percyhendrux123-prog/Axiom-deploy) | The Deploy Axiom website. Static, zero-cost, with a test suite. |

## Stack

Python, Hermes Agent, Claude, MCP, SQLite, launchd, Netlify, Supabase, Stripe.

## Contact

[deployaxiom.com](https://deployaxiom.com)
