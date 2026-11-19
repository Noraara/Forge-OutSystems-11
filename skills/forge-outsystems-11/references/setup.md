# Setup and tool selection

Use [OutSystems’ Service Studio MCP instructions](https://success.outsystems.com/documentation/11/outsystems_mcp/) to enable the local server and register it with the chosen agent. Follow the host-specific configuration and current connection address shown by Service Studio. Install the separate [official `servicestudio-mcp-oml` skill](https://github.com/OutSystems/outsystems11-mcp) when using the Model API. The endpoint, function arguments, user permissions, and available tools come from the live host.

1. Open the intended application and module in the authorized environment. Confirm the app style, environment, module name, and parent application before acting.
2. Follow the official skill for session authorization before using protected Service Studio tools. The user reviews permission prompts in Service Studio. Inspect the available read tools and current module before opening an edit session.
3. Check supported write, merge, reference-refresh, and publish capabilities against the host and current permissions. Follow any applicable [OutSystems beta terms](https://www.outsystems.com/legal/beta-features-agreement) and the official skill’s first-use instructions when using beta write features. Use the authorized manual path or report the blocker if automation is unavailable.
4. For runtime checks, open the served application in the available browser. Use [Playwright CLI](https://github.com/microsoft/playwright-cli) where useful, and use separate browser profiles or contexts for different synthetic users. Keep credentials and saved sessions out of deliverables.

Design tools are optional. Read [design routing](design.md) for choosing them. A missing design tool should only affect the stages that need it. The user’s existing product and interface conventions still guide the work.
