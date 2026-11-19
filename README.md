# Make money with your AI agent, even if you're not a coder

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Richie-lee-cloud/makefun-guide-nigeria/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/Richie-lee-cloud/makefun-guide-nigeria/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **New here? Start with my link:** [https://make.fun/r/e1cybfh9](https://make.fun/r/e1cybfh9)
>
> My referral code is `e1cybfh9`.
>
> This guide is my entry for the "Bring the humans again" bounty — $1,000 shared by the 50 best entries, ending **Saturday, November 21, 11:30 AM WAT**. 1st place gets $150, 2nd gets $80, 3rd gets $50, 4th–10th get $20 each, 11th–25th get $17 each, and 26th–50th get $13 each.

This is a plain, step-by-step guide to make.fun, written for a newcomer in Nigeria — and for anyone who has never coded. You do not need to be a programmer. You need a clear idea, an AI agent that writes the code for you, and the patience to follow the rules.

## What is make.fun?

make.fun is a website where people and their AI coding agents build software for cash bounties. A bounty is a job with a clear task, a deadline, and a prize pool. You and your agent build what it asks for. If your entry places near the top, you get paid.

Rewards are paid in USDC on Solana. When a bounty opens, the prize money is locked in an on-chain escrow, so the money is there waiting before anyone starts work. Top entries claim their reward to their own Solana wallet.

You do not have to be a professional programmer. The agent does most of the coding. Your job is to pick a good bounty, read the rules carefully, guide the agent in plain language, and make sure your entry is submitted properly.

## How a bounty flows

1. **Open** — A bounty is posted with its rules, deadline, and prize pool locked in escrow.
2. **Build** — You and your AI agent build your entry, usually in a public GitHub repository.
3. **Submit** — You submit the link to your repo at a specific commit, together with the transcripts of the agent sessions that built it.
4. **Checked** — Automatic checks verify your entry: the repo, the files, the licence, the transcripts, and that everything matches what the bounty asked for.
5. **Scored** — For most bounties, entries are graded and ranked on a leaderboard. For this bounty, "Bring the humans again", your score is different: it is the number of verified human signups your referral link brought during the competition. The entry with the most verified signups wins, and the 50 highest-ranked entries share the $1,000. Only real signups count — your own account, fake accounts, bots, and idle accounts that never take part do not count.
6. **Paid** — Top entries claim their reward in USDC to their own Solana wallet.

Most bounties are free to enter.

## What you need

- **An AI coding agent** — for example Claude Code, Codex, Cursor, Copilot, Gemini CLI, and many more. If you already chat with an AI assistant that can code, you are probably fine.
- **A GitHub account** — your entry lives in a public GitHub repo, so you will need a free GitHub account.
- **Node.js 22** — the make.fun kit runs on Node 22, so install that version (or newer in the 22 line) on your computer.
- **A Solana wallet** — only needed when you win and want to claim a reward in USDC. Set one up before the deadline of any bounty you enter, so you are not rushing later. I use Solflare, but any Solana wallet works.

Signing in to make.fun itself is flexible: you can use GitHub, Google, Apple, Discord, or a Solana wallet. GitHub is a good choice because you will need GitHub for your entries anyway.

## A short note if you are in Nigeria

You can do this from Nigeria. Sign in with GitHub, link your GitHub account and your Solana wallet on your profile, and build with your agent. No coding is needed from you — your agent writes the code, and you explain what you want in plain words. The reward is paid in USDC to your Solana wallet, not to a bank account. Set the wallet up early, keep your seed phrase private and never share it with anyone, and check the deadline in West Africa Time (WAT) so you do not miss it.

## Contents

- [1. Create your account](#1-create-your-account)
- [2. Pick a bounty](#2-pick-a-bounty)
- [3. Get the kit](#3-get-the-kit)
- [4. Build your entry](#4-build-your-entry)
- [5. Submit it](#5-submit-it)
- [6. Check it, fix it, resubmit](#6-check-it-fix-it-resubmit)
- [7. Claim your reward](#7-claim-your-reward)
- [Your first hour on make.fun](#your-first-hour-on-makefun)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [Questions](#questions)

## 1. Create your account

1. Open [https://make.fun/r/e1cybfh9](https://make.fun/r/e1cybfh9) — that link carries my referral code `e1cybfh9`.
2. Click **Sign in** at the top right.
3. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. GitHub is the best choice, because you will need GitHub for your entries anyway. Signing in costs nothing, and signing in with a wallet sends no transaction.
4. Open your profile (the avatar at the top right) and finish it: a username, a picture, and a short bio.
5. If you signed in another way, link your GitHub account and your Solana wallet from the profile too. Your entries come from your GitHub repositories, and your rewards go to your wallet.

The kit's command line needs to be connected to your account once. That way your agent enters under your account rather than making one of its own. From inside a bounty's kit, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

That prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code, and approve it. If the command stops waiting before you approve, run it again. The first time, it also makes a Solana keypair for this machine, and the commands below sign your entries and claims with it.

## 2. Pick a bounty

Browse the open bounties and pick one that fits your time and interest. The front page lists them under Trending, New, and Ending soon, with categories such as Code, Games, Trading, Forecasting, and Growth.

**Read the rules first.** Every bounty is different. Before you build anything, read the full rules page for that bounty: what exactly to build, what files are required, the deadline, how scoring works, and how many places get paid. Most failed entries do not fail because the work was bad — they fail because a simple rule was missed.

Start small if it is your first time. A smaller bounty with a clear task teaches you the whole flow without pressure.

## 3. Get the kit

Each bounty provides a kit — a starter folder with the tools and files for that competition.

Download or clone the kit for your chosen bounty. For this bounty, the command is:

```sh
curl -sSL "https://make.fun/c/bring-the-humans-02/kit" | tar xz
cd bring-the-humans-02-kit
```

Inside it, find **RULES.txt**. Treat RULES.txt as the word — if anything else disagrees with it, RULES.txt wins. Read RULES.txt fully before you start building. It tells you the exact folder layout, required files, and submission steps for that bounty.

## 4. Build your entry

Open a **fresh session** with your AI coding agent and build inside the kit's rules.

1. Tell the agent what the bounty asks for and point it at RULES.txt.
2. Work in the open: your entry will be a public GitHub repo at a specific commit, so keep your files organised from the start.
3. Create a new public GitHub repository under the GitHub account linked to your make.fun account, and add an OSI-approved licence such as MIT.
4. Save your work to GitHub as you go. Do not leave everything on your computer until the last minute.
5. Keep the agent sessions that do the building — you will need their transcripts when you submit. Do not delete or edit them to look nicer; the checks expect the real sessions that built the entry.

Test what you built. Run it, open it, click through it — whatever applies. A working entry beats a fancy-looking broken one. For this bounty, the entry is a guide, so read it through as a newcomer would: does every step make sense, does every link work, and is your referral link in it?

## 5. Submit it

When your entry is ready:

1. Push your final work to your public GitHub repo and note the exact commit.
2. Bundle the transcripts of the agent sessions that built it, as the kit instructs. From the kit folder, run:

```sh
node cli/makefun.mjs bundle --repo ../makefun-guide-nigeria --out transcripts.tar.gz
```

3. Run the local check provided in the kit first. It catches most problems while you can still fix them quickly:

```sh
node cli/makefun.mjs check --kit . --repo ../makefun-guide-nigeria --transcripts transcripts.tar.gz
```

4. Submit through the kit with your **repo URL + commit** and the transcripts:

```sh
node cli/makefun.mjs submit --competition bring-the-humans-02 \
  --repo-url https://github.com/Richie-lee-cloud/makefun-guide-nigeria --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Replace `<sha>` with the exact commit you want to enter. You can also submit from the **Enter** form on the bounty page, by pasting your repository link and commit and uploading the bundle.

Submit a little before the deadline if you can. Deadlines are strict, and last-minute internet or upload problems are real.

## 6. Check it, fix it, resubmit

```sh
node cli/makefun.mjs status
```

This shows your entries and where each one stands. If an automatic check fails, do not panic and do not spam resubmissions.

- Read the failure message carefully. It usually names the exact check that failed — for example a missing file, a wrong licence, or a transcript problem.
- Fix that one thing properly.
- Run the local check again.
- Resubmit once it passes locally.

Many bounties allow more than one submission, but each attempt should fix a real diagnosed problem. Guessing and re-uploading the same thing rarely helps. Your latest entry is the one that counts.

## 7. Claim your reward

If your entry places in the paid spots:

- Wait for the final results to be confirmed after the deadline.
- Claim your reward from the bounty page to **your own Solana wallet**.
- Rewards are in USDC on Solana, from the escrow that was locked when the bounty opened.

You can also claim from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

Say `--us-person yes` only if you are a US person. Keep your wallet details safe, and double-check the address before you claim. A tax form is asked for only where the law requires one.

## Your first hour on make.fun

Do not try to do everything at once. Here is a simple first hour that sets you up properly:

1. **Sign up (5 minutes)** — Use [https://make.fun/r/e1cybfh9](https://make.fun/r/e1cybfh9), code `e1cybfh9`, and sign in with GitHub if you can.
2. **Complete your profile (5 minutes)** — Add your handle and a short bio, and link your GitHub account and Solana wallet. A finished profile is the first sign of a real, active account.
3. **Open one bounty (10 minutes)** — Pick just one bounty that looks interesting. Do not open ten tabs. One is enough to learn from.
4. **Read its rules properly (15 minutes)** — Read the bounty page and, if you download the kit, its RULES.txt from top to bottom. Note the deadline, the required files, and how many places get paid.
5. **Take part, even in a small way (15 minutes)** — Leave a genuine comment or question on the bounty if comments are open, or start a tiny first entry with your agent — even a rough draft in your repo. The point is to actually use your account, not leave it sitting idle.
6. **Note your next step (10 minutes)** — Write down what you will build, what you still need, and when the deadline is. Then you can come back and build with a clear head.

A few extra tips from my own entry:

- **Small and complete beats big and unfinished.** A simple entry that passes every check can place. A grand entry that misses a required file cannot.
- **Run the local check early**, not just at the end. Run it once with a rough draft so you learn what it looks for.
- **Keep your transcripts.** Start your build in a fresh agent session and do not throw that session away — you need it to submit.
- **Do not wait for the last hour.** Uploads, GitHub, and wallets all choose the deadline day to act up. Submit early if you can.
- **For this bounty, sharing matters.** Your score is verified signups from your link, so a clear guide is only half the work — share it where real people who might genuinely want to try make.fun will see it, and tell them honestly what it is.

## Earn with your own referral link

Every make.fun account gets its own referral link. Mine is [https://make.fun/r/e1cybfh9](https://make.fun/r/e1cybfh9), code `e1cybfh9`.

You earn when people sign up through your link **and actually take part**. Signing up is only the first step. An account that just sits there idle does not count. The person needs to genuinely use the site — look at bounties, complete their profile, join in.

Please do not create fake accounts or sign up the same person multiple times. That does not help anyone and those signups will not count. Referral rewards are reviewed for at least a day before they can be claimed.

Your own link is on the Referrals tab of your profile. If this guide helped, signing up through my link is a nice way to say thanks.

## Questions

**Does it cost money to join?**
Joining make.fun is free, and most bounties are free to enter. You may need your own AI agent subscription depending on which agent you use, but the site itself does not charge you to sign up and browse.

**Is this legitimate?**
make.fun is run by EZO Labs Inc. Prize money for a bounty is locked in an on-chain escrow on Solana when the bounty opens, and top entries claim USDC rewards to their own wallets. As with anything online, start small, read the rules, and judge by your own experience.

**Do I need to know how to code?**
No. Many people enter with an AI coding agent doing the coding. You need to be able to follow the rules, guide the agent in plain language, check the result, and submit carefully. If you can explain what you want clearly, you can take part.

**Which agents work?**
Claude Code, Codex, Cursor, Copilot, Gemini CLI, and many more. Use the agent you already have, as long as it can work with files and code and keep session transcripts.

**What happens to my transcripts?**
Your entry includes the transcripts of the agent sessions that built it. They are uploaded with your submission so the automatic checks can verify that the work was built as claimed and matches the repo. Only submit sessions you are comfortable sharing as part of a public entry.

**When do I get paid if I win?**
After the bounty deadline, entries are checked and scored, final results are confirmed, and then top entries can claim their USDC reward to their own Solana wallet.

**How is this bounty scored?**
"Bring the humans again" is scored by verified human signups, not by a code grader. Your referral link brings people in; only signups that the house's referral check verifies count. A signup counts when a new account is created during the competition with your code bound to it, and each signup is decided after its own 24-hour review hold. The final check runs for 30 hours after the deadline, and only signups verified by the end of it count.

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

Written for newcomers in Nigeria, and for anyone starting with no coding experience. Sign up with my referral link: [https://make.fun/r/e1cybfh9](https://make.fun/r/e1cybfh9) · code `e1cybfh9`
