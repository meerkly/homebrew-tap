# meerkly Homebrew tap

Formulae for [meerkly](https://meerkly.com) — share your machine's connection as a proxy exit
node and earn per GB shared.

## Install

```bash
brew install meerkly/tap/meerkly
```

Then set it up. One command, which asks for your publisher id and starts the background service
at login:

```bash
meerkly init
```

Get a publisher id at [dashboard.meerkly.com](https://dashboard.meerkly.com).

## Running it

```bash
brew services start meerkly     # start at login
brew services stop meerkly
meerkly status                  # is it connected?
```

`brew services` installs a **LaunchAgent**, which runs as you and starts at login. Do not use
`sudo brew services` — that would run the agent as root and put its configuration somewhere
neither you nor the desktop app can edit.

## Upgrading

```bash
brew update && brew upgrade meerkly
```

## What's here

| Formula | Source |
|---|---|
| `meerkly` | [meerkly/meerkly-agent](https://github.com/meerkly/meerkly-agent) |

**`Formula/meerkly.rb` is generated — do not edit it here.** It is rendered from
[`packaging/homebrew/meerkly.rb.tmpl`](https://github.com/meerkly/meerkly-agent/blob/main/packaging/homebrew/meerkly.rb.tmpl)
and pushed by that repository's release workflow on every `v*` tag, so a hand edit is silently
overwritten by the next release. Change the template instead.
