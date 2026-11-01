# API Contract (v0.1)

Base URL: `/api`. All bodies are JSON unless noted. Language codes: `ha` Hausa, `en` English, `pcm` Pidgin, `yo` Yoruba, `ig` Igbo.
Frontend builds against `/mock/*.json` until the backend is live. Shapes below will not change without notice.

## POST /api/ask
Request: `{ "question": string, "language": "ha"|"en"|"pcm"|"yo"|"ig" }`
Response: see `mock/ask.answered.json` and `mock/ask.refused.json`
- `status`: `"answered"` or `"refused"` (refused = not enough official source, tell user to check with INEC)
- `citations[]`: `{ title, source, section, url }` (answered always has at least 1)
- `disclaimer`: string shown under every answer

## POST /api/check-claim
Request: `{ "claim": string, "language": string }`
Response: see `mock/check-claim.json`
- `verdict`: `"supported"` | `"contradicted"` | `"unverified"`
- `sent_to_review`: true if a human must confirm before it is treated as final

## POST /api/transcribe  (multipart/form-data, field `audio`)
Response: see `mock/transcribe.json` -> `{ transcript, language }`

## GET /api/review-queue
Response: see `mock/review-queue.json`

## POST /api/review-queue/{id}/decision
Request: `{ "decision": "approve"|"reject", "note": string }`
Response: `{ "id": string, "status": "approved"|"rejected" }`

## Errors
`{ "error": { "code": string, "message": string } }` with HTTP 4xx/5xx. Show a friendly retry message.
