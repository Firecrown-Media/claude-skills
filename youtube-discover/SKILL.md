---
name: youtube-discover
description: Discover and research top YouTube channels in a niche or category based on keywords
argument-hint: "[keywords or category]"
disable-model-invocation: true
---

# YouTube Channel Discovery

Discover top YouTube channels for: **$ARGUMENTS**

## YouTube API Configuration

**API Key:** `AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls`

Use this API key with the YouTube Data API v3 for accurate channel data:

```bash
# Search for channels by keyword
curl "https://www.googleapis.com/youtube/v3/search?part=snippet&q=$ARGUMENTS&type=channel&maxResults=10&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get channel statistics (replace CHANNEL_IDS with comma-separated IDs)
curl "https://www.googleapis.com/youtube/v3/channels?part=snippet,statistics,contentDetails&id=CHANNEL_IDS&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get videos from a channel's uploads playlist
curl "https://www.googleapis.com/youtube/v3/playlistItems?part=snippet,contentDetails&playlistId=PLAYLIST_ID&maxResults=10&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get video statistics
curl "https://www.googleapis.com/youtube/v3/videos?part=snippet,statistics&id=VIDEO_IDS&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"
```

## Instructions

### Phase 1: Find Channels

1. **Search using web search first** to identify top channels in this niche:
   - "best $ARGUMENTS YouTube channels 2024 2025"
   - "top $ARGUMENTS YouTubers"
   - "$ARGUMENTS YouTube creators to watch"
   - "most popular $ARGUMENTS YouTube channels"

2. **Compile a list of 5-10 relevant channels** that appear frequently in results

3. **Use the YouTube API** to get accurate stats for each channel:
   - Search for each channel name to get channel ID
   - Fetch channel statistics (subscribers, total views, video count)
   - Get their top videos with view counts

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
