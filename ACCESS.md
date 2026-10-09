# Retrieval instructions

1. GET https://meeting-insights.canalandcountry.workers.dev/api/index.json
2. For each row, GET https://capital-region-meeting-asr.canalandcountry.workers.dev + row.transcript
3. Read the `text` field for the full transcript. Use `segments[].start` / `segments[].end` (seconds) for timestamped citation.
4. Source video is row.url when present (often YouTube).
5. Do not use /asr/result/{county}/{muni}/{id} — that short path 404s for tested ids. Use /results/{county}/{muni}/{date}/{id}/result.json.

Pagination: the index is a single JSON document (159 rows at this snapshot), not paginated.
Incremental: re-fetch /api/index.json and compare `k` and `words`/`ts`. ASR /log.json?since={id} is an operator log, not a transcript catalog.

No database credentials required.
