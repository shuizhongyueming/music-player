# music-player

a muisc-player based on [soundManager2](https://github.com/scottschiller/SoundManager2) and [swaggplayer](https://github.com/jray/swaggplayer)

## 说明

本工具的初始绝大多数代码都是来源于swaggplayer，但是对其代码做了点初始处理：

+ 移除自行定义的require
+ 把绑定写死到里面的soundManager2移出来由开发者自行调用

## 特色功能介绍

### 音乐延迟加载

在swaggplayer中，会一开始就自动加载完毕所有的音乐。这样对带宽来说是一个很大的浪费。

在本工具里面，是在播放当前音乐到一半的时候，再开始加载下一个。等下一个播放一半的时候，加载下下一个。依次类推

### 重复播放功能

在swaggplayer中，会在播放到列表最后一个之后结束。

在本工具里面，新增了个isLoop的选项，由调用者决定是循环播放还是播放一次。

## 修改历史

### 1.0

+ 延迟加载音乐文件
+ 重复播放
+ 修复player.play(0) 变成暂停的bug
+ AMD CMD 支持
