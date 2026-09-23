# SKILL: Reddit Trend Analysis

## Purpose
Analyze trends, opinions, and sentiments about any topic on Reddit globally across all subreddits. Works for shoes, stocks, tech, movies, politics, products, news, etc.

## Triggers & Usage Examples
- "/trend <topic>" 
- "What does Reddit say about <topic>?"
- "Reddit trend on: <topic>"
- "How is Reddit feeling about it? What are people discussing about this <topic>?"

## Parameters (Auto-extracted from prompt)
- **Topic** (Required): The subject to search for 
- **Time Range** (Optional, Default: "month"):
  - "day" / "today" / "last 24h"
  - "week" / "last week"
  - "month" / "last Month" (DEFAULT)
  - "year" / "last Jahr"
  - "all" / "no time range" / "all avaiable posts"

- **Sorting** (Optional, Default: relevance):
  - "relevance" (Standard)
  - "hot" (actual hot)
  - "top" (Top in time)
  - "new" (new topics) 

## Workflow & How to operate on Reddit

1. Open the browser at official address `https://www.reddit.com/search/?q=<QUERY>&sort=...&t=<TIME>`.
   - `q` = Suchbegriff (URL-encoded, Leerzeichen als %20)
   - `sort` = relevance | hot | top | new | comments
   - `t` = hour | day | week | month | year | all
   - Example: `https://www.reddit.com/search/?q=nike%20air%20max&sort=top&t=month`

2. Capture Results: Identify the Top 10-15 posts using browser page output (not external tools). 
   Note for every post:
   - Subreddit (r/...)
   - Topic
   - Upvotes (if able to see)
   - how much comments
   - Brief summary of the content (from the title and, where applicable, the preview)

   If the page does not load or does not return any results:
   - Fallback 1: Search directly in relevant subreddits
     `https://www.reddit.com/r/<Subreddit>/search/?q=<TERM>&t=<TIME>`
   - Fallback 2: Use `https://old.reddit.com/search?q=<TERM>&t=<TIME>`
     (simpler HTML structure, less JavaScript)

3. **Grouping themes**: Group results by recurring topics. What's frequently discussed? What stands out as consensus vs debate, or as strong opinions/contradictory trends? 
4. Compile a sentiment summary: 
   - General sentiment: Bullish / Bearish / Neutral / Mixed
   - Key bullish/positive arguments (3–5 points)
   - Key bearish/critical arguments (3–5 points)
   - Notable trends or recurring questions
   - Any alternatives or comparisons mentioned
   - Even if the results are inaccurate or irrelevant, summarise what you have found

## Output Format & Rules
- Always use emojis for easy readability: 🔥 🐂 📝 📌 💬 ⚠️ etc. 
- Keep outputs formatted and clean. Write a summary that looks like this structure:

```markdown
🔥 Reddit Trend Analysis: "<TOPIC>"  
⏱️ Time Range: <TIME> | Sort by: <SORT>
📍 Analyzed Posts: X from various subreddits across the search period  

---  
📊 Top discussions:

    [r/SUBREDDIT] ‘<Title>’ — <Upvotes> upvotes, <Comments> comments

    ...
    (5–10 posts in total, sorted by relevance)

🧠 Trend summary:
<Continuous text, 3–6 sentences: overall sentiment, main topics, trends>

🐂 Positive / Bullish voices:

    <Point 1>

    <Point 2>

    ...

🐻 Critical / Bearish views:

    <Point 1>

    <Point 2>

    ...

💡 Conclusion:
<2–3 sentences: What is the current Reddit consensus? What should one
bear in mind? Is there a clear trend or is opinion divided?>

## Important rules
- **Do not provide links** (users do not want URLs)
- **Search globally**, do not limit the search to a subreddit – unless
  the user explicitly specifies one
- **Respect the time period**: the default is ‘month’, but the user can
  override this
- **For shares**: Also mention sentiment (bullish/bearish/neutral)
- **For products/shoes**: Trends, hypes, “what’s in right now”
- **For controversial topics**: Present both sides fairly
- **Language**: Reply in the language in which the query is asked, even if the Reddit content is in a different language

Finally: Reply in the language of your conversation (if user asks in German, you answer in German). 

`https://www.reddit.com/search/?q=<TOPIC>&sort=top&t=week` → Provide results & analysis using that link as a baseline. Use screenshots only if required to debug and not include them into final reports unless asked!`.
