# Andromeda Dashboard — Releases

Pre-built binaries for [Andromeda Dashboard](https://github.com/Thunder-BluePhoenix/andromeda).

> **Source code is private.** This repository contains only compiled binaries.
> New binaries are published automatically on every release via GitHub Actions.

---

## Install via CLI (recommended)

The [Andromeda CLI](https://github.com/Thunder-BluePhoenix/andromeda-cli) handles downloading, starting, stopping, and managing the dashboard for you.

### Windows

```powershell
irm https://raw.githubusercontent.com/Thunder-BluePhoenix/andromeda-cli/main/scripts/install.ps1 | iex
```

### Linux / macOS

```bash
curl -fsSL https://raw.githubusercontent.com/Thunder-BluePhoenix/andromeda-cli/main/scripts/install.sh | bash
```

Then:

```bash
andromeda setup      # first-time wizard: downloads binary, sets API key
andromeda start      # start the dashboard
andromeda status     # show URLs and API key
```

---

## Direct Download

Download the latest binary for your platform from the [Releases](../../releases/latest) page.

| Platform | File |
|---|---|
| Windows x86_64 | `andromeda-dashboard-windows-x86_64.exe` |
| Linux x86_64 | `andromeda-dashboard-linux-x86_64` |
| macOS x86_64 (Intel) | `andromeda-dashboard-macos-x86_64` |
| macOS aarch64 (Apple Silicon) | `andromeda-dashboard-macos-aarch64` |

### Run directly

```bash
# Linux / macOS
chmod +x andromeda-dashboard-linux-x86_64
./andromeda-dashboard-linux-x86_64

# Windows
.\andromeda-dashboard-windows-x86_64.exe
```

The dashboard starts on `http://localhost:3000`. The API key is printed to the console on first launch.

---

## What is Andromeda Dashboard?

A remote-control web dashboard for your own machine. Access it from any browser:

- **File Manager** — browse, upload, download files
- **Code Execution** — run shell commands and scripts
- **Web Terminal** — full interactive terminal in the browser
- **System Monitor** — live CPU, RAM, disk, network
- **Log Viewer** — stream logs from the dashboard
- **Internet Tunnels** — one-command Cloudflare or ngrok tunnel

---

## Internet Access

After starting the dashboard, expose it to the internet:

```bash
# Cloudflare tunnel (free, no account)
andromeda tunnel cloudflare

# ngrok (requires free account)
andromeda tunnel ngrok

# IPv6 (zero-config if available)
andromeda ipv6
```

---

## License

Apache 2.0 OR MIT
