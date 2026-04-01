# RemotePC 🔐
> Control your computer via a browser · Uses only the standard Python library · Cloudflare Tunnel

## What it can do
- 📊 **Overview** — CPU, RAM, disk, uptime, system info
- ▶ **Terminal** — run commands with history (↑↓ arrows)
- 📁 **Files** — file system browser
- ⚙ **Processes** — list + kill
- 🖥 **Screen** — screenshot (auto-refresh)
- 🔐 **Encryption** — RC4-drop768 + PBKDF2 + HMAC-SHA256 (demo + live)
- 🌐 **Cloudflare Tunnel** — public URL without port forwarding

---

## Installation

```bash
# 1. Copy the files to a folder
mkdir remotepc && cd remotepc
# (copy server.py and page.html)

# 2. Install optional dependencies (recommended)
pip install psutil mss pillow

# 3. Install cloudflared (for public access)
# Linux:
wget -q https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64.deb
sudo dpkg -i cloudflared-linux-amd64.deb

# macOS:
brew install cloudflared

# Windows:
# download the .exe: https://github.com/cloudflare/cloudflared/releases
```

---

## Running

```bash
# http://localhost:8080 only
python server.py

# With Cloudflare Tunnel (public HTTPS URL)
REMOTEPC_KEY=my_super_secret python server.py --tunnel

# Windows:
set REMOTEPC_KEY=my_super_secret
python server.py --tunnel
```

After running with `--tunnel`, a public URL will appear in the terminal:
```
🌐  Public URL : https://xxxx.trycloudflare.com
🔑  Access key  : my_super_secret
```

---




Translated with DeepL.com (free version)
