<p align="center">
  <img src="img/logo.png" alt="Futaba" width="200">
</p>

<p align="center">
    <img alt="GitHub Release" src="https://img.shields.io/github/v/release/adv-inn/futaba">
    <img alt="Downloads" src="https://img.shields.io/github/downloads/adv-inn/futaba/total?style=flat&label=Downloads">
</p>

<p align="center">
    <a href="Readme.md">简体中文</a> | English | Website <a href="https://futaba.lol">futaba.lol</a>
</p>

# Futaba

A League of Legends companion client built with Tauri, supporting both desktop and mobile control. Simple and efficient.

This project is released under the [GPL-3.0](LICENSE) license. Due to previous incidents where malicious users obtained the source code and sold compiled versions online, which goes against the original intent of this project, the source code will not be open-sourced at this stage. It will be open-sourced once the project reaches a certain level of adoption.

## Feedback
QQ Group:1080984368
Github issue:[https://github.com/adv-inn/futaba/issues](https://github.com/adv-inn/futaba/issues)

## Download

| Channel | Notes |
|---|---|
| [GitHub Releases](https://github.com/adv-inn/Futaba/releases) | Official releases |
| [futaba.lol](https://futaba.lol) | Can switch to China-region mirrors, speed-tests them and picks the fastest line |
| [Lanzou](https://wwbgt.lanzout.com/b01i61l0ti) (password `4zy4`) | Backup channel for mainland China, slower |

Every release ships an installer (`installer.exe`) and portable builds (`portable.exe` / `portable.zip`). The installer updates itself, and can retry through a China-region mirror with one click if the official source fails.

I'd appreciate it if you download from GitHub or the mirrors on futaba.lol so I can track actual download counts.

Features
---
**Champion select**
 - [x] Auto-accept matches, auto-pick from your favorite champions, and auto-swap for a higher-ranked favorite during ARAM trades
 - [x] Champ select overlay: champion tiers, win rates and a recommendation panel drawn right on the LoL client
 - [x] OP.GG enhanced integration (item builds / runes / summoner spells / augment picks, applied in one click; covers League Classic too)
 - [x] Dedicated ARAM Mayhem data (champion / augment / item rankings, augment combos, first legendary item, augment build calculator), switchable with OP.GG
 - [x] Auto counter-pick calculation
 - [x] Player lists: mark players you have met and see their badge when you meet them again

**In game**
 - [x] Augment recognition: reads the augment cards off the screen and overlays tier, win rate and synergy picks (ARAM Mayhem / Arena)
 - [x] In-game overlay: next item and full build path from your current items in ARAM Mayhem, AI build recommendations
 - [x] AI game situation analysis

**After the game**
 - [x] Match history (including TFT), player tags and jungle route analysis
 - [x] Share cards: solo or multiple players, MVP / SVP scores and highlight tags, VS layout when allies and enemies are both selected
 - [x] AI post-game review

**Other**
 - [x] Friends (chat / invite / scheduled invite / friend requests / private message alerts)
 - [x] Game mode selection
 - [x] Mobile support (friends / game mode / item builds / augments)
 - [x] Three themes: Clean Light, Clean Dark and Persona 5


<table>
    <tr>
        <td><img alt="" src="img/index_en.png"></td>
    </tr>
</table>

## Augment Recognition

The LoL client API never exposes the augment picker in ARAM Mayhem and Arena. Futaba reads every augment card straight off the screen and overlays tier, win rate, rank for your champion, fitting items and common combos right under each card. No more guessing.

Pure screen capture: no memory reading, no game file changes. The high-accuracy OCR engine is built in and works out of the box.

![](img/hextech-overlay.jpg)

## Champ Select Overlay

No need to leave the client during champ select. Futaba draws a recommendation panel right on the LoL client: champion tier and win rate, summoner spells, skill order, core build and augments. Apply the spells and write the core build to an item set in one click.

![](img/champ-select-overlay.jpg)

## Main Application

Once the League of Legends client is launched, you can minimize it and use Futaba to take over all other functions. (In ARAM / ARAM Mayhem, you can freely swap champions without timer restrictions)

<table>
    <tr>
        <td><img alt="" src="img/create-room.png"></td>
        <td><img alt="" src="img/in-room.png"></td>
        <td><img alt="" src="img/history.png"></td>
    </tr>
    <tr>
        <td><img alt="" src="img/mayhem-data.png"></td>
        <td><img alt="" src="img/player-list.png"></td>
        <td><img alt="" src="img/favorite-champions.png"></td>
    </tr>
</table>

## OP.GG & ARAM Mayhem Data
When you enter champion select, Futaba automatically applies the current patch's strongest item builds, rune pages, and preferred summoner spells based on your selected champion.

In Classic mode (Normal / Ranked), it shows counter and favorable matchups for your selected champion.

In ARAM Mayhem it uses dedicated ARAM Mayhem data by default (you can switch back to OP.GG in settings), with a data page and an augment build calculator: pick the augments you have and get item recommendations, and in game it suggests the next item as you pick more augments.

All of these are also accessible on mobile.

<table>
    <tr>
        <td><img alt="" src="img/opgg-tier.png"></td>
        <td><img alt="" src="img/mayhem-detail.png"></td>
    </tr>
    <tr>
        <td><img alt="" src="img/opgg-detail.png"></td>
        <td><img alt="" src="img/counter-show.png"></td>
    </tr>
</table>

The data panel can also be opened as a standalone mini window. The ARAM Mayhem data source, champ select auto-apply (runes / summoner spells / item sets) and Flash key position can all be changed in settings.

![](img/opgg-setting.png)

## Share Cards

Generate a share image after any match, solo or with multiple players, featuring skin splash art, MVP / SVP scores, highlight tags and augment picks. When allies and enemies are selected together, it switches to a VS layout.

<table>
    <tr>
        <td><img alt="" src="img/share-match.png"></td>
        <td><img alt="" src="img/share-team.png"></td>
    </tr>
</table>

## Themes

Three themes: Clean Light, Clean Dark (graphite + International Klein Blue) and Persona 5.

<table>
    <tr>
        <td><img alt="" src="img/index.png"></td>
        <td><img alt="" src="img/theme-dark.png"></td>
        <td><img alt="" src="img/theme-p5.png"></td>
    </tr>
</table>

## Mobile
Enable LAN data sharing in the settings page. The app will broadcast a `futaba.local` domain via mDNS, which you can visit to access the web interface.

For convenience, you can also scan the QR code displayed on the app page for quick access.

All communication happens locally on your network — no external servers, fully secure.

Now you can accept matches and pick champions even while grabbing takeout or taking a break.

![](img/network-server.png)

<table>
    <tr>
        <td><img alt="" src="img/mobile-create-room.png"></td>
        <td><img alt="" src="img/mobile-bp.png"></td>
    </tr>
    <tr>
        <td><img alt="" src="img/mobile-chat.png"></td>
        <td><img alt="" src="img/mobile-opgg.png"></td>
    </tr>
</table>

## Acknowledgements

China-region mirrors are provided by [gh-proxy](https://github.com/hunshcn/gh-proxy) and [Xget](https://github.com/xixu-me/Xget).
