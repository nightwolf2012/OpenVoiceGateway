# OpenVoiceGateway (OVG)

## Vision

OpenVoiceGateway (OVG) is an open protocol and gateway layer that connects voice assistants, AI agents, and tools through a unified intent-based architecture.

The goal of OVG is to become the standard communication layer between:

- Siri
- Gemini
- Alexa
- Home Assistant
- AI Glasses
- AI Earbuds
- Future Voice Interfaces

and

- OpenClaw
- Hermes Agent
- OpenAI Agents
- Claude
- LangGraph
- Local LLM Agents

## Problem

Today every voice platform has its own integration model.

Developers must build separate integrations for:

- iOS
- Android
- Alexa
- Home Assistant
- Future voice devices

This creates duplicated effort and fragmented ecosystems.

## Solution

OVG introduces a unified Intent Protocol.

Voice platforms send intents to OVG.

OVG routes those intents to AI agents.

Agents execute actions through tools.

Responses are returned back to the original voice platform.

## Architecture

Voice Assistant
↓
OVG Adapter
↓
OVG Gateway
↓
Agent Runtime
↓
Tool Layer

## Principles

1. OVG is not an AI model.
2. OVG is not tied to OpenClaw.
3. OVG is not tied to Siri.
4. OVG is protocol-first.
5. OVG is open and extensible.

## Roadmap

Phase 1:
- Intent Protocol

Phase 2:
- Gateway Core

Phase 3:
- Siri Adapter

Phase 4:
- Android Adapter

Phase 5:
- SDK

Phase 6:
- Registry

Phase 7:
- OVG Cloud

## License

Apache 2.0

## Music Reference Application

OVG Music / 声浪工坊 is the first proposed reference application for the OVG Intent Protocol. It turns requests from Siri, Gemini, AI agents, smart glasses, and car interfaces into provider-neutral music tasks.

Supported intents:

- `generate_music`
- `revise_music`
- `get_music_status`
- `list_music_works`

Resources:

- [Proposed Suno Platform integration](docs/integrations/suno.md)
- [Suno early-access brief](docs/applications/suno-early-access.md)
- [Music intent JSON Schema](schemas/music-intent-v1.schema.json)
- [Generate music example](examples/music/generate_music.json)
- [Revise music example](examples/music/revise_music.json)

Official Suno Platform access is pending. The public reference implementation uses a mock provider until approval and will not scrape the Suno consumer product or present unofficial services as the official Suno API.
