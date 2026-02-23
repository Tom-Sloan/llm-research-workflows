# LLM Research Workflows

Prompts and methodology for using Claude API and OpenClaw to do literature review and generate research reports. I built this for sensor evaluation work at SAM3 (elderly health monitoring), but the approach works for any technical research.

## What this does

You give the agent a research question. It searches academic sources, pulls findings, and generates a formatted report with citations. You review, push back on weak sections, and it refines. The back-and-forth usually takes 2-3 iterations to get something meeting-ready.

## Architecture

```
┌─────────────────┐     ┌──────────────────┐     ┌─────────────────┐
│  Research       │────▶│  Claude API      │────▶│  Structured     │
│  Question       │     │  + OpenClaw      │     │  Report         │
└─────────────────┘     └──────────────────┘     └─────────────────┘
                               │
                               ▼
                        ┌──────────────────┐
                        │  • Web Search    │
                        │  • IEEE/PubMed   │
                        │  • Synthesis     │
                        │  • Citations     │
                        └──────────────────┘
```

## Workflow

1. Start with a specific question ("Find sensors for elderly UTI detection, no cameras, local processing only")
2. Agent searches IEEE Xplore, PubMed, commercial datasheets
3. Extracts specs, reported accuracy, study limitations
4. You review the draft, flag gaps or wrong directions
5. Agent refines until you have a report worth sharing

## Tools

- Claude API for reasoning and synthesis
- OpenClaw for agent orchestration and tool use
- Brave Search API for web and academic sources

## Prompts

- [`prompts/research-agent.md`](prompts/research-agent.md) - System prompt
- [`prompts/literature-synthesis.md`](prompts/literature-synthesis.md) - How to combine sources
- [`prompts/report-generation.md`](prompts/report-generation.md) - Report formatting

## Example

[`examples/sensor-evaluation-report.md`](examples/sensor-evaluation-report.md) - UTI detection sensor evaluation for the envisAGE project

## How I approach prompts

Break research into steps: search, filter, synthesize, format. Define the output structure upfront so you're not reformatting later. Require citations for every claim. Review outputs against the original sources when something sounds too clean.

The main failure mode is hallucinated references. Always verify citations exist before using a report externally.

## When this is useful

- Evaluating sensors or components for a project
- Surveying what's out there before writing a grant
- Competitive analysis
- Getting up to speed on an unfamiliar domain

## Author

Tom Sloan - [tom-sloan.com](https://tom-sloan.com)

Built during research work at SAM3, Carleton University.
