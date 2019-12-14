# 个人阅览周刊【第十期】

![](https://i.loli.net/2019/12/14/ZkHRinP76NWeFsw.jpg)

#### 0、终极密码：「量子通信」

##### 凯撒密码

凯撒大帝——罗马帝国的第一位独裁者,公元前 54 年，想出加密算法——凯撒密码。

凯撒密码的原理现在看来很简单，就是： **替换！** 比如 A->D，B->E。只要收发双方都知道替换表，就能轻松加密和解密。

![](https://i.loli.net/2019/12/13/ItcVFmW8COsaxHw.jpg)

二战时期，德国人谢尔比乌斯造就了让希特勒成也萧何败也萧何的谍报神器——英格玛密码机（ENIGMA）。

这是世界首台全自动的加密机器，基础原理和恺撒密码相同，但字符替换方式是更高级。如果连打 3 个 A，恺撒密码的密文可能是 DDD，但英格玛的密文却可能是 BDA。

![](https://i.loli.net/2019/12/14/QJLfmknOoMpHre6.jpg)

阿兰·图灵 1941 年发明的解码器炸弹（BOMBE）干掉了英格玛，从此军情六处把德军的情报兜了个底朝天。

而图灵的这台机器，就是世界上第一台计算机。

到此为止的方法都是 **「对称加密」** ：加密和解密是互逆的，只要知道如何加密，就一定知道如何解密。

##### RSA 技术

RSA是 **「非对称加密」** ：我可以把加密方法公开（公钥），但解密算法（私钥）只有我一个人知道。

*RSA 为什么能做到「知道加密算法也推不出解密算法」？*

这基于一个数学事实：将两个大素数相乘十分容易，但对乘积因式分解、即还原成两个素数却极其困难，而且数字越大，困难级别指数上升。

解密靠的是私钥，而破解私钥的唯一方法是猜出公钥是哪两个数字的乘积，因此，把大数乘积作为公钥公开是非常安全的。

举个例子：37×97=3589 小学生都会手算，但是，问 3589 是哪两个数的乘积？你回答得出来吗？你可以挑战一下这个：

![rsa-sample.jpeg](https://i.loli.net/2019/12/13/8g2GrxtD1NOcWi9.jpg)

上面那个用来吓人的数字，有 232 位（768 比特），是当今地球上计算机能分解的最大整数。现在大部分网站使用的 https 加密证书，长度有 2048 比特！

##### 量子通信

无论相隔多远的距离，处于「纠缠态」两个孪生粒子零延迟、发生同步反应。这就是*「超距作用」*。

粒子 A 的自旋态始终和 B 的相反，如果把孪生粒子看成一对魔法硬币放在两地，在地球观测硬币 A 发现是正面向上，火星上的粒子 B 会因此而瞬间变成正面向下，相当于接收到了地球发来的一个比特。通信双方重复以上步骤、通过「抛量子硬币」传送信号的方式，就叫作*「量子通信」*。

但是，每次硬币是正是反，是个完全随机事件，无法控制。所以没办法直接利用「超距作用」发送信息。要想用量子传有意义的东西，解决的办法只有一个：配合使用传统通信方式再发一次纠正码。

比如，想要发送的是「正正反反」，通过观测量子通信得到的是「反正反正」，之后再用微信给对方补个留言「错对对错」，告诉对方哪些信号是发错的，让他自己纠正。 爱因斯坦当年担心的「超光速通信」问题，就这样被「随机性乱码」解决了。

更重要的一点是量子通信还自带 **“反窃听”** 属性。


##### 量子计算机

P 是否等于 NP 实际上问的是：P是在一定时间内能够解决的问题，NP是在一定时间内验证答案是否正确的问题。

开始人们觉得，P 显然不等于 NP。比如，「找出大数 53308290611 是哪两个数的乘积？」很难，但要问「224737 是否可以整除 53308290611？」这小学生都会算。

这正是密码学领域所依赖的：加密（相乘）容易解密（因式分解）难。

如果 P=NP，就势必存在一种算法，使得对 53308290611 做因式分解和验证 224737 是否是因子一样快（加密和解密同样容易）。

在某种特定的计算模型下： P=NP 竟然是成立的！这就是 **「量子计算机」** 。

和非 0 即 1 的传统计算机不同，像薛定谔的那只「既死又活」的猫一样，量子计算机的「量子比特」可以处于「既是 0 又是 1」的量子态：量子叠加态。

比如说一个简单的程序：如果Ta是男孩，就选蓝色；如果Ta是女孩，就选粉色。

在传统计算机中，运行一次只能执行一个逻辑分支，要么男孩，要么女孩。想要两个分支都走到，最少需要运行 2 次。

![](https://i.loli.net/2019/12/14/862x4auJqmzGKNt.jpg)

但对于量子计算机，变量 Ta 是量子叠加态，既是男孩，又是女孩，这就意味着，普通计算机要算 2 次的程序，量子计算机只需算 1 次。

把量子比特加到 100 个以上，那么，当今地球上 所有计算机同时运行 100 万年的工作量，量子计算机干完只要几分钟！

##### 量子加密

1941 年，信息论的祖师爷香农，在数学上严格证明了：不知道密码就绝对无法破解的安全系统，是存在的。

只需符合以下 3 个条件：

1. 一次一密：每传一条信息都用不同的密钥加密
1. 随机密钥：生成的密钥是完全随机的，不可预测
1. 明密等长：密钥长度至少要和明文（传输的内容）一样长

在当下的技术条件下，「看上去几乎不可能实现」的三大要求，简直就是为量子通信量身定做的。和 RSA 等依赖计算复杂度增加破解成本的加密方式不同， **量子加密通信是「无条件安全」的** ，对量子计算机的恐怖计算能力先天免疫。

1994 年，全球 1600 个工作站同时运算了 8 个月，才破解了 129 位的 RSA 密钥。若用同样的算力，破解 250 位 RSA 要用 80 万年，1000 位则要 10^25 年。而对于量子计算机，1000 位数的因式分解连 1 秒钟都不到。

虽然量子比特的制备极为困难，目前最高纪录只有 5 个量子比特。

2016年8月，我国成功发射世界首颗量子科学实验卫星——「墨子号」；工商银行在北京用上了量子通信做同城加密传输；阿里云的数据中心已经在用量子通信组网。

![](https://i.loli.net/2019/12/14/SxcRuobFTlKO1I3.jpg)

——[猫、爱因斯坦和密码学：我也能看懂的量子通信](https://www.zhihu.com/pub/book/119555203)


#### 1、macOS「系统偏好设置」中不可用图标

我有一台工作用的 MacBook Pro（macOS Mojave 10.14），系统里有些公司定制的设置。

「系统偏好设置」里面的「系统更新」不可用，图标是灰的。通过 About This Mac 上的 Software Update... 尝试，遇到如下信息：

![macosUpdateErr.png](https://i.loli.net/2019/12/11/rMGLK7PoVh8jwCE.png)

解决方法如下：

0. 确保「系统偏好设置」未运行
1. 打开“应用程序”文件夹，然后找到「系统偏好设置.app」。
2. 右键单击 「系统偏好设置.app」，然后选择“创建重复项”。
3. 右键单击「系统偏好设置-copy.app」，然后选择“显示程序包内容”。
4. 删除文件 `Contents/Resources/NSPrefPaneGroups.xml`
5. 然后双击「系统偏好设置copy.app」来运行它。 所有首选项窗格似乎都消失了！
6. 在「系统偏好设置」应用程序中，单击屏幕顶部的“查看”菜单。 现在可以从“查看”菜单访问所有首选项窗格。

![sysPrefViewMenu.png](https://i.loli.net/2019/12/11/ntyeiKGjfkLqc6z.png)

7. 任何时候您需要访问禁用的系统偏好设置时，只需使用「系统偏好设置copy.app」。

——[Accessing Mac OS X Grayed-out Preference Panes](http://walkingtowel.org/2010/02/25/accessing-mac-os-x-leopard-greyed-out-preference-panes/)

#### 2、fine with/to me

`X` is fine with me means you are OK with something happening.
> The project is fine with me = I'm OK with the project existing or moving forward.

`X` looks fine to me means you approve of the way something looks or is. But you can't use this to approve of an event or something happening.
> The project looks fine to me = The current state or progress of the project is OK. I'm already OK with the project existing (or maybe I'm not and I hate working on this project).

——[Difference between “It's fine with me” and “it's fine to me”?](https://ell.stackexchange.com/questions/100879/difference-between-its-fine-with-me-and-its-fine-to-me)

#### 3、计算机字符集发展简史

##### ASCII（美国信息交换标准代码）

最开始只有 32-127 被用到，包括英文字母、数字和符号。比如空格是32，A是65，a是97。

![](https://i.loli.net/2019/11/14/ZITPYWiaBMXKdlA.png)

计算机的最小寻址单位是一字节（8个比特位），可表示的数值范围是 0-255。

127只需要7个比特位就能表示，所以还有一比特位空闲（值 128-255）。

这些空闲的值在不同的语言地区被赋予不同的用法。比如美洲地区用130来表示(é)，但是以色列的电脑用130来表示希伯来字符(ג)。那么在美洲电脑上显示的单词`résumés`，在以色列的电脑上就成了 `rגsumגs`。这导致了同一文档内容在不同的电脑上可能有不同的显示。

##### Code Page（代码页）

代码页的128以下是一样的，只有128以上不同。如，以色列使用code page 862，希腊使用 code page 737。

这样在同一电脑上可以有多个不同的代码页可供选择。

##### DBCS（双字节字符集）

亚洲语言的字符没办法用一字节（8比特）表示。
DBCS 是对英文字符使用单字节，其他字符（如中日韩文）使用双字节。

但是使用DBCS对字符串进行操作和处理比较麻烦，非常容易出错。

##### Unicode

一套可以适用于全世界所有国家的字符集。

Unicode 中对所有字母表中的每个字符分配一个数字——code point，是一个概念定义。

比如code point 是 U+0041的字符 A，它与B不同，也不同于a，但是斜体的A、粗体的A、正常的A，它们应该是一样的，都是字符A。

不同字体文件决定的是：字符A具体显示出来时什么样子。

##### UCS-2 / UTF-16

那么字符串 He 用 Unicode 可以表示成 `00 48 00 65`。当然也可以是 `48 00 65 00`。因为特定的 CPU 用特定的顺序会更快。

这两种表示分别是——大端序和小端序。为了区分，在文本开头加上字节顺序标记位，大端序用 FE FF，小端序用 FF FE。

这种方式对于新生成的文档没有任何问题，但是**无法兼容已有的ASCII和DBCS文档**。

##### UTF-8

所以，出现了另一种实现 Unicode 字符集的系统——UTF-8。它采用变长的编码，用一个字节存储 code point 0-127，对 128 以上的使用 2字节、3字节，最多到 6 字节。

**对于英文文档来说完全兼容**，UTF-8 和 ASCII是一样的，不需要任何转换。

##### Encodings（编码）

Unicode是字符集，上面说的 UCS-2、UTF-8等是实现Unicode的方法——Encoding。

![](https://i.loli.net/2019/11/14/vRPyLox4Th7Xksj.jpg)

所以， 必须确定所用的Encoding才能正确处理一个字符串 。

在浏览器中看到这每个网页会有Encoding的信息：

```
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
```

可是，在不知道encoding的情况下怎么去读这个HTML文件来取到encoding的信息呢？

绝大多数encoding对 32-127 的code point的处理方式是一样的，可以把文件开头的内容默认当作ASCII来处理。所以encoding信息越早出现越好，避免出现在任何code point大于127的字符之后。

——[每个程序员都应该知道的字符集发展简史](https://mp.weixin.qq.com/s/79xuaAxuJLxxYbhAo8VN5A)

#### 4、公主为你加冕

![](https://i.loli.net/2019/12/14/una3h1viWFkfBD2.jpg)

——[罗马假日 Roman Holiday](https://movie.douban.com/subject/1293839/)


【完】

**Reference:**
```
猫、爱因斯坦和密码学：我也能看懂的量子通信：https://www.zhihu.com/pub/book/119555203
Accessing Mac OS X Grayed-out Preference Panes：http://walkingtowel.org/2010/02/25/accessing-mac-os-x-leopard-greyed-out-preference-panes
Difference between “It's fine with me” and “it's fine to me”?：https://ell.stackexchange.com/questions/100879/difference-between-its-fine-with-me-and-its-fine-to-me
每个程序员都应该知道的字符集发展简史：https://mp.weixin.qq.com/s/79xuaAxuJLxxYbhAo8VN5A
罗马假日 Roman Holiday：https://movie.douban.com/subject/1293839/
```

👉 [**有任何想说的话欢迎到Github提Issue**](https://github.com/AidySun/jiyue/issues)
