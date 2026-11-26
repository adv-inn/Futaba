<p align="center">
  <img src="img/logo.png" alt="Futaba" width="200">
</p>

<p align="center">
    <img alt="GitHub Release" src="https://img.shields.io/github/v/release/adv-inn/futaba">
    <img alt="Downloads" src="https://img.shields.io/github/downloads/adv-inn/futaba/total?style=flat&label=Downloads">
</p>

<p align="center">
    简体中文 | <a href="Readme_en.md">English</a> | 官网 <a href="https://futaba.lol">futaba.lol</a>
</p>

# Futaba
一款使用 Tauri 开发的支持双端操作的英雄联盟客户端，简洁，高效

本程序发布时将遵循[GPL-3.0](LICENSE)协议，由于此前遇到过恶意用户多次获取源代码并编译自己的版本到互联网售卖，这破坏了我的初衷，所以本项目现阶段并不会开源，会在传播度到达一定程度时进行开源

## 问题反馈/优化建议
QQ群:1080984368
Github issue:[https://github.com/adv-inn/futaba/issues](https://github.com/adv-inn/futaba/issues)

## 下载

| 渠道 | 说明 |
|---|---|
| [GitHub Releases](https://github.com/adv-inn/Futaba/releases) | 官方发布页 |
| [官网 futaba.lol](https://futaba.lol) | 可切换国内镜像，自动测速选择最快线路 |
| [蓝奏云](https://wwbgt.lanzout.com/b01i61l0ti)（密码 `4zy4`） | 国内直连备用通道，速度较慢 |

每个版本提供安装版（`installer.exe`）与便携版（`portable.exe` / `portable.zip`）。安装版支持自动更新，官方源下载失败时可一键切换国内镜像重试。

我希望大家优先通过 GitHub 或官网的国内镜像下载，这样我可以统计实际的下载次数

已实现的功能
---
**选人阶段**
 - [x] 自动接受对局，按常用英雄列表自动选用，大乱斗交换期自动换取更靠前的常用英雄
 - [x] 选人客户端浮窗：直接在英雄联盟客户端上叠加英雄梯度、胜率与推荐面板
 - [x] OP.GG 增强适配（出装 / 符文 / 召唤师技能 / 海克斯强化推荐，一键应用，覆盖怀旧服）
 - [x] 海克斯大乱斗专属数据（英雄 / 强化 / 装备榜、强化组合、命运之武器、强化出装计算器），可与 OP.GG 切换
 - [x] 对局 Counter 位自动计算
 - [x] 玩家红黑榜：标记遇到过的玩家，再次遇到时显示徽章

**对局中**
 - [x] 海克斯强化识别：截屏识别强化卡，叠加梯度、胜率与搭配推荐（海克斯大乱斗 / 斗魂竞技场）
 - [x] 游戏内悬浮窗：海克斯大乱斗按当前装备推荐下一件与完整出装路线，AI 出装推荐
 - [x] AI 局势分析

**对局后**
 - [x] 战绩查询（含云顶之弈），玩家评价标签与打野路线分析
 - [x] 战绩分享图：单人 / 多人同框，MVP / SVP 评分与高光标签，敌我同框 VS 对抗布局
 - [x] AI 对局评价

**其他**
 - [x] 好友交互（聊天 / 邀请 / 预约邀请 / 好友申请 / 私聊提醒）
 - [x] 模式选择
 - [x] 移动端（好友交互 / 模式选择 / 出装推荐 / 海克斯）
 - [x] 三套主题：简洁浅色、简洁深色、Persona 5


<table>
    <tr>
        <td><img alt="" src="img/index.png"></td>
    </tr>
</table>

## 海克斯强化识别

海克斯大乱斗与斗魂竞技场的强化选项，客户端 API 根本不提供。Futaba 直接截屏识别每张强化卡，把梯度、胜率、本英雄排名、适配装备与通用搭配叠在卡牌下方，选强化不再靠猜。

纯屏幕识别，不读取游戏内存，不修改游戏文件；高精度 OCR 引擎内置，开箱即用。

![](img/hextech-overlay.jpg)

## 选人客户端浮窗

选人阶段不用切出客户端。Futaba 直接在英雄联盟客户端上叠加推荐面板：英雄梯度与胜率、召唤师技能、技能主次、核心出装和海克斯强化。召唤师技能一键应用，核心出装一键写入装备集。

![](img/champ-select-overlay.jpg)

## 主程序

启动英雄联盟客户端之后，你就可以将客户端缩小化，并使用本程序来接管其他所有功能。(在极地大乱斗/海克斯大乱斗下，你可以无视定时设置随意更换英雄)

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

## OP.GG 与海克斯大乱斗数据
当用户进入对局时，会根据用户选中的英雄快速应用版本强势的装备与符文和首选召唤师技能

如果你处在英雄联盟的经典模式(传统匹配/Rank)，会显示选中英雄的counter与逆counter

如果你处在海克斯大乱斗下，默认使用海克斯大乱斗专属数据（可在设置中切回 OP.GG），并提供海斗数据页与强化出装计算器：选择已拿到的强化，组合推荐装备，对局中跟随已选强化推荐下一件

这在移动端均可以查看

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

数据面板可以开成独立小窗随时查看；海克斯大乱斗数据源、选人阶段自动应用（符文 / 召唤师技能 / 装备集）、闪现位置等都可以在设置中调整

![](img/opgg-setting.png)

## 战绩分享

对局结束一键生成分享图，单人战绩或多人同框，带皮肤原画、MVP / SVP 评分、高光标签与海克斯选择；敌我同框时自动切换为 VS 对抗布局

<table>
    <tr>
        <td><img alt="" src="img/share-match.png"></td>
        <td><img alt="" src="img/share-team.png"></td>
    </tr>
</table>

## 主题

提供简洁浅色、简洁深色（石墨灰 + 克莱因蓝）与 Persona 5 三套主题

<table>
    <tr>
        <td><img alt="" src="img/index.png"></td>
        <td><img alt="" src="img/theme-dark.png"></td>
        <td><img alt="" src="img/theme-p5.png"></td>
    </tr>
</table>

## 移动端
你需要在设置页面中开启局域网数据共享，程序将会通过mDNS映射一个futaba.local的域名，你可以访问来控制网页端

考虑到部分玩家的便捷性，你也可以扫描程序页面的二维码来快速访问

这个环节只在本地交互，并不会与外部网络产生任何交互，安全可靠。

拿外卖上厕所的时候也不影响你进入对局和抢英雄了

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

## 致谢

国内镜像加速由 [gh-proxy](https://github.com/hunshcn/gh-proxy) 与 [Xget](https://github.com/xixu-me/Xget) 提供
