# LLM Research Workflows

Agent-assisted research workflows using Claude API and OpenClaw for automated literature review, sensor evaluation, and structured report generation.

## Overview

This repository contains prompts and methodology for using LLM agents to accelerate technical research. Developed for IoT sensor evaluation in healthcare contexts (elderly monitoring, fall detection, UTI prediction) but applicable to broader research tasks.

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

1. **Input**: Research question (e.g., "Find sensors suitable for elderly UTI detection in home settings")
2. **Literature Search**: Agent searches IEEE Xplore, PubMed, and web sources
3. **Synthesis**: Extracts key findings, compares approaches, identifies gaps
4. **Iteration**: Human reviews, provides feedback, agent refines
5. **Output**: Formatted report with tables, specifications, and citations

## Tools

- **Claude API**: Primary LLM for reasoning and synthesis
- **OpenClaw**: Agent orchestration, tool use, persistent memory
- **Web Search**: Brave Search API for academic and commercial sources

## Prompts

- [`prompts/research-agent.md`](prompts/research-agent.md) - System prompt for research tasks
- [`prompts/literature-synthesis.md`](prompts/literature-synthesis.md) - Template for literature review
- [`prompts/report-generation.md`](prompts/report-generation.md) - Structured report formatting

## Example Output

- [`examples/sensor-evaluation-report.md`](examples/sensor-evaluation-report.md) - Sample sensor evaluation report

## Methodology

### Prompt Engineering Approach

1. **Clear task decomposition**: Break research into discrete steps (search → filter → synthesize → format)
2. **Explicit output structure**: Define expected format upfront (tables, sections, citation style)
3. **Iterative refinement**: Review outputs, provide specific feedback, regenerate
4. **Source verification**: Require citations, verify claims against original sources

### Evaluation

- **Relevance**: Does output address the research question?
- **Accuracy**: Are cited sources real and correctly summarized?
- **Completeness**: Are key approaches/products covered?
- **Actionability**: Can decisions be made from the output?

## Use Cases

- Sensor selection for IoT healthcare systems
- Technology landscape analysis
- Competitive product research
- Literature review for grant proposals

## Author

Tom Sloan - [tom-sloan.com](https://tom-sloan.com)

Part of research work at SAM3 (Sensors and Analytics for Measuring Mobility and Memory), Carleton University.
