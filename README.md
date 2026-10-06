# 一加手电筒增强版 · 简体中文版

> 基于 [Bartixxx32/Opflashcontrol-app](https://github.com/Bartixxx32/Opflashcontrol-app) 修改的一加手机手电筒亮度控制应用，界面全面汉化，操作更简洁。

[![Release](https://img.shields.io/github/v/release/bardenjohn383-rgb/Opflashcontrol-app?label=release)](https://github.com/bardenjohn383-rgb/Opflashcontrol-app/releases)

## 简介

OnePlus Flash Control 是一款专为 **已 root 的一加手机** 设计的 Android 应用，可以精细控制双色温 LED 闪光灯的亮度。

本仓库是在原作者项目基础上的修改版，主要做了三件事：把亮度控制合并成一个滑块、界面改为简体中文、简化状态栏快捷开关。核心的灯光控制功能来自原项目，感谢原作者的开源贡献。

## 与原版的区别

| 项目 | 原版 | 本修改版 |
| --- | --- | --- |
| 主界面亮度 | 总亮度、白光、黄光多个滑块 | 只有一个"总亮度"滑块（0–500） |
| 开灯逻辑 | 可分别设置白光、黄光亮度 | 两颗灯同时使用总亮度 |
| 界面语言 | 随系统语言（含波兰语等） | 固定显示简体中文，与系统语言无关 |
| 状态栏快捷开关 | 单击切换亮度档位，支持双击 | 单击即开/关，开启时使用应用内设定的"默认亮度" |

### 详细说明

1. **亮度合并**
   主界面只剩一个"总亮度"滑块（0–500），白光、黄光滑块已删除。开灯时两颗灯都使用总亮度。默认隐藏的四灯界面保持不变。
2. **简体中文**
   界面文字、提示、报错信息全部改为中文。波兰语资源已删除，所以无论手机系统是什么语言都显示中文。应用名称和右下角的 "Buy me a coffee" 保留原样（它属于原作者）。
3. **状态栏开关**
   单击即开或关，开启时使用应用中设定的"默认亮度"。亮度档位循环和双击功能已移除。

## 使用要求

- 一加（OnePlus）手机，带双色温 LED 闪光灯
- 已获取 **root 权限**（应用需要通过 root 写入灯光亮度）
- Android 系统（具体版本要求以原项目和实际测试为准）

> ⚠️ 本应用需要 root 权限并直接操作硬件相关节点。请在了解风险的前提下使用，使用不当造成的任何问题由使用者自行承担。

## 安装

1. 打开 [Releases 页面](https://github.com/bardenjohn383-rgb/Opflashcontrol-app/releases)，下载最新版本的 APK。
2. 在手机上安装（如提示"未知来源"，请在系统设置中允许安装）。
3. 首次打开时授予 root 权限。

## 使用方法

1. **应用内**：拖动"总亮度"滑块调整亮度，点击开关开灯。
2. **默认亮度**：在应用中设定默认亮度，状态栏开关开启时会使用这个值。
3. **状态栏快捷开关**：下拉通知栏，编辑快捷设置，把手电筒磁贴拖到面板里。之后单击即可开关。

## 从源码构建

```bash
git clone https://github.com/bardenjohn383-rgb/Opflashcontrol-app.git
cd Opflashcontrol-app
./gradlew assembleRelease
```

构建产物在 `app/build/outputs/apk/` 下。也可以直接用 Android Studio 打开项目构建。

## 反馈

遇到问题或有建议，欢迎在 [Issues](https://github.com/bardenjohn383-rgb/Opflashcontrol-app/issues) 中反馈。反馈时请附上手机型号和系统版本，方便排查。

## 致谢与声明

- 原项目：[Bartixxx32/Opflashcontrol-app](https://github.com/Bartixxx32/Opflashcontrol-app)，作者 Bartixxx32。核心功能和大部分代码归原作者所有。
- 本修改版仅对界面、亮度控制逻辑和状态栏开关做了调整，与原作者无官方关联。
- 许可证：沿用原项目的开源许可证，详见仓库中的 `LICENSE` 文件。
