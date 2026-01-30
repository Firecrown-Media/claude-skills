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

# Search for top videos in the niche (by view count)
curl "https://www.googleapis.com/youtube/v3/search?part=snippet&q=$ARGUMENTS&type=video&order=viewCount&maxResults=25&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"
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

### Phase 3: Top 25 Video Analysis

**IMPORTANT:** This phase analyzes the top-performing videos across the entire niche.

1. **Search for top videos** using the YouTube API:
   ```bash
   # Search with multiple relevant keyword variations
   curl "https://www.googleapis.com/youtube/v3/search?part=snippet&q=$ARGUMENTS&type=video&order=viewCount&maxResults=25&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"
   ```

2. **Get detailed video statistics** for the video IDs returned:
   ```bash
   curl "https://www.googleapis.com/youtube/v3/videos?part=snippet,statistics,contentDetails&id=VIDEO_ID1,VIDEO_ID2,...&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"
   ```

3. **For each video, analyze and categorize:**
   - Video title and URL
   - View count, likes, comments
   - Channel name
   - Publish date
   - Video duration
   - **Topic Category** (assign one of: Tutorial/How-To, Entertainment, Review, Documentary, Vlog, News/Update, Challenge, Compilation, Interview, Other)
   - **Content Theme** (specific subject matter within the niche)
   - **Title Style** (clickbait, educational, emotional, question-based, list-based, etc.)

4. **Aggregate analysis:**
   - Count videos per category
   - Identify top-performing topics/themes
   - Analyze title patterns that drive views
   - Note video length trends for top performers
   - Calculate average engagement (likes/views ratio)

### Phase 4: Comparative Analysis

Analyze patterns across all channels:
- Common content themes that perform well
- Title formulas that get views
- Gaps in the market (underserved topics)
- Audience size distribution (mega vs mid-tier creators)
- Content formats (tutorials, vlogs, reviews, etc.)

### Phase 5: Output

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

---

## Top 25 Videos Analysis

### Video Rankings

| Rank | Title | Channel | Views | Likes | Category | Theme |
|------|-------|---------|-------|-------|----------|-------|
| 1 | [Title] | [Channel] | X | X | [Category] | [Theme] |
| 2 | [Title] | [Channel] | X | X | [Category] | [Theme] |
| ... | ... | ... | ... | ... | ... | ... |
| 25 | [Title] | [Channel] | X | X | [Category] | [Theme] |

### Category Breakdown

| Category | # of Videos | % of Top 25 | Avg Views | Top Performer |
|----------|-------------|-------------|-----------|---------------|
| Tutorial/How-To | X | X% | X | "[Title]" |
| Entertainment | X | X% | X | "[Title]" |
| Review | X | X% | X | "[Title]" |
| Documentary | X | X% | X | "[Title]" |
| Vlog | X | X% | X | "[Title]" |
| News/Update | X | X% | X | "[Title]" |
| Challenge | X | X% | X | "[Title]" |
| Compilation | X | X% | X | "[Title]" |
| Interview | X | X% | X | "[Title]" |

### Topic/Theme Analysis

**Most Common Themes in Top 25:**
1. [Theme 1] - X videos (X% of top 25)
2. [Theme 2] - X videos (X% of top 25)
3. [Theme 3] - X videos (X% of top 25)
4. [Theme 4] - X videos (X% of top 25)
5. [Theme 5] - X videos (X% of top 25)

**Emerging/Underrepresented Themes:**
- [Theme A] - Only X video(s), but high engagement
- [Theme B] - Gap opportunity

### Title Pattern Analysis

**Successful Title Formulas:**
1. **[Pattern Name]** - X videos use this
   - Examples: "[Title 1]", "[Title 2]"
   - Why it works: [explanation]

2. **[Pattern Name]** - X videos use this
   - Examples: "[Title 1]", "[Title 2]"
   - Why it works: [explanation]

3. **[Pattern Name]** - X videos use this
   - Examples: "[Title 1]", "[Title 2]"
   - Why it works: [explanation]

**Common Title Elements:**
- Numbers/Lists: X videos (X%)
- Questions: X videos (X%)
- Emotional words: X videos (X%)
- How-to/Tutorial language: X videos (X%)
- Caps/emphasis: X videos (X%)

### Video Length Analysis

| Duration Range | # of Videos | Avg Views | Best Performer |
|----------------|-------------|-----------|----------------|
| Under 5 min | X | X | "[Title]" |
| 5-10 min | X | X | "[Title]" |
| 10-20 min | X | X | "[Title]" |
| 20-30 min | X | X | "[Title]" |
| 30+ min | X | X | "[Title]" |

### Engagement Metrics

- **Average likes/views ratio:** X%
- **Average comments/views ratio:** X%
- **Highest engagement video:** "[Title]" (X% engagement)
- **Most commented video:** "[Title]" (X comments)

---

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
