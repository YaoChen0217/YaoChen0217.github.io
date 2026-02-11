# Arch Linux 安装与使用 Wiki

本 Wiki 用于记录 Arch Linux 的安装步骤与日常使用经验，方便后续查阅与复现。

## 目录

- [安装前准备](#安装前准备)
- [系统安装](#系统安装)
- [基础配置](#基础配置)
- [常用软件安装](#常用软件安装)
- [问题与解决方案](#问题与解决方案)
- [参考资料](#参考资料)

---

## 安装前准备

- 下载 Arch Linux 官方镜像
- 制作启动 U 盘（推荐使用 balenaEtcher 或 dd 命令）
- 备份重要数据

## 系统安装

1. 启动进入 Live 环境
2. 连接网络（`iwctl` 或 `wifi-menu`）
2.1. 这步骤小白可以选择用archinstall了，换源教程在下面
2.1.1 换源 
    reflector --verbose --country China --sort rate --save /etc/pacman.d/mirrorlist
    !!!换源后在archinstall里的mirror不要改！！！
    删掉浙大，据说是容易被ban
    sed -i 'zju/d' /etc/pacman.d/mirrorlist
    然后你可以archinstall了
3. 分区与格式化（`fdisk`/`parted` + `mkfs`）
4. 挂载分区
5. 安装基础系统（`pacstrap`）
6. 生成 fstab（`genfstab`）
7. 切换到新系统（`arch-chroot`）
8. 设置时区、语言、主机名、root 密码
9. 安装引导程序（如 `grub`）

## 基础配置

- 添加新用户
- 配置 sudo 权限
- 配置网络（NetworkManager）
- 配置镜像源（`reflector`）跟着我上一步换源的在archinstal里就不要选了

## 常用软件安装

- 图形界面（如 GNOME/KDE/xfce）
- 输入法（fcitx5）
- 浏览器、终端、编辑器等

##美化

-shorin niri 不方便放出来，去bili或者github搜吧，可以先在archinstall安装niri然后挂魔法

## 问题与解决方案

- 常见启动问题
- 驱动安装
- 字体与显示优化

## 参考资料

- [Arch Wiki](https://wiki.archlinux.org/)
- [Arch 安装指南](https://wiki.archlinux.org/title/Installation_guide)
