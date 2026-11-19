# Forge OutSystems 11 Skill

**Build OutSystems 11 features you can verify in Service Studio and in the browser.** Forge helps Codex and Claude Code turn a brief into a scoped Reactive Web or Mobile change, from the first model inspection through delivery. It connects design decisions, server-side rules, and rendered checks in one workflow.

Use it to adjust an existing screen, build a form that saves and reloads data, or diagnose a feature that passes model validation but fails after publishing.

## Quick start

### Connect Service Studio

Use OutSystems 11 Service Studio with a development module open. Enable the Service Studio MCP server and connect your host using the [official setup for Codex or Claude Code](https://success.outsystems.com/documentation/11/outsystems_mcp/#supported-mcp-hosts). Install the separate [official Service Studio model skill](https://github.com/OutSystems/outsystems11-mcp) for Model API edits. Forge coordinates the workflow. The official skill and live tool schemas supply the model API contract.

### Install Forge

Use [GitHub CLI](https://cli.github.com/) with support for [`gh skill install`](https://cli.github.com/manual/gh_skill_install).

```sh
# Codex
gh skill install Noraara/Forge-OutSystems-11 forge-outsystems-11 --agent codex --scope user

# Claude Code
gh skill install Noraara/Forge-OutSystems-11 forge-outsystems-11 --agent claude-code --scope user
```

Run the command from your project’s Git checkout with `--scope project` to install in one project. For a local checkout, use its path in place of `Noraara/Forge-OutSystems-11` and add `--from-local`.

For manual setup, copy the entire [`skills/forge-outsystems-11`](skills/forge-outsystems-11) folder into your agent’s skill directory.

| Agent | One project | All projects |
| --- | --- | --- |
| Codex | `.agents/skills/` | `~/.agents/skills/` |
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |

### Try it

Open a fresh session with your development module connected. Try this in Codex.

> Use $forge-outsystems-11 to inspect the open module. Tell me where the Equipment Notes example would fit and which dependencies or existing edits matter. Keep this read-only.

In Claude Code, start with `/forge-outsystems-11`. Expect a target and scope summary based on the open module. For the full example, follow the [Equipment Notes walkthrough](examples/equipment-notes/README.md) and its [browser verification checklist](examples/equipment-notes/verification.md).

## How it works

| Stage | What Forge checks |
| --- | --- |
| Inspect | Identify the application, open module, app style, roles, dependencies, and existing changes. |
| Plan and design | Define the user action, allowed data, expected states, and the smallest implementation scope. |
| Implement | Use native OutSystems widgets, blocks, themes, and actions. Enforce data rules and authorization on the server. |
| Verify | Record model validation, publication, browser behavior, accessibility, and device checks as applicable. |

For a visual feature, Forge can use existing design tools and browser testing. [Impeccable](https://github.com/pbakaus/impeccable), [Figma](https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Figma-MCP-server), and [Playwright CLI](https://github.com/microsoft/playwright-cli) are optional. Use a browser against the served web application to verify the actual result. A native or offline mobile requirement needs the appropriate device and sync tests. See [tool setup](skills/forge-outsystems-11/references/setup.md) and [verification guidance](skills/forge-outsystems-11/references/verification.md).

Forge can use source-backed context from [Atlas’ Notes](https://github.com/Noraara/Atlas-Notes) through the [`atlas-workflow/v1` handoff](skills/forge-outsystems-11/assets/packet.md). A vault is optional.

## Help and contributing

For a bug report, include the Service Studio and agent versions, module style, workflow stage, expected result, and a small redacted example. For a change to the skill, describe the behavior and which checks ran. Use synthetic data and keep credentials, private URLs, and session state out of shared evidence.

See the [sample delivery record](examples/equipment-notes/sample-delivery.md) for how to report model validation while merge, deployment, and runtime checks are still pending.

## License

Released under the [MIT license](LICENSE).

## Credit

Made by [Noraara](https://github.com/Noraara).
