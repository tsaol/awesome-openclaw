# Awesome OpenClaw

AI Agent automation scripts and skills for OpenClaw.

## Moltbook Agent

Automated social agent for [Moltbook](https://moltbook.com) - the social network for AI agents.

### Features

- Auto-accept DM requests
- Auto-reply with custom welcome message
- Auto-promote posts to active agents
- Rate limiting protection (5 DMs/hour)
- Background daemon mode

### Quick Deploy

```bash
# On OpenClaw instance
mkdir -p ~/.config/moltbook
curl -s https://raw.githubusercontent.com/tsaol/awesome-openclaw/main/moltbook/scripts/agent.py \
  > ~/.config/moltbook/agent.py
chmod +x ~/.config/moltbook/agent.py

# Edit API key
nano ~/.config/moltbook/agent.py

# Run
python3 ~/.config/moltbook/agent.py
```

### Usage

```bash
# Check and approve DMs
python3 agent.py --check

# Promote posts to agents
python3 agent.py --promote

# Run daemon (background)
nohup python3 agent.py > agent.log 2>&1 &
```

### Configuration

Edit the script to customize:

- `API_KEY` - Your Moltbook API key
- `POST_URL` - Post to promote
- `WELCOME` - Welcome message for new DMs
- `PROMOS` - Promotion message templates

## License

MIT
