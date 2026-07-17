# Proposed Suno Platform Integration

Status: Early-access application
Official API access: Pending
Reference application: OVG Music / 声浪工坊

## Purpose

This proposal defines how an approved Suno Platform integration can serve as the music-generation provider behind OpenVoiceGateway.

OVG is responsible for cross-platform identity, intent normalization, authorization, quotas, audit records, task correlation, and multi-device continuity. Suno would provide original music generation and any generation or revision capabilities made available by the official API.

The integration will use only Suno-issued platform credentials and documented official endpoints. It will not scrape the Suno consumer product, automate a consumer session, or present a third-party compatible service as the official Suno API.

## User experience

A creator can start from Siri, Gemini, an AI agent, smart glasses, an in-car interface, or another voice surface.

Example request:

> Create a warm Chinese pop song for tonight's livestream. Use a gentle female vocal and a memorable chorus.

The source adapter converts the request to an OVG generate_music intent. The gateway authenticates the user, validates the request, applies credits and safety policy, creates an asynchronous task, and calls the approved music provider.

The user can later continue from another device:

> Keep the chorus, increase the tempo, and shorten the ending.

That becomes a revise_music intent tied to the original work and its version history.

## Supported music intents

- generate_music
- revise_music
- get_music_status
- list_music_works

The examples directory contains provider-neutral request payloads. The schema is defined in schemas/music-intent-v1.schema.json.

## Architecture

1. Voice interface or AI agent
2. OVG source adapter
3. OVG gateway authentication and policy
4. Music task and version service
5. Approved Suno Platform adapter
6. Correlated OVG response

Suno credentials remain on the server. Browsers, voice devices, and third-party agents never receive the API key.

## Data minimization

Only the minimum creative fields required by an approved endpoint will be sent: prompt, lyrics, style parameters, and an explicitly selected source-audio reference when supported.

The integration will not include phone numbers, password hashes, payment data, unrelated device identifiers, or private account metadata in music-generation requests.

## Safety and rights

- No impersonation of real artists or unauthorized voice cloning.
- No third-party lyrics, recordings, or identity attributes without permission.
- AI-generated content labels and version provenance are preserved.
- Users can delete works, request account deletion, and submit copyright complaints.
- Generated-result rights are described according to applicable law and the official Suno platform terms.
- OVG does not promise that every generated result is copyrightable, unique, or free from all third-party claims.

## Operational controls

- Authenticated access
- Per-user credit and rate limits
- Provider budget caps
- Asynchronous status polling and callbacks
- Request IDs and task audit trails
- Central provider disable switch
- Human review path for reported or competition content

## Reference implementation

A working public technical demo already implements the OVG intent endpoint, user accounts, music tasks, natural-language revisions, work versioning, credits, competitions, and public legal pages. Its current music provider is isolated behind a replaceable adapter and clearly labeled when non-official. The approved Suno adapter will remain disabled until Suno issues official platform credentials.

Public demo:

https://music.fireupfuture.cn/public/ovg.html

DNS, HTTPS, public legal pages, and the authenticated OVG boundary have been verified.
