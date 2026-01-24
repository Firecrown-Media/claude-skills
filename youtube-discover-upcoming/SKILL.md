---
name: youtube-discover-upcoming
description: Find emerging YouTube channels in a niche for potential partnership and sponsorship outreach
argument-hint: "[keywords or category]"
disable-model-invocation: true
---

# YouTube Upcoming Channel Discovery (Partnership Outreach)

Find emerging/upcoming YouTube channels for partnerships in: **$ARGUMENTS**

## YouTube API Configuration

**API Key:** `AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls`

Use this API key with the YouTube Data API v3 for accurate data:

```bash
# Search for channels by keyword
curl "https://www.googleapis.com/youtube/v3/search?part=snippet&q=$ARGUMENTS&type=channel&maxResults=25&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get channel statistics (filter by subscriber count for emerging channels)
curl "https://www.googleapis.com/youtube/v3/channels?part=snippet,statistics,contentDetails,brandingSettings&id=CHANNEL_IDS&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"

# Get videos to check engagement rates
curl "https://www.googleapis.com/youtube/v3/videos?part=snippet,statistics&id=VIDEO_IDS&key=AIzaSyCkpwkCPkEPh-gtLhLUZWNepUWc_uBFDls"
```

**Note:** The `brandingSettings` part includes the channel's business email if they've made it public.

## Instructions

### Phase 1: Find Emerging Channels

Focus on **rising creators** (not mega-channels) who are more likely to respond to partnership deals.

1. **Search for upcoming/rising creators**:
   - "rising $ARGUMENTS YouTubers 2024 2025"
   - "up and coming $ARGUMENTS YouTube channels"
   - "small $ARGUMENTS YouTubers to watch"
   - "$ARGUMENTS YouTube channels under 100k subscribers"
   - "fastest growing $ARGUMENTS YouTubers"
   - "underrated $ARGUMENTS YouTube channels"

2. **Target subscriber ranges** (sweet spot for partnerships):
   - Micro: 10K - 50K subscribers
   - Small: 50K - 100K subscribers
   - Mid-tier: 100K - 500K subscribers

   These creators are often more responsive and offer better ROI than mega-influencers.

3. **Use the YouTube API to verify and filter**:
   - Get channel IDs from search results
   - Fetch statistics to confirm subscriber counts are in target range
   - Filter OUT channels with 500K+ subscribers
   - Get brandingSettings to find business emails

### Phase 2: Evaluate Each Channel

For each discovered channel, gather:

**Basic Info:**
- Channel name and URL
- Subscriber count
- Total views / average views per video
- Upload frequency
- Content focus

**Partnership Indicators:**
- Engagement rate (comments/likes relative to views)
- Do they already do sponsorships? (good = experienced, knows the process)
- Content quality and production value
- Audience demographics (if discernible)
- Growth trajectory (are they trending up?)

**Contact Info (if available):**
- Business email (usually in About section or description)
- Social media handles
- Management/agency (if any)

**Partnership Fit Assessment:**
- Brand safety (content appropriate?)
- Audience alignment
- Estimated sponsorship rate (industry standard: $10-50 per 1K views)

### Phase 3: Rank by Partnership Potential

Score channels on:
1. **Engagement** - High engagement = loyal audience
2. **Growth rate** - Fast growth = good momentum
3. **Content quality** - Professional = reflects well on partners
4. **Accessibility** - Has business email, responds to comments
5. **Sponsorship experience** - Has done deals before

### Phase 4: Output

Save the research to: `Youtube Research/$ARGUMENTS-partnership-prospects.md`

## Output File Structure

```markdown
# Partnership Prospects: [Keywords/Category]

**Research Date:** [Today's Date]
**Category:** $ARGUMENTS

## Executive Summary
- Total channels identified: X
- Top prospects: [names]
- Estimated reach: X combined subscribers
- Budget range: $X - $X for sponsored content

---

## Top Partnership Prospects

### Tier 1: High Priority (Best Fit)

#### 1. [Channel Name]
| Metric | Value |
|--------|-------|
| **URL** | [link] |
| **Subscribers** | X |
| **Avg Views** | X per video |
| **Upload Frequency** | X/week |
| **Engagement Rate** | X% |
| **Has Done Sponsors** | Yes/No |
| **Business Email** | [email or "Check About page"] |
| **Est. Sponsorship Rate** | $X - $X |

**Why They're a Good Fit:**
- [Reason 1]
- [Reason 2]

**Content Examples:**
- [Video 1] - X views
- [Video 2] - X views

**Outreach Notes:**
- [Any relevant info for reaching out]

---

#### 2. [Channel Name]
...

---

### Tier 2: Medium Priority (Worth Considering)

#### 3. [Channel Name]
...

---

### Tier 3: Watch List (Growing, Check Back Later)

| Channel | Subscribers | Why Watch |
|---------|-------------|-----------|
| [Name]  | X           | [reason]  |

---

## Outreach Template

Subject: Partnership Opportunity with [Your Company]

Hi [Creator Name],

I've been following your content on [specific topic] and really enjoyed [specific video].

I'm reaching out from [Company] - we [brief description]. I think there's a great fit between your audience and what we offer.

Would you be open to discussing a potential collaboration? We're flexible on format (dedicated video, integration, etc.).

Looking forward to hearing from you!

[Your Name]

---

## Market Insights

### What's Working in This Niche
- [Insight 1]
- [Insight 2]

### Sponsorship Trends
- [Trend 1]
- [Trend 2]

### Recommended Partnership Formats
- [ ] Dedicated sponsor video
- [ ] Product integration/mention
- [ ] Affiliate deal
- [ ] Long-term ambassador
```
