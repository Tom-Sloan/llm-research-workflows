# Literature Synthesis Prompt

Template for synthesizing findings from multiple sources into a coherent analysis.

## Prompt Template

```
Given the following sources on [TOPIC], synthesize the key findings:

## Sources
[List of papers/articles with key extracted information]

## Synthesis Requirements

1. **Consensus Findings**: What do multiple sources agree on?
2. **Conflicting Results**: Where do sources disagree? Why might this be?
3. **Methodology Comparison**: How do study designs differ? Which are more rigorous?
4. **Gaps Identified**: What questions remain unanswered?
5. **Practical Implications**: What does this mean for [specific application]?

## Output Format

### Executive Summary
[2-3 sentences capturing the main takeaway]

### Key Findings Table
| Finding | Supporting Sources | Confidence |
|---------|-------------------|------------|
| ... | ... | High/Medium/Low |

### Detailed Analysis
[Organized by theme or sensor type]

### Limitations of Current Research
[What should readers be cautious about]

### Recommendations
[Actionable next steps based on evidence]
```

## Confidence Levels

- **High**: Multiple peer-reviewed studies with consistent findings, adequate sample sizes
- **Medium**: Single peer-reviewed study OR multiple non-peer-reviewed sources with consistency
- **Low**: Limited evidence, conflicting results, or primarily commercial claims

## Example Usage

When the research agent has gathered sources, this template structures the synthesis phase to ensure balanced, evidence-based conclusions.
