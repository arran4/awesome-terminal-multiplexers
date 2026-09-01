## Awesome Terminal Multiplexers

This list provides a curated selection of terminal multiplexers. Please contribute if you can.

### Scope / inclusion criteria

To qualify as a terminal multiplexer, terminal-based software must directly and dynamically manage PTYs or equivalent terminal sessions. Graphical software must additionally support terminal sessions that can remain alive independently of the graphical frontend and later be reattached. Merely providing terminal tabs/panes or delegating the actual multiplexing to another program is insufficient for classification as a terminal multiplexer; related tools are listed separately below.

### Terminal-based multiplexers

* **3mux** (Go - 2018) (https://github.com/aaronjanse/3mux): Terminal multiplexer inspired by i3.
* **abduco** (C - 2014) (https://github.com/martanne/abduco): PTY-backed session manager supporting persistent sessions and detach/reattach; commonly paired with dvtm for pane/window management.
* **Boo** (Zig - 2024) (https://github.com/coder/boo): A GNU screen style terminal multiplexer built on libghostty.
* **dtach** (C - 2004) (https://github.com/crigler/dtach): A simple program that emulates the detach feature of screen.
* **dvtm** (C - 2007) (https://github.com/martanne/dvtm): Tiling window management for the console.
* **FbTerm** (C++ - 2008) (https://code.google.com/archive/p/fbterm/): A fast framebuffer based terminal emulator for Linux with multiplexing capabilities.
* **GNU Screen** (C - 1987) (https://opensource.com/article/17/3/introduction-gnu-screen): The prototypical terminal multiplexer.
* **mtm** (C - 2014) (https://github.com/deadpixi/mtm): Billed as "perhaps the smallest useful terminal multiplexer in the world".
* **neercs** (C - 2007) (https://sourceforge.net/projects/neercs/): A GNU Screen workalike with window thumbnailing and graphical animated screensavers, supports 3D console switching.
* **pymux** (Python - 2014) (https://github.com/prompt-toolkit/pymux): A terminal multiplexer (like tmux) in Python.
* **splitvt** (C - 1990s) (https://manpages.debian.org/stretch/splitvt/splitvt.1.en.html): A split terminal utility.
* **tab** (Rust - 2018) (https://github.com/austinjones/tab-rs): A terminal multiplexer.
* **term39** (Rust - 2025) (https://github.com/alejandroqh/term39): A modern, retro-styled terminal multiplexer inspired by Norton Disk Doctor (MS-DOS)
* **tmate** (C - 2013) (https://github.com/tmate-io/tmate): Instant Terminal Sharing.
* **tmux** (C - 2009) (https://github.com/tmux/tmux/wiki): A modern GNU Screen workalike, released in 2007; it is BSD-licensed, allows multiple panes (with optional Xterm mouse support), and has a scriptable command interface.
* **TUIOS** (Go - 2025) (https://github.com/Gaurav-Gosain/tuios): Terminal UI OS (Terminal Multiplexer).
* **Twin ("Text mode WINdow environment")** (C - 1999) (https://github.com/cosmos72/twin): A full-fledged window manager for text windows, initially started as an MS-DOS project and later ported to Linux.
* **vtm** (C++ - 2019) (https://github.com/directvt/vtm): A virtual terminal multiplexer and text-based desktop environment.
* **VWM** (C - 2007) (https://sourceforge.net/projects/vwm/): A window manager and user-interface for the console. Its extensible design allows for easy development of native applications as shared-library plugins.
* **vwm** (C - 2015) (https://github.com/TragicWarrior/vwm): Virtual window manager for the terminal.
* **Zellij** (Rust - 2019) (https://github.com/zellij-org/zellij): A modern terminal workspace with batteries included.

### Graphical / detachable multiplexers

* **WezTerm** (Rust - 2017) (https://github.com/wez/wezterm): Terminal emulator with a separate multiplexer/server architecture supporting reconnectable multiplexing domains.

### Technically valid, but not primary purpose

Some applications satisfy the technical definition of terminal multiplexing even though multiplexing is not their primary purpose. These are listed separately to keep the main sections focused without arbitrarily excluding technically valid implementations.

* **dekit (formerly mprocs)** (Rust - 2021) (https://github.com/pvolok/dekit): A PTY-backed TUI process manager for running and interacting with multiple commands in parallel.
* **GNU Emacs** (C/Emacs Lisp - 1985) (https://www.gnu.org/software/emacs/): Can dynamically create PTY-backed terminal subprocesses/buffers and expose multiple terminal sessions, though its primary purpose is the Emacs editor/environment.
* **Neovim** (C/Lua - 2014) (https://neovim.io/): Terminal buffers use its PTY/job infrastructure and can be created dynamically, but its primary purpose is text editing.
* **Vim** (C - 1991) (https://www.vim.org/): When built with terminal support it can dynamically create and manage terminal jobs backed by PTYs, exposing multiple terminal sessions, though its primary purpose is text editing.

### Historical / proprietary

* **TD/SMP** (Proprietary - DEC VT330/340): Introduced by DEC on their VT330/340 terminals, TD/SMP was proprietary and only widely supported by their own terminal servers.

### Multiplexer clients, frontends, configuration and session-management tools

These tools do not need to qualify as terminal multiplexers themselves. They must provide substantial, purpose-built functionality for directly using, controlling, configuring, restoring, or automating one or more qualifying multiplexers. This includes dedicated clients and frontends as well as configuration and session managers. Merely being a terminal, SSH, remote-access, tab/pane, or workspace application is not enough; incidental support such as only launching or attaching to a multiplexer is insufficient.

* **tmuxinator** (Ruby - 2010) (https://github.com/tmuxinator/tmuxinator): A tool to automate the creation of sessions with tmux.
* **tmuxp** (Python - 2013) (https://github.com/tmux-python/tmuxp): A configuration and session manager for tmux, built on libtmux.

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related or neighboring rights to this work.
