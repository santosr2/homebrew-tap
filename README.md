# homebrew-tap

Homebrew tap for [santosr2](https://github.com/santosr2)'s projects. One tap,
however many projects end up needing one.

## Install

```sh
brew tap santosr2/tap
```

Then install anything in it. You can also skip the tap step and use the fully
qualified name directly.

## Available

Nothing here is installable yet. Casks are written by each project's release
pipeline, so a project appears in this tap only once it has cut a release since
being wired up.

| Project | Install | Status |
| --- | --- | --- |
| [TerraTidy](https://github.com/santosr2/TerraTidy) — Terraform/Terragrunt quality platform | `brew install --cask santosr2/tap/terratidy` | Lands with its next release |

Until then, install TerraTidy from its
[releases page](https://github.com/santosr2/TerraTidy/releases) or by any of the
other methods in its [README](https://github.com/santosr2/TerraTidy#installation).

## Upgrading and removing

```sh
brew update && brew upgrade <name>
brew uninstall <name>
brew untap santosr2/tap      # removes the tap itself
```

## How this repository is maintained

**Almost everything under `Casks/` and `Formula/` is generated.** Each project's
own release pipeline writes its file here when it publishes a release, so edits
made directly in this repository are overwritten by the next release of that
project.

The one exception is `Formula/terratidy.rb`, which is hand-written and disabled.
TerraTidy moved from a formula to a cask, and that file exists only so the old
`brew install santosr2/tap/terratidy` reports the move instead of failing with
"no available formula". It cannot be installed and is never regenerated.

If something is wrong with a cask or formula, fix it in the project that
generates it — for TerraTidy that is `.goreleaser.yml` — not here.

Casks are preferred over formulae: they install pre-built release binaries and
work on both macOS and Linux, so there is no need to compile from source.

Only stable releases are published. Pre-releases (`-alpha`, `-beta`, `-rc`) are
available from each project's GitHub releases page instead.

## Issues

Report problems against the project the cask belongs to, not against this
repository. Its contents are generated, so a bug here is almost always a bug
there.

## License

MIT. See [LICENSE](LICENSE).
