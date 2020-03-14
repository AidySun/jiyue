# 个人阅览周刊【第十七期】

![2017年3月 故宫](https://i.loli.net/2020/03/15/3oenLxDCu61VrUH.jpg)

#### 0、从收音机里下载游戏

![PET2001-TRS80-AppleII-磁带](https://i.loli.net/2020/03/08/zmIMtSCNvW2YpEl.jpg)

1977年，世界上第一台微处理器驱动的个人电脑发布，包括 Apple II、Commodore PET、TRS-80等。由于当时的硬盘相当昂贵，这些电脑有一个共同特点：使用录音带（audio cassettes）来存储。

荷兰全国公营广播电视机构（Nederlandse Omroep Stichting）的工程师们意识到了一些不可思议的事情。由于计算机程序和视频游戏都储存在音频磁带中，这意味着它们的数据可以轻松地通过无线电传输。 他们开始制作节目和电子游戏，并设立广播，让人们可以在自己的个人电脑上“下载”游戏。

韦斯特电台（Radio West）在英国的首次播出是一张明星 Cheryl Ladd 的 40 * 80 像素的黑白照片。

后来出现的 16 位计算机处理器速度更快，需要更多的存储能力，这意味着磁带存储不再可行，制造商将开始使用软盘和硬盘来进行计算机大容量存储。这也使得这种有趣、新潮的数据传输方式终结在 80 年代末。
直到 1991 年 Wi-Fi 发明，才又出现广泛使用的无线传输游戏数据的方法。

所以，在20世纪80年代早期，打开收音机意味着你可能会听到悠扬的歌曲，也有可能听到让很多人不明所以的、刺耳、尖锐的哔哔声。

-- [You Could Download Video Games From the Radio in the 1980s](https://interestingengineering.com/you-could-download-video-games-from-the-radio-in-the-1980s?utm_source=rss&utm_medium=article&utm_content=08032020)

#### 1、Windows 效率工具

##### Q-Dir

![Q-Dir](https://i.loli.net/2020/03/09/DOYx2V7SeZjwAJB.png)

资源管理器替代应用，支持多窗口分割、每个窗口支持多Tab、拖拽复制等。 
http://www.softwareok.com/?Download=Q-Dir

##### Everything

![Everything](https://i.loli.net/2020/03/09/fQmB4sWUjl5x9yD.jpg)

本地文件搜索工具，比系统自带搜索速度快，支持正则表达式等。 
https://www.voidtools.com

#### 2、无线连接 iPhone 到 Xcode

![](https://help.apple.com/xcode/mac/9.0/en.lproj/Art/debug_network_iPhone_connect.png)

1. Xcode 里选择菜单 “窗口 > 设备和模拟器“，选择 “设备” 标签。
2. 用数据线连接 iPhone 与 Mac。
3. 勾选上 “通过网络连接”（Connect via network）。
4. 断开数据线。

--[Pair a wireless device with Xcode](https://help.apple.com/xcode/mac/9.0/index.html?localePath=en.lproj#/devbc48d1bad)

#### 3、谨慎使用 git checkout

`git checkout` 除了切换分支，还有一个功能就是恢复工作树上的文件。

危险的地方在于对本地未提交的修改，`git checkout` 命令在覆盖修改之前不会有任何的提示，会有丢失本地修改的风险。并且 `git` 没有恢复、撤销此类修改的方式，这并非设计缺陷，属于使用者的人为失误。

如同众所周知的 `rm` 命令类似，对这个潜在风险可以用如下的 alias 预防：

```
alias gco="git stash push -m \"git checkout backup\";git stash apply; git checkout \"$@\"" 
```

- `git stash push -m "git checkout backup"` - 会隐藏（快照）本地修改，并加 comment
- `git stash apply` - 将 stash 的修改应用回工作树
- `git checkout` - 执行最终的 checkout 

每次 `checkout` 都会有一个 `stash`，所以本地修改不会丢失。

-- [Get back the changes after accidental checkout?](https://stackoverflow.com/questions/2961240/get-back-the-changes-after-accidental-checkout)

#### 4、网课App被小学生一星”好评“

受新冠肺炎疫情的影响导致全国大中小学延迟开学，不少学校实行在线直播的云课堂形式开展网课。导致阿里巴巴的在线办公、直播工具「钉钉」在各大应用市场遭受大量来自小学生的一星“好评”。App Store 上的评分一天内从 4.9 跌倒 1.4。

钉钉官方于2月16日发布了一个名为《钉钉本钉，在线求饶》的视频跪求“少侠们饶命吧，大家都是我爸爸”、“此生无悔入钉钉，五星求一次付清”。

--[钉钉本钉，在线求饶](https://www.bilibili.com/video/av89441613)

#### 5、张国荣《春夏秋冬》

幻夏海峡：`你在，春华秋实夏蝉冬雪。 你不在，春夏秋冬。`

![](https://i.loli.net/2020/03/15/9MJ34gG7DtbajuL.jpg)

--[春夏秋冬](https://music.163.com/song?id=186453)

```
You Could Download Video Games From the Radio in the 1980s：https://interestingengineering.com/you-could-download-video-games-from-the-radio-in-the-1980s?utm_source=rss&utm_medium=article&utm_content=08032020
Pair a wireless device with Xcode：https://help.apple.com/xcode/mac/9.0/index.html?localePath=en.lproj#/devbc48d1bad
钉钉本钉，在线求饶：https://www.bilibili.com/video/av89441613
春夏秋冬：https://music.163.com/song?id=186453
```
