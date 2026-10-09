# Canal & Country meeting transcripts — read-only access

Snapshot of the public publication index as of **2026-10-09T07:27:19.044Z**.

Access tested from Grok's environment; awaiting ChatGPT verification.

## Start here

- HTML insights shell (JS): https://meeting-insights.canalandcountry.workers.dev/?view=library
- Machine inventory (159 meetings, 1,288,008 indexed words): https://meeting-insights.canalandcountry.workers.dev/api/index.json
- ASR status: https://capital-region-meeting-asr.canalandcountry.workers.dev/status

## Full transcript JSON

Each index row has a `transcript` path. Prefix the ASR worker host:

`https://capital-region-meeting-asr.canalandcountry.workers.dev` + `transcript`

The JSON object includes `text` (full transcript), `segments` (start/end in seconds), and usually `word_count`.

### Tested examples (one per region)

- Capital Region / Niskayuna / 2026-10-02 / Economic Development: https://capital-region-meeting-asr.canalandcountry.workers.dev/results/schenectady-county/niskayuna/2026-10-02/xbDpw2nIpt8/result.json
- Rochester / Hamlin / 2026-09-14: https://capital-region-meeting-asr.canalandcountry.workers.dev/results/monroe-county/hamlin/2026-09-14/mZZZxhB0kG8/result.json
- Mid-Hudson / Marbletown / 2026-10-06: https://capital-region-meeting-asr.canalandcountry.workers.dev/results/ulster-county/marbletown/2026-10-06/mDBr7iyDzHg/result.json
- Rochester / Pittsford / 2026-07-14 (also verified): https://capital-region-meeting-asr.canalandcountry.workers.dev/results/monroe-county/pittsford/2026-07-14/1035587/result.json

## Counts at cutoff

- Insights index: 159 rows (capital-region 145, rochester 7, mid-hudson 7), 1,288,008 words, generated_at 2026-10-09T07:27:19.044Z.
- ASR status around 2026-10-09T16:08:20Z: 190 completed, 85 failed, 5,304 not started of 5,579 tracked gap meetings. Word telemetry ~1.58M including estimates.
- Difference: Insights is a publication/index lag behind the ASR completion ledger (about 31). Not proof of missing files.

## What is not in this repo

Server-rendered HTML pages containing every transcript, plain-text mirrors, and a dated ZIP of all transcripts were not published here. The Worker source repo is a stub and this environment has no Cloudflare deploy credentials. Existing result.json URLs are the authoritative full text.

Retention: live worker objects are the system of record. This README is a handoff, not a second store.
