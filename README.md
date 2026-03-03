# Gallagher Tracker
![GitHub forks](https://img.shields.io/github/forks/AbusiveAlcoholic/gallagher-tracker?style=for-the-badge) ![GitHub issues](https://img.shields.io/github/issues/AbusiveAlcoholic/gallagher-tracker?style=for-the-badge) ![Node.js](https://img.shields.io/badge/node-%3E%3D18-green?style=for-the-badge&logo=node.js) ![Discord](https://img.shields.io/badge/discord-bot-blue?style=for-the-badge&logo=discord) ![Status](https://img.shields.io/badge/status-active-success?style=for-the-badge)

<p align="center">
  <b>Game update tracker with Discord notifications and a web dashboard.</b>
</p>

<p align="center">
  Automatically detect game updates and post them to Discord with a link to a version history page.
</p>

---

## Overview

Gallagher Tracker monitors games for new builds and announcements and posts update notifications directly to Discord.
Each notification includes a link to the tracker website where the version history and update information can be viewed.

The project includes:

* Discord bot for update notifications
* Web dashboard for viewing update history
* Per-server tracking configuration
* Automatic deduplication of updates
* Steam build and news tracking

Credits: https://github.com/AbusiveAlcoholic

---

## Features

### Discord Bot

* Automatic update detection
* Slash command configuration
* Per-server tracking
* Per-game channel routing
* Optional role pings
* Quiet hours support
* Manual update checks
* Duplicate event prevention

### Web Dashboard

* List of tracked games
* Version history viewer
* Update timestamps
* Event history table
* Lightweight interface

### Tracking Sources

* Steam build updates
* Steam news announcements

---

## Example Discord Notification

When a game update is detected the bot posts a message containing a link to the tracker page.

Example message:

```id="t3a0hx"
https://yourtracker.site/g/730
```

Example embed:

**Counter-Strike 2 Update Detected**

New build detected
Version: 31804200

---

## Web Interface

The tracker website displays game update history.

Pages:

| Page         | Description                       |
| ------------ | --------------------------------- |
| `/`          | List of tracked games             |
| `/g/<appId>` | Version history and update events |

Example page:

```id="95v0ri"
https://yourtracker.site/g/730
```

---

## Installation

Clone the repository

```bash id="n0q9vh"
git clone https://github.com/YOUR_USERNAME/gallagher-tracker
cd gallagher-tracker
```

Install dependencies

```bash id="8bdg02"
npm install
```

Create the environment file

```bash id="l0u1p4"
cp .env.example .env
```

Configure the environment variables

```id="uef7vl"
DISCORD_TOKEN=
DISCORD_CLIENT_ID=
WEBSITE_BASE_URL=http://localhost:8787
```

---

## Register Discord Commands

```bash id="0pryl8"
npm run register:commands
```

---

## Start the Bot

```bash id="u9c9h1"
npm start
```

---

## Start the Web Dashboard

```bash id="u7mep9"
npm run start:web
```

Default website URL:

```id="rcf6k0"
http://localhost:8787
```

---

## Docker Deployment

```bash id="s7j9st"
docker compose up -d
```

---

## Commands

| Command               | Description              |
| --------------------- | ------------------------ |
| `/track add`          | Track a game             |
| `/track remove`       | Stop tracking a game     |
| `/track list`         | Show tracked games       |
| `/track test`         | Send a test notification |
| `/track check`        | Force update check       |
| `/config quiet-hours` | Configure quiet hours    |
| `/config timezone`    | Set server timezone      |

---

## License

MIT License
