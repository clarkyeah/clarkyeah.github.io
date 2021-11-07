### Configure on Linux clash for accessing google
I was so struggling every day when looking for some descent reference material or simply wanted to download some package from a website outside Great Fire Wall. This was later perfectly solved with help from many VPN providers using their client tools. You just click on the client and select which VPN line you want to use and everything turns smooth. However, most of the client tools are developed for Windows or Mac but i have seldom seen any straightforward linux client. Luckily i finally figured out this "Clash" tool. I know may people are already familiar with this but I would like to write down here all the tips just in case you are still new developer and working in China.

### Clash install
从如下地址下载clash

https://github.com/Dreamacro/clash/releases

执行 `cd && mkdir clash` 在用户目录下创建 clash 文件夹。

下载适合的 Clash 二进制文件并解压重命名为 `clash`

一般个人的64位电脑下载 clash-linux-amd64.tar.gz 即可。

在终端 `cd` 到 Clash 二进制文件所在的目录，执行 `wget -O config.yaml [clash订阅地址]`

上文中[ ]中的文字需要购买相应供应商的订阅。这里config.yaml如果在linux环境下无法下载（这个可能时下载的时候网络问题），可以在window下先预先下载好。

执行 `./clash -d .` 即可启动 Clash，同时启动 HTTP 代理和 Socks5 代理。

如提示权限不足，请执行 `chmod +x clash`

启动clash后将其设为系统代理

打开系统设置，选择网络，点击网络代理右边的 ⚙ 按钮，选择手动，填写 HTTP 和 HTTPS 代理为 `127.0.0.1:7890`，填写 Socks 主机为 `127.0.0.1:7891`，即可启用系统代理
