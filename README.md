# 🔌 Kasa Skill

> *"Turn on the bedroom fan"* — done.

A [Clawdbot](https://github.com/clawdbot/clawdbot) skill for controlling TP-Link Kasa smart plugs, switches, and bulbs locally.

## ✨ What This Does

Control your Kasa devices without the cloud:

- 🔌 *"Turn on the lamp"*
- 🌀 *"Bedroom fan off"*
- 💡 *"Toggle the living room light"*

Works locally — no TP-Link cloud needed (for most devices).

## 📋 Requirements

- **Python 3.8+**
- **Kasa devices** on your local network
- **pip3 install python-kasa**

## 🚀 Quick Start

### 1. Install python-kasa

```bash
pip3 install python-kasa
```

### 2. Discover your devices

```bash
./scripts/kasa.sh discover
```

This finds all Kasa devices and saves them to `~/.clawdbot/kasa/devices.json`

### 3. Control stuff

```bash
./scripts/kasa.sh "Bedroom fan" on
./scripts/kasa.sh "Bedroom fan" off
./scripts/kasa.sh "Bedroom fan" toggle
./scripts/kasa.sh "Bedroom fan" status
```

Or use IP directly:

```bash
./scripts/kasa.sh 192.168.68.51 on
```

## 🔧 Finding Device IPs

If discovery doesn't work (newer devices require auth):

1. Open **Kasa app** → tap device → **Device Info**
2. Note the **MAC address**
3. Check your router's DHCP list for that MAC → get IP
4. Add manually to `~/.clawdbot/kasa/devices.json`:

```json
{
  "Bedroom fan": "192.168.68.51"
}
```

## 🤖 For Clawdbot / Claude

Check `SKILL.md` for agent instructions. The script handles discovery and control. Just tell it what to do! 🍌

## 📜 License

MIT — Do whatever you want with it.

---

*Made with 🍌 by a Minion and their human*
