## Awesome Terminal Multiplexers

This list provides a curated selection of terminal multiplexers. Please contribute if you can.

### How this list is organized

For this list, a **terminal multiplexer** multiplexes terminal interfaces, not merely processes or windows. Entries in the main terminal-multiplexer category must satisfy all of these requirements:

* **Terminal-native interface:** the multiplexer itself runs inside a terminal and presents its multiplexed terminal sessions through that terminal interface.
* **PTY-backed terminal instances:** it directly manages multiple PTY-backed terminal sessions, or equivalent terminal endpoints. For a remote session, ownership of the remote process and PTY may be delegated to SSH or a comparable transport; merely owning or supervising ordinary subprocesses is not sufficient.
* **Direct terminal emulation:** it directly interprets each terminal stream and independently maintains the terminal state for each multiplexed instance, including at minimum its normal screen, alternate-screen state, and scrollback/history. An embedded terminal-emulation library counts as part of the implementation; delegating this state to another terminal emulator or an existing multiplexer does not.
* **Switching continuity:** the user can select or switch between multiple independently maintained terminal instances without recreating them. Switching away and back must return to the same managed terminal instance and its continuing terminal state. Split panes and other layouts may supplement this, but layout alone is not a substitute for switching between multiplexed terminals.

Detach/reattach, persistence after the multiplexer exits, daemon or client/server architecture, remote access, and simultaneous pane layouts are useful features but are **not requirements** for terminal multiplexing.

Software that uses, configures, or manages an existing multiplexer rather than implementing the multiplexing itself is listed separately under **Multiplexer clients, configuration and management tools**. Software that performs related multiplexing but does not satisfy the terminal-native requirement may be listed separately when useful.

### Terminal multiplexers

* **3mux** (Go - 2018) (https://github.com/aaronjanse/3mux): Terminal multiplexer inspired by i3.
* **Boo** (Zig - 2024) (https://github.com/coder/boo): A GNU screen style terminal multiplexer built on libghostty.
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

### Detachable terminal session managers

These tools directly own or supervise PTY-backed sessions and support detaching and later reattaching, but do not necessarily implement multiple independently emulated terminals with switching between them. Detach/reattach is treated here as a useful session-management feature, not as a defining requirement of terminal multiplexing.

* **abduco** (C - 2014) (https://github.com/martanne/abduco): PTY-backed session manager supporting persistent sessions and detach/reattach; commonly paired with dvtm for pane/window management.
* **dtach** (C - 2004) (https://github.com/crigler/dtach): A simple program that emulates the detach feature of screen.

### Related graphical terminal multiplexing

These applications implement substantial terminal multiplexing or multiplexer-style session management but present it through a graphical frontend rather than running the multiplexing interface inside a terminal. They are kept separate from the terminal-native definition above. Detach/reconnect behavior may be noted as a feature, but is not what determines this classification.

* **Rune** (Go - 2026) (https://github.com/unstablebuild/rune): A GPU-accelerated graphical IDE that directly manages multiple PTY-backed terminal sessions with its own terminal emulation and terminal tabs/windows.
* **WezTerm** (Rust - 2017) (https://github.com/wez/wezterm): Terminal emulator with a separate multiplexer/server architecture supporting reconnectable multiplexing domains.

### Terminal multiplexing as a secondary purpose

Applications in this section are expected to satisfy the same core terminal-multiplexer requirements above — terminal-native presentation, multiple PTY-backed terminal instances, direct per-instance terminal emulation, and switching continuity — even though terminal multiplexing is not their primary purpose. Merely embedding terminal processes, terminal widgets, or a generic split/tab interface is not enough.

* **dekit (formerly mprocs)** (Rust - 2021) (https://github.com/pvolok/dekit): A PTY-backed TUI process manager for running and interacting with multiple commands in parallel.
* **GNU Emacs** (C/Emacs Lisp - 1985) (https://www.gnu.org/software/emacs/): Can dynamically create PTY-backed terminal subprocesses/buffers and expose multiple terminal sessions, though its primary purpose is the Emacs editor/environment.
* **Neovim** (C/Lua - 2014) (https://neovim.io/): Terminal buffers use its PTY/job infrastructure and can be created dynamically, but its primary purpose is text editing.
* **Vim** (C - 1991) (https://www.vim.org/): When built with terminal support it can dynamically create and manage terminal jobs backed by PTYs, exposing multiple terminal sessions, though its primary purpose is text editing.

### Historical / proprietary

* **TD/SMP** (Proprietary - DEC VT330/340): Introduced by DEC on their VT330/340 terminals, TD/SMP was proprietary and only widely supported by their own terminal servers.

### Multiplexer clients, configuration and management tools

These tools use, configure, or manage an existing terminal multiplexer rather than implementing the multiplexing themselves. Clients and frontends here expose the multiplexer itself as a first-class interface — for example, its sessions, windows/tabs, and panes — and let users navigate or manage that state directly. Configuration, session-management, and automation tools provide similarly substantial multiplexer-specific functionality. Generic terminal or remote-access applications with only launch or attach shortcuts are not included here.

* **tmuxinator** (Ruby - 2010) (https://github.com/tmuxinator/tmuxinator): A tool to automate the creation of sessions with tmux.
* **tmuxp** (Python - 2013) (https://github.com/tmux-python/tmuxp): A configuration and session manager for tmux, built on libtmux.

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related or neighboring rights to this work.
