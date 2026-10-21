# Plain Craft Launcher (PCL) NoAutoUpdate 修改版

> ⚠️ **本仓库是第三方基于 [Plain Craft Launcher (PCL)](https://github.com/Meloong-Git/PCL) 的独立修改版本，非官方产物，与龙腾猫跃及官方无任何隶属关系。**

本修改版基于 PCL **2.14.0.0** 的源代码，仅针对「自动更新」相关功能做处理，其余功能与原版保持一致。

## 修改内容

- 上游开源仓库中，更新相关模块本身为空实现（作者未开源自动更新逻辑），因此该源码编译出的版本天然不具备自动更新能力。
- 本修改版在此基础上：
  - 保持更新模块的空实现，不恢复、不新增任何自动更新逻辑；
  - 在「关于」页面增加第三方修改版声明，并保留原作者署名与赞助链接；
  - 仓库根目录保留《PCL 分发有限许可》与《PCL 存储库合理使用指南》（LICENCE 文件）。
- 未修改 Minecraft 启动、下载、Mod 管理等核心逻辑。

## 命名与署名

- 名称：**Plain Craft Launcher (PCL) NoAutoUpdate 修改版**
- 原作者：**龙腾猫跃** — 赞助链接：<https://meloong.com/afd/a/LTCat>
- 原项目：<https://github.com/Meloong-Git/PCL>
- 本修改版维护者：`r1895111`

## 许可协议

本修改版遵循《PCL 分发有限许可》与《PCL 存储库合理使用指南》（详见仓库 [LICENCE](./LICENCE)）：

- 已明确标注为第三方二次创作产物；
- 名称以 Plain Craft Launcher (PCL) 开头并带有第三方修改后缀；
- 关于页首位保留龙腾猫跃署名与赞助链接，且公开源代码；
- 保留原版的正版购买劝导逻辑，界面主色相保持蓝色；
- **免费分发，不以软件为收费主体，不收取任何费用。**

## 构建

基于 PCL 2.14.0.0 的源代码构建（Visual Studio 2022 + .NET 9 SDK），构建方式与上游一致：

```bash
# 1. 先构建 SDK 风格的依赖项目
dotnet build PCLCS/PCLCS.csproj -c Release
dotnet build MeloongCore/Shared/MeloongCore.csproj -c Release
dotnet build MeloongCore/Wpf/MeloongCore.Wpf.csproj -c Release

# 2. 用 Visual Studio 打开 Plain Craft Launcher 2.sln，选择 Release 编译主项目
#    产物位于：Plain Craft Launcher 2\bin\Plain Craft Launcher 2.exe
```

> 注意：本版本未注入 `PCL_MS_CLIENT_ID` / `PCL_CURSEFORGE_API_KEY`，正版登录与 CurseForge 下载功能不可用；离线登录及其它资源源不受影响。

## 免责声明

- 本项目仅用于个人学习与本地分发，使用本软件的 Minecraft 相关功能请遵守当地法律法规及 Minecraft 最终用户许可协议；
- 本修改版与官方无关，因使用本修改版产生的任何问题，由使用者自行承担。
