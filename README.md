# Upbit Agent Skills

English | [한국어](./README_KR.md)

AI agent skills built on the [Upbit](https://www.upbit.com) API, for digital asset trading.

Upbit Agent Skills enables AI agents to perform key Upbit functions through natural language, such as checking market data, checking balances, and placing orders. Integrated with an Upbit API-based CLI, it allows AI to carry out the necessary tasks based on context-aware instructions.

This project is designed not only for professional developers but also for traders who are eager to leverage AI technology. We invite you to build and experiment with your own flexible trading environment alongside AI, significantly reducing the burden of writing code from scratch.

## Installation

Requires [Node.js](https://nodejs.org) 18+.

```bash
npx skills add upbit-official/upbit-agent-skills
```

This installs the skill for your active coding agent (Claude Code, Cursor, Codex, etc.). Use `-g` for global installation:

```bash
npx skills add upbit-official/upbit-agent-skills -g
```

This skill integrates with [upbit-cli](https://github.com/upbit-official/upbit-cli). Install it with:

```bash
npm install -g @upbit-official/upbit-cli
```

## Skills

| Skill | Description |
|---|---|
| [`upbit`](skills/upbit/upbit/) | Upbit REST API via CLI — orders, market data, deposits, withdrawals, and setup |

## Authentication

After installing, configure API credentials using the CLI:

```bash
upbit config set
```

Credentials are saved to `~/.upbit/config` and automatically used for all CLI commands. Get API keys from [Upbit API Management](https://www.upbit.com/mypage/open_api_management).

Alternatively, set credentials via environment variables:

```bash
export UPBIT_ACCESS_KEY=<your-access-key>
export UPBIT_SECRET_KEY=<your-secret-key>
```

For a detailed setup guide, see [`setup.md`](skills/upbit/upbit/references/setup.md).

## Contributing

Upbit Agent Skills is in its initial release phase, and public contributions (Issues/PRs) are currently closed.
For bug reports and feedback, please email open-api@upbit.com.
We are considering opening external contribution channels in phases as this project becomes more stable.

## Disclaimer

See [DISCLAIMER.md](./DISCLAIMER.md) for full disclaimer.

© 2026 Dunamu Inc. All rights reserved.
