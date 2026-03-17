# OpenClaw AI Deployment

https://openclaw.ai/

## Purpose

- To feel god-like having a little AI of my own. Yet mostly to see what all the hype is about.

## Configuration

```bash
# Prepare Environment Ubuntu
apt update
apt upgrade -y

# Install Node.js 22
curl -sL https://deb.nodesource.com/setup_22.x | bash -
apt install -y nodejs

# Restore Backup (Optional)
# Install OpenClaw
npm install -g openclaw
openclaw onboard
```

## Usage

1. Connect to Deployment,
   1. Run, `kubectl exec --stdin --tty openclaw-ma-npm -- /bin/bash`
1. Open one terminal for `openclaw gateway`
2. Open second terminal for `openclaw tui`
3. ENJOY

## Requirements

- An isolated environment with limited local resources. 
  - Testing as a research agent on the open internet, writing editorial scripts, and simple data mining.
  - Be aware of prompt injection. Assume the platform itself is a backdoor or trojan hourse. Lockdown on network.

- An `npm` based environment for package management. This platform may be used with later Python projects.

- Persistent storage at `/root/.openclaw/` for configuration. 
  - For other applications, I've done a home directory. `export OPENCLAW_WORKSPACE=/home/openclaw`
  - To restore backup tar ball, `tar -xzpf openclaw-backup-YYYYMMDD-HHMMSS. tar.gz -C /`

/EOF/