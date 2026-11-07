# Squeek Maze

A maze puzzle game powered by [Squeekchain](https://squeekchain.com)'s live API. Guide Squeektoshi the hamster through a maze to collect all the cheese and reach the nest — while dodging patrolling beetles.

**Play it live:** https://fadliferdian28.github.io/squeek-dash

## How to play

- Move with **Arrow keys / WASD**, the on-screen **D-pad**, or **swipe** (mobile).
- Collect all the **cheese** (🧀), then reach the **nest** to clear the level.
- Avoid the **beetles** — getting bitten costs 1 life (3 lives per run). After a bite you get a short pause and 2.2s of invulnerability.
- Clear a maze to advance to the next level (more, faster beetles).

## Powered by the live Squeekchain API

The game polls `https://api.squeekchain.com/v1/status` every 15 seconds:

- **Maze seed:** each level's maze is generated deterministically from the real **block height** (`builder.anchor.blockHeight`) — a new block means a new maze, and the same block always regrows the same maze. The seeding block is shown above the maze.
- **Beetle speed:** the real wheel **RPM** (`measurement.rpmMilli`) scales beetle patrol speed. When the real hamster is **RUNNING**, all points are **doubled**.
- **Live panel:** core status (RUNNING/IDLE), RPM, block height + build progress, and total work units, with live/stale/offline indicators. If the feed is down, the game keeps running at base speed.

## Wallet (optional)

The game is **fully playable without a wallet**. Connecting a wallet is optional and only unlocks:

- **Connect Wallet** — MetaMask / browser wallet on **Sepolia testnet** (Chain ID 11155111). The header shows your shortened address; wrong-network prompts help you switch.
- **Daily Check-In** — check in once a day (recorded locally per wallet + date, no gas, no transaction) to build a streak and earn **+1 extra life** on your next run.

## Share

After a run ends, the summary screen shows your score, time, cheese collected, level reached, and the wheel status at finish — with a **Share on X** button that posts your score plus the game link (`#Squeekchain`).

## Built with

- No build step — a single `index.html` plus `logo.png`.
- Live data: [Squeekchain status API](https://api.squeekchain.com/v1/status).
- Submit a project like this at https://squeekchain.com/genesis (Build on Squeekchain).

## Credits

Built for the Squeekchain Genesis "Build on Squeekchain" program. Squeekchain and Squeektoshi belong to their respective owners. No wallet, tokens, or payments are required to play.
