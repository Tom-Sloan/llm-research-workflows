# Report Generation Prompt

Template for generating structured technical reports from research findings.

## Prompt Template

```
Generate a technical report on [TOPIC] for [AUDIENCE].

## Report Structure

### 1. Executive Summary
- Problem statement (1 sentence)
- Key findings (2-3 bullet points)
- Recommendation (1 sentence)

### 2. Background
- Context and motivation
- Scope of this analysis
- Key terminology

### 3. Methodology
- Sources consulted
- Selection criteria
- Limitations of this review

### 4. Findings

#### 4.1 [Category 1]
| Product/Approach | Key Specs | Strengths | Limitations | Source |
|-----------------|-----------|-----------|-------------|--------|
| ... | ... | ... | ... | ... |

[Narrative analysis]

#### 4.2 [Category 2]
[Repeat structure]

### 5. Comparison Matrix
| Criteria | Option A | Option B | Option C |
|----------|----------|----------|----------|
| Cost | ... | ... | ... |
| Accuracy | ... | ... | ... |
| Privacy | ... | ... | ... |
| Integration | ... | ... | ... |

### 6. Recommendations
- Primary recommendation with rationale
- Alternative approaches
- Suggested next steps

### 7. References
[Full citations in consistent format]

## Formatting Guidelines

- Use markdown for structure
- Tables for comparisons (keep to 4-5 columns max)
- Bullet points for lists
- Bold for emphasis sparingly
- Include DOI or URL for each reference when available
```

## Audience Adaptation

- **Technical team**: Include specifications, implementation details
- **Management**: Focus on cost, timeline, risk
- **Grant proposal**: Emphasize novelty, impact, preliminary evidence
