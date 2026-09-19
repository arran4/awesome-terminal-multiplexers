## Proposed entry

- Project:
- Proposed section:
- Project/source URL:

## Why it fits

Briefly describe the functionality that makes the project relevant to the proposed section.

For **terminal multiplexer** submissions, address each core requirement:

- **Terminal-native interface:** show that the multiplexer itself runs inside a terminal and presents the multiplexed sessions through that terminal interface.
- **PTY-backed terminal instances:** show that it manages multiple PTY-backed terminal sessions or equivalent terminal endpoints. For remote sessions, the remote process/PTY may be delegated to SSH or a comparable transport; ordinary subprocess ownership alone is not enough.
- **Direct terminal emulation:** show that each multiplexed terminal has independently maintained terminal state, including its normal screen, alternate-screen state, and scrollback/history. Embedded terminal-emulation libraries are fine; delegating the terminal state to another terminal emulator or multiplexer is not.
- **Switching continuity:** show that the user can select or switch between multiple independently maintained terminal instances without recreating them, and can switch back to the same continuing terminal state. A fixed split/pane layout alone is not sufficient.

Detach/reattach, persistence after exit, daemon/client-server architecture, remote access, and simultaneous pane layouts are useful features but are not required.

For **terminal multiplexing as a secondary purpose**, the same four core requirements apply; explain the application's broader primary purpose as well.

For **related graphical terminal multiplexing**, explain which multiplexing behavior is implemented and make clear that the presentation is graphical rather than terminal-native.

For **detachable terminal session managers**, describe the PTY-backed session ownership/supervision and detach/reattach behavior. These tools do not need to satisfy the full terminal-multiplexer test above.

For **multiplexer clients, configuration and management tools**:
- client/front-end submissions should expose the multiplexer itself as a first-class interface, including its own session/window-or-tab/pane structure where the multiplexer provides those concepts;
- describe multiple meaningful operations the client can perform beyond simply launching or attaching (for example: browsing, switching, creating, renaming, splitting, zooming, killing, restoring, or otherwise controlling multiplexer state);
- configuration/session-management/automation tools should likewise provide substantial multiplexer-specific behavior rather than a generic terminal or remote-access feature.

## Evidence

Link to evidence that a reviewer can reasonably verify, such as source code, public documentation, screenshots/video, release notes, or reproducible steps.

For a terminal-multiplexer submission, provide evidence for all four core requirements above. In particular, evidence should distinguish actual per-session terminal emulation and switching continuity from generic process management, terminal widgets, or layout features.

For a client/front-end submission, the evidence should demonstrate the multiplexer-specific interface and representative management operations, not just state that the integration exists.

Closed-source projects are welcome when the relevant behavior can still be verified from public material or a publicly accessible build. Generated explanations or repeated eligibility arguments are not a substitute for evidence; if eligibility is questioned, please provide materially new evidence or clarification.

## Disclosure

If you are the author, maintainer, employee, or otherwise affiliated with the project, please say so here.
