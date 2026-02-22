<p align="center">
  <img src="img/logo.png" alt="Futaba" width="200">
</p>

<p align="center">
    <img alt="GitHub Release" src="https://img.shields.io/github/v/release/adv-inn/futaba">
    <img src="https://img.shields.io/github/downloads/adv-inn/futaba/total?style=flat&label=Downloads"></a>
</p>

# Futaba
一款使用Tauri开发的支持双端操作的英雄联盟客户端

本程序发布时将遵循[GPL-3.0](LICENSE)协议，由于此前遇到过恶意用户多次获取源代码并编译自己的版本到互联网售卖，这破坏了我的初衷，所以本项目现阶段并不会开源，会在传播度到达一定程度时进行开源

## 问题反馈/优化建议
QQ群:1080984368
Github issue:[https://github.com/adv-inn/futaba/issues](https://github.com/adv-inn/futaba/issues)

已实现的功能
---
 - [x] 自动接受对局
 - [x] 战绩查询
 - [x] 好友交互(聊天/邀请/预约邀请)
 - [x] 模式选择
 - [x] OP.GG增强适配(海克斯强化推荐/出装推荐/符文推荐/召唤师技能推荐)
 - [x] 对局Counter位自动计算
 - [x] AI局势分析
 - [x] AI对局评价
 - [x] 移动端(好友交互/模式选择/出装推荐/海克斯)


<table>
    <tr>
        <td><img alt="" src="img/index.png"></td>
    </tr>
</table>

## 主程序

启动英雄联盟客户端之后，你就可以将客户端缩小化，并使用本程序来接管其他所有功能。(在极地大乱斗/海克斯大乱斗下，你可以无视定时设置随意更换英雄)

<table>
    <tr>
        <td><img alt="" src="img/create-room.png"></td>
        <td><img alt="" src="img/in-room.png"></td>
        <td><img alt="" src="img/detail.png"></td>
    </tr>
    <tr>
        <td><img alt="" src="img/history.png"></td>
        <td><img alt="" src="img/rank-bp.png"></td>
        <td><img alt="" src="img/diff-detail.png"></td>
    </tr>
</table>

## OP.GG兼容
当用户进入对局时，会根据用户选中的英雄快速应用版本强势的装备与符文和首选召唤师技能

如果你处在英雄联盟的经典模式(传统匹配/Rank)，会显示选中英雄的counter与逆counter

如果你处在海克斯大乱斗下，则会显示选中英雄的强势海克斯符文

这在移动端均可以查看

<table>
    <tr>
        <td><img alt="" src="img/opgg-tier.png"></td>
        <td><img alt="" src="img/opgg-setting.png"></td>
    </tr>
    <tr>
        <td><img alt="" src="img/opgg-detail.png"></td>
        <td><img alt="" src="img/counter-show.png"></td>
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

## 下载

通过[releases](https://github.com/adv-inn/Futaba/releases)，我希望大家可以通过github下载，这样我可以统计实际的下载次数
