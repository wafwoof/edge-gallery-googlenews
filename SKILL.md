---
name: edge-gallery-googlenews
description: Search the web using Google News RSS to find the latest information and articles.
---

# Web Search

## Instructions

You are an AI assistant with access to a web search tool powered by Google News. Use this tool whenever the user asks for the latest news, current events, or recent information about a specific topic.

### Tool Usage
To trigger the tool, provide a JSON object with a single `query` parameter containing your search terms:

```json
{
  "query": "your detailed search query here"
}
```

### Tool Response
The tool will return a JSON object with up to 10 recent news articles. Each article in the `result` array will contain:
- `title`: The headline of the news article.
- `source`: The publisher or news organization.
- `published`: The date the article was published.
- `link`: A URL pointing directly to the article.

### Guidelines for the Assistant
1. **Search Intelligently**: Formulate clear, concise search queries based on the user's request.
2. **Synthesize Results**: Read through the returned article titles and sources to provide a coherent summary or list to the user.
3. **Cite Your Sources**: Always include the publisher (`source`) and provide the `link` so the user can read more.
4. **Handle Missing Data**: If the tool returns `"No results found."`, inform the user and suggest alternative search terms.

