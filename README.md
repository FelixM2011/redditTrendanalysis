# Reddit Trend Analysis Skill for Hermes Agent

This skill integrates a deep, web-based sentiment and trend analysis engine directly into the Hermes Agent workflow. It allows you to discover how Twitter/X threads or the broader global internet reacts instantly to any real-world event, stocks, shoes, elections, or product news without needing custom APIs! 

## Author & Credits
### Created by **Felix Morocutti**

This is an open-source skill developed with love for data intelligence on Reddit specifically. 


## What it does:

Instead of manually searching, this **Hermes Skill** gives you an instant snapshot of global discussions: 

1. Identify what's trending on a specific topic (e.g., "Apple iPhone release", "Crypto Bear Market") using built-in web search tools & AI-powered context aggregation.  
2. Gather upvotes + comment counts from the Top posts per query across Reddit. 
3. Automatically summarize sentiment into Bullish / Neutral / Bearish insights!

## Installation:  

To install this skill in your personal Agent, simply add `~/.hermes/skills` to the skills directory.
For GitHub integration, it works perfectly inside Hermes' browser workflow (like using `camoufox`). If you are looking for Reddit specifically, ensure that's allowed at runtime and that permissions match up with any required proxies configured in your environment!

## Usage: 
Once installed and available globally, simply say to ChatGPT / GPT-4 model based agent what is in focus. A prompt like this works best: 

```bash
"hey reddit trend on 'Topic'" OR
"What's the current Reddit mood about 'Company X' ?"
```

It will output a highly structured report showing the Top Discussions, sentiment cluster analysis + conclusions for all users!


### Rules & Capabilities to use for publishing this SKILL: 
1. If you need more control of results in specific markets or languages, make sure your config file (.yaml) has that language configured correctly.
2. Always keep an eye on local timezones and proxy server limits when running browser queries against Reddit directly via headless setups like `Camoufox`.


## License
Permission is hereby granted under the MIT License to anyone wishing this into other projects as long as you reference back with a link!

Feel free to clone it at https://github.com/FelixM2011/redditTrendAnalysis if this becomes public.

# Keywords: NLP, Public Sentiment, Trend Discovery, Reddit, Browser-AI, Hermes Agent Skill.  
