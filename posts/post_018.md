# 个人阅览周刊【第十八期】

![2012年8月 圆明园](https://i.loli.net/2020/03/24/PdAb2Wlih7qRySx.jpg)

#### 0、11个世界上最受欢迎的幸运数字

2014年，英国作家亚历克斯•贝洛斯(Alex Bellos)在全球范围内进行了一项3万人参与的调查，列出了世界上最幸运的数字。

以下是排名前11的幸运数字榜单。

```
7、3、8、4、5、13、9、6、2、11、42
```

`7` 成为了最受欢迎的幸运数字，在西方国家中 `7` 是普遍受欢迎的数字，老虎机上的数字 `7` 可以证明这一点。

`8` 在东方文化中是一个与财富相关的吉利数字，特别是在中国和日本。

而西方国家中普常见的不吉利的数字 `13` ，和东方国家中不受欢迎的数字 `4` 都出现在榜单中，作者归因于互联网投票中“叛逆”行为的低风险与无后果的局限。

--[11 popular lucky numbers world](https://11points.com/11-popular-lucky-numbers-world/)

#### 1、iOS 应用推荐

- 界面清新的全屏时钟

![](https://i.loli.net/2020/03/24/89kziNJxhIMDqfy.png)

扫描二维码打开 App Store 下载[「桌面时钟」：](https://apps.apple.com/cn/app/%E6%A1%8C%E9%9D%A2%E6%97%B6%E9%92%9F-%E5%85%A8%E5%B1%8F%E7%94%B5%E5%AD%90%E6%97%B6%E9%92%9F/id1385371863)

![](https://i.loli.net/2020/03/24/3sV1ikLEfDabcgW.png)

- 恐龙造型的儿童计算器

![](https://i.loli.net/2020/03/24/ZyMuQm79altSfHp.png)

扫描二维码打开 App Store 下载[「恐龙语音计算」：](https://apps.apple.com/cn/app/%E6%81%90%E9%BE%99%E8%AF%AD%E9%9F%B3%E8%AE%A1%E7%AE%97-%E5%8F%A3%E7%AE%97%E8%AE%AD%E7%BB%83/id1314360935)

![](https://i.loli.net/2020/03/24/lQEeNvRWALY6UsS.png)


#### 2、macOS 去除窗口截屏中的阴影

![](https://support.apple.com/library/content/dam/edam/applecare/images/en_US/accessories/Keyboards/mac-key-combo-diagram-shift-command-4-space.png)

用 `Shift+Command+4` 和`空格键`，将指针会变为相机图标可以捕捉窗口。

**要从截屏中去除窗口的阴影，请在点按时按住 `Option 键`。**

--[在 Mac 上拍摄截屏](https://support.apple.com/en-us/HT201361)

#### 3、At a risk 而不是 On a risk

固定词组是 `on your onw risk`，英语母语的人从不会说 `on your own risk`。

--['At your own risk' or 'On your own risk'?](https://ell.stackexchange.com/questions/13918/at-your-own-risk-or-on-your-own-risk)

#### 4、查找 iOS 项目中使用的类

2020年4月起，苹果不再接受使用`UIWebView`的新提交的App，2020年12月起不再接受使用`UIWebView`的应用更新。

如何查找项目中（特别是第三方库）是否使用了`UIWebView`？

1. 对于使用源代码的库（如Cocoapods）可使用`grep`命令

```shell
❯ grep -r 'UIWebView' .
./RxCocoa/iOS/UIWebView+Rx.swift://  UIWebView+Rx.swift
./RxCocoa/iOS/UIWebView+Rx.swift:    extension Reactive where Base: UIWebView {
```

2. 对于不包含源码的第三方`.framework`，可用`nm`命令查找符号表

```shell
❯ nm AWSDK.framework/AWSDK | grep -i UIWebView
                 U _OBJC_CLASS_$_UIWebView
                 U _OBJC_CLASS_$_UIWebView
0000000000002a00 S __OBJC_LABEL_PROTOCOL_$_UIWebViewDelegate
0000000000002998 D __OBJC_PROTOCOL_$_UIWebViewDelegate
```

--[Determining which frameworks use UIWebView](https://blog.kulman.sk/determining-which-frameworks-use-uiwebview/)


#### 5、As Time Passes

By Jenni-Fiere M. Bivens

```
As the seconds pass,
We look back
At what our lives have held.

As the minutes pass,
We see what fell through the cracks.
Parts of our lives we withheld.

As the hours pass,
We think of what we learned,
What we have taught,
What we have forgot.

As the days pass,
We wish a lot could be returned.
We wish we would have never fought
You hope they forget me not.

As years pass,
You stand alone.
They have all grown,
Married and gone
Or on their own.

As your life passes,
You stand proud,
Looking how well they raise their own.
You did well.
Live on...
```

--[Life Lesson Poem](https://www.familyfriendpoems.com/poem/as-time-passes)

【完】

**Reference:**
```
桌面时钟：https://apps.apple.com/cn/app/%E6%A1%8C%E9%9D%A2%E6%97%B6%E9%92%9F-%E5%85%A8%E5%B1%8F%E7%94%B5%E5%AD%90%E6%97%B6%E9%92%9F/id1385371863
恐龙语音计算：https://apps.apple.com/cn/app/%E6%81%90%E9%BE%99%E8%AF%AD%E9%9F%B3%E8%AE%A1%E7%AE%97-%E5%8F%A3%E7%AE%97%E8%AE%AD%E7%BB%83/id1314360935
在 Mac 上拍摄截屏：https://support.apple.com/en-us/HT201361
'At your own risk' or 'On your own risk'?：https://ell.stackexchange.com/questions/13918/at-your-own-risk-or-on-your-own-risk
Determining which frameworks use UIWebView：https://blog.kulman.sk/determining-which-frameworks-use-uiwebview/
Life Lesson Poem：https://www.familyfriendpoems.com/poem/as-time-passes
```