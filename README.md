## 点滴记录开发 Tao's Pages

我用这个服务记录在平时开发中的一些操作经验，一方面自己忘记的时候可以重新温习，如果对于你们也有帮助，那似乎也很棒。这里并一定是原创，因为基础的知识遍布网络，所以我只是按照自己的工作和生活中的遇到的情形，将这些知识组织起来。

### 1. Macbook Pro 使用和安装homebrew

Macbook Pro with Apple Silicon 是苹果第二次变更器CPU架构，homebrew有尝试性进行支持。

使用如下命令安装homebrew
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
F

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/clarkyeah/clarkyeah.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
