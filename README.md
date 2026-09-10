# homebrew-tap

Homebrew tap for [TerraTidy](https://github.com/santosr2/TerraTidy), a single-binary
Terraform/Terragrunt quality platform.

## Install

```sh
brew install santosr2/tap/terratidy
```

Or add the tap first, then install:

```sh
brew tap santosr2/tap
brew install terratidy
```

## Upgrade

```sh
brew update && brew upgrade terratidy
```

## Uninstall

```sh
brew uninstall terratidy
brew untap santosr2/tap
```

## What lives here

`Casks/` holds the cask definitions, which install the pre-built binaries published
with each TerraTidy release. Homebrew on Linux is supported alongside macOS.

**These files are generated.** Every release, GoReleaser writes the cask from the
TerraTidy repository as part of publishing. Editing them here by hand will be
overwritten by the next release. Fixes belong in `.goreleaser.yml` upstream.

Only stable releases are published here; pre-releases (`-alpha`, `-beta`, `-rc`) are
available from the [GitHub releases page](https://github.com/santosr2/TerraTidy/releases)
instead.

## Issues

Report problems against the main repository:
[santosr2/TerraTidy/issues](https://github.com/santosr2/TerraTidy/issues).

## License

MIT, matching TerraTidy itself. See [LICENSE](LICENSE).
