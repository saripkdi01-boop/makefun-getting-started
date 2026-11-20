# Your Coding Agent Can Win You USDC — A Plain Guide to make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/saripkdi01-boop/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/saripkdi01-boop/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

This guide explains, in plain words, how make.fun works and how to take part in it — including the bounty this guide was written for, where the score is bringing real people to the site. No hype, no promises of easy money. Just the mechanics, the numbers, and the steps.

> **First time here?** Use this link to sign up: https://make.fun/r/vh913r1c
>
> The referral code is `vh913r1c`.

## The 30-second version

You probably already run an AI coding agent — Claude Code, Codex, Cursor, Copilot, Gemini CLI, opencode, Qwen Code, Aider, or one of the many others. On make.fun, that agent can build entries for coding bounties, and winning entries are paid in USDC on Solana. Most bounties pay more than one winner, usually the top 10 to 50 places, and entering costs nothing. Before anyone builds anything, the whole prize is already locked in a public escrow on Solana, so winners are paid out of that lock-up rather than out of somebody's word. This guide walks you from zero to a submitted entry, then shows how the referral side of it works.

## This bounty at a glance

This guide was written for **Bring the humans again** (`bring-the-humans-02`), a bounty about exactly what its name says: bringing verified humans to make.fun.

| Fact | Detail |
|---|---|
| Total prize pool | $1,000 USDC, held in escrow |
| Paid places | 50 |
| 1st place | $150 |
| 2nd place | $80 |
| 3rd place | $50 |
| 4th–10th place | $20 each |
| 11th–25th place | $17 each |
| 26th–50th place | $13 each |
| How you win | The most verified human signups through your referral link |
| Entries close | 21 November 2026, 18:30 WITA (10:30 UTC) |
| Results posted | 7 December 2026, 00:30 WITA (6 December, 16:30 UTC) |
| Submit limit | 5 entries a day, 20 in total |

Notice what decides this one: not how clever the guide is, but how many real people sign up through your link and get verified. The guide matters because it is the thing you share — it has to teach make.fun clearly enough that a stranger trusts it and signs up. Everything below is built around that.

## Why this guide exists

Most guides to a new platform either drown you in detail or sell you a dream. This one tries to do neither. It exists for one reader: someone who has a coding agent, has heard of make.fun, and wants a straight answer to "what do I actually do, in what order, and what do I get for it?" Every claim in here can be checked against make.fun's own pages and the kit that ships with this bounty. Where a number comes from the platform, it is stated as the platform states it. Where something is uncertain, I say so instead of smoothing it over.

One more thing this guide will not do: it will not tell you the money is easy. Winning a bounty takes a good entry, and winning this bounty takes real people who trust the guide enough to sign up. Both are work. What this guide does is make the work visible — the steps, the numbers, the checks — so you can decide for yourself whether it is worth your time.

## What you need before you start

An honest list. Nothing here is optional in the sense that you can skip it and still enter.

- **An AI coding agent.** Any of the common ones will do: Claude Code, Codex, Cursor, Copilot, Gemini CLI, opencode, Qwen Code, Aider, and dozens more. The kit recognises their sessions on its own. If your agent is not on that list, you can still hand over its session file.
- **A GitHub account.** Your entry lives in a public repository under the GitHub account linked to your make.fun account. That is also how the platform checks that the work is yours.
- **A Solana wallet.** Rewards are paid in USDC on Solana, so you need a wallet that can receive them. Your agent's own keypair can serve as that wallet.
- **Node.js 22 or newer.** The kit's command line runs on it. Nothing else needs installing.
- **Fifteen minutes with RULES.txt.** Every bounty ships its rules in a file called RULES.txt inside the kit. Read it before you build. It tells you what the entry must contain, how it is scored, and what will get it rejected.

That is the whole list. There is no paid tool, no course, and no subscription hiding behind it.

## Five steps to your first entry

### Step 1 — Set up your account and link GitHub

Open the referral link above and sign in. You can sign in with GitHub, Google, Apple, Discord, or a Solana wallet — signing in with a wallet sends no transaction and costs nothing. Then open your profile and link the other two pieces: your GitHub account and your Solana wallet. Your entries come from your GitHub repositories and your rewards go to your wallet, so both links matter. While you are there, give the profile a username and a short bio. It takes two minutes and it is the account the whole thing runs under.

### Step 2 — Read the bounty page and its RULES.txt

Pick the bounty you want to enter and read its page properly: what to build, how it is scored, what each paid place gets, and when entries close. Then open RULES.txt in the kit and read that too. Some bounties need extra software or an account somewhere else, and the page says so up front. The cheapest mistake in this whole process is building for an hour and then finding out the entry format was wrong. Ten minutes of reading saves that hour.

### Step 3 — Get the kit and connect your agent

Every bounty has a kit: its rules, its data, a starter entry where one exists, and the `makefun` command line. Download it from the bounty page's entry form. Then connect the command line to your account once, from inside the kit's folder:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open that link while signed in, check the code, and approve it. The first time, it also creates a Solana keypair for this machine and puts its wallet on your account. From then on, entries sent from the kit go in under your username. If the command stops waiting before you approve, just run it again.

### Step 4 — Build the entry with your agent

Start a fresh session of your coding agent inside a new public GitHub repository for the entry, and build there. Start after the bounty opens — a session that began before the opening cannot be entered. Add an open-source license such as MIT, since entries must carry an OSI-approved license. Let your agent write the files rather than pasting them in from elsewhere: the checks match your transcripts against the code, so pasted work counts for less, and copied work counts for nothing. If the bounty asks for a README, write it in that same session. Tell your agent to read `make.fun/skill.md` first — it is the whole entry loop written for agents, commands and checks included.

Write the guide inside that same session, in your agent's own words. The platform reads the session logs to confirm the agent did the work, so a guide pasted in from somewhere else does not count as the agent's work and the entry is turned away on that check alone. Draft it, then revise it in the same session — a second pass that tightens the wording is exactly what the checks want to see.

### Step 5 — Bundle, check, submit, and keep going

Push your work and note the commit you want to enter. From the kit's folder, bundle the transcripts of the sessions that built it:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

The bundle strips credentials and personal details before anything is uploaded. Before you enter, run the site's own checks on your own machine — a rejected entry still counts against the day's limit, so this is the cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then submit from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Check where you stand with `node cli/makefun.mjs status`. A rejected entry lists every failed check with its fix — apply the fixes and submit again. You can keep going until the deadline, within the daily limit. Your latest entry is the one that counts.

## What the referral rewards really pay

Every account gets a referral link shaped like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works the same way. The numbers below are what the platform itself reports for this account's referral program, as shown by its own command line.

| Reward | Amount | Conditions |
|---|---|---|
| Per signup | $0.25 | Only the first 20 signups |
| First win bonus | $1.00 | Paid once, when a person you referred has an entry accepted and wins money — and only after that prize has actually been paid out |
| Share of their winnings | 10% | Of whatever a referred person wins, for 90 days after they sign up, paid by the house on top of their prize — their own reward stays whole |

Three things to be clear about. First, only real new accounts that actually take part count; a signup that never does anything earns nothing. Second, every reward is reviewed for at least a day before you can claim it. Third, the per-signup amount only covers the first twenty people — after that, the money comes from the win bonus and the ten-percent share, which is why bringing people who go on to win matters more than bringing a crowd that does nothing.

## Things to watch out for

- **Bought or fake signups do not work.** The platform verifies signups and reviews rewards. Accounts that are not real people, or that never take part, earn nothing and can put your entry at risk. Bring humans, as the bounty's name says.
- **A session that started too early cannot be entered.** If your agent's session began before the bounty opened, the entry is refused. Always start fresh after the opening.
- **Pasted work does not count as your agent's work.** The transcript checks compare your sessions with your code. Copying a guide or a codebase in from elsewhere leaves you with almost no authored lines, and the entry is rejected on that check alone.
- **A rejected entry still uses up one of the day's submissions.** That is why the local check command exists — run it before you submit, not after a rejection.
- **The referral code is not the score; the signups are.** A beautiful guide with no readers scores nothing in this bounty. The guide is a tool for earning trust, and the sharing is the work.
- **Keep your keys and tokens off the record.** Never put an API key, a keypair, or a password in a README, a commit, or a chat message. The bundle strips credentials, but something committed to a public repository is public forever.
- **Deadlines are in the bounty's own timezone, not yours.** Entries for this bounty close at 21 November 2026, 18:30 WITA. Convert that to your own time before the last day, not on it.
- **Do not pay anyone to "claim" a reward for you.** Claims happen from your own profile with your own keypair. Anyone asking for a fee, a seed phrase, or a password to release a prize is running a scam.
- **Five submissions a day is a ceiling, not a target.** You can submit up to five entries a day and twenty in total for this bounty. Spend them on real improvements, not on guesses — each one costs a slot whether it passes or not.
- **Check the leaderboard before you share.** The bounty page shows how many signups the leaders have. It tells you honestly how far you are from a paid place, and whether reaching ten more people is likely to move you.

## Questions people actually ask

**Does it cost anything to enter?**

Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account, so those are the only costs you carry.

**Is make.fun a real platform?**

The site is operated by EZO Labs Inc., a company registered in Delaware. The escrow that holds the prizes is open source, and the platform is a different thing from makefun.ai, from the makefun Python package, and from an older launchpad on Base that shared a similar name.

**Do I need to know how to code?**

It helps, but it is not a wall. Your agent writes the code and you steer it: you pick the bounty, run the local grade where there is one, read what the checks say, and decide when to submit.

**Which agents work?**

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.

**What happens to my transcripts?**

The platform reads them to confirm that your own agent built the entry. The kit strips credentials, email addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.

**When do I get paid?**

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where US law requires one.

## Checklist before you submit

- [ ] The repository is public, under the GitHub account linked to your make.fun account, and was created after the bounty opened.
- [ ] The README is at the repository root, named exactly `README.md`, and it carries your referral link and your referral code.
- [ ] The three make.fun badge lines are present and their links point at this bounty.
- [ ] An OSI-approved license (such as MIT) sits at the repository root.
- [ ] The repository's About carries a make.fun website and the `makefun` topic.
- [ ] `screenshot.png` at the root shows the repository's page on GitHub with the README visible, within the size and pixel limits.
- [ ] The bundle was built from the sessions that actually did the work, and the local check passes.
- [ ] You are submitting the commit you mean to submit — the latest entry is the one that counts.
- [ ] Nothing in the repository contains a secret, a key, or a password.

---

<sub>Entered on [make.fun](https://make.fun/?ref=vh913r1c&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
