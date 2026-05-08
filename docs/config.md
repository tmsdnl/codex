# Configuration

For basic configuration instructions, see [this documentation](https://developers.openai.com/codex/config-basic).

For advanced configuration instructions, see [this documentation](https://developers.openai.com/codex/config-advanced).

For a full configuration reference, see [this documentation](https://developers.openai.com/codex/config-reference).

## Shell selection

Codex normally detects the user's default shell and falls back to a supported
platform shell when needed. To override the shell used by shell-based tools, set
`shell_path` in `config.toml`:

```toml
shell_path = "/bin/bash"
```

Profiles can override the top-level value:

```toml
[profiles.work]
shell_path = "bash"
```

The `CODEX_SHELL` environment variable has the highest precedence over
`shell_path`. Values must be either a supported bare shell name or an absolute
path to a supported shell executable. Codex currently supports `zsh`, `bash`,
`sh`, `pwsh`/`powershell`, and `cmd`.
