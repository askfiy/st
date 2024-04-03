# README

## Introduction

A `st` simple-terminal built by yourself.

Basically they can meet their daily needs.

Since I'm using it with tmux, I didn't add a scroll patch.

Install the following fonts:

```zsh
$ yay -S ttf-recursive
$ yay -S nerd-fonts-go
```

At the same time, some default buttons have been modified:

- ControlMask + XK_0    : font-resize
- ControlMask + XK_equal: font-size + 1
- ControlMask + XK_minus: font-size - 1

For some monospaced fonts, `st` doesn't seem to be well supported. When you encounter font problems (cjk), please do not file an issue, and try to use the font configured by default in the repository, which can work well.

## builds and patches

Edit the 'config.h' file to update your config and rebuild 'st' with the following command:

```zsh
$ sudo make clean install
```

This repository uses the following patches, and the patch files are in the [patches](./patches) directory:

- st-alpha-osc11-20220222-0.8.5.diff
- st-anysize-20220718-baa9357.diff
- st-boxdraw_v2-0.8.5.diff
- st-charoffsets-20220311-0.8.5.diff
- st-font2-0.8.5.diff
- st-glyph-wide-support-boxdraw-20220411-ef05519.diff
- st-hidecursor-0.8.3.diff
- st-undercurl-0.9-20240103.diff

To add a new patch, you can use the 'patch' command:

```zsh
$ patch -p1 < patches/example_patch.diff
```

For more patches, see：[st.suckless.org](https://st.suckless.org/patches/)
