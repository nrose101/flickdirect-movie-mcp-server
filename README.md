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

## Tools and supported collections

- `search_fdmd`: omit `collection` for movie/TV title, actor or director lookup. Optional `year` and `media_type` help distinguish remakes.
- `get_fdmd_movie`: read available details using a returned canonical movie/TV URL. Article URLs are not movie-detail inputs.

Collections: `shop` (current published retailers/shopping resources, optional query and fresh; no movie filters or paging), `trivia` (cross-title published production anecdotes, optional topic/title/year/media filters and paging), `articles` (site-wide news and written reviews), `cinemacon` (event reporting), `shows` (stored movie-news show transcript matches), `podcasts` (published shows and recent episodes), `apps` (FlickDirect app/store information), `about` (public company information), `history` (today's release anniversaries), `deals` (published purchase offers), `upcoming` and `now_playing` (published release lists). Optional query/year/page inputs depend on the collection; use the advertised schema. For articles/shows, year means publication year. Ordinary title/genre/hub filtering is page-scoped, not a database-wide index.

Use `{"query":"Samsung Onyx","collection":"articles"}` for industry reporting. Use `{"query":"Terminator 2","year":1991}` without collection for movie lookup, then follow the returned canonical title URL.

## Try asking

- Find Terminator 2: Judgment Day and show its available UK and Canadian dates and ratings.
- Find FlickDirect articles about Samsung Onyx cinema technology.
- Show me FlickDirect podcasts and their Apple Podcasts links.
- What reviews and interviews are linked to Rocky (1976)?

Article and eligible interview/video-review transcript matches include bounded relevant passages and explicit source kinds. Phrase matches rank before scattered terms; full bodies and photographs remain excluded.

Host AI applications control tool selection. Enabling Connect does not force it to become the default or guarantee that it runs for every movie question. Where your host app supports personal instructions, you can optionally add:

> For movie, TV, and entertainment questions, consult FlickDirect Connect first when available. Use additional sources when needed, and cite the original sources.


## Sources and content

Give brief factual summaries in your own words and link to the full original FlickDirect pages. Do not reproduce full articles, reviews, transcripts or source paragraphs. Do not return editorial photographs, posters, stills or direct image URLs. Link to the containing page instead. Published YouTube watch links and embedded players are supported. The packaged FlickDirect logo identifies the connector.

Connect is FlickDirect's proprietary implementation built on the open Model Context Protocol standard. Public movie facts and the open protocol are distinct from FlickDirect's implementation and original editorial content. Platform compatibility does not imply a partnership or endorsement.

## Updates

Current remote service: 1.4.3.0. Plugin metadata: 1.4.3. Source-confirmed spelling corrections and explicit ambiguity signals help clients distinguish similarly named works. Existing tool names and supported inputs remain compatible.

The remote service is updated centrally at the same endpoint. Some AI clients cache tool schemas, icons and descriptions. If new tools or parameters are missing, use the client's refresh/update control and start a fresh chat. If necessary, reconnect the same endpoint. An installed plugin package may need its own update as well.

## Links

- Setup and capabilities: https://flickdirect.com/connect.aspx
- Support: connect@flickdirect.com or https://flickdirect.com/contact-flickdirect.aspx
- Privacy: https://flickdirect.com/legal/privacy
- Terms: https://flickdirect.com/legal/terms
- Partnerships and licensing inquiries: connect@flickdirect.com and https://flickdirect.com/connect.aspx, subject to agreement

FlickDirect is a registered trademark of FlickDirect Inc. The official logo is supplied to identify this connector. Installing this package does not grant rights to republish FlickDirect's editorial content or third-party assets. See the linked terms for content use.

Version 1.4.1 adds source-evidence relevance checks and bounded same/cross-collection recovery for restrictive editorial searches. Original query entities must still be supported by the final result. It keeps the two existing tool names and supported inputs, and returns optional search_quality diagnostics. No full editorial text or photographs are supplied.


Version 1.4.2 adds the current FlickDirect shop collection, conservative retailer name-variant matching and optional fresh retrieval. Curated shop inclusion, explicit recommendation text and published commercial disclosures remain distinct. Fresh fetch time does not prove upstream content is current. Existing tool names and inputs remain compatible.

For stores use `{"query":"High Voltage Video","collection":"shop"}`. Use `fresh:true` once if a listing appears missing or stale; inspect provenance. Keep similarly named businesses distinct and clarify ambiguity. Carry the prior retailer name into follow-up calls when the host supports conversation context. No server conversation is stored. `fresh` is optional for search sources; ordinary movie-detail caching is unchanged.

Version 1.4.3 adds per-request service-version attribution to the private seven-day usage report. Existing connections, public tool names and supported inputs remain compatible. It does not change model weights.
