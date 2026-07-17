# Suno API Early Access Brief

## Product

Product name: OpenVoiceGateway Music / 声浪工坊
Repository: https://github.com/nightwolf2012/OpenVoiceGateway
Stage: Working public technical demo; official Suno access pending
Public demo: https://music.fireupfuture.cn/public/ovg.html

## Short description

OpenVoiceGateway Music is a voice-first creation gateway that lets users create and revise original music from Siri, Gemini, AI glasses, car interfaces, or any AI agent. OVG normalizes each request into a provider-neutral intent, while the reference application handles lyrics, generation tasks, version history, creator rights, contests, billing, and safety. Suno would be the official music-generation provider behind this workflow.

## What we are building

We are building the first music reference application for the open OVG intent protocol: a cross-device, conversational music workflow.

A user can say, "Create a warm Chinese pop song for my livestream," receive a generated work, and later say, "Keep the chorus, increase the tempo, and shorten the ending." The request may begin on a phone and continue from a car, smart glasses, or desktop agent while remaining attached to the same authenticated task and version history.

OVG solves orchestration: identity, intent normalization, authorization, quotas, audit trails, task status, and multi-device continuity. We want the official Suno API to provide the original music-generation capabilities. The official integration will use only Suno-issued credentials and documented endpoints. We will not scrape or automate the Suno consumer product. Any current independent provider adapter is isolated, clearly labeled as non-official, and will never be presented as the Suno Platform API.

## Why this is different

Most music-generation products begin inside a dedicated editor. OVG turns generative music into a safe capability that any voice interface or AI agent can invoke.

The same provider-neutral intent can move between Siri, Gemini, Home Assistant, car systems, and future voice hardware. Music becomes a conversational creative object with an auditable chain of versions instead of a one-shot prompt result.

## Target users

- Chinese-speaking short-video and livestream creators
- Podcasters and small teams needing original intros or background music
- Independent creators who prefer voice-first workflows
- AI-device and agent developers needing a provider-neutral music capability

## Current readiness

- Public HTTPS Egg.js and MongoDB reference application
- User accounts and authenticated access
- Lyrics generation through an isolated provider interface
- Music tasks, polling, works, and natural-language revision
- Version history and task correlation
- Credit wallet, billing flow, competitions, and scoring
- OVG music intents and JSON Schema
- Public user agreement, privacy policy, copyright/content rules, and refund rules
- Apache-2.0 protocol repository and RFC-0001

## Data and safety

Only creative inputs required by an approved endpoint will be sent to Suno. API keys stay server-side. Account credentials and payment information are never included in generation requests.

The product prohibits real-artist impersonation, unauthorized voice cloning, and unlicensed third-party content. It preserves AI labels and provenance and provides deletion and copyright-complaint paths.

## Business model

The planned model uses creator credits and optional subscriptions for music creation, revisions, and competition entry. The product will not resell raw Suno credentials or expose a pass-through API that bypasses the user experience.

## Pilot

The initial pilot will be intentionally small and invitation-based, with per-user credits, rate limits, a global provider budget, and human review for reported content. Volume will grow only after quality, safety, and unit economics have been validated with Suno.

## Before submission

- Confirm the application contact email and authority to apply for the legal operator.
- Record a 60–90 second product walkthrough.
- Review every application answer before final submission.
