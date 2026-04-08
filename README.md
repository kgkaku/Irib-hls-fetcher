<h1 align="center">
  <br>
  <a href="https://github.com/kgkaku/IRIB-Live-Channels-Playlist">
    <img src="https://upload.wikimedia.org/wikipedia/en/thumb/9/97/IRIB_Logo.svg/500px-IRIB_Logo.svg.png" alt="IRIB Logo" width="80%">
  </a>
  <br>
  IRIB Live Channels Playlist
  <br>
</h1>

<h2 align="center">Auto-updating IRIB Live Channels — M3U + JSON + EPG</h2>

<p align="center">
  <strong>🕒 Auto-updates every 6 hours • 🇮🇷 All IRIB channels • 📺 Works with any IPTV player</strong>
</p>

<p align="center">
  <a href="#">
    <img src="https://img.shields.io/badge/Maintained-Yes-brightgreen?style=flat-square" alt="Maintained">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Made%20in-Bangladesh_🇧🇩-green?colorA=%23ff0000&colorB=%23017e40&style=flat-square" alt="Bangladesh">
  </a>
</p>

---

## 📒 Introduction

**IRIB Live Channels Playlist** automatically fetches live streaming links from **Telewebion** (the official IRIB streaming platform). The script runs every 6 hours via GitHub Actions, collects channel metadata, stream URLs, authentication tokens, and EPG data, then generates ready-to-use `.m3u` playlists and `.json` output.

Perfect for IPTV players, custom apps, or personal use — no manual work needed.

---

## 💥 Key Features

| Feature | Description |
|---------|-------------|
| ⏰ **Auto-updates** | Runs every 6 hours via GitHub Actions |
| 📡 **All IRIB Channels** | National, Provincial, Exclusive, International, Radio |
| 🎥 **HD Streams** | 240p, 480p, 720p, 1080p available |
| 🔑 **Token Support** | Automatic JWT token extraction for authorized streams |
| 📺 **EPG Included** | Full XMLTV EPG for all channels |
| 📂 **Multiple Outputs** | Simple M3U, Extvlcopt M3U, JSON, EPG XML |
| ⚡ **Plug & Play** | Works with any IPTV player |

---

## 📁 Available Files

| File | Description | Link |
|------|-------------|------|
| `irib.m3u` | Simple M3U playlist (for most players) | [View](https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/irib.m3u) |
| `irib-extvlcopt.m3u` | Extended M3U with headers (VLC, OTT Navigator) | [View](https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/irib-extvlcopt.m3u) |
| `irib.json` | Complete channel metadata JSON | [View](https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/irib.json) |
| `epg.xml` | XMLTV EPG data | [View](https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/epg.xml) |

---

## 🕹️ How To Use

### 📱 Android (Mobile)

**Recommended Player:** [Televizo](https://play.google.com/store/apps/details?id=com.ottplayertv) or [NS Player](https://play.google.com/store/apps/details?id=com.genuine.leone)

```

https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/irib.m3u

```

### 📺 Android TV / Firestick

**Recommended Player:** [OTT Navigator](https://play.google.com/store/apps/details?id=studio.scillarium.ottnavigator) or [Tivimate](https://tivimate.com/)

```

https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/irib-extvlcopt.m3u

```

### 🖥️ Windows / Mac / Linux (VLC)

1. Open **VLC Media Player**
2. `Media` → `Open Network Stream` (Ctrl+N)
3. Paste: `https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/irib.m3u`
4. To see EPG: `View` → `Guide` (Ctrl+G)

### 🔧 EPG Setup (For Advanced Players)

Add this EPG source in your player:

```

https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/epg.xml

```

---

## 📊 Channel Statistics

| Type | Count |
|------|-------|
| 🇮🇷 National | 19 |
| 📍 Provincial | 33 |
| ✨ Exclusive | 16 |
| 🌍 International | 1 |
| 📻 Radio | 16 |
| **Total** | **85+** |

---

## 🛠️ Developer Guide

### Auto-updated JSON File

Use the JSON endpoint for programmatic access:

```
https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/irib.json
```

### JSON Structure

```json
{
  "generated": "2026-04-07T20:11:57",
  "credit": "@kgkaku",
  "total_channels": 85,
  "channels": [
    {
      "descriptor": "tv1",
      "name_fa": "شبکه 1",
      "name_en": "channel 1",
      "type": "سراسری",
      "type_descriptor": "national",
      "group_name_en": "National",
      "has_archive": true,
      "logo_url": "https://static.telewebion.ir/channelsLogo/...",
      "stream_url": "https://ncdn.telewebion.ir/tv1/live/playlist.m3u8"
    }
  ]
}
```

## ❓How It Works

1. GitHub Actions runs irib.py every **6 hours.** 
2. Script fetches channel list from gateway.telewebion.ir
3. Fetches EPG data for each channel
4. Generates .m3u, .json, and epg.xml files
5. Commits and pushes changes back to the repository

---

## 🧪 Preview

<h1 align="center">
  <img src="https://raw.githubusercontent.com/kgkaku/IRIB-Live-Channels-Playlist/refs/heads/main/images/preview.jpg" width="80%">
</h1>

---

## 📝 Legal Notice

· ⛔ I do not host any content. All stream URLs are fetched from publicly available sources (Telewebion.ir).
· ⚠️ This project is for educational and research purposes only. It demonstrates how to authenticate and stream IPTV using public APIs.
· 🚫 If this code affects the revenue of the content owners, please contact me and I will remove it.
· 🇮🇷 Some content may be geo-restricted to Iran.

---

## ✉️ Contact Me

* [GitHub](https://github.com/kgkaku)  
* [Telegram](https://t.me/kgkaku_bot)


---

## ⭐ Support This Project

If you find this useful, **please star the repository on GitHub!**

---

## 📜 License

This project is open-source and available under the **MIT License.**
