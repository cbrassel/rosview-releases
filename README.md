# Rosview

Native macOS app that monitors Linux servers over SSH, in the spirit of **xosview**: compact, segmented horizontal bars you can read at a glance.

<p align="center"><img src="docs/live.png" width="677" alt="Rosview live view: CPU, memory, swap, network, disk and file system bars for a Linux server"></p>

- CPU, memory, swap, network, disk I/O and file systems
- Live bars, history graphs (2 to 30 min) and top processes
- Refresh interval from 1 s to 60 s
- Window background turns yellow, then red, as the load average nears a per-host threshold
- One window per host
- Nothing to install on the server: Rosview uses your Mac's `/usr/bin/ssh`, your keys and ssh-agent
- English and French

## Screenshots

**History** — graphs over the last 2 to 30 minutes, with the peak network and disk rates

<img src="docs/history.png" width="590" alt="Rosview history view with CPU, memory, swap, network and disk graphs over 10 minutes">

**Top processes** — the 15 busiest processes, sorted by CPU or memory

<img src="docs/processes.png" width="611" alt="Rosview process view listing the busiest processes with CPU and memory usage">

**High load** — the window turns red when the load average reaches the host's threshold

<img src="docs/high-load.png" width="553" alt="Rosview window with a red background on a heavily loaded server">

**Hosts** — each host is just a name and an `ssh` command

<img src="docs/hosts.png" width="502" alt="Rosview host list with two servers and their ssh commands">

## Install

With [Homebrew](https://brew.sh):

```sh
brew tap cbrassel/tap
brew trust cbrassel/tap   # Homebrew 7 and later
brew install --cask rosview
```

Or download the latest `Rosview-x.y.dmg` from [Releases](../../releases), open it and drag **Rosview** into **Applications**.

The app is signed with a Developer ID and notarized by Apple.

## Requirements

- macOS 14 or later
- A Linux server reachable with `ssh` using key or ssh-agent authentication (no passwords are stored)

## Feedback

Please open an [issue](../../issues).
