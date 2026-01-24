---
name: youtube
description: Research a YouTube channel and output a detailed analysis with top videos, view counts, and content insights
argument-hint: "[channel-name]"
disable-model-invocation: true
---

# YouTube Channel Research

Research the YouTube channel: **$ARGUMENTS**

## YouTube API Configuration

**API Key:** `AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls`

Use this API key with the YouTube Data API v3 for accurate data. Example API calls:

```bash
# Search for channel by name
curl "https://www.googleapis.com/youtube/v3/search?part=snippet&q=$ARGUMENTS&type=channel&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get channel details (replace CHANNEL_ID)
curl "https://www.googleapis.com/youtube/v3/channels?part=snippet,statistics,contentDetails&id=CHANNEL_ID&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get channel's uploads playlist videos (replace PLAYLIST_ID)
curl "https://www.googleapis.com/youtube/v3/playlistItems?part=snippet,contentDetails&playlistId=PLAYLIST_ID&maxResults=50&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get video statistics (replace VIDEO_IDS with comma-separated IDs)
curl "https://www.googleapis.com/youtube/v3/videos?part=snippet,statistics,contentDetails&id=VIDEO_IDS&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"
```

## Instructions

1. **Find the channel using the API**:
   - Use the search endpoint to find the channel ID for "$ARGUMENTS"
   - Get full channel details using the channels endpoint
   - Get the uploads playlist ID from contentDetails.relatedPlaylists.uploads

2. **Fetch video data**:
   - Get videos from the uploads playlist (up to 50)
   - Get detailed stats for each video using the videos endpoint
   - Sort by view count to find top performers

3. **Supplement with web search** (for additional context):
   - Search for "$ARGUMENTS YouTube channel analytics" or "socialblade $ARGUMENTS"
   - Look for any news/articles about the channel

4. **Gather the following data**:
   - Channel name and URL
   - Subscriber count (approximate)
   - Total video count
   - Channel description/niche
   - Top 10-15 most viewed videos with:
     - Video title
     - View count
     - Upload date (if available)
     - Video duration (if available)
   - Recent upload frequency
   - Average views per video (estimate)

3. **Analyze content patterns**:
   - What topics/themes get the most views?
   - What title patterns are used in top-performing videos?
   - What video lengths perform best?
   - What thumbnail styles are common?
   - What posting schedule do they follow?

4. **Generate insights**:
   - What's working well for this channel?
   - Content gaps or opportunities
   - Engagement patterns
   - Growth trajectory (if data available)

5. **Output the research** to a markdown file:
   - Save to: `Youtube Research/$ARGUMENTS-research.md`
   - Use clear sections and formatting
   - Include the date of research
   - Format numbers with commas for readability

## Output File Structure

```markdown
# YouTube Channel Research: [Channel Name]

**Research Date:** [Today's Date]
**Channel URL:** [URL]

## Channel Overview
- Subscribers: X
- Total Videos: X
- Niche/Category: X
- Upload Frequency: X

## Top Performing Videos

| # | Title | Views | Upload Date |
|---|-------|-------|-------------|
| 1 | ...   | ...   | ...         |

## Content Analysis

### What's Working
- [Insight 1]
- [Insight 2]

### Title Patterns
- [Pattern 1]
- [Pattern 2]

### Content Themes
- [Theme 1]
- [Theme 2]

## Key Takeaways
1. [Takeaway 1]
2. [Takeaway 2]
3. [Takeaway 3]

## Recommendations
- [Recommendation 1]
- [Recommendation 2]
```
