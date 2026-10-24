# simplero. CLI

*make it simpler*

`simplero` is the command line for [Simplero](https://simplero.com). Sign in
once with your browser. Then use your Simplero account from your terminal,
your scripts, or an AI coding agent like Claude Code or Codex.

This repo holds the Homebrew tap and the release downloads.

## Install

**macOS and Linux**

```sh
# Homebrew
brew install simplero/tap/simplero

# Or the install script. It downloads the latest release and checks its SHA-256.
curl -fsSL https://simplero.com/cli/install | sh
```

**Windows** (PowerShell)

```powershell
# The install script. It downloads the latest release, checks its SHA-256,
# and adds simplero to your PATH.
irm https://simplero.com/cli/install.ps1 | iex

# Or Scoop
scoop bucket add simplero https://github.com/Simplero/homebrew-tap
scoop install simplero
```

Open a new terminal after installing, so it picks up the new PATH.

## Get started

```sh
simplero
```

The first run opens your browser to sign in. Pick an account. The CLI creates
an API key for that account and saves it in your system keychain. You can see
the key in Simplero under **Settings > Integrations > API Keys**.

API access must be included in your plan. If it isn't, the CLI tells you and
shows the link to upgrade.

```sh
simplero products list
simplero contacts list --per-page 10
simplero product show 123
simplero --help
```

Commands come from the live Simplero API, so new API features show up in the
CLI without an update.

## Use it with an AI agent

Tell your agent to run `simplero skill`. That prints a guide for AI agents
that shows how to use the CLI.

## Update

```sh
brew upgrade simplero      # Homebrew
scoop update simplero      # Scoop
# or run the install script again
```

## Help

- Simplero: https://simplero.com
- API reference: https://simplero.com/api/v2/reference
