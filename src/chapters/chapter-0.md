---
permalink: /ch-0/
layout: default
title: Chapter 0 | Beginnings
nav_order: 2
---

# Chapter 0 -- Beginnings

Welcome! Before you embark on your journey, you will need to download and set up the Zig compiler. For a number of reasons, it is recommended *not* to use the latest tagged release, and instead, you should use the latest `master` build. This is down to the fact that Zig is a young, rapidly-changing language, where releases quickly become outdated, and so most resources (including this guide) target `master`, instead of the latest tagged release.

## Binary Download

From [ziglang.org](https://ziglang.org/download/), download the appropriate build of Zig from below the `master` subheading. You can then extract it into a directory, and add the directory to your `PATH` environment variable. 

### Linux, MacOS, and *BSD

To add Zig to your `PATH`, add an export line to your shell profile (`.profile`, `.zprofile`, etc):

```shell
export PATH=$PATH:$HOME/path/to/zig
```

### Windows

Run the following command in PowerShell to add Zig to the user `PATH`:

```powershell
[Environment]::SetEnvironmentVariable(
    "PATH",
    [Environment]::GetEnvironmentVariable("PATH", "User") + ";C:\path\to\zig",
    "User"
)
```

If you wish to apply this system-wide, run the command in an elevated prompt, and replace the two `"User"` strings with `"Machine"`.

## Package Managers

Many package managers provide a Zig package. A list is available [here](https://github.com/ziglang/zig/wiki/Install-Zig-from-a-Package-Manager). Presently, it is not recommended to use this, as packages may lag behind tagged releases, and will certainly not provide the latest `master` builds (or any at all, for that matter).

## Text Editors

Most text editors will provide syntax highlighting for Zig, although some may need a plugin. Plugins for major editors include:
- [VSCode](https://github.com/ziglang/vscode-zig)
- [Sublime Text](https://packagecontrol.io/packages/Zig%20Language)
- [Vim](https://github.com/ziglang/zig.vim)
- [Emacs](https://github.com/ziglang/zig-mode)

Additionally, Zig has a language server implementation, providing completions, symbol-renaming, and more. You can find it, along with instructions on how to add it to your editor, [here](https://github.com/zigtools/zls).

## Summary

After all this, you should now have a fully-functional Zig compiler set up, along with editor integration, if you chose to set that up. In the next chapter, you will write your 'Hello, world!' in Zig.
