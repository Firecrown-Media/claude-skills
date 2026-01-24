---
name: youtube-discover
description: Discover and research top YouTube channels in a niche or category based on keywords
argument-hint: "[keywords or category]"
disable-model-invocation: true
---

# YouTube Channel Discovery

Discover top YouTube channels for: **$ARGUMENTS**

## Instructions

### Phase 1: Find Channels

1. **Search for top channels** in this niche using web search:
   - "best $ARGUMENTS YouTube channels 2024 2025"
   - "top $ARGUMENTS YouTubers"
   - "$ARGUMENTS YouTube creators to watch"
   - "most popular $ARGUMENTS YouTube channels"

2. **Compile a list of 5-10 relevant channels** that appear frequently in results

### Phase 2: Research Each Channel

For each discovered channel, gather:
- Channel name and URL
- Subscriber count
- Content focus/sub-niche
- Top 3-5 videos with view counts
- What makes them stand out
- Upload frequency

### Phase 3: Comparative Analysis

Analyze patterns across all channels:
- Common content themes that perform well
- Title formulas that get views
- Gaps in the market (underserved topics)
- Audience size distribution (mega vs mid-tier creators)
- Content formats (tutorials, vlogs, reviews, etc.)

### Phase 4: Output

Save the research to: `Youtube Research/$ARGUMENTS-niche-research.md`

## Output File Structure

```markdown
# YouTube Niche Research: [Keywords/Category]

**Research Date:** [Today's Date]
**Search Terms:** $ARGUMENTS

## Top Channels in This Niche

### 1. [Channel Name]
- **URL:** [link]
- **Subscribers:** X
- **Focus:** [specific sub-niche]
- **Top Videos:**
  - [Video 1] - X views
  - [Video 2] - X views
  - [Video 3] - X views
- **Why They Work:** [brief insight]

### 2. [Channel Name]
...

## Niche Overview

| Channel | Subscribers | Avg Views | Focus |
|---------|-------------|-----------|-------|
| ...     | ...         | ...       | ...   |

## Content Patterns

### What's Working in This Niche
- [Pattern 1]
- [Pattern 2]
- [Pattern 3]

### Common Title Formulas
- [Formula 1]
- [Formula 2]

### Popular Content Formats
- [Format 1]
- [Format 2]

## Market Gaps & Opportunities
- [Gap 1]
- [Gap 2]
- [Gap 3]

## Key Takeaways
1. [Takeaway 1]
2. [Takeaway 2]
3. [Takeaway 3]

## Recommended Channels to Study Further
1. [Channel] - [reason]
2. [Channel] - [reason]
```
