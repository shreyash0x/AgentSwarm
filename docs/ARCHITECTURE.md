# Initial architecture

The planned implementation is modular so provider-specific behavior remains separate from orchestration and the terminal interface.

- `cli` owns command parsing and process lifecycle.
- `config` validates global and project settings.
- `providers` contains supported Antigravity adapters.
- `agents` manages roles, sessions, permissions, and lifecycle state.
- `orchestration` schedules dependency-aware work with bounded concurrency.
- `workspace` manages Git branches and worktrees.
- `github` enforces milestone-controlled remote operations.
- `persistence` stores sessions, messages, checkpoints, and project knowledge.
- `tui` renders the interactive terminal experience.
- `integrations/rea` exposes optional authorized analysis capabilities.

The first implementation decision will be made after validating the currently supported provider interfaces and REA setup documentation.
