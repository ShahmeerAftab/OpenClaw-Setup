OpenClaw Setup & Usage Guide
Overview

OpenClaw is a headless AI agent framework. It runs in the background (terminal/server) and lets you deploy AI agents that can work like “always-on employees.”

Use it for:

Persistent AI tasks

Multi-channel monitoring & automation

CLI/TUI-based control

Supports:

OpenAI GPT models (GPT-4, GPT-4o-mini, GPT-3.5)

Claude (requires paid API key & credits)

1. Requirements

Windows 10/11 (WSL2) or Linux

Node.js v20+

npm latest

Git

OpenAI API Key (for testing, free trial works)

Optional: Claude API key (paid)

2. WSL Setup (Windows only)

Open PowerShell as admin:

wsl --install


Restart PC.

Install Ubuntu from Microsoft Store.

Open Ubuntu terminal and create a UNIX username when prompted.

Update packages:

sudo apt update && sudo apt upgrade -y

3. Node.js & npm

Install Node.js v20+:

curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs


Check versions:

node -v
npm -v


Upgrade npm (optional):

npm install -g npm@latest

4. OpenClaw Installation

Clone the repo:

git clone https://github.com/openclaw/openclaw.git
cd openclaw


Install dependencies:

npm install


Install TUI daemon (optional):

openclaw onboard --install-daemon

5. API Key Setup

OpenAI example:

export OPENAI_API_KEY="sk-your-openai-key"


Check key:

echo $OPENAI_API_KEY


⚠️ Claude needs paid API key and credits.

6. Running OpenClaw
a) TUI mode (recommended)
openclaw tui

b) Hatch an agent
openclaw hatch


Inside TUI:

Change model: /model gpt-4o-mini

Send message: /say hello

7. Optional Skills

During setup, OpenClaw may ask to install skills:

1password, blogwatcher, camsnap, clawhub, github, openai-whisper, etc.


Skip any you don’t need

Some skills require API keys (e.g., GOOGLE_PLACES_API_KEY)

8. Troubleshooting

No response in TUI: check API key, Node.js ≥20

Network/npm issues:

npm config set registry https://registry.npmjs.org/
npm install


Node.js version error: upgrade using NodeSource script

Command not found:

npm install -g


or run npx openclaw tui

9. Tips

Test with OpenAI free trial first

Persistent agents require paid API

Export API key in terminal before running OpenClaw

Keep dependencies updated: npm update

10. Example Commands
# Set API key
export OPENAI_API_KEY="sk-xxxx"

# Start TUI
openclaw tui

# Hatch main agent
openclaw hatch --agent main

# Change model
/model gpt-4o-mini

# Send a message
/say Hello OpenClaw!
