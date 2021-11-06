## 点滴记录开发 Tao's Pages

我用这个服务记录在平时开发中的一些操作经验，一方面自己忘记的时候可以重新温习，如果对于你们也有帮助，那似乎也很棒。这里并一定是原创，因为基础的知识遍布网络，所以我只是按照自己的工作和生活中的遇到的情形，将这些知识组织起来。

### 1. Macbook Pro 使用和安装homebrew

Macbook Pro with Apple Silicon 是苹果第二次变更器CPU架构，homebrew有尝试性支持基于Arm架构的程序的安装。此时的homebrew安装分成了安装基于arm架构的homebrew安装和支持x86_64架构homebrew的安装

#### 1.1 使用如下命令安装支持arm架构的homebrew
```markdown

% cd /opt
% mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
% sudo chown -R $(whoami) /opt/homebrew

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```
然后将如下文件内容添加
```markdown
% sudo nano /etc/path
Add the two paths
/opt/homebrew/bin
/opt/homebrew/opt
```
#### 1.2 安装基于x86_64架构homebrew

这一步的安装受到源的影响，及时有翻墙工具也无法成功。
我们首先需要把install.sh文件（也就是官网给出的安装脚本链接的地址）下载
https://raw.githubusercontent.com/Homebrew/install/master/install.sh
然后将文件中如下内容修改为中科大的源
OMEBREW_BREW_DEFAULT_GIT_REMOTE="https://mirrors.ustc.edu.cn/brew.git"
HOMEBREW_CORE_DEFAULT_GIT_REMOTE="https://mirrors.ustc.edu.cn/homebrew-core.git"
保存到桌面后，运行
arch -x86_64 /bin/bash ~/Desktop/install.sh

#### 1.3 设置环境变量(zsh shell为例）
nano ~/.zshrc, 将如下内容添加进去
```markdown
export PATH="/opt/homebrew/bin:/usr/local/bin:$PATH"
alias ibrew='arch -x86_64 /usr/local/bin/brew'
```
在终端中执行source !/.zshrc

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/clarkyeah/clarkyeah.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
