## 04.01.26 - Status command + CLI writing

- Implemented `status` command to show disk usage using `df`.
- Chose to filter by filesystem **type**.
- Used a bash array + loop to build exclusion flags cleanly and run `df` once.

- Created `bin/lcc` as the CLI entrypoint
    - Acts as a dispatcher
    - `lcc status` executes `lib/status`

- Learned somewhat how command execution works on Linux
    - Shell (`zsh`) finds the command via `$PATH`
    - Kernel reads the shebang to choose the interpreter (`bash`)
    - Login shell and script interpreter are independent

- Added project `bin/` directory to `$PATH` via `~/.zshrc` for development so `lcc status` can be run from anywhere.
    - Temporary

