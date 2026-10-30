# Percy Keith

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
| [Axiom-deploy](https://github.com/percyhendrux123-prog/Axiom-deploy) | The Deploy Axiom website. Static, zero-cost, with a test suite. |

## Stack

Python, Hermes Agent, Claude, MCP, SQLite, launchd, Netlify, Supabase, Stripe.

## Contact

[deployaxiom.com](https://deployaxiom.com)
