# RYNTA AI

**Research Your Next Trend Automatically**

RYNTA AI is a social-content intelligence and production-automation platform. It helps creators discover promising subjects, assess content opportunities, generate evidence-backed scripts and media assets, render short-form videos, and coordinate production workflows.

> This repository is a public project showcase. Production source code, workflow definitions, credentials, database migrations, and proprietary assets are maintained privately and are not distributed.

## My Role

**AI Automation Engineer / Full-Stack Engineer**

- Designed the customer-facing application and workflow architecture.
- Built research, scoring, script, media-generation, and rendering pipelines.
- Developed retry-safe orchestration with persistent workflow state and controlled downstream handoffs.
- Designed a private AI gateway for provider execution, runtime model selection, credential resolution, and usage accounting.
- Implemented project, niche, role, plan, and capability configuration.
- Built security boundaries that keep provider credentials out of browser code and workflow payloads.

## Product Flow

```text
Discover -> Analyze -> Research -> Score -> Create -> Publish -> Learn
```

## What the Platform Demonstrates

- Topic discovery, research, scoring, intelligence, and daily selection
- Evidence-backed script generation, review, and controlled revision
- Image, narration, transcription, caption, and video generation
- Vertical video assembly and inspection with FFmpeg and ffprobe
- Per-project AI provider, model, and capability configuration
- Secure user-managed provider credentials
- Retry-safe workflow jobs, idempotent persistence, and provider-usage accounting
- Role- and plan-aware product access

## Architecture

1. **Next.js dashboard** - authentication, projects, niches, credentials, and administration
2. **Supabase** - users, application data, workflow state, audit records, and media storage
3. **n8n workflows** - research, selection, script, asset, and rendering orchestration
4. **Private AI gateway** - provider selection, credential resolution, execution, and normalized responses
5. **Configured AI providers** - text, embeddings, image, voice, transcription, and video generation
6. **FFmpeg render layer** - final assembly, burned-in captions, overlays, and technical inspection

## Reliability Design

- Atomic job claiming and explicit running, completed, and failed states
- Retry limits and controlled recovery paths
- Versioned payload and validation contracts
- Idempotent downstream handoffs and repeatable upserts
- Success, no-result, review-required, and failure branches
- Audit snapshots for AI decisions and provider responses

## Technology

- Next.js 16, React 19, and TypeScript
- Tailwind CSS 4
- Supabase, PostgreSQL, and object storage
- n8n workflow orchestration
- OpenAI and configurable AI-provider integrations
- Embeddings, image, voice, transcription, and video-generation APIs
- FFmpeg and ffprobe
- Docker Compose

## Demo Availability

RYNTA AI is an actively developed pre-release platform.

- [Product Walkthrough](https://youtu.be/zteFUe7v3g0)

Additional technical walkthroughs and selected implementation details are available upon request.

## Source Availability

This repository intentionally contains no production source code, n8n workflow exports, environment configuration, credentials, access tokens, database exports, migrations, generated media, or proprietary assets.

## Usage and Rights

All project descriptions and materials are provided for portfolio review only. No license is granted to copy, redistribute, or reuse the private implementation.
