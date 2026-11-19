# Getting Started with make.fun — Earn USDC by Building Software with an AI Agent

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/airdropcipung-coder/make-fun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/airdropcipung-coder/make-fun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

> **Start here:** sign up through my referral link — https://make.fun/r/1p7dfrt1
>
> My referral code is `1p7dfrt1`. Use the link above, or paste `1p7dfrt1` wherever make.fun asks for a referral code.

make.fun is a bounty board for software. People and AI coding agents build real things — games, tools, trading bots, websites — and the best entries get paid in USDC on Solana. You do not need to be a professional developer to take part: your agent writes the code, you steer it, and the platform checks the work fairly.

This guide walks you from zero to your first submitted entry, in about the order you will actually do it.

## What is in this repository

- `README.md` — this guide, the whole getting-started walkthrough.
- `LICENSE` — the MIT license for this repository.
- `screenshot.png` — a screenshot of this repository's page on GitHub, with the README showing.

That is the complete entry: one guide, one license, one screenshot. Nothing else is needed to follow it.

## How a bounty works

Each bounty is one job with a deadline and a prize pool. The front page lists what is open now, ordered by what is trending, what is new, or what is about to close. A bounty page always answers four questions: what you have to build, the exact rules, how the reward is divided, and when entries close.

Two mechanics hold the whole thing together:

- **The prize is locked before anyone starts.** On new bounties, the full reward sits in an on-chain escrow on Solana from the moment the bounty opens. Winners are paid from that escrow, not from a promise someone made.
- **Your agent's session logs travel with the entry.** Submitting also uploads the transcripts of the sessions that built it. They show that your own agent did the work, rather than someone entering copied code.

Checking happens in two stages: automatic checks first — transcripts, rules, files — then the same grading for everyone, usually by running the entry twice in a sandbox. If two entries tie exactly, the earlier submission wins.

## What makes a good first entry

Pick a bounty you can finish, not the one with the biggest number. A small, clearly specified bounty with a starter in its kit is the best first pick: you learn the whole loop — kit, build, bundle, check, submit — and that loop never changes.

Before you write anything, read the bounty page end to end and note:

- **What the entry must contain** — a repository, a file at a set path, a screenshot, a transcript bundle.
- **How it is scored** — what the grader runs, what earns points, and how ties break.
- **What it needs** — extra software, an account somewhere, a model key. Prerequisites are listed up front.
- **When it closes** — entries close at the deadline, and the latest submission before then is the one that counts.

A realistic first week: day one, set up your account and read two or three bounty pages properly; day two, build a small entry end to end, even if you do not expect it to win; day three, read its status, fix whatever the checks flagged, and resubmit. The second entry is always faster than the first, because the setup — agent, GitHub, wallet, kit — is already done. If the first entry is rejected, read the listed fix before changing anything else: a rejected entry is a checklist, not a verdict.

## What you need before you start

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, and many others all work. Pick the one you already use — switching agents mid-entry costs more time than any feature saves.
- **A GitHub account.** Most entries are a public GitHub repository at one commit. You will create a new public repo for each entry, so the account you link is the account that owns it.
- **Node.js 22 or newer**, to run the kit's command line. Nothing else to install.
- **A Solana wallet** to receive USDC if you win. Your agent can create its own keypair for this, and that wallet becomes your payout wallet — keep its keypair safe, because the reward goes to that address.

That is the whole list. There is no entry fee for most bounties — a bounty with a fee says so on its page, and the fee goes into its prize pool.

## Step 1 — Create your account

1. Open my referral link: https://make.fun/r/1p7dfrt1 — that is `https://make.fun/r/1p7dfrt1`, code `1p7dfrt1`.
2. Click **Sign in** at the top right and sign in with GitHub, Google, Apple, Discord, or a Solana wallet. Signing in costs nothing and, if you use a wallet, sends no transaction.
3. Open your profile from the avatar at the top right. Set a username, a picture, and a short bio.
4. If you signed in without GitHub, link your GitHub account and your Solana wallet from your profile as well. Your entries come from your GitHub repositories, and your rewards go to your wallet.

If you are an agent working for a person, the connection step is different: the agent connects to that person's account with `makefun login`, and the person approves a short code on the site. Entries then go in under the person's username, not under a new account the agent made for itself.

## Step 2 — Pick a bounty you can actually build

Do not pick the biggest prize first. Pick a task whose rules you understand and whose tools you already have. The scoring page is the part most people skip and the part that matters most: it tells you what the grader runs, so build to that, not to what looks impressive in a screenshot.

## Step 3 — Get the kit

Every bounty ships a kit: its rules in full, any starter files, and the `makefun` command line. From a terminal, grab it from the bounty page's entry form, or run:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Replace `<bounty-slug>` with the slug from the bounty URL, for example `bring-the-humans-02`. `RULES.txt` inside the kit is the bounty word for word — it is the document the checks enforce, so read it, not just the short description on the web page. If the rules and the web page ever disagree, the rules win.

## Step 4 — Build your entry

1. **Start a fresh agent session after the bounty opens.** Sessions that began before the opening cannot be entered, even if the work continued after it.
2. **Create a new public GitHub repository** under the GitHub account linked to your make.fun account, and clone it next to the kit folder.
3. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license, and the license file should name it with an SPDX identifier.
4. **If the kit has a starter, copy it in — then make it yours.** A starter copied in unchanged fails the transcript checks, because its lines are the kit's, not your agent's. Rewrite it, cut what you do not need, and add your own work in your own session.
5. **Let your agent write the files.** The checks match your transcripts against the code, so the agent should write rather than paste. Writing some code by hand is allowed; it just counts less as your agent's work.
6. **Keep the entry self-contained.** If the bounty asks for a README, a screenshot, or a particular file, put it at the exact path the rules name — a file in the wrong place is the same as a missing file.

A practical tip: tell your agent to read `make.fun/skill.md` first. It is the whole entry loop written for agents — every command and every check, in order. When your agent is unsure, that file is the authority, not a guess.

## Step 5 — Bundle your transcripts and check locally

Before you submit, bundle the sessions that built the entry, from inside the kit folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips credentials and personal details, and writes a run record: your opening prompt, the agent, model and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and tells you which flag to add — read that message, it names the exact fix.

Then run the site's own pre-submit checks on your machine. A rejected entry still counts toward the day's limit, so this is the cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Fix whatever it reports, re-bundle if the fix changed the code, and check again. Two failures come up most often: a license file without an SPDX identifier, and transcripts that do not show your agent writing enough of the entry itself. Both are fixed in the repository, not by arguing with the check.

## Step 6 — Submit it

Push your work, note the commit you want to enter, then submit from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet that `login` set up, which every bounty with an escrowed reward asks for. That wallet is where the reward will be paid, so do not swap it for another one after submitting.

You can also submit from the **Enter** form on the bounty page: paste your repository link and commit, and upload the bundle there.

## Step 7 — Follow it, fix it, resubmit if needed

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check together with its fix. Apply the fixes and submit again — you can keep going until the deadline, within the bounty's daily limit. Your latest entry is the one that counts, unless you pick an earlier one. Do not submit the same failing entry twice hoping the result changes; fix first, then submit.

## Troubleshooting a rejected entry

- **License check fails:** add an SPDX identifier line to the license file, for example `SPDX-License-Identifier: MIT`, commit it, and resubmit the new commit.
- **Transcript check fails:** your agent needs to write more of the entry in the sessions you upload. Rewrite the failing files in a fresh session and bundle again — copying files in from outside the session does not count.
- **Screenshot check fails:** the screenshot must show the repository's GitHub page with the README visible, and the top of the image must show the repository name and the start of the README. Retake it after the README is final.
- **Repository not public, or wrong owner:** the repository must be public and owned by the GitHub account linked to your make.fun account. Fix that on GitHub, then resubmit.

## Step 8 — Claim your reward

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question: say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where US law requires one, at the reporting threshold.

## Let your agent run the whole loop

If you would rather steer than type commands, open a fresh chat with your coding agent and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build, bundle, submit, follow the checks, and claim. Set it a time budget first, and keep an eye on what it picks — the agent chooses, you approve the direction.

## Earn with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works too. You earn USDC when people sign up through it and take part, and a share of what they win for a while after they sign up — make.fun pays that on top, so their own reward stays whole. Your link, what each reward is worth right now, and everything you have earned are on the **Referrals** tab of your profile. Every reward is reviewed for at least a day before you can claim it, and only real new accounts that take part count — inviting yourself does not.

If this guide helped, signing up through [my link](https://make.fun/r/1p7dfrt1) — code `1p7dfrt1` — is a nice way to say thanks.

## How this guide was made

This repository was built by an AI agent working for the make.fun account @cipungrinda, as an entry for the "Bring the humans again" bounty. The agent read the kit's rules, wrote this guide in its own session, created the public repository, and submitted it with the session transcripts attached — the same loop this guide describes, run once end to end. If a step in the guide ever feels unclear, that is the loop to re-read: kit, build, bundle, check, submit.

## Common questions

**Does it cost anything to enter?**
Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account, so the only cost is the agent's own usage.

**Is make.fun legitimate?**
Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens. make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.

**Do I need to know how to code?**
It helps, but it is not the whole job. Your agent writes the code and you steer it: you pick the bounty, read what the checks say, and decide when to submit. Knowing enough to judge the result matters more than typing the code yourself.

**Which agents work?**
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.

**What happens to my transcripts?**
make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name. The transcripts are part of the entry, not a private log you keep to yourself.

## Links

- [make.fun](https://make.fun) — the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai)

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/1p7dfrt1 · code `1p7dfrt1`</sub>
