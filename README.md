# FlickDirect Connect: Movie MCP Server

FlickDirect Connect is FlickDirect's free, read-only movie MCP server. This repository contains the public plugin manifests, official brand assets and research skill used to connect compatible AI applications to the hosted service. The service implementation is maintained separately.

## Connect

- MCP endpoint: `https://connect.flickdirect.com/mcp`
- Transport: Streamable HTTP
- Authentication: None. No FlickDirect account, API key or paid subscription is required.
- Setup guide: https://flickdirect.com/connect.aspx

Use your AI application's custom remote MCP setup, enter the endpoint and select no authentication. Compatibility, installation controls and plan requirements vary by application. For plugin-capable clients, this package includes the portable Agent Plugins format and a Cursor compatibility manifest.

## What you can find

- Movie and television facts, cast, trivia and published source links.
- Stored release dates and ratings for the United States, United Kingdom, Canada and Germany. Missing values are omitted.
- Site-wide news, written reviews, cinema-industry and CinemaCon coverage, including stories without a movie association.
- Movie-news show matches in stored transcripts, podcast shows and recent episode previews with Apple Podcasts links.
- FlickDirect apps, public company information and today's published release anniversaries.
- Published streaming, soundtrack and daily-deal links when available. Destination availability and prices can change.

Tools: `search_fdmd` and `get_fdmd_movie`. Use `search_fdmd` with `collection: "articles"` for site-wide articles, rather than restricting every query to movie titles.

## Try asking

- Find Terminator 2: Judgment Day and show its available UK and Canadian dates and ratings.
- Find FlickDirect articles about Samsung Onyx cinema technology.
- Show me FlickDirect podcasts and their Apple Podcasts links.

## Sources and content

Give brief factual summaries in your own words and link to the full original FlickDirect pages. Do not reproduce full articles, reviews, transcripts or source paragraphs. Do not return editorial photographs, posters, stills or direct image URLs. Link to the containing page instead. Published YouTube watch links and embedded players are supported. The packaged FlickDirect logo identifies the connector.

Connect is FlickDirect's proprietary implementation built on the open Model Context Protocol standard. Public movie facts and the open protocol are distinct from FlickDirect's implementation and original editorial content. Platform compatibility does not imply a partnership or endorsement.

## Updates

The remote service is updated centrally at the same endpoint. Some AI clients cache tool schemas, icons and descriptions. If new tools or parameters are missing, use the client's refresh/update control and start a fresh chat. If necessary, reconnect the same endpoint. An installed plugin package may need its own update as well.

## Links

- Setup and capabilities: https://flickdirect.com/connect.aspx
- Support: https://flickdirect.com/contact-flickdirect.aspx
- Privacy: https://flickdirect.com/legal/privacy
- Terms: https://flickdirect.com/legal/terms
- Partnerships and licensing inquiries: https://flickdirect.com/legal/licensing

FlickDirect is a registered trademark of FlickDirect Inc. The official logo is supplied to identify this connector. Installing this package does not grant rights to republish FlickDirect's editorial content or third-party assets. See the linked terms for content use.
