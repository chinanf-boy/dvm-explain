# justjavac/dvm [![explain]][source] [![translate-svg]][translate-list]

<!-- [![size-img]][size] -->

[explain]: http://llever.com/explain.svg
[source]: https://github.com/chinanf-boy/Source-Explain
[translate-svg]: http://llever.com/translate.svg
[translate-list]: https://github.com/chinanf-boy/chinese-translate-list
[size-img]: https://packagephobia.now.sh/badge?p=Name
[size]: https://packagephobia.now.sh/result?p=Name

「 Deno版本管理器 」

---

## explain 🀄️

<!-- doc-templite START generated -->
<!-- time = 'true' -->
<!-- name = 'justjavac' -->
<!-- repo = 'dvm' -->
<!-- commit = 'true' -->

| 版本     | 与日期  | 最新更新   | 更多               |
| -------- | ------- | ---------- | ------------------ |
| [commit] | ⏰ true | ![version] | [源码解释][source] |

[commit]: https://github.com/justjavac/dvm/tree/true
[version]: https://img.shields.io/npm/v/dvm.svg

<!-- doc-templite END generated -->

### 贡献

欢迎 👏 勘误/校对/更新贡献 😊 [具体贡献请看](https://github.com/chinanf-boy/chinese-translate-list#贡献)

## 生活

[help me live , live need money 💰](https://github.com/chinanf-boy/live-need-money)

---

### 目录

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Deno版本管理器](#deno%E7%89%88%E6%9C%AC%E7%AE%A1%E7%90%86%E5%99%A8)
    - [TODO](#todo)
  - [安装](#%E5%AE%89%E8%A3%85)
  - [用法](#%E7%94%A8%E6%B3%95)
    - [验证安装](#%E9%AA%8C%E8%AF%81%E5%AE%89%E8%A3%85)
    - [初始化](#%E5%88%9D%E5%A7%8B%E5%8C%96)
  - [注意对于Windows用户](#%E6%B3%A8%E6%84%8F%E5%AF%B9%E4%BA%8Ewindows%E7%94%A8%E6%88%B7)
  - [已知的deno下载注册表镜像](#%E5%B7%B2%E7%9F%A5%E7%9A%84deno%E4%B8%8B%E8%BD%BD%E6%B3%A8%E5%86%8C%E8%A1%A8%E9%95%9C%E5%83%8F)
  - [例子](#%E4%BE%8B%E5%AD%90)
    - [上市版本](#%E4%B8%8A%E5%B8%82%E7%89%88%E6%9C%AC)
    - [切换版本](#%E5%88%87%E6%8D%A2%E7%89%88%E6%9C%AC)
  - [作者](#%E4%BD%9C%E8%80%85)
  - [贡献者](#%E8%B4%A1%E7%8C%AE%E8%80%85)
  - [执照](#%E6%89%A7%E7%85%A7)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Deno版本管理器

[![npm package](https://nodei.co/npm/dvm.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/dvm/)

[![Build Status](https://travis-ci.com/justjavac/dvm.svg?branch=master)](https://travis-ci.com/justjavac/dvm)
[![NPM version](https://img.shields.io/npm/v/dvm.svg)](https://www.npmjs.com/package/dvm)
[![NPM Downloads](https://img.shields.io/npm/dm/dvm.svg?style=flat)](https://npmcharts.com/compare/dvm?minimal=true)
[![Install Size](https://packagephobia.now.sh/badge?p=dvm)](https://packagephobia.now.sh/result?p=dvm)

在[deno](https://github.com/denoland/deno)不同版本之间切换

### TODO

-   [ ] `dvm ls-remote`
-   [ ] `dvm install x.x.x -r denocn`

## 安装

目前你可以使用npm来安装dvm:

```sh
npm install -g dvm
```

## 用法

```
➜  ~  dvm --help

Usage: dvm [options] [command]

Options:

  -v, --version      输出版本号
  -d, --debug        打印详细信息以进行调试
  -h, --help         输出使用信息

Commands:

  arch               显示deno是以32位还是64位模式运行
  list               列出所有已安装的版本
  install <version>  安装deno <version>
  use [version]      切换到使用指定的版本
```

### 验证安装

要验证是否已安装dvm,请执行以下操作:

```bash
dvm -v
```

如果安装成功,应该输出dvm的版本.

### 初始化

如果`~/.dvm/`目录不存在, 调用`dvm`会创造一个,并将所有已安装的deno版本放入`~/.dvm`.

```
➜  ~  dvm
Creating /Users/justjavac/.dvm
```

## 注意对于Windows用户

你可能要跑`dvm`在shell(cmd,PowerShell,Git Bash等)中具有提升(管理员)权限以使其运行.

```
➜  ~  dvm use 0.1.2
You may have to run dvm in a shell (cmd, PowerShell, Git Bash, etc) with elevated (Administrative) privileges to get it to run.
```

## 已知的deno下载注册表镜像

*TODO*

为方便起见,使用时`dvm install`要安装特定版本的deno,您可以选择一个注册表.目前我们提供内置的这些注册表:

-   [deno](https://github.com/denoland/deno):`dvm install 0.1.2 -r deno`
-   [denocn](https://deno.js.cn):`dvm install 0.1.2 -r denocn`

## 例子

### 上市版本

列出所有已安装的版本

```
➜  ~  dvm list
 * 0.1.0
   0.1.1
   0.1.2
```

带星号的版本(`*`)表示此版本是当前使用的版本.

### 切换版本

```
➜  ~  dvm use 0.1.2
now use 0.1.2
➜  ~  dvm use 0.0.2
deno v0.0.2 is not installed. Use `dvm install 0.0.2` to install it first.
```

## 作者

-   [justjavac](http://github.com/justjavac)

## 贡献者

-   [justjavac](http://github.com/justjavac)
-   [jysperm](http://github.com/jysperm)

## 执照

Deno版本管理器(dvm)根据GPL许可证发布.看[许可](./LICENSE)文件了解详情.
