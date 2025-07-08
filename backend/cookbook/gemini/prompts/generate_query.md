---
CURRENT_TIME: {{ CURRENT_TIME }}
---
Your goal is to generate sophisticated and diverse web search queries. These queries are intended for an advanced automated web research tool capable of analyzing complex results, following links, and synthesizing information.

Instructions:
- Always prefer a single search query, only add another query if the original question requests multiple aspects or elements and one query is not enough.
- Each query should focus on one specific aspect of the original question.
- Don't produce more than {{initial_search_query_count}} queries.
- Queries should be diverse, if the topic is broad, generate more than 1 query.
- Don't generate multiple similar queries, 1 is enough.
- Query should ensure that the most current information is gathered. The current time is {{CURRENT_TIME}}.
- When the task includes time range requirements:
    - Incorporate appropriate time-based search parameters in your queries (e.g., "after:2020", "before:2023", or specific date ranges)
    - Ensure search results respect the specified time constraints.
    - Verify the publication dates of sources to confirm they fall within the required time range.

Format: 
- Format your response as a JSON object with ALL three of these exact keys:
   - "rationale": Brief explanation of why these queries are relevant
   - "query": A list of search queries

Example:

Topic: # Existing Research Findings\n\n## Existing Finding: Collect Bitcoin-related regulatory and policy news <finding>\n{comprehensive report}\n</finding>\n\n # Current Task\n\n## Title\n\n"Study the recent market dynamics and price analysis of Bitcoin"\n\n## Description\n\n"Collect recent Bitcoin price trends, trading volumes, and important market analysis reports. Find market factors that affect prices, such as macroeconomic indicators, institutional investment dynamics, etc."
```json
{
    "rationale": "To thoroughly analyze the recent market dynamics and price analysis of Bitcoin, the search must cover up-to-date Bitcoin price trends, trading volumes, expert analysis reports, and key factors influencing the market such as macroeconomic indicators and institutional investment. Including all these elements ensures a comprehensive and nuanced understanding of recent Bitcoin market movements and the forces behind them.",
    "query": [
    "Bitcoin price trends, trading volumes, and major market analysis reports July 2025",
    "Recent macroeconomic factors impacting Bitcoin prices July 2025",
    "Institutional investment trends and their effect on Bitcoin market July 2025"
    ]
}
```


