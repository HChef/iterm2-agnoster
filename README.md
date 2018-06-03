## 安装 iterm2
官网：https://www.iterm2.com/

## 安装 Oh My Zsh
1. 通过 `cat /etc/shells` 可以查看当前系统可以使用哪些 shell
```bash
# List of acceptable shells for chpass(1).
# Ftpd will not allow users to connect who are not using
# one of these shells.

/bin/bash
/bin/csh
/bin/ksh
/bin/sh
/bin/tcsh
/bin/zsh
```

2. 通过 `echo $SHELL` 可以查看正在使用的 Shell
```bash
/bin/zsh
```
如果当前不是 `zsh`，可以通过 `chsh -s /bin/zsh` 切换

3. 安装 Oh My Zsh
官网：http://ohmyz.sh/
```bash
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## 配置 agnoster 主题
在线预览地址：https://github.com/robbyrussell/oh-my-zsh/wiki/Themes. 
### 安装 Powerline
官方地址：https://github.com/powerline/fonts
```bash
# clone
git clone https://github.com/powerline/fonts.git --depth=1
# install
cd fonts
./install.sh
# clean-up a bit
cd ..
rm -rf fonts
```
### 特殊字体安装
- iterm2 -> Preferences -> Profiles -> Text -> Font -> Change Font -> 12pt Meslo LG L DZ Regular for Powerline
- iterm2 -> Preferences -> Profiles -> Text -> Font -> Use a different font for non-ASCII text -> Non-ASCII Font -> Change Font -> 12pt Meslo LG L DZ Regular for Powerline

### 调整配色方案
iterm2 -> Preferences -> Profiles -> Color Presets -> Solarized Dark

通过 `echo "\ue0b0 \u00b1 \ue0a0 \u27a6 \u2718 \u26a1 \u2699"` 可以测试安装

## 修改主题
通过 `vim ~/.zshrc` 设置 `ZSH_THEME="agnoster"`

> 参考：http://www.siguoya.name/pc/home/article/256 
