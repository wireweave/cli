Beta — Wireweave v2.0 베타 단계

# @wireweave/cli

Command-line companion for the Wireweave wireframe DSL. Authenticate, render `.wf`
files, and talk to the Wireweave AI agent from your terminal.

> Status: **beta**. Published under the `beta` dist-tag on npm. APIs and command
> shape may still change before `1.0.0`.

## Install

```bash
npm install -g @wireweave/cli@beta
```

Requires Node.js 18+.

## Usage

```bash
# Sign in (paste an API key from https://dashboard.wireweave.org/dashboard/keys)
wireweave login

# Confirm you are signed in
wireweave whoami

# Render a wireframe file to HTML
wireweave render design.wf

# Ask the Wireweave agent for help
wireweave agent "make the hero section more compact"
```

## Environment

| Variable            | Default                     | Purpose                                |
| ------------------- | --------------------------- | -------------------------------------- |
| `WIREWEAVE_API_URL` | `https://api.wireweave.org` | Override the API base (self-hosted).   |
| `WIREWEAVE_API_KEY` | —                           | Per-shell override of the saved token. |

The persistent token lives at `~/.wireweave/config.json` with shape
`{ "token": string, "apiUrl"?: string }` and is shared with
`@wireweave/skill-cursor`.

## Beta scope

The first public beta ships these subcommands as functional stubs that resolve
exit code 0 and print a friendly "coming soon" message where the network call
is not yet wired:

- `login` — prints the dashboard URL and the config file location
- `whoami` — reads the local token and reports the trailing 4 chars
- `render` — reserved for the local HTML renderer
- `agent` — reserved for the v2.0 agent stream

Each release on the `beta` tag will fill in one of these calls end-to-end.

## License

MIT
