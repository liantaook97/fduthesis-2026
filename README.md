# fduthesis-2026

## 欢迎使用 fduthesis-2026（复旦大学 2026 学位论文新规范适配版）

> **关于本版本（请先阅读）**
>
> 这是 `fduthesis` 的**最新适配版本**。2026年6月15日，复旦大学研究生院发布 2026 学位论文新规范，官方与原 LaTeX 模板均尚未跟进，本仓库基于 [stone-zeng/fduthesis](https://github.com/stone-zeng/fduthesis) v0.9a，适配了新版封面、摘要等版式，供急需按新规范排版的同学使用。
>
> - **新规范原文**：[复旦大学研究生院·学位论文规范页面](https://gs.fudan.edu.cn/6b/9f/c2806a27551/page.htm)，本仓库的适配以此为依据。
> - **临时命名**：依 [LPPL-1.3c](http://www.latex-project.org/lppl.txt) 要求，文档类暂重命名为 `fduthesis-2026`（`\documentclass{fduthesis-2026}`）以与原版区分。**未来命名可能变更**，请留意。
> - **按需维护**：本仓库为个人业余适配，如发现问题欢迎提交 issue 或 PR，但**无法保证及时响应或长期维护**。
> - **重要说明**：本模板未经复旦大学任何部门审核或授权，使用前请务必斟酌；因使用本模板引起的格式审查问题概由使用者自负。
> - **致谢**：核心模板由 [曾祥东（Xiangdong Zeng）](https://github.com/stone-zeng) 开发，本仓库仅做规范适配，感谢原作者以及社区的历史贡献。

本模板支持中英文的博士、硕士学位论文以及本科毕业论文撰写。借助现代 LaTeX 技术，希望达到用户接口简明、内容格式规范和模板样式可定制的统一。

本模板目前支持 XeTeX 和 LuaTeX 引擎，对其他引擎（包括 pdfTeX 和 [ApTeX](https://github.com/clerkma/ptex-ng)）的支持仍在实验阶段。本模板仅支持 UTF-8 编码。

模板的用户接口与原版基本一致，详细用法请参阅原版文档 [fduthesis.pdf](http://mirrors.ctan.org/macros/latex/contrib/fduthesis/fduthesis.pdf)（2026 适配部分的差异以本仓库为准）。

### 模板组成

- 核心文档类
  - `fduthesis-2026.cls`
  - `fduthesis-2026-en.cls`
- 配置文件
  - `fduthesis-2026.def`
- 附属宏包
  - `fdulogo.sty`
  - `fdudoc.cls`

### 构建与安装

先把本仓库拉到本地（任选其一）：

```bash
git clone https://github.com/liantaook97/fduthesis.git
cd fduthesis
```

或在[仓库首页](https://github.com/liantaook97/fduthesis)点 **Code → Download ZIP**，解压后进入该目录。

`fduthesis-2026.cls/def` 等模板文件需要先用 [l3build](https://github.com/latex3/l3build)（TeX Live、MiKTeX 已自带）从 `source/fduthesis.dtx` 生成。在项目根目录操作，根据你写论文的环境二选一：

**A. 在本机 TeX 环境（TeX Live / MiKTeX）写（推荐）**

运行一次，把模板安装到本地 TeX 树，之后任意目录都能直接 `\documentclass{fduthesis-2026}`：

```bash
l3build install
```

**B. 用 Overleaf，或想把模板和论文放在同一目录**

先生成模板文件：

```bash
l3build unpack
```

再把自动生成的 `build/unpacked/` 下的 `fduthesis-2026.cls`、`fduthesis-2026-en.cls`、`fduthesis-2026.def`、`fdulogo.sty`、`fdudoc.cls` 跟论文 `.tex` 放在一起（用 Overleaf 就把这些文件一并上传到项目里）。

### 使用示例

```latex
% !TeX program  = XeLaTeX
% !TeX encoding = UTF-8

\documentclass{fduthesis-2026}

\fdusetup{
  style = {
    font-size = 5,
    fullwidth-stop = catcode,
  },
  info = {
    title = {论文标题},
    title* = {Thesis Title},
    author = {你的名字},
    supervisor = {某某某},
    supervisor-title = {教授},
    major = {物理学},
    degree = academic,
    department = {物理系},
    student-id = {12300000000},
    % student-category = equivalent,
    %   可选；同等学力人员用 equivalent，英文项目用 english-program，
    %   默认为一般项目，封面不显示特殊标注
    keywords = {不确定关系, 量子力学, 理论物理},
    keywords* = {Uncertainty principle, quantum mechanics, theoretical physics},
    clc = {O413.1}
  }
}

\begin{document}

\tableofcontents

\begin{abstract}
  中文摘要
\end{abstract}

\begin{abstract*}
  English abstract
\end{abstract*}

\mainmatter

<论文主体>

\backmatter

\end{document}
```

### 反馈

与 2026 适配相关的问题，欢迎在 [本仓库的 issues](https://github.com/liantaook97/fduthesis/issues) 反馈（维护说明见上文「关于本版本」）。与 2026 适配无关的通用功能问题，建议直接反馈到[原项目](https://github.com/stone-zeng/fduthesis)。

### 许可证

本模板的发布遵守 [LaTeX Project Public License](http://www.latex-project.org/lppl.txt)（版本 1.3c 或更高）。

<br>

## Welcome to fduthesis-2026 (community adaptation for Fudan University's 2026 latest thesis regulations)

> **About this version (please read first)**
>
> This is a **latest community adaptation**. After Fudan University released its 2026 thesis regulations, neither an official template nor the original LaTeX template had caught up, so this repository adapts [stone-zeng/fduthesis](https://github.com/stone-zeng/fduthesis) v0.9a (cover and abstract layout) for students who urgently need to typeset under the new regulations.
>
> - **Official regulations:** [Fudan Graduate School thesis-format page](https://gs.fudan.edu.cn/6b/9f/c2806a27551/page.htm), which this adaptation is based on.
> - **Temporary name:** As required by [LPPL-1.3c](http://www.latex-project.org/lppl.txt), the document class is renamed to `fduthesis-2026` (`\documentclass{fduthesis-2026}`) to distinguish it from the original. This is only a transitional name and **may change in the future**.
> - **Best-effort maintenance:** This is a personal, spare-time adaptation. **Timely updates, issue responses and long-term maintenance are NOT guaranteed.** Please assess the risk before relying on it for your thesis, and keep backups.
> - **Not reviewed:** This template has NOT been reviewed or authorized by any department of Fudan University. Any problem of format censorship caused by its use is the user's own responsibility.
> - **Credit:** The core template was created by [Xiangdong Zeng](https://github.com/stone-zeng); this repository only adapts it to the new regulations, and all credit goes to the original author.

This template supports doctoral or master dissertion and undergraduate thesis, both in Chinese or English. With the help of modern LaTeX technology, `fduthesis` aims to create a simple interface, a normative format, as well as a hackable class for the users.

At present, this template only supports XeTeX and LuaTeX engines. Support for pdfTeX and [ApTeX](https://github.com/clerkma/ptex-ng) is still under development. Only UTF-8 encoding is allowed.

The user interface is largely the same as the original; for detailed usage please refer to the original document [fduthesis-en.pdf](http://mirrors.ctan.org/macros/latex/contrib/fduthesis/fduthesis-en.pdf) (where the 2026 adaptation differs, this repository takes precedence).

### Components

- Main document classes:
  - `fduthesis-2026.cls`
  - `fduthesis-2026-en.cls`
- Configuration file:
  - `fduthesis-2026.def`
- Affiliated packages:
  - `fdulogo.sty`
  - `fdudoc.cls`

### Build & installation

First get the repository (either way):

```bash
git clone https://github.com/liantaook97/fduthesis.git
cd fduthesis
```

Or click **Code → Download ZIP** on the [repository page](https://github.com/liantaook97/fduthesis) and unzip it.

`fduthesis-2026.cls/def` and friends are not in the repository; you first generate them from `source/fduthesis.dtx` with [l3build](https://github.com/latex3/l3build) (bundled with TeX Live and MiKTeX). The commands below are run in the repository root; choose based on where you write your thesis:

**A. On a local TeX installation (TeX Live / MiKTeX), recommended**

Run once to install the template into your local TeX tree; afterwards `\documentclass{fduthesis-2026}` works from any directory:

```bash
l3build install
```

**B. On Overleaf, or keeping the template next to your thesis**

Generate the tempalte files first:

```bash
l3build unpack
```

Then put `fduthesis-2026.cls`, `fduthesis-2026-en.cls`, `fduthesis-2026.def`, `fdulogo.sty` and `fdudoc.cls` from `build/unpacked/` in the same folder as your `.tex` (with Overleaf, upload them to your project).

### Sample

```latex
\documentclass{fduthesis-2026-en}

\fdusetup{
  style/font-size = 5,
  info = {
    title = {论文标题},
    title* = {Thesis Title},
    author = {你的名字},
    supervisor = {某某某},
    supervisor-title = {教授},
    major = {物理学},
    degree = academic,
    department = {物理系},
    student-id = {12300000000},
    % student-category = equivalent,
    %   optional; use equivalent for equivalent-qualification students,
    %   english-program for English-track programs; defaults to the
    %   regular program with no special marking on the cover
    keywords = {不确定关系, 量子力学, 理论物理},
    keywords* = {Uncertainty principle, quantum mechanics, theoretical physics},
    clc = {O413.1}
  }
}

\begin{document}

\tableofcontents

\begin{abstract}
  Abstract
\end{abstract}

\mainmatter

<Main body of your thesis>

\backmatter

\end{document}
```

### Feedback

Issues about the 2026 adaptation are welcome in [this repository](https://github.com/liantaook97/fduthesis/issues) (see the maintenance note under "About this version" above). For general feature requests unrelated to the 2026 adaptation, please use the [original project](https://github.com/stone-zeng/fduthesis).

### License

This work may be distributed and/or modified under the conditions of the [LaTeX Project Public License](http://www.latex-project.org/lppl.txt), either version 1.3c of this license or (at your option) any later version.

---

Original template Copyright (C) 2017&ndash;2024 by Xiangdong Zeng.
2026 adaptation by 李桉涛 (Antao Li, [@liantaook97](https://github.com/liantaook97)).