---
name: forge-outsystems-11
description: Design, build, troubleshoot, and verify OutSystems 11 Reactive Web or Mobile features in Service Studio. Use for native UI changes, model edits, permissions, data workflows, publishing, and browser or device verification.
license: MIT
---

# Forge OutSystems 11

Turn an OutSystems 11 request into verified behavior. Scope the work to the authorized application, module, environment, and user outcomes. Use prior project context when relevant. Standalone work needs no vault.

1. Read [discovery](references/discovery.md) to confirm the real target, ownership, app style, and current behavior. Use [setup](references/setup.md) if tool access needs checking. Treat read-only requests as inspection.
2. Match the plan to the change. For UI work, use [design](references/design.md). For new behavior, identify the actor, data ownership, server permissions, state changes, and acceptance checks. Prefer the existing product and design specifications.
3. For model changes, read [implementation](references/implementation.md) and the complete installed official `servicestudio-mcp-oml` skill before calling its tools. Use live schemas and supported OutSystems patterns. Preserve unrelated module and user changes.
4. Use [verification](references/verification.md) to check the affected model and served result. Publish to the authorized environment only. Record model validation, merge, deployment, runtime, visual review, and mobile checks as distinct evidence.
5. Return the [delivery record](assets/delivery.md), or hand scoped results back to a requesting workflow through the [`atlas-workflow/v1` packet](assets/packet.md).

A visual prototype can guide an implementation. Service Studio owns OutSystems application changes. Traditional Web work needs the matching platform lifecycle and tool guidance.
