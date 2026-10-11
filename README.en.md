# open-design-assistant

[中文](README.md) | [English](README.en.md)

A design skill focused exclusively on workflow orchestration. Open Design handles requirements interpretation, design decisions, and all intermediate and final artifacts. This skill manages stage transitions, presents results, and relays user feedback.

## Workflow

Requirements discovery and research → Three design directions → User selection → Early alignment → Development and iteration → Review and verification → Export and delivery.

By default, three actual visual drafts are presented before the user selects a direction for further development. Explicit requests to skip exploration, iterations on an approved direction, and mechanical operations proceed through the applicable stages.

## Installation and usage

Place this repository in a skills directory recognized by your runtime, keeping the directory name as `open-design-assistant`, for example `~/.agents/skills/open-design-assistant/`. Reload the skill, then invoke it:

```text
$open-design-assistant Create a product launch presentation using the connected Open Design integration.
```

## Prerequisites and boundaries

A connected Open Design MCP integration with execution capabilities, or an installed Open Design Codex plugin, is required. Use the actual entry points and tool names exposed by your runtime.

This skill does not include an execution engine, automatically install services, or target a specific product named Open Design. An integration that only provides a design library, brief templates, and artifact registration does not provide production and export capabilities. A genuine plugin execution workflow may run on the host agent; the orchestration layer must not independently interpret requirements or produce work and then attribute it to Open Design.

All intermediate and final files follow the user's project output rules. Existing resources are used on a read-only basis.

## Validation status

Independent agents have completed simulated tests of responsibility boundaries and stage transitions. Plugin delegation and exemptions from the three-direction gate were refined and retested. Actual end-to-end testing with Open Design has not yet been completed, and compatibility across all runtimes and models has not been verified.

## References

The workflow draws on [huashu-design](https://github.com/alchaincyf/huashu-design). For an example of integration differences, see the [Open Design agent-kit MCP documentation](https://github.com/feimacode/open-design-agent-kit/blob/main/packages/mcp-server/README.md).

This is an independent workflow skill. The referenced projects are not installation dependencies.
