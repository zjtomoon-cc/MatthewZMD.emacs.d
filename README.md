<a id="org7bcfd50"></a>

# M-EMACS


# Table of Contents     :TOC_2_ORG:

-   [M-EMACS](#org7bcfd50)
-   [About EMACS](#org55621e5)
-   [About M-EMACS](#org9be5082)
    -   [Community Responses ❤️](#org2626c54)
    -   [About README](#org17ae25a)
    -   [Installation](#orgc56480f)
    -   [Modification](#org622db59)
    -   [Contribution](#orgac281f4)
    -   [Special Thanks](#org68b41a2)
-   [Startup](#org34312b5)
    -   [Lexical Binding](#org98eb7cd)
    -   [Early Init](#org391b00c)
    -   [Garbage Collection](#org435b517)
    -   [Load Path](#org00ce2da)
    -   [Define Constants](#orgec48a8a)
    -   [Load Private File](#org5564757)
-   [Package Management](#orgd5ea34c)
    -   [Melpa Packages](#org31e4546)
    -   [Non-Melpa Packages](#orgbec2cd7)
    -   [Configure Package Manager](#org303a9d9)
    -   [Use Package](#org60f826a)
    -   [Auto Package Update](#org71785f6)
    -   [Diminish](#orgd08962b)
-   [Global Functionalities](#org59905b5)
    -   [User Information](#org2565d52)
    -   [Bindings](#orga053e2c)
    -   [Avy](#orgf1abce6)
    -   [Crux](#org51992df)
    -   [Ivy, Amx, Counsel, Swiper](#orgac0062a)
    -   [Color Ripgrep](#org76e2c53)
    -   [Find File In Project](#orgd46572c)
    -   [Files Directories](#orga63f069)
    -   [Winner](#org7785d31)
    -   [Which Key](#org73948f4)
    -   [Popup Kill Ring](#orga95cee1)
    -   [Undo Tree](#org9da9f9c)
    -   [Discover My Major](#orgff65386)
    -   [Ace Window](#orgd86117a)
    -   [Terminal](#org0b601da)
    -   [Sudo Edit](#orgf5c14db)
    -   [Ibuffer](#org955e4dd)
    -   [Config](#org4e42742)
    -   [Functions](#org8b9615a)
-   [UI Enhancements](#orgf295218)
    -   [Doom Themes](#org5ff6e50)
    -   [Doom Modeline](#orga2ce52d)
    -   [Dashboard](#orgc633774)
    -   [Fonts and Icons](#org7226924)
    -   [Smooth Scrolling](#orgea94152)
    -   [Highlight Lines](#org9b3a1ec)
    -   [Prettify Symbols](#org833a13d)
    -   [UI Configs](#org88d48d8)
-   [General Programming](#org90d2e48)
    -   [Magit](#orgfbfd407)
    -   [Projectile](#orgd182f76)
    -   [YASnippet](#org809e4da)
    -   [Dumb Jump](#org30269b2)
    -   [Parenthesis](#org069bf41)
    -   [Indentation](#orgc480821)
    -   [Quickrun](#orgdb1fb0f)
    -   [Format All](#org5a90b40)
    -   [Ediff](#org1b808b4)
    -   [Evil Nerd Commenter](#org77bd567)
    -   [Editing](#orga17e03b)
    -   [Headers](#orga6c7209)
    -   [Jupyter Notebook](#org0be1bae)
    -   [Completion / LSP](#org6fa6bff)
-   [Programming](#org9e93c54)
    -   [C/C++/Objective C](#orga429a7b)
    -   [Golang](#org7961933)
    -   [Rust](#org5f48088)
    -   [Python](#org8829535)
    -   [Haskell](#org800a36a)
    -   [ESS](#org5e93050)
    -   [TeX](#org779ed99)
    -   [Yaml](#org4ee9775)
    -   [Buildsystem](#orga6c62d3)
-   [Web Development](#org84a3b37)
    -   [Web](#org254e7a6)
    -   [JavaScript/TypeScript](#orgb200642)
    -   [Emmet](#orgcff2c8f)
    -   [Instant Rename Tag](#org6b57af0)
    -   [JSON](#orge094ccd)
-   [Office](#org1f6da9b)
    -   [Org](#org2e82a58)
    -   [PDF Tools](#org38cf7a0)
-   [Internet](#org3d3a1a7)
    -   [EAF](#org80e93b9)
    -   [Popweb](#org53a99ca)
    -   [ERC](#org6186551)
    -   [MU4E](#org6c76e74)
    -   [Tramp](#orgff0e9e8)
    -   [LeetCode](#orgbbd118f)
    -   [Debbugs](#org5775fb7)
    -   [Hacker News](#org24ba65c)
    -   [EWW](#org3f2d4cd)
-   [Miscellaneous](#org1f94fb2)
    -   [Chinese](#org8a911ff)
    -   [Tetris](#org766c45b)
    -   [Speed Type](#org9a4e85e)
    -   [2048 Game](#org2818cea)
    -   [Snow](#orgb619100)
    -   [EPaint](#orge6e0ba9)
    -   [Zone](#orgd62e69b)


<a id="org55621e5"></a>

# About EMACS

Emacs changes how you *think* about programming.

Emacs is **totally introspectable**. You can always find out 'what code runs when I press this button?'.

Emacs is an **incremental programming environment**. There's no edit-compile-run cycle. There isn't even an edit-run cycle. You can execute snippets of code and gradually turn them into a finished project. There's no distinction between your editor and your interpreter.

Emacs is a **mutable environment**. You can set variables, tweak functions with advice, or redefine entire functions. Nothing is off-limits.

Emacs provides **functionality without applications**. Rather than separate applications, functionality is all integrated into your Emacs instance. Amazingly, this works. Ever wanted to use the same snippet tool for writing C++ classes as well as emails?

Emacs is full of **incredible software concepts that haven't hit the mainstream yet**. For example:

-   Many platforms have a single item clipboard. Emacs has an **infinite clipboard**.
-   If you undo a change, and then continue editing, you can't redo the original change. Emacs allows **undoing to any historical state**, even allowing tree-based exploration of history.
-   Emacs supports a **reverse variable search**: you can find variables with a given value.
-   You can perform **structural editing** of code, allowing you to make changes without breaking syntax. This works for lisps (paredit) and non-lisps (smartparens).
-   Many applications use a modal GUI: for example, you can't do other edits during a find-and-replace operation. Emacs provides **recursive editing** that allow you to suspend what you're currently doing, perform other edits, then continue the original task.

Emacs has a **documentation culture**. Emacs includes a usage manual, a lisp programming manual, pervasive docstrings and even an interactive tutorial.

Emacs has a **broad ecosystem**. If you want to edit code in a niche language, there's probably an Emacs package for it.

Emacs doesn't have a monopoly on good ideas, and there are other great tools out there. Nonetheless, we believe the [Emacs learning curve](https://i.stack.imgur.com/7Cu9Z.jpg) pays off.

*This beautifully written **About EMACS** section credits to [Remacs](https://github.com/remacs/remacs).*


<a id="org9be5082"></a>

# About M-EMACS

M-EMACS is a custom GNU Emacs setup and configuration distribution that aims not only to enhance the default Emacs experience, and hopefully be a sample that everyone can easily navigate and reference through a highly detailed README that contains 99% of the **entire** configuration code.

As a young EMACSer, I have experienced the struggle to find a detailed configuration that is loosely coupled and highly readable. This mostly due to the nature of source codes, sometimes comments are harder to notice or simply not enough. Therefore I decided to construct this README and present any human-readable explanation in a much more human-friendly way. Anyone, particularly Emacs beginners who have no idea where to start with their personal config, is more than welcome to read through this document and copy/paste any part to use it on their own.

This distribution is designed and tested for **GNU Emacs 26.1 and above only**. However, it is always suggested to use **Emacs 27**, the latest stable version released, for its significant improvement in the core that's out of the scope of M-EMACS. ![img](images/Sample.png)


<a id="org2626c54"></a>

## Community Responses ❤️

Some heartwarming responses from the Emacs community:

-   *"Actually I understated how much I liked reading through your config&#x2026; What makes me excited about this config is the readability and possibility of extending in a similar way."* &#x2013; from [u/Orgmonics](https://www.reddit.com/r/emacs/comments/eewwyh/officially_introducing_memacs/fc5x1lz?utm_source=share&utm_medium=web2x&context=3)
-   *"I have to say Matt's setup has the best clarity of all emacs setups I have ever tried. It's really a good template to develop your own emacs config. Thanks again&#x2026;"* &#x2013; from [u/fqye](https://www.reddit.com/r/emacs/comments/eewwyh/officially_introducing_memacs/fbxk831?utm_source=share&utm_medium=web2x&context=3)
-   *"Thanks for the fantastic emacs setup, I love emacs, but trying to get lsp working right was killing me, yours worked out of the box and all I had to do was add some bindings, it's really a time saver"* &#x2013; from [ahonnecke](https://github.com/MatthewZMD/.emacs.d/issues/48#issuecomment-877827124)
-   *"Thank you for helping a guy out and for sharing this. I hope this evolves to be into something really big."* &#x2013; from [d3v-S](https://github.com/MatthewZMD/.emacs.d/issues/38#issuecomment-706657288)
-   and more&#x2026; Love you guys! ❤️❤️


<a id="org17ae25a"></a>

## About README

This README is originated from `init.org` that is generated using `M-x org-gfm-export-to-markdown`. Every block of code is generated through this function - it exports sections of code from the `elisp/` directory. You will not see their presence in `init.org`. This not only enables a cleaner organization but also significantly improves Emacs start-up time than the traditional *everything in an org file* approach.


<a id="orgc56480f"></a>

## Installation

1.  Install [GNU Emacs](https://www.gnu.org/software/emacs/).
    -   (Optional) On Ubuntu, `emacs-snapshot` is a great way to get latest version of Emacs.

        ```bash
        sudo add-apt-repository -y ppa:ubuntu-elisp
        sudo apt-get update
        sudo apt-get install emacs-snapshot
        ```
    -   (Optional) Build latest Emacs from source.

        ```bash
        # Install essential build tools
        sudo apt-get install build-essential texinfo libx11-dev libxpm-dev libjpeg-dev libpng-dev libgif-dev libtiff-dev libgtk2.0-dev libncurses-dev gnutls-dev libgtk-3-dev git autoconf
        # Clone source
        git clone --depth=1 https://github.com/emacs-mirror/emacs.git
        # Go to source
        cd emacs/
        # Build Emacs
        ./autogen.sh
        ./configure --with-mailutils
        make
        # Install (optional)
        sudo make install
        ```
2.  Clone this repo to `HOME` or `~/` path using [git](https://git-scm.com/) and update all the submodules.

    ```bash
    cd ~
    git clone --recurse-submodules -j8 https://github.com/MatthewZMD/.emacs.d.git
    cd .emacs.d
    ```
3.  Ensure a stable connection to Melpa Packages, then open Emacs.
4.  Enter `y` when prompted with `Auto-update packages now?`, wait for all packages to install.
5.  In your favorite browser, `Ctrl-f Prerequisite` through this README and follow the **Prerequisite** instructions.
6.  Restart Emacs.


### Further Updates

I will be updating M-EMACS from time to time, it is best to `git pull` once a while to stay up to date.

Please also execute `git submodule update --recursive --remote` to sync with all the submodules.


<a id="org622db59"></a>

## Modification

You have the permission to use, modify, distribute in any way you want.

However, what is *free* stays *free*. After all, this is [GPL](LICENSE).

**Remember** you must manually sync this README with all the new changes you made by:

1.  Please do **NOT** edit this `README.md` file, edit `init.org` instead!
2.  If you add a new mode, create a new `<file-name>.el` file in `elisp/` directory.
3.  Put `(require '<file-name>)` in [init.el](init.el) accordingly.
4.  Add `#+INCLUDE: "~/.emacs.d/elisp/<place-holder>.el" src emacs-lisp :range-begin "<start-line-wrapper-exclusive>" :range-end "<end-line-wrapper-exclusive>"` in the appropriate section in `init.org`.
5.  Enter `C-x C-s` to save and update `:lines`. (if you don't see the updated effect, run `M-x save-and-update-includes` manually)
6.  Call `M-x org-gfm-export-to-markdown` to update `README.md` automatically.


<a id="orgac281f4"></a>

## Contribution

If you spotted a bug or you have any suggestions, please fill in an issue. If you have something to fix, feel free to create a pull request.


<a id="org68b41a2"></a>

## Special Thanks

Everyone starts somewhere, and I started here.

-   [Vincent Zhang's Centaur Emacs](https://github.com/seagle0128/.emacs.d)
-   [Henrik Lissner's Doom Emacs](https://github.com/hlissner/doom-emacs)
-   [Poncie Reyes's .emacs.d](https://github.com/poncie/.emacs.d)


<a id="org34312b5"></a>

# Startup


<a id="org98eb7cd"></a>

## Lexical Binding

Use lexical-binding. [Why?](https://nullprogram.com/blog/2016/12/22/)

> Until Emacs 24.1 (June 2012), Elisp only had dynamically scoped variables, a feature, mostly by accident, common to old lisp dialects. While dynamic scope has some selective uses, it’s widely regarded as a mistake for local variables, and virtually no other languages have adopted it.

```emacs-lisp
;;; init.el --- -*- lexical-binding: t -*-
```


<a id="org391b00c"></a>

## Early Init

Emacs27 introduces `early-init.el`, which is run before `init.el`, before package and UI initialization happens.


### Compatibility With 26

Ensure `emacs-version>=26`, manually require `early-init` configurations if `emacs-version<27`.

```emacs-lisp
(cond ((version< emacs-version "26.1")
       (warn "M-EMACS requires Emacs 26.1 and above!"))
      ((let* ((early-init-f (expand-file-name "early-init.el" user-emacs-directory))
              (early-init-do-not-edit-d (expand-file-name "early-init-do-not-edit/" user-emacs-directory))
              (early-init-do-not-edit-f (expand-file-name "early-init.el" early-init-do-not-edit-d)))
         (and (version< emacs-version "27")
              (or (not (file-exists-p early-init-do-not-edit-f))
                  (file-newer-than-file-p early-init-f early-init-do-not-edit-f)))
         (make-directory early-init-do-not-edit-d t)
         (copy-file early-init-f early-init-do-not-edit-f t t t t)
         (add-to-list 'load-path early-init-do-not-edit-d)
         (require 'early-init))))
```


### Defer Garbage Collection

Defer garbage collection further back in the startup process, according to [hlissner](https://github.com/hlissner/doom-emacs/blob/develop/docs/faq.org#how-does-doom-start-up-so-quickly).

> The GC eats up quite a bit of time, easily doubling startup time. The trick is to turn up the memory threshold as early as possible.

```emacs-lisp
(setq gc-cons-threshold 100000000)
```


### Disable `package-enable-at-startup`

Package initialize occurs automatically, before `user-init-file` is loaded, but after `early-init-file`. We handle package initialization, so we must prevent Emacs from doing it early!

```emacs-lisp
(setq package-enable-at-startup nil)
```


### Unset `file-name-handler-alist`

Every file opened and loaded by Emacs will run through this list to check for a proper handler for the file, but during startup, it won’t need any of them.

```emacs-lisp
(defvar file-name-handler-alist-original file-name-handler-alist)
(setq file-name-handler-alist nil)
```


### Disable `site-run-file`

```emacs-lisp
(setq site-run-file nil)
```


### Disable Unnecessary Interface

It will be faster to disable them here before they've been initialized.

```emacs-lisp
(menu-bar-mode -1)
(unless (and (display-graphic-p) (eq system-type 'darwin))
  (push '(menu-bar-lines . 0) default-frame-alist))
(push '(tool-bar-lines . 0) default-frame-alist)
(push '(vertical-scroll-bars) default-frame-alist)
```


<a id="org435b517"></a>

## Garbage Collection


### Set `gc-cons-threshold` Smaller for Interactive Use

A large `gc-cons-threshold` may cause freezing and stuttering during long-term interactive use.

If you experience freezing, decrease this amount, if you experience stuttering, increase this amount.

```emacs-lisp
(defvar better-gc-cons-threshold 134217728 ; 128mb
  "The default value to use for `gc-cons-threshold'.

If you experience freezing, decrease this.  If you experience stuttering, increase this.")

(add-hook 'emacs-startup-hook
          (lambda ()
            (setq gc-cons-threshold better-gc-cons-threshold)
            (setq file-name-handler-alist file-name-handler-alist-original)
            (makunbound 'file-name-handler-alist-original)))
```

Garbage Collect when Emacs is out of focus and avoid garbage collection when using minibuffer.

```emacs-lisp
(add-hook 'emacs-startup-hook
          (lambda ()
            (if (boundp 'after-focus-change-function)
                (add-function :after after-focus-change-function
                              (lambda ()
                                (unless (frame-focus-state)
                                  (garbage-collect))))
              (add-hook 'after-focus-change-function 'garbage-collect))
            (defun gc-minibuffer-setup-hook ()
              (setq gc-cons-threshold (* better-gc-cons-threshold 2)))

            (defun gc-minibuffer-exit-hook ()
              (garbage-collect)
              (setq gc-cons-threshold better-gc-cons-threshold))

            (add-hook 'minibuffer-setup-hook #'gc-minibuffer-setup-hook)
            (add-hook 'minibuffer-exit-hook #'gc-minibuffer-exit-hook)))
```


<a id="org00ce2da"></a>

## Load Path

Since all the configuration files are stored in `elisp/` folder, they need to be added to `load-path` now.

```emacs-lisp
(defun update-to-load-path (folder)
  "Update FOLDER and its subdirectories to `load-path'."
  (let ((base folder))
    (unless (member base load-path)
      (add-to-list 'load-path base))
    (dolist (f (directory-files base))
      (let ((name (concat base "/" f)))
        (when (and (file-directory-p name)
                   (not (equal f ".."))
                   (not (equal f ".")))
          (unless (member base load-path)
            (add-to-list 'load-path name)))))))

(update-to-load-path (expand-file-name "elisp" user-emacs-directory))
```


<a id="orgec48a8a"></a>

## Define Constants

```emacs-lisp
(defconst *sys/win32*
  (eq system-type 'windows-nt)
  "Are we running on a WinTel system?")

(defconst *sys/linux*
  (eq system-type 'gnu/linux)
  "Are we running on a GNU/Linux system?")

(defconst *sys/mac*
  (eq system-type 'darwin)
  "Are we running on a Mac system?")

(defconst python-p
  (or (executable-find "python3")
      (and (executable-find "python")
           (> (length (shell-command-to-string "python --version | grep 'Python 3'")) 0)))
  "Do we have python3?")

(defconst pip-p
  (or (executable-find "pip3")
      (and (executable-find "pip")
           (> (length (shell-command-to-string "pip --version | grep 'python 3'")) 0)))
  "Do we have pip3?")

(defconst clangd-p
  (or (executable-find "clangd")  ;; usually
      (executable-find "/usr/local/opt/llvm/bin/clangd"))  ;; macOS
  "Do we have clangd?")

(defconst eaf-env-p
  (and (display-graphic-p) python-p pip-p)
  "Do we have EAF environment setup?")
```


<a id="org5564757"></a>

## Load Private File

An `init-private.el` file has been designated at `user-emacs-directory` for you to store personal configurations that you don't want to source-control.

```emacs-lisp
;; Load init-private.el if it exists
(when (file-exists-p (expand-file-name "init-private.el" user-emacs-directory))
  (load-file (expand-file-name "init-private.el" user-emacs-directory)))
```


<a id="orgd5ea34c"></a>

# Package Management

Some packages are disabled with the `:disabled` tag, because I don't use them very often. You can disable packages similarly yourself too:

```emacs-lisp
(use-package foo
  :disabled)
```


<a id="org31e4546"></a>

## Melpa Packages

Configure package archives, where to install online packages and add them to `load-path`.

```emacs-lisp
;; Select the folder to store packages
;; Comment / Uncomment to use desired sites
(setq package-user-dir (expand-file-name "elpa" user-emacs-directory)
      package-archives
      '(("gnu"   . "https://elpa.gnu.org/packages/")
        ("melpa" . "https://melpa.org/packages/")
        ("cselpa" . "https://elpa.thecybershadow.net/packages/")
        ;; ("melpa-cn" . "http://mirrors.cloud.tencent.com/elpa/melpa/")
        ;; ("gnu-cn"   . "http://mirrors.cloud.tencent.com/elpa/gnu/")
        ))
```


<a id="orgbec2cd7"></a>

## Non-Melpa Packages

Add packages contained in `site-elisp/` to `load-path` too.


### Add Packages Manually from Git

```bash
cd site-elisp/
git submodule add https://github.com/foo/bar.git
```

Verify `.gitmodules` file that the newly added package exist.


### Update Manually Added Packages

```bash
git submodule init
git submodule update
```


<a id="org303a9d9"></a>

## Configure Package Manager

```emacs-lisp
(unless (bound-and-true-p package--initialized)
  (setq package-enable-at-startup nil)          ; To prevent initializing twice
  (package-initialize))

;; set use-package-verbose to t for interpreted .emacs,
;; and to nil for byte-compiled .emacs.elc.
(eval-and-compile
  (setq use-package-verbose (not (bound-and-true-p byte-compile-current-file))))
```


<a id="org60f826a"></a>

## Use Package

My Emacs configuration is almost entirely dependant on [use-package](https://github.com/jwiegley/use-package).

> The `use-package` macro allows you to isolate package configuration in your .emacs file in a way that is both performance-oriented and, well, tidy. I created it because I have over 80 packages that I use in Emacs, and things were getting difficult to manage. Yet with this utility my total load time is around 2 seconds, with no loss of functionality!

```emacs-lisp
;; Install use-package if not installed
(unless (package-installed-p 'use-package)
  (package-refresh-contents)
  (package-install 'use-package))

(eval-and-compile
  (setq use-package-always-ensure t)
  (setq use-package-expand-minimally t)
  (setq use-package-compute-statistics t)
  (setq use-package-enable-imenu-support t))

(eval-when-compile
  (require 'use-package)
  (require 'bind-key))
```


<a id="org71785f6"></a>

## Auto Package Update

[Auto package update](https://github.com/rranelli/auto-package-update.el) automatically updates installed packages if at least `auto-package-update-interval` days have passed since the last update.

```emacs-lisp
(use-package auto-package-update
  :if (not (daemonp))
  :custom
  (auto-package-update-interval 7) ;; in days
  (auto-package-update-prompt-before-update t)
  (auto-package-update-delete-old-versions t)
  (auto-package-update-hide-results t)
  :config
  (auto-package-update-maybe))
```


<a id="orgd08962b"></a>

## Diminish

[Diminish](https://github.com/emacsmirror/diminish), a feature that removes certain minor modes from mode-line.

```emacs-lisp
(use-package diminish)
```


<a id="org59905b5"></a>

# Global Functionalities


<a id="org2565d52"></a>

## User Information

**Prerequisite**: Please update this file your personal info.

```emacs-lisp
(setq user-full-name "Mingde (Matthew) Zeng")
(setq user-mail-address "matthewzmd@gmail.com")
```


<a id="orga053e2c"></a>

## Bindings

```emacs-lisp
;; Unbind unneeded keys
(global-set-key (kbd "C-z") nil)
(global-set-key (kbd "M-z") nil)
(global-set-key (kbd "M-m") nil)
(global-set-key (kbd "C-x C-z") nil)
(global-set-key (kbd "M-/") nil)
;; Truncate lines
(global-set-key (kbd "C-x C-l") #'toggle-truncate-lines)
;; Adjust font size like web browsers
(global-set-key (kbd "C-=") #'text-scale-increase)
(global-set-key (kbd "C-+") #'text-scale-increase)
(global-set-key (kbd "C--") #'text-scale-decrease)
;; Move up/down paragraph
(global-set-key (kbd "M-n") #'forward-paragraph)
(global-set-key (kbd "M-p") #'backward-paragraph)
```


<a id="orgf1abce6"></a>

## Avy

[Avy](https://github.com/abo-abo/avy), a nice way to move around text.

```emacs-lisp
(use-package avy
  :defer t
  :bind
  (("C-z c" . avy-goto-char-timer)
   ("C-z l" . avy-goto-line))
  :custom
  (avy-timeout-seconds 0.3)
  (avy-style 'pre)
  :custom-face
  (avy-lead-face ((t (:background "#51afef" :foreground "#870000" :weight bold)))));
```


<a id="org51992df"></a>

## Crux

[Crux](https://github.com/bbatsov/crux), a Collection of Ridiculously Useful eXtensions for Emacs.

```emacs-lisp
(use-package crux
  :bind
  (("C-a" . crux-move-beginning-of-line)
   ("C-x 4 t" . crux-transpose-windows)
   ("C-x K" . crux-kill-other-buffers)
   ("C-k" . crux-smart-kill-line))
  :config
  (crux-with-region-or-buffer indent-region)
  (crux-with-region-or-buffer untabify)
  (crux-with-region-or-point-to-eol kill-ring-save)
  (defalias 'rename-file-and-buffer #'crux-rename-file-and-buffer))
```


<a id="orgac0062a"></a>

## Ivy, Amx, Counsel, Swiper

[Ivy](https://github.com/abo-abo/swiper), a generic completion mechanism for Emacs. It utilizes [Amx](https://github.com/DarwinAwardWinner/amx), [Counsel](https://github.com/abo-abo/swiper) and [Swiper](https://github.com/abo-abo/swiper).

```emacs-lisp
(use-package ivy
  :diminish
  :init
  (use-package amx :defer t)
  (use-package counsel :diminish :config (counsel-mode 1))
  (use-package swiper :defer t)
  (ivy-mode 1)
  :bind
  (("C-s" . swiper-isearch)
   ("C-z s" . counsel-rg)
   ("C-z b" . counsel-buffer-or-recentf)
   ("C-z C-b" . counsel-ibuffer)
   (:map ivy-minibuffer-map
         ("M-RET" . ivy-immediate-done))
   (:map counsel-find-file-map
         ("C-~" . counsel-goto-local-home)))
  :custom
  (ivy-use-virtual-buffers t)
  (ivy-height 10)
  (ivy-on-del-error-function nil)
  (ivy-magic-slash-non-match-action 'ivy-magic-slash-non-match-create)
  (ivy-count-format "【%d/%d】")
  (ivy-wrap t)
  :config
  (defun counsel-goto-local-home ()
      "Go to the $HOME of the local machine."
      (interactive)
    (ivy--cd "~/")))
```


<a id="org76e2c53"></a>

## Color Ripgrep

[Color rg](https://github.com/manateelazycat/color-rg), a search and refactoring tool based on *ripgrep* that is used to search text.

**Prerequisite**: Ensure [ripgrep](https://github.com/BurntSushi/ripgrep#installation) and ensure `rg` is in `PATH`.

```emacs-lisp
(use-package color-rg
  :load-path (lambda () (expand-file-name "site-elisp/color-rg" user-emacs-directory))
  :if (executable-find "rg")
  :bind ("C-M-s" . color-rg-search-input))
```


<a id="orgd46572c"></a>

## Find File In Project

[Find File In Project](https://github.com/technomancy/find-file-in-project), quick access to project files in Emacs.

**Prerequisite**: Ensure `GNU Find` is in `PATH`. Install [Gow](https://github.com/bmatzelle/gow) or Cygwin or MYSYS2 on Windows.

```emacs-lisp
(use-package find-file-in-project
  :if (executable-find "find")
  :init
  (when (executable-find "fd")
    (setq ffip-use-rust-fd t))
  :bind (("C-z o" . ffap)
         ("C-z p" . ffip)))
```


<a id="orga63f069"></a>

## Files Directories


### Dired

Dired, the directory editor.

```emacs-lisp
(use-package dired
  :ensure nil
  :bind
  (("C-x C-j" . dired-jump))
  :custom
  ;; Always delete and copy recursively
  (dired-listing-switches "-lah")
  (dired-recursive-deletes 'always)
  (dired-recursive-copies 'always)
  ;; Auto refresh Dired, but be quiet about it
  (global-auto-revert-non-file-buffers t)
  (auto-revert-verbose nil)
  ;; Quickly copy/move file in Dired
  (dired-dwim-target t)
  ;; Move files to trash when deleting
  (delete-by-moving-to-trash t)
  ;; Load the newest version of a file
  (load-prefer-newer t)
  ;; Detect external file changes and auto refresh file
  (auto-revert-use-notify nil)
  (auto-revert-interval 3) ; Auto revert every 3 sec
  :config
  ;; Enable global auto-revert
  (global-auto-revert-mode t)
  ;; Reuse same dired buffer, to prevent numerous buffers while navigating in dired
  (put 'dired-find-alternate-file 'disabled nil)
  :hook
  (dired-mode . (lambda ()
                  (local-set-key (kbd "<mouse-2>") #'dired-find-alternate-file)
                  (local-set-key (kbd "RET") #'dired-find-alternate-file)
                  (local-set-key (kbd "^")
                                 (lambda () (interactive) (find-alternate-file ".."))))))
```


### Disk Usage

[Disk Usage](https://gitlab.com/ambrevar/emacs-disk-usage), a file system analyzer that offers a tabulated view of file listings sorted by size.

```emacs-lisp
(use-package disk-usage
  :commands (disk-usage))
```


### Save All Buffers

```emacs-lisp
(defun save-all-buffers ()
  "Instead of `save-buffer', save all opened buffers by calling `save-some-buffers' with ARG t."
  (interactive)
  (save-some-buffers t))
(global-set-key (kbd "C-x C-s") nil)
(global-set-key (kbd "C-x C-s") #'save-all-buffers)
```


<a id="org7785d31"></a>

## Winner

Winner, a mode to restore previous window layouts.

```emacs-lisp
(use-package winner
  :ensure nil
  :custom
  (winner-boring-buffers
   '("*Completions*"
     "*Compile-Log*"
     "*inferior-lisp*"
     "*Fuzzy Completions*"
     "*Apropos*"
     "*Help*"
     "*cvs*"
     "*Buffer List*"
     "*Ibuffer*"
     "*esh command on file*"))
  :config
  (winner-mode 1))
```


<a id="org73948f4"></a>

## Which Key

[Which Key](https://github.com/justbur/emacs-which-key), a feature that displays the key bindings following the incomplete command.

```emacs-lisp
(use-package which-key
  :diminish
  :custom
  (which-key-separator " ")
  (which-key-prefix-prefix "+")
  :config
  (which-key-mode))
```


<a id="orga95cee1"></a>

## Popup Kill Ring

[Popup Kill Ring](https://github.com/waymondo/popup-kill-ring), a feature that provides the ability to browse Emacs kill ring in autocomplete style popup menu.

```emacs-lisp
(use-package popup-kill-ring
  :bind ("M-y" . popup-kill-ring)
  :custom (kill-do-not-save-duplicates t))
```


<a id="org9da9f9c"></a>

## Undo Tree

[Undo tree](https://www.emacswiki.org/emacs/UndoTree), a feature that provides a visualization of the undos in a file.

```emacs-lisp
(use-package undo-tree
  :defer t
  :diminish undo-tree-mode
  :init (global-undo-tree-mode)
  :custom
  (undo-tree-visualizer-diff t)
  (undo-tree-history-directory-alist `(("." . ,(expand-file-name ".backup" user-emacs-directory))))
  (undo-tree-visualizer-timestamps t))
```


<a id="orgff65386"></a>

## Discover My Major

[Discover my major](https://github.com/jguenther/discover-my-major), a feature that discovers key bindings and their meaning for the current Emacs major mode.

```emacs-lisp
(use-package discover-my-major
  :bind ("C-h C-m" . discover-my-major))
```


<a id="orgd86117a"></a>

## Ace Window

[Ace Window](https://github.com/abo-abo/ace-window), a package for selecting windows to switch to.

```emacs-lisp
(use-package ace-window
  :bind ("C-x C-o" . ace-window))
```


<a id="org0b601da"></a>

## Terminal


### Shell Here

[Shell Here](https://github.com/ieure/shell-here), a tool that opens a shell buffer in (or relative to) `default-directory`.

```emacs-lisp
(use-package shell-here
  :bind ("M-~" . shell-here)
  :config
  (when *sys/linux*
    (setq explicit-shell-file-name "/bin/bash")))
```


### Multi Term

[Multi Term](https://github.com/manateelazycat/multi-term), a mode based on term.el, for managing multiple terminal buffers in Emacs.

```emacs-lisp
(use-package multi-term
  :load-path (lambda () (expand-file-name "site-elisp/multi-term" user-emacs-directory))
  :commands (multi-term)
  :bind
  (("M-$" . multi-term)
   (:map dired-mode-map ("M-$" . multi-term)))
  :custom
  (multi-term-program (executable-find "bash"))
  (term-bind-key-alist
   '(("C-c C-c" . term-interrupt-subjob)
     ("C-c C-e" . term-send-esc)
     ("C-p" . previous-line)
     ("C-n" . next-line)
     ("C-m" . term-send-return)
     ("C-y" . term-paste)
     ("C-v" . scroll-up-command)
     ("M-v" . scroll-down-command)
     ("M-f" . term-send-forward-word)
     ("M-b" . term-send-backward-word)
     ("M-o" . term-send-backspace)
     ("M-p" . term-send-up)
     ("M-n" . term-send-down)
     ("M-M" . term-send-forward-kill-word)
     ("M-N" . term-send-backward-kill-word)
     ("<C-backspace>" . term-send-backward-kill-word)
     ("<M-backspace>" . term-send-backward-kill-word)
     ("M-r" . term-send-reverse-search-history)
     ("M-d" . term-send-delete-word)
     ("M-," . term-send-raw)
     ("M-." . comint-dynamic-complete))))
```


### Term Keys

[Term Keys](https://github.com/CyberShadow/term-keys), a lossless keyboard input for Emacs in terminal emulators.

```emacs-lisp
(use-package term-keys
  :if (not (display-graphic-p))
  :config (term-keys-mode t))
```


### Exec Path From Shell

[Exec Path From Shell](https://github.com/purcell/exec-path-from-shell), a library to ensure environment variables inside Emacs look the same as in the user's shell.

```emacs-lisp
(use-package exec-path-from-shell
  :if (memq window-system '(mac ns x))
  :config
  (exec-path-from-shell-initialize))
```


<a id="orgf5c14db"></a>

## Sudo Edit

[Sudo Edit](https://github.com/nflath/sudo-edit), an utility for opening files with `sudo`.

```emacs-lisp
(use-package sudo-edit
  :commands (sudo-edit))
```


<a id="org955e4dd"></a>

## Ibuffer

[Ibuffer](https://www.emacswiki.org/emacs/IbufferMode), an advanced replacement for BufferMenu, which lets you operate on buffers much in the same manner as Dired.

It uses [IBuffer VC](https://github.com/purcell/ibuffer-vc) that group buffers by git project and show file state.

```emacs-lisp
(use-package ibuffer
  :ensure nil
  :bind ("C-x C-b" . ibuffer)
  :init
  (use-package ibuffer-vc
    :commands (ibuffer-vc-set-filter-groups-by-vc-root)
    :custom
    (ibuffer-vc-skip-if-remote 'nil))
  :custom
  (ibuffer-formats
   '((mark modified read-only locked " "
           (name 35 35 :left :elide)
           " "
           (size 9 -1 :right)
           " "
           (mode 16 16 :left :elide)
           " " filename-and-process)
     (mark " "
           (name 16 -1)
           " " filename))))
```


<a id="org4e42742"></a>

## Config

Some essential configs that make my life a lot easier.


### UTF-8 Coding System

Use UTF-8 as much as possible with unix line endings.

```emacs-lisp
(unless *sys/win32*
  (set-selection-coding-system 'utf-8)
  (prefer-coding-system 'utf-8)
  (set-language-environment "UTF-8")
  (set-default-coding-systems 'utf-8)
  (set-terminal-coding-system 'utf-8)
  (set-keyboard-coding-system 'utf-8)
  (setq locale-coding-system 'utf-8))
;; Treat clipboard input as UTF-8 string first; compound text next, etc.
(when (display-graphic-p)
  (setq x-select-request-type '(UTF8_STRING COMPOUND_TEXT TEXT STRING)))
```


### Optimize Editing Experience

```emacs-lisp
;; Remove useless whitespace before saving a file
(defun delete-trailing-whitespace-except-current-line ()
  "An alternative to `delete-trailing-whitespace'.

The original function deletes trailing whitespace of the current line."
  (interactive)
  (let ((begin (line-beginning-position))
        (end (line-end-position)))
    (save-excursion
      (when (< (point-min) (1- begin))
        (save-restriction
          (narrow-to-region (point-min) (1- begin))
          (delete-trailing-whitespace)
          (widen)))
      (when (> (point-max) (+ end 2))
        (save-restriction
          (narrow-to-region (+ end 2) (point-max))
          (delete-trailing-whitespace)
          (widen))))))

(defun smart-delete-trailing-whitespace ()
  "Invoke `delete-trailing-whitespace-except-current-line' on selected major modes only."
  (unless (member major-mode '(diff-mode))
    (delete-trailing-whitespace-except-current-line)))

(defun toggle-auto-trailing-ws-removal ()
  "Toggle trailing whitespace removal."
  (interactive)
  (if (member #'smart-delete-trailing-whitespace before-save-hook)
      (progn
        (remove-hook 'before-save-hook #'smart-delete-trailing-whitespace)
        (message "Disabled auto remove trailing whitespace."))
    (add-hook 'before-save-hook #'smart-delete-trailing-whitespace)
    (message "Enabled auto remove trailing whitespace.")))
;; Add to hook during startup
(add-hook 'before-save-hook #'smart-delete-trailing-whitespace)

;; Replace selection on insert
(delete-selection-mode 1)

;; Map Alt key to Meta
(setq x-alt-keysym 'meta)
```


### History

```emacs-lisp
(use-package recentf
  :ensure nil
  :hook (after-init . recentf-mode)
  :custom
  (recentf-auto-cleanup "05:00am")
  (recentf-max-saved-items 200)
  (recentf-exclude '((expand-file-name package-user-dir)
                     ".cache"
                     ".cask"
                     ".elfeed"
                     "bookmarks"
                     "cache"
                     "ido.*"
                     "persp-confs"
                     "recentf"
                     "undo-tree-hist"
                     "url"
                     "COMMIT_EDITMSG\\'")))

;; When buffer is closed, saves the cursor location
(save-place-mode 1)

;; Set history-length longer
(setq-default history-length 500)
```


### Small Configs

```emacs-lisp
;; Move the backup fies to user-emacs-directory/.backup
(setq backup-directory-alist `(("." . ,(expand-file-name ".backup" user-emacs-directory))))

;; Ask before killing emacs
(setq confirm-kill-emacs 'y-or-n-p)

;; Automatically kill all active processes when closing Emacs
(setq confirm-kill-processes nil)

;; Turn Off Cursor Alarms
(setq ring-bell-function 'ignore)

;; Show Keystrokes in Progress Instantly
(setq echo-keystrokes 0.1)

;; Don't Lock Files
(setq-default create-lockfiles nil)

;; Better Compilation
(setq-default compilation-always-kill t) ; kill compilation process before starting another

(setq-default compilation-ask-about-save nil) ; save all buffers on `compile'

(setq-default compilation-scroll-output t)

;; ad-handle-definition warnings are generated when functions are redefined with `defadvice',
;; they are not helpful.
(setq ad-redefinition-action 'accept)

;; Move Custom-Set-Variables to Different File
(setq custom-file (concat user-emacs-directory "custom-set-variables.el"))
(load custom-file 'noerror)

;; So Long mitigates slowness due to extremely long lines.
;; Currently available in Emacs master branch *only*!
(when (fboundp 'global-so-long-mode)
  (global-so-long-mode))

;; Add a newline automatically at the end of the file upon save.
(setq require-final-newline t)

;; Enable `erase-buffer' function
(put 'erase-buffer 'disabled nil)

;; Default .args, .in, .out files to text-mode
(add-to-list 'auto-mode-alist '("\\.in\\'" . text-mode))
(add-to-list 'auto-mode-alist '("\\.out\\'" . text-mode))
(add-to-list 'auto-mode-alist '("\\.args\\'" . text-mode))
(add-to-list 'auto-mode-alist '("\\.bb\\'" . shell-script-mode))
(add-to-list 'auto-mode-alist '("\\.bbclass\\'" . shell-script-mode))
(add-to-list 'auto-mode-alist '("\\.Rmd\\'" . markdown-mode))
```


<a id="org8b9615a"></a>

## Functions

Important functions.


### Resize Window Width / Height Functions

```emacs-lisp
;; Resizes the window width based on the input
(defun resize-window-width (w)
  "Resizes the window width based on W."
  (interactive (list (if (> (count-windows) 1)
                         (read-number "Set the current window width in [1~9]x10%: ")
                       (error "You need more than 1 window to execute this function!"))))
  (message "%s" w)
  (window-resize nil (- (truncate (* (/ w 10.0) (frame-width))) (window-total-width)) t))

;; Resizes the window height based on the input
(defun resize-window-height (h)
  "Resizes the window height based on H."
  (interactive (list (if (> (count-windows) 1)
                         (read-number "Set the current window height in [1~9]x10%: ")
                       (error "You need more than 1 window to execute this function!"))))
  (message "%s" h)
  (window-resize nil (- (truncate (* (/ h 10.0) (frame-height))) (window-total-height)) nil))

;; Setup shorcuts for window resize width and height
(global-set-key (kbd "C-z w") #'resize-window-width)
(global-set-key (kbd "C-z h") #'resize-window-height)

(defun resize-window (width delta)
  "Resize the current window's size.  If WIDTH is non-nil, resize width by some DELTA."
  (if (> (count-windows) 1)
      (window-resize nil delta width)
    (error "You need more than 1 window to execute this function!")))

;; Setup shorcuts for window resize width and height
(defun window-width-increase ()
  (interactive)
  (resize-window t 5))

(defun window-width-decrease ()
  (interactive)
  (resize-window t -5))

(defun window-height-increase ()
  (interactive)
  (resize-window nil 5))

(defun window-height-decrease ()
  (interactive)
  (resize-window nil -5))

(global-set-key (kbd "M-W =") #'window-width-increase)
(global-set-key (kbd "M-W M-+") #'window-width-increase)
(global-set-key (kbd "M-W -") #'window-width-decrease)
(global-set-key (kbd "M-W M-_") #'window-width-decrease)

(global-set-key (kbd "M-E =") #'window-height-increase)
(global-set-key (kbd "M-E M-+") #'window-height-increase)
(global-set-key (kbd "M-E -") #'window-height-decrease)
(global-set-key (kbd "M-E M-_") #'window-height-decrease)
```


### Edit This Configuration File Shortcut

```emacs-lisp
(defun edit-configs ()
  "Opens the README.org file."
  (interactive)
  (find-file "~/.emacs.d/init.org"))

(global-set-key (kbd "C-z e") #'edit-configs)
```


### Update Org Mode Include Automatically

Update Org Mode INCLUDE Statements Automatically from [Artur Malabarba](http://endlessparentheses.com/updating-org-mode-include-statements-on-the-fly.html).

```emacs-lisp
(defun save-and-update-includes ()
  "Update the line numbers of #+INCLUDE:s in current buffer.
Only looks at INCLUDEs that have either :range-begin or :range-end.
This function does nothing if not in `org-mode', so you can safely
add it to `before-save-hook'."
  (interactive)
  (when (derived-mode-p 'org-mode)
    (save-excursion
      (goto-char (point-min))
      (while (search-forward-regexp
              "^\\s-*#\\+INCLUDE: *\"\\([^\"]+\\)\".*:range-\\(begin\\|end\\)"
              nil 'noerror)
        (let* ((file (expand-file-name (match-string-no-properties 1)))
               lines begin end)
          (forward-line 0)
          (when (looking-at "^.*:range-begin *\"\\([^\"]+\\)\"")
            (setq begin (match-string-no-properties 1)))
          (when (looking-at "^.*:range-end *\"\\([^\"]+\\)\"")
            (setq end (match-string-no-properties 1)))
          (setq lines (decide-line-range file begin end))
          (when lines
            (if (looking-at ".*:lines *\"\\([-0-9]+\\)\"")
                (replace-match lines :fixedcase :literal nil 1)
              (goto-char (line-end-position))
              (insert " :lines \"" lines "\""))))))))

(add-hook 'before-save-hook #'save-and-update-includes)

(defun decide-line-range (file begin end)
  "Visit FILE and decide which lines to include.
BEGIN and END are regexps which define the line range to use."
  (let (l r)
    (save-match-data
      (with-temp-buffer
        (insert-file-contents file)
        (goto-char (point-min))
        (if (null begin)
            (setq l "")
          (search-forward-regexp begin)
          (setq l (line-number-at-pos (match-beginning 0))))
        (if (null end)
            (setq r "")
          (search-forward-regexp end)
          (setq r (1+ (line-number-at-pos (match-end 0)))))
        (format "%s-%s" (+ l 1) (- r 1)))))) ;; Exclude wrapper
```


### MiniBuffer Functions

```emacs-lisp
(defun abort-minibuffer-using-mouse ()
  "Abort the minibuffer when using the mouse."
  (when (and (>= (recursion-depth) 1) (active-minibuffer-window))
    (abort-recursive-edit)))

(add-hook 'mouse-leave-buffer-hook 'abort-minibuffer-using-mouse)

;; keep the point out of the minibuffer
(setq-default minibuffer-prompt-properties '(read-only t point-entered minibuffer-avoid-prompt face minibuffer-prompt))
```


### Display Line Overlay

```emacs-lisp
(defun display-line-overlay+ (pos str &optional face)
  "Display line at POS as STR with FACE.

FACE defaults to inheriting from default and highlight."
  (let ((ol (save-excursion
              (goto-char pos)
              (make-overlay (line-beginning-position)
                            (line-end-position)))))
    (overlay-put ol 'display str)
    (overlay-put ol 'face
                 (or face '(:background null :inherit highlight)))
    ol))
```


### Read Lines From File

```emacs-lisp
(defun read-lines (file-path)
  "Return a list of lines of a file at FILE-PATH."
  (with-temp-buffer (insert-file-contents file-path)
                    (split-string (buffer-string) "\n" t)))
```


### Where Am I

```emacs-lisp
(defun where-am-i ()
  "An interactive function showing function `buffer-file-name' or `buffer-name'."
  (interactive)
  (message (kill-new (if (buffer-file-name) (buffer-file-name) (buffer-name)))))
```


<a id="orgf295218"></a>

# UI Enhancements


<a id="org5ff6e50"></a>

## Doom Themes

[Doom Themes](https://github.com/hlissner/emacs-doom-themes), an UI plugin and pack of themes.

```emacs-lisp
(use-package doom-themes
  :custom-face
  (cursor ((t (:background "BlanchedAlmond"))))
  :config
  ;; flashing mode-line on errors
  (doom-themes-visual-bell-config)
  ;; Corrects (and improves) org-mode's native fontification.
  (doom-themes-org-config)
  (load-theme 'doom-one t)
  (defun switch-theme ()
    "An interactive funtion to switch themes."
    (interactive)
    (disable-theme (intern (car (mapcar #'symbol-name custom-enabled-themes))))
    (call-interactively #'load-theme)))
```


<a id="orga2ce52d"></a>

## Doom Modeline

[Doom Modeline](https://github.com/seagle0128/doom-modeline), a modeline from DOOM Emacs, but more powerful and faster.

```emacs-lisp
(use-package doom-modeline
  :custom
  ;; Don't compact font caches during GC. Windows Laggy Issue
  (inhibit-compacting-font-caches t)
  (doom-modeline-minor-modes t)
  (doom-modeline-icon t)
  (doom-modeline-major-mode-color-icon t)
  (doom-modeline-height 15)
  :config
  (doom-modeline-mode))
```


<a id="orgc633774"></a>

## Dashboard


### Dashboard

[Dashboard](https://github.com/rakanalh/emacs-dashboard), an extensible Emacs startup screen.

Use either `KEC_Dark_BK.png` or `KEC_Light_BK.png` depends on the backgrond theme.

```emacs-lisp
(use-package dashboard
  :demand
  :diminish (dashboard-mode page-break-lines-mode)
  :bind
  (("C-z d" . open-dashboard)
   :map dashboard-mode-map
   (("n" . dashboard-next-line)
    ("p" . dashboard-previous-line)
    ("N" . dashboard-next-section)
    ("F" . dashboard-previous-section)))
  :custom
  (dashboard-banner-logo-title "Close the world. Open the nExt.")
  (dashboard-startup-banner (expand-file-name "images/KEC_Dark_BK_Small.png" user-emacs-directory))
  (dashboard-items '((recents  . 7)
                     (bookmarks . 7)
                     (agenda . 5)))
  (initial-buffer-choice (lambda () (get-buffer dashboard-buffer-name)))
  (dashboard-set-heading-icons t)
  (dashboard-set-navigator t)
  (dashboard-navigator-buttons
   (if (featurep 'all-the-icons)
       `(((,(all-the-icons-octicon "mark-github" :height 1.1 :v-adjust -0.05)
           "M-EMACS" "Browse M-EMACS Homepage"
           (lambda (&rest _) (browse-url "https://github.com/MatthewZMD/.emacs.d")))
          (,(all-the-icons-fileicon "elisp" :height 1.0 :v-adjust -0.1)
           "Configuration" "" (lambda (&rest _) (edit-configs)))
          (,(all-the-icons-faicon "cogs" :height 1.0 :v-adjust -0.1)
           "Update" "" (lambda (&rest _) (auto-package-update-now)))))
     `((("" "M-EMACS" "Browse M-EMACS Homepage"
         (lambda (&rest _) (browse-url "https://github.com/MatthewZMD/.emacs.d")))
        ("" "Configuration" "" (lambda (&rest _) (edit-configs)))
        ("" "Update" "" (lambda (&rest _) (auto-package-update-now)))))))
  :custom-face
  (dashboard-banner-logo-title ((t (:family "Love LetterTW" :height 123))))
  :config
  (dashboard-setup-startup-hook)
  ;; Open Dashboard function
  (defun open-dashboard ()
    "Open the *dashboard* buffer and jump to the first widget."
    (interactive)
    (dashboard-insert-startupify-lists)
    (switch-to-buffer dashboard-buffer-name)
    (goto-char (point-min))
    (delete-other-windows)))
```


### Page Break Lines

[Page-break-lines](https://github.com/purcell/page-break-lines), a feature that displays ugly form feed characters as tidy horizontal rules.

```emacs-lisp
(use-package page-break-lines
  :diminish
  :init (global-page-break-lines-mode))
```


<a id="org7226924"></a>

## Fonts and Icons

**Prerequisite**: Install all the available fonts and icons from `fonts/`. Execute `M-x all-the-icons-install-fonts` and `M-x nerd-icons-install-fonts`.


### Fonts

```emacs-lisp
;; Input Mono, Monaco Style, Line Height 1.3 download from http://input.fontbureau.com/
(defvar font-list '(("Input" . 11) ("Hack" . 12) ("Consolas" . 12) ("Love LetterTW" . 12.5))
  "List of fonts and sizes.  The first one available will be used.")
```

Function to switch between fonts.

```emacs-lisp
(defun change-font ()
  "Interactively change a font from a list a available fonts."
  (interactive)
  (let* (available-fonts font-name font-size font-setting)
    (dolist (font font-list (setq available-fonts (nreverse available-fonts)))
      (when (member (car font) (font-family-list))
        (push font available-fonts)))
    (if (not available-fonts)
        (message "No fonts from the chosen set are available")
      (if (called-interactively-p 'interactive)
          (let* ((chosen (assoc-string (completing-read "What font to use? " available-fonts nil t) available-fonts)))
            (setq font-name (car chosen) font-size (read-number "Font size: " (cdr chosen))))
        (setq font-name (caar available-fonts) font-size (cdar available-fonts)))
      (setq font-setting (format "%s-%d" font-name font-size))
      (set-frame-font font-setting nil t)
      (add-to-list 'default-frame-alist (cons 'font font-setting)))))

(when (display-graphic-p)
  (change-font))
```


### All The Icons

[All The Icons](https://github.com/domtronn/all-the-icons.el), a utility package to collect various Icon Fonts. Enable only in GUI Emacs.

```emacs-lisp
(use-package all-the-icons :if (display-graphic-p))
```


<a id="orgea94152"></a>

## Smooth Scrolling

Configurations to smooth scrolling.

```emacs-lisp
;; Vertical Scroll
(setq scroll-step 1)
(setq scroll-margin 1)
(setq scroll-conservatively 101)
(setq scroll-up-aggressively 0.01)
(setq scroll-down-aggressively 0.01)
(setq auto-window-vscroll nil)
(setq fast-but-imprecise-scrolling nil)
(setq mouse-wheel-scroll-amount '(1 ((shift) . 1)))
(setq mouse-wheel-progressive-speed nil)
;; Horizontal Scroll
(setq hscroll-step 1)
(setq hscroll-margin 1)
```


<a id="org9b3a1ec"></a>

## Highlight Lines

```emacs-lisp
(global-hl-line-mode 1)
```


<a id="org833a13d"></a>

## Prettify Symbols

[Prettify symbols mode](https://www.emacswiki.org/emacs/PrettySymbol), a built-in mode for displaying sequences of characters as fancy characters or symbols.

```emacs-lisp
(global-prettify-symbols-mode 1)
(defun add-pretty-lambda ()
  "Make some word or string show as pretty Unicode symbols.  See https://unicodelookup.com for more."
  (setq prettify-symbols-alist
        '(("lambda" . 955)
          ("delta" . 120517)
          ("epsilon" . 120518)
          ("->" . 8594)
          ("<=" . 8804)
          (">=" . 8805))))
(add-hook 'prog-mode-hook 'add-pretty-lambda)
(add-hook 'org-mode-hook 'add-pretty-lambda)
```


<a id="org88d48d8"></a>

## UI Configs


### Title Bar

```emacs-lisp
(setq-default frame-title-format '("M-EMACS - " user-login-name "@" system-name " - %b"))
```


### Simplify Yes/No Prompts

```emacs-lisp
(fset 'yes-or-no-p 'y-or-n-p)
(setq use-dialog-box nil)
```


### Disable Splash Screen

```emacs-lisp
(setq inhibit-startup-screen t)
(setq initial-major-mode 'text-mode)
;; https://www.youtube.com/watch?v=NfjsLmya1PI
(setq initial-scratch-message "Present Day, Present Time...\n")
```


### Line Numbers

Display line numbers, and column numbers in modeline.

```emacs-lisp
;; Hook line numbers to only when files are opened, also use linum-mode for emacs-version< 26
(if (version< emacs-version "26")
    (global-linum-mode)
  (add-hook 'text-mode-hook #'display-line-numbers-mode)
  (add-hook 'prog-mode-hook #'display-line-numbers-mode))
;; Display column numbers in modeline
(column-number-mode 1)
```


### Modeline Time and Battery

Display time and battery information in modeline.

```emacs-lisp
(display-time-mode 1)
(when (and battery-status-function
           (not (string-match-p "N/A" (battery-format "%B" (funcall battery-status-function)))))
  (display-battery-mode 1))
```


### Pixel Scroll Precision Mode

Pixel scroll precision mode, introduced in Emacs 29.1, displays text pixel-by-pixel.

```emacs-lisp
(when (version<= "29.1" emacs-version)
  (pixel-scroll-precision-mode 1))
```


<a id="org90d2e48"></a>

# General Programming


<a id="orgfbfd407"></a>

## Magit

[Magit](https://magit.vc/), an interface to the version control system Git.

```emacs-lisp
(use-package magit
  :if (executable-find "git")
  :bind
  (("C-x g" . magit-status)
   (:map magit-status-mode-map
         ("M-RET" . magit-diff-visit-file-other-window)))
  :config
  (defun magit-log-follow-current-file ()
    "A wrapper around `magit-log-buffer-file' with `--follow' argument."
    (interactive)
    (magit-log-buffer-file t)))
```


<a id="orgd182f76"></a>

## Projectile

[Projectile](https://github.com/bbatsov/projectile), a Project Interaction Library for Emacs.

**Prerequisite**: Windows OS: Install [Gow](https://github.com/bmatzelle/gow/releases) and ensure it's in `PATH`.

[Gow](https://github.com/bmatzelle/gow) is a lightweight installer that installs useful open source UNIX applications compiled as native win32 binaries. Specifically, `tr` is needed for Projectile alien indexing.

```emacs-lisp
(use-package projectile
  :bind
  ("C-c p" . projectile-command-map)
  :custom
  (projectile-completion-system 'ivy)
  :config
  (projectile-mode 1)
  (when (and *sys/win32*
             (executable-find "tr"))
    (setq projectile-indexing-method 'alien))
  (add-to-list 'projectile-globally-ignored-directories "node_modules"))
```


<a id="org809e4da"></a>

## YASnippet


### YASnippet

[YASnippet](https://github.com/joaotavora/yasnippet), a programming template system for Emacs. It loads [YASnippet Snippets](https://github.com/AndreaCrotti/yasnippet-snippets), a collection of yasnippet snippets for many languages.

```emacs-lisp
(use-package yasnippet
  :diminish yas-minor-mode
  :init
  (use-package yasnippet-snippets :after yasnippet)
  :hook ((prog-mode LaTeX-mode org-mode markdown-mode) . yas-minor-mode)
  :bind
  (:map yas-minor-mode-map ("C-c C-n" . yas-expand-from-trigger-key))
  (:map yas-keymap
        (("TAB" . smarter-yas-expand-next-field)
         ([(tab)] . smarter-yas-expand-next-field)))
  :config
  (yas-reload-all)
  (defun smarter-yas-expand-next-field ()
    "Try to `yas-expand' then `yas-next-field' at current cursor position."
    (interactive)
    (let ((old-point (point))
          (old-tick (buffer-chars-modified-tick)))
      (yas-expand)
      (when (and (eq old-point (point))
                 (eq old-tick (buffer-chars-modified-tick)))
        (ignore-errors (yas-next-field))))))
```


<a id="org30269b2"></a>

## Dumb Jump

[Dumb jump](https://github.com/jacktasia/dumb-jump), an Emacs "jump to definition" package.

```emacs-lisp
(use-package dumb-jump
  :bind
  (:map prog-mode-map
        (("C-c C-o" . dumb-jump-go-other-window)
         ("C-c C-j" . dumb-jump-go)
         ("C-c C-i" . dumb-jump-go-prompt)))
  :custom (dumb-jump-selector 'ivy))
```


<a id="org069bf41"></a>

## Parenthesis


### Smartparens

[Smartparens](https://github.com/Fuco1/smartparens), a minor mode for dealing with pairs.

```emacs-lisp
(use-package smartparens
  :hook (prog-mode . smartparens-mode)
  :diminish smartparens-mode
  :bind
  (:map smartparens-mode-map
        ("C-M-f" . sp-forward-sexp)
        ("C-M-b" . sp-backward-sexp)
        ("C-M-a" . sp-backward-down-sexp)
        ("C-M-e" . sp-up-sexp)
        ("C-M-w" . sp-copy-sexp)
        ("C-M-k" . sp-change-enclosing)
        ("M-k" . sp-kill-sexp)
        ("C-M-<backspace>" . sp-splice-sexp-killing-backward)
        ("C-S-<backspace>" . sp-splice-sexp-killing-around)
        ("C-]" . sp-select-next-thing-exchange))
  :custom
  (sp-escape-quotes-after-insert nil)
  :config
  ;; Stop pairing single quotes in elisp
  (sp-local-pair 'emacs-lisp-mode "'" nil :actions nil)
  (sp-local-pair 'org-mode "[" nil :actions nil))
```


### Match Parenthesis

Match and automatically pair parenthesis, and show parenthesis even when it went offscreen from [Clemens Radermacher](https://with-emacs.com/posts/editing/show-matching-lines-when-parentheses-go-off-screen/).

```emacs-lisp
;; Show matching parenthesis
(show-paren-mode 1)
;; we will call `blink-matching-open` ourselves...
(remove-hook 'post-self-insert-hook
             #'blink-paren-post-self-insert-function)

;; this still needs to be set for `blink-matching-open` to work
(setq blink-matching-paren 'show)
(let ((ov nil)) ; keep track of the overlay
  (advice-add
   #'show-paren-function
   :after
    (defun show-paren--off-screen+ (&rest _args)
      "Display matching line for off-screen paren."
      (when (overlayp ov)
        (delete-overlay ov))
      ;; check if it's appropriate to show match info,
      ;; see `blink-paren-post-self-insert-function'
      (when (and (overlay-buffer show-paren--overlay)
                 (not (or cursor-in-echo-area
                          executing-kbd-macro
                          noninteractive
                          (minibufferp)
                          this-command))
                 (and (not (bobp))
                      (memq (char-syntax (char-before)) '(?\) ?\$)))
                 (= 1 (logand 1 (- (point)
                                   (save-excursion
                                     (forward-char -1)
                                     (skip-syntax-backward "/\\")
                                     (point))))))
        ;; rebind `minibuffer-message' called by
        ;; `blink-matching-open' to handle the overlay display
        (cl-letf (((symbol-function #'minibuffer-message)
                   (lambda (msg &rest args)
                     (let ((msg (apply #'format-message msg args)))
                       (setq ov (display-line-overlay+
                                 (window-start) msg))))))
          (blink-matching-open))))))
```


<a id="orgc480821"></a>

## Indentation

[Highlight Indent Guides](https://github.com/DarthFennec/highlight-indent-guides), a feature that highlights indentation levels.

```emacs-lisp
(use-package highlight-indent-guides
  :if (display-graphic-p)
  :diminish
  ;; Enable manually if needed, it a severe bug which potentially core-dumps Emacs
  ;; https://github.com/DarthFennec/highlight-indent-guides/issues/76
  :commands (highlight-indent-guides-mode)
  :mode ("\\.yml\\'" . highlight-indent-guides-mode)
  :custom
  (highlight-indent-guides-method 'character)
  (highlight-indent-guides-responsive 'top)
  (highlight-indent-guides-delay 0)
  (highlight-indent-guides-auto-character-face-perc 7))
```

Indentation Configuration

```emacs-lisp
(setq-default indent-tabs-mode nil)
(setq-default indent-line-function 'insert-tab)
(setq-default tab-width 4)
(setq-default c-basic-offset 4)
(setq-default js-switch-indent-offset 4)
(c-set-offset 'comment-intro 0)
(c-set-offset 'innamespace 0)
(c-set-offset 'case-label '+)
(c-set-offset 'access-label 0)
(c-set-offset (quote cpp-macro) 0 nil)
(defun smart-electric-indent-mode ()
  "Disable 'electric-indent-mode in certain buffers and enable otherwise."
  (cond ((and (eq electric-indent-mode t)
              (member major-mode '(erc-mode text-mode)))
         (electric-indent-mode 0))
        ((eq electric-indent-mode nil) (electric-indent-mode 1))))
(add-hook 'post-command-hook #'smart-electric-indent-mode)
```


<a id="orgdb1fb0f"></a>

## Quickrun

[Quickrun](https://github.com/syohex/emacs-quickrun), compile and run source code quickly.

```emacs-lisp
(use-package quickrun
  :custom
  (quickrun-timeout-seconds 60)
  :bind
  (("<f5>" . quickrun)
   ("M-<f5>" . quickrun-shell)
   ("C-c e" . quickrun)
   ("C-c C-e" . quickrun-shell)))
```


<a id="org5a90b40"></a>

## Format All

[Format all](https://github.com/lassik/emacs-format-all-the-code), a feature that lets you auto-format source code.

**Prerequisite**: Read [Supported Languages](https://github.com/lassik/emacs-format-all-the-code#supported-languages) to see which additional tool you need to install for the specific language.

```emacs-lisp
(use-package format-all
  :bind ("C-c C-f" . format-all-buffer))
```


<a id="org1b808b4"></a>

## Ediff

[Ediff](https://www.gnu.org/software/emacs/manual/html_mono/ediff.html), a mode to simultaneously browse through the differences between a pair of files or buffers.

```emacs-lisp
(use-package ediff
  :custom
  (ediff-split-window-function #'split-window-horizontally)
  (ediff-window-setup-function #'ediff-setup-windows-plain))
```


<a id="org77bd567"></a>

## Evil Nerd Commenter

[Evil Nerd Commenter](https://github.com/redguardtoo/evil-nerd-commenter), a tool that helps you comment code efficiently.

```emacs-lisp
(use-package evil-nerd-commenter
  :bind
  (("C-c M-;" . c-toggle-comment-style)
   ("M-;" . evilnc-comment-or-uncomment-lines)))
```


<a id="orga17e03b"></a>

## Editing


### Iedit

[Iedit](https://github.com/victorhge/iedit), a minor mode that allows editing multiple regions simultaneousy in a buffer or a region.

```emacs-lisp
(use-package iedit
  :bind ("C-z ," . iedit-mode)
  :diminish)
```


### Delete Block

[Delete Block](https://github.com/manateelazycat/delete-block), a feature that deletes block efficiently.

```emacs-lisp
(use-package delete-block
  :load-path (lambda () (expand-file-name "site-elisp/delete-block" user-emacs-directory))
  :bind
  (("M-d" . delete-block-forward)
   ("C-<backspace>" . delete-block-backward)
   ("M-<backspace>" . delete-block-backward)
   ("M-DEL" . delete-block-backward)))
```


<a id="orga6c7209"></a>

## Headers

[Header2](https://www.emacswiki.org/emacs/header2.el), a support for creation and update of file headers.

```emacs-lisp
(use-package header2
  :load-path (lambda () (expand-file-name "site-elisp/header2" user-emacs-directory))
  :custom
  (header-copyright-notice (concat "Copyright (C) 2019 " (user-full-name) "\n"))
  :hook (emacs-lisp-mode . auto-make-header)
  :config
  (add-to-list 'write-file-functions 'auto-update-file-header)
  (autoload 'auto-make-header "header2")
  (autoload 'auto-update-file-header "header2"))
```


<a id="org0be1bae"></a>

## Jupyter Notebook

[Emacs IPython Notebook](https://github.com/millejoh/emacs-ipython-notebook), a [Jupyter](https://jupyter.org/) (formerly IPython) client in Emacs.


### Usage

1.  Execute `M-x ein:run` to launch a local Jupyter session.
2.  Login with `M-x ein:login` to a local or remote session.
3.  Open `.ipynb` file and press `C-c C-o`.

```emacs-lisp
(use-package ein
  :if (executable-find "jupyter")
  :bind
  (("C-c e" . ein:worksheet-execute-cell)
   ("C-c C-e" . ein:worksheet-execute-all-cells))
  :custom-face
  (ein:basecell-input-area-face ((t (:extend t :background "#303640"))))
  :defer t
  :custom
  (ein:worksheet-enable-undo t))
```


<a id="org6fa6bff"></a>

## Completion / LSP

Instead of the popular [Company](http://company-mode.github.io/), I opt-ed to use [lsp-bridge](https://github.com/manateelazycat/lsp-bridge) that is completely **multi-threading** technology, handles almost all of my completion needs.

```emacs-lisp
(use-package lsp-bridge
  :load-path (lambda () (expand-file-name "site-elisp/lsp-bridge" user-emacs-directory))
  :defer 1
  :commands (global-lsp-bridge-mode lsp-bridge-mode)
  :custom
  (acm-enable-codeium t)
  (acm-enable-tabnine nil)
  (acm-enable-quick-access t)
  (lsp-bridge-enable-hover-diagnostic t)
  :bind (("M-." . lsp-bridge-find-def)
         ("M-," . lsp-bridge-find-def-return)
         ("M-i" . lsp-bridge-popup-documentation)
         :map lsp-bridge-ref-mode-map
         ("n" . lsp-bridge-ref-jump-next-keyword)
         ("p" . lsp-bridge-ref-jump-prev-keyword)
         ("M-n" . lsp-bridge-ref-jump-next-file)
         ("M-p" . lsp-bridge-ref-jump-prev-file)
         ("C-x C-q" . lsp-bridge-ref-switch-to-edit-mode)
         :map lsp-bridge-ref-mode-edit-map
         ("C-x C-q" . lsp-bridge-ref-apply-changed)
         ("C-x C-s" . lsp-bridge-ref-apply-changed)
         ("C-c C-k" . lsp-bridge-ref-quit)
         ("M-n" . lsp-bridge-ref-jump-next-file)
         ("M-p" . lsp-bridge-ref-jump-prev-file)
         :map acm-mode-map
         ([remap next-line] . nil)
         ([remap previous-line] . nil))
  :config
  (global-lsp-bridge-mode))
```


<a id="org9e93c54"></a>

# Programming


<a id="orga429a7b"></a>

## C/C++/Objective C

**Prerequisite**: Since all completion features are provided by [LSP Mode](https://github.com/emacs-lsp/lsp-mode), it needs to setup.

-   Install [CMake](https://cmake.org/download/) >= 3.8 for all OS.
-   \*nix OS:
    -   It is suggested to use [CCLS](https://github.com/MaskRay/ccls) as LSP server. Now [build](https://github.com/MaskRay/ccls/wiki/Build) it.
    -   Set `ccls-executable` to the directory where your ccls is built.
-   Windows OS:
    -   Install [MinGW](http://www.mingw.org/wiki/Install_MinGW) for Compilation.
    -   It is a pain to build CCLS on Windows, install [Clangd](https://clang.llvm.org/extra/clangd/Installation.html) and ensure it's in `PATH` instead.


### CCLS

[Emacs CCLS](https://github.com/MaskRay/emacs-ccls), a client for [CCLS](https://github.com/MaskRay/ccls), a C/C++/Objective-C language server supporting multi-million line C++ code-bases, powered by libclang.

```emacs-lisp
(use-package modern-cpp-font-lock
  :diminish t
  :init (modern-c++-font-lock-global-mode t))
;; -CPPFontLockPac

;; GoPac
(use-package go-mode
  :mode "\\.go\\'"
  :hook (before-save . gofmt-before-save)
  :custom (gofmt-command "goimports"))
;; -GoPac

;; RustPac
(use-package rust-mode
  :mode "\\.rs\\'"
  :custom
  (rust-format-on-save t)
  :bind (:map rust-mode-map ("C-c C-c" . rust-run))
  :config
  (use-package flycheck-rust
    :after flycheck
    :config
```


### Modern C++ Font Lock

[Modern CPP Font Lock](https://github.com/ludwigpacifici/modern-cpp-font-lock), font-locking for "Modern C++".

```emacs-lisp
(provide 'init-cc)
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
```


<a id="org7961933"></a>

## Golang

[Go Mode](https://github.com/dominikh/go-mode.el), an Emacs mode for Golang programming.

**Prerequisite**: [gopls](https://github.com/golang/tools/blob/master/gopls/README.md) is required for Golang's LSP support.

```bash
go get golang.org/x/tools/gopls@latest
```

```emacs-lisp

```


<a id="org5f48088"></a>

## Rust

[Rust Mode](https://github.com/rust-lang/rust-mode), an Emacs mode for Rust programming.

```emacs-lisp

```


<a id="org8829535"></a>

## Python

```emacs-lisp
(use-package python-mode
  :ensure nil
  :mode "\\.py\\'"
  :custom
  (python-indent-offset 4)
  (flycheck-python-pycompile-executable "python3")
  (python-shell-interpreter "python3"))
```


<a id="org800a36a"></a>

## Haskell

[Haskell Mode](https://github.com/haskell/haskell-mode), an Emacs mode for Haskell programming.

```emacs-lisp
(use-package haskell-mode
  :mode "\\.hs\\'")
```


<a id="org5e93050"></a>

## ESS

[Emacs Speaks Statistics](https://ess.r-project.org/), short for ESS, it's designed to support editing of scripts and interaction with various statistical analysis programs such as R, S-Plus, SAS, Stata and OpenBUGS/JAGS.

**Prerequisite**: Install [R](https://cran.r-project.org/mirrors.html) to start using ESS with R.

```emacs-lisp
(use-package ess
  :defer t
  :commands R
  :config
  (load "ess-autoloads"))
```


<a id="org779ed99"></a>

## TeX

**Prerequisite**: Please install [TeX Live](https://www.tug.org/texlive/quickinstall.html).


### AUCTeX

[AUCTeX](https://www.gnu.org/software/auctex/), an extensible package for writing and formatting TeX files. It supports many different TeX macro packages, including AMS-TEX, LaTeX, Texinfo, ConTEXt, and docTEX (dtx files).

```emacs-lisp
(use-package tex
  :ensure auctex
  :defer t
  :custom
  (TeX-auto-save t)
  (TeX-parse-self t)
  (TeX-master nil)
  ;; to use pdfview with auctex
  (TeX-view-program-selection '((output-pdf "pdf-tools"))
                              TeX-source-correlate-start-server t)
  (TeX-view-program-list '(("pdf-tools" "TeX-pdf-tools-sync-view")))
  (TeX-after-compilation-finished-functions #'TeX-revert-document-buffer)
  :hook
  (LaTeX-mode . (lambda ()
                  (turn-on-reftex)
                  (setq reftex-plug-into-AUCTeX t)
                  (reftex-isearch-minor-mode)
                  (setq TeX-PDF-mode t)
                  (setq TeX-source-correlate-method 'synctex)
                  (setq TeX-source-correlate-start-server t)))
  :config
  (when (version< emacs-version "26")
    (add-hook LaTeX-mode-hook #'display-line-numbers-mode)))
```


<a id="org4ee9775"></a>

## Yaml

[Yaml mode](https://github.com/yoshiki/yaml-mode), the Emacs major mode for editing files in the YAML data serialization format.

```emacs-lisp
(use-package yaml-mode
  :defer t
  :bind (("C-c p" . yaml-get-path-at-point))
  :mode "\\.yml\\'"
  :config
  (use-package yaml-pro
    :hook (yaml-mode . yaml-pro-mode)
    :bind (("C-c M-p" . yaml-pro-move-subtree-up)
           ("C-c M-n" . yaml-pro-move-subtree-down)))
  ;; Based on https://github.com/chopmo/dotfiles/blob/master/.emacs.d/customizations/yaml.el
  (defun yaml-indentation-level (s)
    (if (string-match "^ " s)
        (+ 1 (yaml-indentation-level (substring s 1)))
      0))
  (defun yaml-clean-string (s)
    (let* ((s (replace-regexp-in-string "^[ -:]*" "" s))
           (s (replace-regexp-in-string ":$" "" s)))
      s))
  (defun yaml-path-at-point ()
    (save-excursion
      (let* ((line (buffer-substring-no-properties (point-at-bol) (point-at-eol)))
             (level (yaml-indentation-level line))
             result)
        (while (> (point) (point-min))
          (beginning-of-line 0)
          (setq line (buffer-substring-no-properties (point-at-bol) (point-at-eol)))
          (let ((new-level (yaml-indentation-level line)))
            (when (and (string-match "[^[:blank:]]" line)
                       (< new-level level))
              (setq level new-level)
              (setq result (push (yaml-clean-string line) result)))))
        (mapconcat 'identity result " => "))))
  (defun yaml-get-path-at-point ()
    "Display the yaml path at point for 5 seconds"
    (interactive)
    (let ((ov (display-line-overlay+ (window-start) (yaml-path-at-point))))
      (run-with-timer 1 nil (lambda () (when (overlayp ov)
                                         (delete-overlay ov)))))))
```


<a id="orga6c62d3"></a>

## Buildsystem


### Docker

[Docker](https://github.com/Silex/docker.el), a mode to manage docker from Emacs.

```emacs-lisp
(use-package docker :defer t)
```

[Dockerfile Mode](https://github.com/spotify/dockerfile-mode), an Emacs mode for handling Dockerfiles.

```emacs-lisp
(use-package dockerfile-mode :defer t)
```


### Groovy

[Groovy Mode](https://github.com/Groovy-Emacs-Modes/groovy-emacs-modes), a groovy major mode, grails minor mode, and a groovy inferior mode.

```emacs-lisp
(use-package groovy-mode :defer t)
```


### Cmake

[Cmake Mode](https://melpa.org/#/cmake-mode), a library that provides syntax highlighting and indentation for CMakeLists.txt and \*.cmake source files.

```emacs-lisp
(use-package cmake-mode :defer t)
```


### Bazel

[Bazel Mode](https://github.com/bazelbuild/emacs-bazel-mode), a library that provides major modes for editing Bazel `BUILD` files, `WORKSPACE` files, `.bazelrc` files, as well as `Starlark` files.

```emacs-lisp
(use-package bazel :defer t)
```


<a id="org84a3b37"></a>

# Web Development

**Prerequisite**: Install [NodeJS](https://nodejs.org/en/download/) and ensure it's in `PATH`. Execute following commands to enable LSP for JavaScript/TypeScript/HTML:

```bash
npm i -g typescript
npm i -g typescript-language-server
```


<a id="org254e7a6"></a>

## Web

[Web mode](https://github.com/fxbois/web-mode), a major mode for editing web templates.

```emacs-lisp
(use-package web-mode
  :custom-face
  (css-selector ((t (:inherit default :foreground "#66CCFF"))))
  (font-lock-comment-face ((t (:foreground "#828282"))))
  :mode
  ("\\.phtml\\'" "\\.tpl\\.php\\'" "\\.[agj]sp\\'" "\\.as[cp]x\\'"
   "\\.erb\\'" "\\.mustache\\'" "\\.djhtml\\'" "\\.[t]?html?\\'"))
```


<a id="orgb200642"></a>

## JavaScript/TypeScript


### JavaScript2

[JS2 mode](https://github.com/mooz/js2-mode), a feature that offers improved JavsScript editing mode.

```emacs-lisp
(use-package js2-mode
  :mode "\\.js\\'"
  :interpreter "node")
```


### TypeScript

[TypeScript mode](https://github.com/emacs-typescript/typescript.el), a feature that offers TypeScript support for Emacs.

```emacs-lisp
(use-package typescript-mode
  :mode "\\.ts\\'"
  :commands (typescript-mode))
```


### Vue

[Vue mode](https://github.com/AdamNiederer/vue-mode), a major mode for Vue.js.

```emacs-lisp
(use-package vue-mode
  :mode "\\.vue\\'"
  :commands (vue-mode))
```


<a id="orgcff2c8f"></a>

## Emmet

[Emmet](https://github.com/smihica/emmet-mode), a feature that allows writing HTML using CSS selectors along with `C-j`. See [usage](https://github.com/smihica/emmet-mode#usage) for more information.

```emacs-lisp
(use-package emmet-mode
  :hook ((web-mode . emmet-mode)
         (css-mode . emmet-mode)))
```


<a id="org6b57af0"></a>

## Instant Rename Tag

[Instant Rename Tag](https://github.com/manateelazycat/instant-rename-tag), a plugin that provides ability to rename html tag pairs instantly.

```emacs-lisp
(use-package instant-rename-tag
  :load-path (lambda () (expand-file-name "site-elisp/instant-rename-tag" user-emacs-directory))
  :bind ("C-z <" . instant-rename-tag))
```


<a id="orge094ccd"></a>

## JSON

[JSON Mode](https://github.com/joshwnj/json-mode), a major mode for editing JSON files.

```emacs-lisp
(use-package json-mode
  :mode "\\.json\\'")
```


<a id="org1f6da9b"></a>

# Office


<a id="org2e82a58"></a>

## Org

[Org](https://orgmode.org/), a Emacs built-in tool for keeping notes, maintaining TODO lists, planning projects, and authoring documents with a fast and effective plain-text system.

**Prerequisite**: Configure `(org-agenda-files (list "~/org/agenda/"))` to your agenda folder to use org-agenda. Once this is set, the agenda items tagged with `DEADLINE` or `SCHEDULED` will be displayed on the [Dashboard](#orgc633774) (hopefully the dashboard will be more detailed in the [future](https://github.com/MatthewZMD/.emacs.d/issues/37)).

```emacs-lisp
(use-package org
  :ensure nil
  :defer t
  :bind (("C-c l" . org-store-link)
         ("C-c a" . org-agenda)
         ("C-c c" . org-capture)
         (:map org-mode-map (("C-c C-p" . eaf-org-export-to-pdf-and-open)
                             ("C-c ;" . nil))))
  :custom
  (org-log-done 'time)
  (calendar-latitude 43.65107) ;; Prerequisite: set it to your location, currently default: Toronto, Canada
  (calendar-longitude -79.347015) ;; Usable for M-x `sunrise-sunset' or in `org-agenda'
  (org-export-backends (quote (ascii html icalendar latex md odt)))
  (org-use-speed-commands t)
  (org-confirm-babel-evaluate 'nil)
  (org-latex-listings-options '(("breaklines" "true")))
  (org-latex-listings t)
  (org-deadline-warning-days 7)
  (org-todo-keywords
   '((sequence "TODO" "IN-PROGRESS" "REVIEW" "|" "DONE" "CANCELED")))
  (org-agenda-window-setup 'other-window)
  (org-latex-pdf-process
   '("pdflatex -shelnl-escape -interaction nonstopmode -output-directory %o %f"
     "pdflatex -shell-escape -interaction nonstopmode -output-directory %o %f"))
  :custom-face
  (org-agenda-current-time ((t (:foreground "spring green"))))
  :config
  (add-to-list 'org-latex-packages-alist '("" "listings"))
  (unless (version< org-version "9.2")
    (require 'org-tempo))
  (when (file-directory-p "~/org/agenda/")
    (setq org-agenda-files (list "~/org/agenda/")))
  (org-babel-do-load-languages
   'org-babel-load-languages
   '(;; other Babel languages
     (C . t)
     (python . t)
     (plantuml . t)))
  (defun org-export-toggle-syntax-highlight ()
    "Setup variables to turn on syntax highlighting when calling `org-latex-export-to-pdf'."
    (interactive)
    (setq-local org-latex-listings 'minted)
    (add-to-list 'org-latex-packages-alist '("newfloat" "minted")))

  (defun org-table-insert-vertical-hline ()
    "Insert a #+attr_latex to the current buffer, default the align to |c|c|c|, adjust if necessary."
    (interactive)
    (insert "#+attr_latex: :align |c|c|c|")))
```


### Org Roam

[Org Roam](https://www.orgroam.com/), a plain-text personal knowledge management system.

```emacs-lisp
(use-package org-roam
  :after org
  :custom
  (org-roam-node-display-template
   (concat "${title:*} "
           (propertize "${tags:10}" 'face 'org-tag)))
  (org-roam-completion-everywhere t)
  :bind
  (("C-c n l" . org-roam-buffer-toggle)
   ("C-c n f" . org-roam-node-find)
   ("C-c n i" . org-roam-node-insert)
   ("C-c n h" . org-id-get-create))
  :config
  (when (file-directory-p "~/org/roam/")
    (setq org-roam-directory (file-truename "~/org/roam")))
  (org-roam-db-autosync-mode))
```


### TOC Org

[TOC Org](https://github.com/snosov1/toc-org) generates table of contents for `.org` files

```emacs-lisp
(use-package toc-org
  :hook (org-mode . toc-org-mode))
```


### HTMLize

[HTMLize](https://github.com/hniksic/emacs-htmlize), a tool that converts buffer text and decorations to HTML.

```emacs-lisp
(use-package htmlize :defer t)
```


### GFM Exporter

[OX-GFM](https://github.com/larstvei/ox-gfm), a Github Flavored Markdown exporter for Org Mode.

```emacs-lisp
(use-package ox-gfm :defer t)
```


### PlantUML and Graphviz

[PlantUML Mode](https://github.com/skuro/plantuml-mode), a major mode for editing PlantUML sources.

**Prerequisite**:

1.  Install [plantuml](http://plantuml.com/download) and configure `(org-plantuml-jar-path (expand-file-name "path/to/plantuml.jar"))`.
2.  Install [Graphviz](https://graphviz.gitlab.io/download/) on your system to support graph visualization. Execute `sudo apt install graphviz` in Ubuntu.

```emacs-lisp
(use-package plantuml-mode
  :defer t
  :custom
  (org-plantuml-jar-path (expand-file-name "~/tools/plantuml/plantuml.jar")))
```


<a id="org38cf7a0"></a>

## PDF Tools

[PDF Tools](https://github.com/politza/pdf-tools), an Emacs support library for PDF files. It works best on non-Windows OS.

**Note**: You need [convert](https://linux.die.net/man/1/convert) provided from imagemagick to *Pick a Link and Jump* with F.

```emacs-lisp
(use-package pdf-tools-install
  :ensure pdf-tools
  :if (and (display-graphic-p) (not *sys/win32*) (not eaf-env-p))
  :mode "\\.pdf\\'"
  :commands (pdf-loader-install)
  :custom
  (TeX-view-program-selection '((output-pdf "pdf-tools")))
  (TeX-view-program-list '(("pdf-tools" "TeX-pdf-tools-sync-view")))
  :hook
  (pdf-view-mode . (lambda () (display-line-numbers-mode -1)))
  :config
  (pdf-loader-install))
```


<a id="org3d3a1a7"></a>

# Internet


<a id="org80e93b9"></a>

## EAF

[Emacs Application Framework](https://github.com/manateelazycat/emacs-application-framework), a GUI application framework that revolutionizes Emacs graphical capabilities.

**Prerequisite**: Please ensure `python3` and `pip3` are installed, then follow [install](https://github.com/manateelazycat/emacs-application-framework#install) instructions.

```emacs-lisp
(use-package eaf
  :load-path (lambda () (expand-file-name "site-elisp/emacs-application-framework" user-emacs-directory))
  :if eaf-env-p
  :custom
  (eaf-start-python-process-when-require nil)
  (browse-url-browser-function #'eaf-open-browser) ;; Make EAF Browser my default browser
  (eaf-start-python-process-when-require t)
  (eaf-browser-dark-mode nil)
  (eaf-browser-enable-adblocker t)
  (eaf-webengine-continue-where-left-off t)
  (eaf-webengine-default-zoom 1.25)
  (eaf-webengine-scroll-step 200)
  (eaf-pdf-dark-mode "ignore")
  :demand
  :bind
  (("M-z r" . eaf-open-rss-reader)
   ("M-m r" . eaf-open-rss-reader)
   ("M-#" . eaf-open-pyqterminal))
  :config
  ;; Require all EAF apps unconditionally, change to apps you're interested in.
  (require 'eaf-file-manager nil t)
  (require 'eaf-music-player nil t)
  (require 'eaf-image-viewer nil t)
  (require 'eaf-camera nil t)
  (require 'eaf-demo nil t)
  (require 'eaf-airshare nil t)
  (require 'eaf-markdown-previewer nil t)
  (require 'eaf-video-player nil t)
  (require 'eaf-vue-demo nil t)
  (require 'eaf-file-sender nil t)
  (require 'eaf-pdf-viewer nil t)
  (require 'eaf-mindmap nil t)
  (require 'eaf-netease-cloud-music nil t)
  (require 'eaf-jupyter nil t)
  (require 'eaf-org-previewer nil t)
  (require 'eaf-system-monitor nil t)
  (require 'eaf-rss-reader nil t)
  (require 'eaf-pyqterminal nil t)
  (require 'eaf-file-browser nil t)
  (require 'eaf-browser nil t)
  (require 'eaf-git nil t)
  (when (display-graphic-p)
    (require 'eaf-all-the-icons))
  (defalias 'browse-web #'eaf-open-browser)
  (eaf-bind-key nil "M-q" eaf-browser-keybinding)
  (eaf-bind-key nil "M-z" eaf-browser-keybinding)
  (eaf-bind-key open_link "C-M-s" eaf-browser-keybinding)
  (eaf-bind-key open_devtools "M-i" eaf-browser-keybinding)
  (eaf-bind-key insert_or_recover_prev_close_page "X" eaf-browser-keybinding)
  (eaf-bind-key scroll_up "RET" eaf-pdf-viewer-keybinding)
  (eaf-bind-key delete_cookies "C-M-q" eaf-browser-keybinding)
  (eaf-bind-key delete_all_cookies "C-M-Q" eaf-browser-keybinding)
  (eaf-bind-key clear_history "C-M-p" eaf-browser-keybinding)
  (eaf-bind-key scroll_down_page "DEL" eaf-pdf-viewer-keybinding)
  (eaf-bind-key scroll_down_page "u" eaf-pdf-viewer-keybinding)
  (eaf-bind-key scroll_up_page "d" eaf-pdf-viewer-keybinding)
  (eaf-bind-key scroll_to_end "M->" eaf-pdf-viewer-keybinding)
  (eaf-bind-key scroll_to_begin "M-<" eaf-pdf-viewer-keybinding)
  (eaf-bind-key quit-window "q" eaf-pdf-viewer-keybinding)
  (eaf-bind-key zoom_in "C-=" eaf-pdf-viewer-keybinding)
  (eaf-bind-key zoom_out "C--" eaf-pdf-viewer-keybinding)
  (eaf-bind-key take_photo "p" eaf-camera-keybinding))
```


<a id="org53a99ca"></a>

## Popweb

[Popweb](https://github.com/manateelazycat/popweb), a lightweight version of EAF that provides multimedia capabilities.

```emacs-lisp
(use-package popweb
  :if eaf-env-p
  :load-path (lambda () (expand-file-name "site-elisp/popweb" user-emacs-directory))
  :init
  (add-to-list 'load-path (expand-file-name "site-elisp/popweb/extension/latex" user-emacs-directory))
  (add-to-list 'load-path (expand-file-name "site-elisp/popweb/extension/dict" user-emacs-directory))
  (require 'popweb-latex)
  (require 'popweb-dict)
  :custom
  (popweb-popup-pos "point-bottom")
  :hook ((org-mode . popweb-latex-mode)
         (tex-mode . popweb-latex-mode)
         (ein:markdown-mode . popweb-latex-mode))
  )
```


<a id="org6186551"></a>

## ERC

[Emacs Relay Chat](https://www.emacswiki.org/emacs/ERC), a powerful, modular, and extensible [IRC](http://www.irc.org/) client for Emacs. It utilizes [erc-hl-nicks](https://github.com/leathekd/erc-hl-nicks) for nickname highlighting and [erc-image](https://github.com/kidd/erc-image.el) to fetch and show received images in ERC.

**Prerequisite**: Put IRC credentials in the file `~/.authinfo` and configure `my-irc-nick` to your IRC nickname.

```text
machine irc.freenode.net login <nickname> password <password> port 6697
```

```emacs-lisp
(use-package erc
  :ensure nil
  :init
  ;; Prerequisite: Configure this to your IRC nickname
  (defcustom my-irc-nick ""
    "The nickname used to login into ERC"
    :type 'string)
  (use-package erc-hl-nicks :defer t)
  (use-package erc-image :defer t)
  :custom-face
  (erc-notice-face ((t (:foreground "#ababab"))))
  :custom
  (erc-autojoin-channels-alist '(("irc.libera.chat" "#emacs")))
  (erc-user-full-name user-full-name)
  (erc-track-exclude-types '("NICK" "PART" "MODE" "324" "329" "332" "333" "353" "477"))
  (erc-server-coding-system '(utf-8 . utf-8))
  (erc-interpret-mirc-color t)
  (erc-kill-buffer-on-part t)
  (erc-kill-queries-on-quit t)
  (erc-kill-server-buffer-on-quit t)
  (erc-autojoin-timing 'ident)
  (erc-fill-function 'erc-fill-static)
  (erc-fill-static-center 15)
  (erc-lurker-threshold-time 43200)
  (erc-server-reconnect-attempts 5)
  (erc-server-reconnect-timeout 3)
  (erc-prompt-for-password nil)
  (erc-prompt-for-nickserv-password nil)
  (erc-fill-column 100)
  (erc-save-buffer-on-part t)
  (erc-nick-uniquifier "_")
  (erc-log-channels-directory (expand-file-name ".erc-logs" user-emacs-directory))
  :bind
  (("M-z i" . erc-start-or-switch)
   ("M-m i" . erc-start-or-switch)
   ("C-c C-b" . erc-switch-to-buffer)
   (:map erc-mode-map
         ("M-RET" . newline)))
  :hook
  (ercn-notify . erc-notify)
  :config
  (make-directory (expand-file-name ".erc-logs" user-emacs-directory) t)
  (add-to-list 'erc-modules 'notifications)
  (erc-track-mode t)
  (erc-services-mode 1)
  (defun erc-start-or-switch ()
    "Start ERC or switch to ERC buffer if it has started already."
    (interactive)
    (if (get-buffer "irc.libera.chat:6697")
        (erc-track-switch-buffer 1)
      (erc-tls :server "irc.libera.chat" :port 6697 :nick my-irc-nick :full-name user-full-name)))

  (defun erc-notify (nickname message)
    "Displays a notification message for ERC."
    (let* ((channel (buffer-name))
           (nick (erc-hl-nicks-trim-irc-nick nickname))
           (title (if (string-match-p (concat "^" nickname) channel)
                      nick
                    (concat nick " (" channel ")")))
           (msg (s-trim (s-collapse-whitespace message))))
      (alert (concat nick ": " msg) :title title))))
```


<a id="org6c76e74"></a>

## MU4E

[Mu4e](https://www.djcbsoftware.nl/code/mu/mu4e.html), a package that provides an emacs-based e-mail client which uses [mu](https://www.djcbsoftware.nl/code/mu/) as its backend. [Mu4e Thread Folding](https://github.com/rougier/mu4e-thread-folding) is used to toggle between long threads.

**Note**: This mu4e configuration is tailored for Gmail.

**Prerequisite**:

1.  Configure IMAP using [isync/mbsync](https://wiki.archlinux.org/index.php/Isync), put your `.mbsyncrc` config file in `~/.emacs.d/mu4e/`. A [sample](https://gist.github.com/MatthewZMD/39cc00260486d17450f7228a4f36891f) is provided.
2.  Install [mu](https://www.djcbsoftware.nl/code/mu/).
3.  Execute the follwing commands

    ```bash
    mkdir -p ~/Maildir/gmail/
    mbsync -c ~/.emacs.d/mu4e/.mbsyncrc -Dmn gmail
    mbsync -c ~/.emacs.d/mu4e/.mbsyncrc -a
    mu init --maildir=~/Maildir/ --my-address=YOUR_EMAIL1 --my-address=YOUR_EMAIL2
    mu index
    ```

    -   If you are getting `Invalid Credentials` error and you are sure the password is correct, check [this](https://appuals.com/fix-your-imap-server-wants-to-alert-you-invalid-credentials/) link.
4.  (Optional) If you want to track meetings using `org-mode`, set `gnus-icalendar-org-capture-file` to the meeting's file.

```emacs-lisp
(use-package mu4e
  :ensure nil
  :commands (mu4e make-mu4e-context)
  :init
  (use-package mu4e-alert
    :defer t
    :config
    (when (executable-find "notify-send")
      (mu4e-alert-set-default-style 'libnotify))
    :hook
    ((after-init . mu4e-alert-enable-notifications)
     (after-init . mu4e-alert-enable-mode-line-display)))
  (use-package mu4e-overview :defer t)
  :bind
  (("M-z m" . mu4e)
   ("M-m m" . mu4e)
   (:map mu4e-view-mode-map
         ("e" . mu4e-view-save-attachment)))
  :custom
  (mu4e-maildir (expand-file-name "~/Maildir"))
  (mu4e-get-mail-command "mbsync -c ~/.emacs.d/mu4e/.mbsyncrc -a")
  (mu4e-view-prefer-html t)
  (mu4e-update-interval 180)
  (mu4e-headers-auto-update t)
  (mu4e-compose-format-flowed t)
  (mu4e-view-show-images t)
  (mu4e-change-filenames-when-moving t) ; work better for mbsync
  (mu4e-attachment-dir "~/Downloads")
  (message-kill-buffer-on-exit t)
  (mu4e-compose-dont-reply-to-self t)
  (mu4e-view-show-addresses t)
  (mu4e-confirm-quit nil)
  (mu4e-use-fancy-chars t)
  (mu4e-headers-results-limit 1000)
  (mu4e-view-use-gnus t)
  (gnus-icalendar-org-capture-file "~/org/agenda/meetings.org") ; Prerequisite: set it to meetings org fie
  (gnus-icalendar-org-capture-headline '("Meetings")) ; Make sure to create Calendar heading first
  :hook
  ((mu4e-view-mode . visual-line-mode)
   (mu4e-compose-mode . (lambda ()
                          (visual-line-mode)
                          (use-hard-newlines -1)
                          (flyspell-mode)))
   (mu4e-view-mode . (lambda() ;; try to emulate some of the eww key-bindings
                       (local-set-key (kbd "<tab>") 'shr-next-link)
                       (local-set-key (kbd "<backtab>") 'shr-previous-link)))
   (mu4e-headers-mode . (lambda ()
                          (interactive)
                          (setq mu4e-headers-fields
                                `((:human-date . 25) ;; alternatively, use :date
                                  (:flags . 6)
                                  (:from . 22)
                                  (:thread-subject . ,(- (window-body-width) 70)) ;; alternatively, use :subject
                                  (:size . 7))))))
  :init
  (use-package mu4e-thread-folding
    :load-path (lambda () (expand-file-name "site-elisp/mu4e-thread-folding" user-emacs-directory))
    :after mu4e
    :bind
    ((:map mu4e-headers-mode-map
           ("TAB" . mu4e-headers-toggle-at-point)
           ("C-<tab>" . mu4e-headers-toggle-fold-all))
     (:map mu4e-search-minor-mode-map
           ("S" . mu4e-kill-update-mail)))
    :custom
    (mu4e-thread-folding-default-view `folded)
    (mu4e-headers-fields '((:empty         .    2)
                           (:human-date    .   12)
                           (:flags         .    6)
                           (:mailing-list  .   10)
                           (:from          .   22)
                           (:subject       .   nil)))
    :config
    (add-to-list 'mu4e-header-info-custom
                 '(:empty . (:name "Empty"
                                   :shortname ""
                                   :function (lambda (msg) "  ")))))
  :config
  (require 'mu4e-icalendar)
  (setq mail-user-agent (mu4e-user-agent))
  (mu4e-icalendar-setup)
  (gnus-icalendar-org-setup)
  (defalias 'mu4e-add-attachment 'mail-add-attachment
    "I prefer the add-attachment function to begin wih mu4e so I can find it easily.")

  (add-to-list 'mu4e-view-actions
               '("ViewInBrowser" . mu4e-action-view-in-browser) t)
  (setq mu4e-contexts
        (list
         (make-mu4e-context
          :name "gmail"
          :enter-func (lambda () (mu4e-message "Entering context gmail"))
          :leave-func (lambda () (mu4e-message "Leaving context gmail"))
          :match-func
          (lambda (msg)
            (when msg
              (string-match "gmail" (mu4e-message-field msg :maildir))))
          :vars '((mu4e-sent-folder . "/gmail/Sent Mail")
                  (mu4e-drafts-folder . "/gmail/Drafts")
                  (mu4e-trash-folder . "/gmail/Trash")
                  (mu4e-sent-messages-behavior . sent)
                  (mu4e-compose-signature . user-full-name)
                  (user-mail-address . user-mail-address) ; Prerequisite: Set this to your email
                  (mu4e-compose-format-flowed . t)
                  (smtpmail-queue-dir . "~/Maildir/gmail/queue/cur")
                  (message-send-mail-function . smtpmail-send-it)
                  (smtpmail-smtp-user . "matthewzmd") ; Set to your username
                  (smtpmail-starttls-credentials . (("smtp.gmail.com" 587 nil nil)))
                  (smtpmail-auth-credentials . (expand-file-name "~/.authinfo.gpg"))
                  (smtpmail-default-smtp-server . "smtp.gmail.com")
                  (smtpmail-smtp-server . "smtp.gmail.com")
                  (smtpmail-smtp-service . 587)
                  (smtpmail-debug-info . t)
                  (smtpmail-debug-verbose . t)
                  (mu4e-maildir-shortcuts . ( ("/gmail/INBOX"            . ?i)
                                              ("/gmail/Sent Mail" . ?s)
                                              ("/gmail/Trash"       . ?t)
                                              ("/gmail/All Mail"  . ?a)
                                              ("/gmail/Starred"   . ?r)
                                              ("/gmail/Drafts"    . ?d))))))))
```


<a id="orgff0e9e8"></a>

## Tramp

[Tramp](https://www.emacswiki.org/emacs/TrampMode), short for Transparent Remote Access, Multiple Protocols is a package for editing remote files using a remote shell connection (rlogin, telnet, ssh).


### Google Cloud Platform

Connect to Google Cloud Platform using the following:

```text
/gssh:some-instance:/path/to/file
```

```emacs-lisp
(use-package tramp
  :ensure nil
  :defer 1
  :config
  (add-to-list 'tramp-remote-path 'tramp-own-remote-path)
  ;; TRAMP gcloud ssh
  (add-to-list 'tramp-methods
               '("gssh"
                 (tramp-login-program        "gcloud compute ssh")
                 (tramp-login-args           (("%h")))
                 (tramp-async-args           (("-q")))
                 (tramp-remote-shell         "/bin/bash")
                 (tramp-remote-shell-args    ("-c"))
                 (tramp-gw-args              (("-o" "GlobalKnownHostsFile=/dev/null")
                                              ("-o" "UserKnownHostsFile=/dev/null")
                                              ("-o" "StrictHostKeyChecking=no")))
                 (tramp-default-port         22))))
```


<a id="orgbbd118f"></a>

## LeetCode

[LeetCode](https://github.com/kaiwk/leetcode.el), an Emacs LeetCode client. Note that this package is dependant on [aio](https://github.com/skeeto/emacs-aio) and [GraphQL](https://github.com/davazp/graphql-mode).

```emacs-lisp
(use-package leetcode
  :load-path (lambda () (expand-file-name "site-elisp/leetcode.el" user-emacs-directory))
  :commands (leetcode)
  :init
  (use-package graphql :defer t)
  (use-package aio :defer t)
  :custom
  (url-debug t)
  (leetcode-prefer-language "python3"))
```


<a id="org5775fb7"></a>

## Debbugs

[Debbugs](https://elpa.gnu.org/packages/debbugs.html), a package lets you access the GNU Bug Tracker from within Emacs.

```emacs-lisp
(use-package debbugs
  :commands (debbugs-gnu))
```


<a id="org24ba65c"></a>

## Hacker News

A simple [Hacker News](https://github.com/clarete/hackernews.el) Emacs client.

```emacs-lisp
(use-package hackernews
  :commands (hackernews)
  :bind
  (("M-z h" . hackernews)
   ("M-m h" . hackernews)))
```


<a id="org3f2d4cd"></a>

## EWW

Emacs Web Wowser, the HTML-based Emacs Web Browser.

```emacs-lisp
(use-package eww
  :ensure nil
  :commands (eww)
  :hook (eww-mode . (lambda ()
                      "Rename EWW's buffer so sites open in new page."
                      (rename-buffer "eww" t)))
  :config
  ;; I am using EAF-Browser instead of EWW
  (unless eaf-env-p
    (setq browse-url-browser-function 'eww-browse-url))) ; Hit & to browse url with system browser
```


<a id="org1f94fb2"></a>

# Miscellaneous


<a id="org8a911ff"></a>

## Chinese

Packages and configurations suitable for Chinese users. Non-Chinese users feel free to add `:disabled` tags for them.


### Pyim

-   [Pyim](https://github.com/tumashu/pyim), an Emacs Chinese Pinyin Input. It uses [posframe](https://github.com/tumashu/posframe) package to display candidates.
-   [Pyim BaseDict](https://github.com/tumashu/pyim-basedict), the default Chinese-Pyim dictionary.

我已经停止使用作者推荐的无痛中英切换，它对需要同时打英文和中文的情况不是很友好。如需切换输入法，请善用 `C-\` 。

```emacs-lisp
(use-package pyim
  :init
  (use-package posframe :defer t)
  :custom
  (default-input-method "pyim")
  (pyim-default-scheme 'quanpin)
  (pyim-page-tooltip 'posframe)
  (pyim-page-length 9)
  :config
  (use-package pyim-basedict
    :after pyim
    :config (pyim-basedict-enable))
  (pyim-isearch-mode 1)
  (diminish pyim-isearch-mode "")
  (setq-default pyim-english-input-switch-functions
                '(pyim-probe-isearch-mode
                  pyim-probe-org-structure-template))
  (setq-default pyim-punctuation-half-width-functions
                '(pyim-probe-punctuation-line-beginning
                  pyim-probe-punctuation-after-punctuation))
  :bind
  ("M-j" . pyim-convert-string-at-point)) ; M-j 强制将光标前的拼音字符串转换为中文。
```


### Youdao

[Youdao](https://github.com/xuchunyang/youdao-dictionary.el) interface for Emacs.

```emacs-lisp
(use-package youdao-dictionary
  :commands (youdao-dictionary-search
             youdao-dictionary-search-at-point
             youdao-dictionary-search-at-point-posframe)
  :bind ("C-M-y" . youdao-dictionary-search-at-point-posframe))
```


<a id="org766c45b"></a>

## Tetris

Although [Tetris](https://www.emacswiki.org/emacs/TetrisMode) is part of Emacs, but there still could be some configurations.

```emacs-lisp
(use-package tetris
  :ensure nil
  :commands (tetris)
  :bind
  (:map tetris-mode-map
        ("C-p" . tetris-rotate-prev)
        ("C-n" . tetris-rotate-down)
        ("C-b" . tetris-move-left)
        ("C-f" . tetris-move-right)
        ("C-SPC" . tetris-move-bottom))
  :config
  (defadvice tetris-end-game (around zap-scores activate)
    (save-window-excursion ad-do-it)))
```


<a id="org9a4e85e"></a>

## Speed Type

[Speed type](https://github.com/hagleitn/speed-type), a game to practice touch/speed typing in Emacs.

```emacs-lisp
(use-package speed-type
  :commands (speed-type-text))
```


<a id="org2818cea"></a>

## 2048 Game

[2048 Game](https://bitbucket.org/zck/2048.el), an implementation of 2048 in Emacs.

```emacs-lisp
(use-package 2048-game
  :commands (2048-game))
```


<a id="orgb619100"></a>

## Snow

Let it [snow](https://github.com/alphapapa/snow.el) in Emacs!

```emacs-lisp
(use-package snow
  :load-path (lambda () (expand-file-name "site-elisp/snow.el" user-emacs-directory))
  :commands (snow))
```


<a id="orge6e0ba9"></a>

## EPaint

[EPaint](https://github.com/chuntaro/epaint), a simple paint tool for emacs.

```emacs-lisp
(use-package epaint
  :if (display-graphic-p)
  :load-path (lambda () (expand-file-name "site-elisp/epaint" user-emacs-directory))
  :commands (epaint)
  :init
  (with-eval-after-load (quote epaint-context)
    (unless (boundp (quote cl-struct-epaint-drawable))
      (defvar cl-struct-epaint-drawable (quote epaint-drawable)))
    (unless (boundp (quote cl-struct-epaint-gc))
      (defvar cl-struct-epaint-gc (quote epaint-gc)))))
```


<a id="orgd62e69b"></a>

## Zone

[Zone](https://www.emacswiki.org/emacs/ZoneMode), a minor-mode 'zones' Emacs out, choosing one of its random modes to obfuscate the current buffer.

```emacs-lisp
(use-package zone
  :ensure nil
  :defer 5
  :config
  ;; (zone-when-idle 600) ; in seconds
  (defun zone-choose (pgm)
    "Choose a PGM to run for `zone'."
    (interactive
     (list
      (completing-read
       "Program: "
       (mapcar 'symbol-name zone-programs))))
    (let ((zone-programs (list (intern pgm))))
      (zone))))
```
