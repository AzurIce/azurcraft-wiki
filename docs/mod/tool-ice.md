!!! danger "Working In Progress"
    本页面仍在完善过程中，内容仍不完整

为了化简 mod 安装与更新的操作，[@Azur冰弦](https://github.com/AzurIce) 搓了一个命令行工具 [AzurIce/ice: A minecraft cli helper](https://github.com/AzurIce/ice)。

简单来说，可以通过一个 `mods.toml` 来定义 Mod 信息，然后 Ice 可以根据这个文件进行 Mod 的下载、更新。

## 安装

=== "Windows - Scoop"

    1. 安装 [ScoopInstaller/Scoop: A command-line installer for Windows](https://github.com/ScoopInstaller/Scoop)
    2. 运行如下命令
    ```
    scoop bucket add ice https://github.com/azurice/ice
    scoop install ice/ice
    ```

## 使用

首先，把 `mods.toml` 丢到要下载 Mod 的文件夹（比如 `.minecraft/mods`）。

然后在这个目录下运行 `ice modrinth sync`，则会根据 `mods.toml` 下载缺失的 Mod，更新版本不对的 Mod，删除多余的 Mod（仅限于 Modrinth 上的 Mod）。

使用 `ice modrinth update`，可以将 Mod 更新到符合 `loader` 和 `version` 要求的最新版本，并且更新 `mods.toml`。


使用 `ice modrinth add <slug>`，可以添加一个 Mod（这里的 `<slug>` 是 Modrinth 的 Mod 页面 Url 中的 Mod 英文名）。

更多详细内容可以看 Ice 的仓库。
