# scoop-github-agent-cli

Scoop bucket for [github-agent-cli](https://pypi.org/project/github-agent-cli/) — a repository and
wiki steward for GitHub: one command per documentation job, no runtime dependencies.

## Install

```powershell
scoop bucket add github-agent-cli https://github.com/paulmann/scoop-github-agent-cli
scoop install github-agent-cli
ghagent --version        # github-agent 1.2.2
```

The manifest installs the Windows bundle from the GitHub release: `ghagent.cmd` plus the wheel
contents under `lib/`. Python 3.11+ is declared as a dependency (`depends: python`), so Scoop
installs the interpreter if it is missing.

## Update

```powershell
scoop update; scoop update github-agent-cli
```

`checkver` reads the PyPI JSON API; `autoupdate` takes the bundle URL from the release and its
hash from the release `SHA256SUMS.txt`.

## Other install paths

`uv tool install github-agent-cli`, `pipx`, `pip`, Homebrew
(`brew install paulmann/homebrew-github-agent-cli/github-agent-cli`) and the reusable GitHub Action
are documented in the [main repository](https://github.com/paulmann/github-agent).

## License

MIT