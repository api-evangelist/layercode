# Layercode (layercode)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Layercode provides voice-AI agent infrastructure - low-latency voice pipelines that turn any LLM or text-based agent into a conversational voice agent for web, mobile, and phone. A REST API manages agents, sessions, and outbound calls, while a realtime WebSocket transport streams audio to the browser and a signed webhook delivers transcripts to your backend, which streams text-to-speech responses back over Server-Sent Events.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/layercode/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/layercode/refs/heads/main/apis.yml)

## Tags

- AI
- Voice
- Voice Agents
- Realtime
- Low Latency

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Layercode Agents API

List, create, retrieve, and update voice agents (pipelines) and authorize browser client sessions against an agent using an org-scoped API key.

- **Human URL:** [https://docs.layercode.com/api-reference/rest-api](https://docs.layercode.com/api-reference/rest-api)
- **Base URL:** `https://api.layercode.com/v1`

#### Tags

- Agents
- Pipelines
- Management

#### Properties

- [Documentation](https://docs.layercode.com/api-reference/rest-api)
- [API Reference](https://docs.layercode.com/api-reference/rest-api)
- [OpenAPI](openapi/layercode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/layercode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/layercode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Layercode Sessions API

Retrieve session detail - transcript, duration, metadata, and recording status - for a conversation handled by an agent, and download the session audio recording, plus initiate outbound phone calls.

- **Human URL:** [https://docs.layercode.com/api-reference/rest-api](https://docs.layercode.com/api-reference/rest-api)
- **Base URL:** `https://api.layercode.com/v1`

#### Tags

- Sessions
- Conversations
- Recordings

#### Properties

- [Documentation](https://docs.layercode.com/api-reference/rest-api)
- [API Reference](https://docs.layercode.com/api-reference/rest-api)
- [OpenAPI](openapi/layercode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/layercode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/layercode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Layercode Realtime Voice API

Bidirectional realtime WebSocket transport that streams base64 PCM microphone audio from the browser to Layercode and streams synthesized speech, transcripts, and structured data back, authorized with a short-lived client_session_key.

- **Human URL:** [https://docs.layercode.com/api-reference/frontend-ws-api](https://docs.layercode.com/api-reference/frontend-ws-api)
- **Base URL:** `wss://api.layercode.com/v1/agents/web/websocket`

#### Tags

- Realtime
- WebSocket
- Voice
- Audio

#### Properties

- [Documentation](https://docs.layercode.com/api-reference/frontend-ws-api)
- [API Reference](https://docs.layercode.com/api-reference/frontend-ws-api)
- [AsyncAPI](asyncapi/layercode-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Layercode Webhooks API

HMAC-signed webhook Layercode POSTs to your backend with session and transcript events (session.start, message, data, session.update, session.end); your backend streams response.tts / response.data / response.end events back as Server-Sent Events that drive the agent's speech.

- **Human URL:** [https://docs.layercode.com/api-reference/webhook-sse-api](https://docs.layercode.com/api-reference/webhook-sse-api)
- **Base URL:** `https://docs.layercode.com/api-reference/webhook-sse-api`

#### Tags

- Webhooks
- SSE
- Events

#### Properties

- [Documentation](https://docs.layercode.com/api-reference/webhook-sse-api)
- [API Reference](https://docs.layercode.com/api-reference/webhook-sse-api)
- [AsyncAPI](asyncapi/layercode-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

## Common Properties

- [GitHub Organization](https://github.com/layercodedev)
- [LinkedIn](https://www.linkedin.com/company/layercode)
- [Website](https://layercode.com)
- [Documentation](https://docs.layercode.com)
- [Plans](plans/layercode-plans-pricing.yml)
- [Rate Limits](rate-limits/layercode-rate-limits.yml)
- [Fin Ops](finops/layercode-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
