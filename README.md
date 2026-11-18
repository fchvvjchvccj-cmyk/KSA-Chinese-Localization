# Kitten Space Agency 简体中文汉化

适用版本：**2026.11.16.5901**（Windows）。这是非官方简体中文汉化补丁。请从 [2026.11.16.5901 Release](https://github.com/fchvvjchvccj-cmyk/KSA-Chinese-Localization/releases/tag/2026.11.16.5901) 下载 `KSA-zh-CN-2026.11.16.5901.zip`。

## 安装、启动与还原

1. 确认安装的是 RocketWerkz 官方 5901 游戏，并正常退出游戏。
2. 完整解压压缩包。双击 **简体中文启动.cmd**，首次使用时粘贴包含 `KSA.exe` 的游戏安装目录。普通首次安装会显示可直接关闭的自愿赞赏说明，不要求付款。
3. **原版英文启动.cmd** 以英语启动，保留汉化。**仅安装汉化.cmd** 不启动游戏。**检查汉化包.cmd** 只检查包。**还原原始游戏.cmd** 恢复受补丁影响的 5901 原始文件，不改动存档。

首次安装应使用 5901 原版文件，不能覆盖 5801 或其他版本的旧补丁。安装器会拒绝版本不符和未知同名文件，并把被替换的原版文件保存在游戏目录的 `.ksa-zh-backup`。请保留该备份。此包还原的是 **5901 原版**，不是降级到 5801。直接运行已装补丁的 `KSA.exe` 默认使用简体中文。旧的 5801 启动入口不适用于此版。

需要后台安装且不打开赞赏提示时，可从本包目录运行：

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\scripts\install.ps1 -Action Install -GameDirectory 'C:\Games\Kitten Space Agency' -NoSupportNotice
```

此包只含差分补丁、译文、汉化运行库和本地安装工具，不包含完整游戏 DLL、游戏资源、存档或 Windows 字体。系统黑体从本机 Windows 字体目录复制，不修改系统字体。

## 汉化和检查

- 4,362 条词典记录，全部 379 条原生语言记录均有译文。
- 主要补译任务和补给规划、生命保障、乘员倒计时、探测器核心供电和辐射状态、发射前物资核对，并适配重整后的生命保障窗口。
- 265 个部件模板、66 条资源描述、104 条资源提示全部通过覆盖检查；187 处拼接文案经按方法定位验证。保留格式占位符、技术缩写和控件隐藏 ID。
- 中文与英文各通过 2,577 项后台运行库检查；验证差分重建、拒绝错版与损坏补丁、干净安装、重复安装、完整还原和存档标记不变。结果见 `reports/distribution-tests.json`、`reports/package-tests.json` 和 `reports/version-adaptation.json`。旧版本的历史报告仍保留，不算作本次验证。
- 未打开游戏窗口，不包含实际画面或自动驾驶模组兼容性验证。kFS 的部分调试界面、编译器技术诊断、底层输出和固定刻字可能仍为英文。

`src/` 中的词表、拼接文案和汉化运行库源码可供维护。本项目有权授权的原创部分采用 [MIT](LICENSE-MIT) 或 [GNU GPL v3.0](LICENSE-GPL-3.0) 双许可。游戏及第三方素材仍归原权利人所有。
