
OpenClaw Setup & Usage Guide – Windows / Linux (Simple)

A beginner‑friendly guide to run OpenClaw on Windows (via WSL2) or Linux.
OpenClaw lets you run persistent AI agents that act like “always-on employees.”

What You Need

Windows 10/11 with WSL2 or Linux

Node.js v20+

npm latest

Git

OpenAI API Key (free trial works for testing)

Optional: Claude API key (paid)

Step 0: Install WSL2 (Windows Only)

Open PowerShell as administrator and run:

wsl --install


Restart your PC.

Install Ubuntu from Microsoft Store.

Open Ubuntu terminal → create a UNIX username when prompted.

Update packages:

sudo apt update && sudo apt upgrade -y

Step 1: Install Node.js & npm

Check if Node.js is installed:

node -v


✅ If version is v20+, skip installation
❌ If not, install Node.js:

curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs


Check versions:

node -v
npm -v


(Optional) Upgrade npm:

npm install -g npm@latest

Step 2: Install OpenClaw

Clone the OpenClaw repository:

git clone https://github.com/openclaw/openclaw.git
cd openclaw


Install dependencies:

npm install


(Optional) Install TUI daemon:

openclaw onboard --install-daemon

Step 3: Set Your API Key

OpenAI Example (free trial works):

export OPENAI_API_KEY="sk-your-openai-key"


Check key:

echo $OPENAI_API_KEY


⚠️ Claude API key requires a paid subscription and credits.

Step 4: Start Using OpenClaw

Option A: TUI mode (recommended)

openclaw tui


Option B: Hatch an agent

openclaw hatch --agent main


Inside TUI:

Change model:

/model gpt-4o-mini


Send a message:

/say hello

Step 5: Optional Skills

During setup, OpenClaw may ask to install skills:

1password, blogwatcher, camsnap, clawhub, github, openai-whisper, etc.

Skip any you don’t need

Some skills require API keys (e.g., GOOGLE_PLACES_API_KEY)

Step 6: Troubleshooting

No response → check API key & Node.js version ≥20

Network/npm issues:

npm config set registry https://registry.npmjs.org/
npm install


Node.js version error → upgrade using NodeSource script

Command not found → try:

npm install -g
# or
npx openclaw tui


TUI stuck on start → wait 20–30 seconds

Step 7: Quick Test

Start TUI:

openclaw tui


Send:

/say Hello OpenClaw!


✅ If OpenClaw replies, setup is working!

Step 8: Daily Workflow

Terminal 1 → run TUI or Hatch agent

Terminal 2 → interact with agent

Exit anytime with Ctrl + C

🎉 Done!
You now have OpenClaw running on Windows/Linux and can start testing AI agents.
