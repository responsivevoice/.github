<p align="center">
  <img src="https://cdn.responsivevoice.org/assets/logo-250.svg" width="180" height="180" alt="ResponsiveVoice">
</p>

<h1 align="center">ResponsiveVoice</h1>

<p align="center">
  Modern, TypeScript-first text-to-speech for the web.
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/@responsivevoice/core"><img src="https://img.shields.io/npm/v/@responsivevoice/core.svg?label=%40responsivevoice%2Fcore" alt="npm version"></a>
  <a href="https://www.npmjs.com/package/@responsivevoice/core"><img src="https://img.shields.io/npm/dm/@responsivevoice/core.svg" alt="npm downloads"></a>
  <img src="https://img.shields.io/badge/types-included-3178C6?logo=typescript&logoColor=white" alt="TypeScript types included">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">
</p>

---

**ResponsiveVoice** turns text into speech with one small, well-typed API. The same `speak()` call works with the browser's built-in voices, a hosted multilingual catalog, or premium neural voices from your own provider keys — voice resolution, fallback, chunking, and streaming are handled for you.

- **One simple API** — `speak(text, voice, options)` is most of the surface area.
- **TypeScript-first** — full type definitions, shipped as ESM, CJS, and a browser IIFE.
- **Browser-native + cloud** — speaks via the Web Speech API out of the box, with hosted voices when you want them.
- **Bring your own key (BYOK)** — route premium voices from Google Cloud, Microsoft Azure, and OpenAI through the _same_ call, with more providers on the way.
- **Streaming** — HTTP and WebSocket audio streaming for low-latency playback.
- **Free to start** — demo mode needs no account, and everything is MIT licensed.

## Quick start

```bash
npm install @responsivevoice/core
```

```typescript
import { getResponsiveVoice } from '@responsivevoice/core';

const rv = await getResponsiveVoice({ apiKey: 'YOUR_API_KEY' });

rv.speak('Hello world', 'UK English Female');
```

Prefer a script tag? Drop in the browser bundle from the CDN:

```html
<script src="https://cdn.responsivevoice.org/sdk/latest/responsivevoice.js"></script>
<script>
  responsiveVoice.init({ apiKey: 'YOUR_API_KEY' });
  responsiveVoice.speak('Hello world', 'UK English Female');
</script>
```

## Unlock the full voice catalog

Out of the box, core runs in **demo mode** and speaks with the browser's default voice — no account required. To unlock the hosted multilingual catalog:

1. [Register for a free account](https://responsivevoice.org/register) — a default website is created for you, and its identifier is your **API key**.
2. Initialize core with that key.
3. Verify your website's domain in the dashboard so requests from your site are recognized.

## One API, every voice engine

You write against a single interface; ResponsiveVoice picks the right engine and gets out of the way.

| Tier               | Voices                                   | Needs                        |
| ------------------ | ---------------------------------------- | ---------------------------- |
| **Browser**        | The device's built-in Web Speech voices  | Nothing — works in demo mode |
| **Hosted**         | Multilingual server voice catalog        | A free API key               |
| **Premium (BYOK)** | Google Cloud, Microsoft Azure, OpenAI, … | Your own provider key        |

Bring your own key and premium neural voices route through the exact same `speak()` call — no SDK swaps, no per-provider glue code. More providers are on the way.

## Packages

| Package                                                                      | Description                                         | Links                                                                                                                    |
| ---------------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **[@responsivevoice/core](https://github.com/responsivevoice/core)**         | Browser & Node.js TTS client — start here           | [npm](https://www.npmjs.com/package/@responsivevoice/core) · [repo](https://github.com/responsivevoice/core)             |
| [@responsivevoice/api-client](https://github.com/responsivevoice/api-client) | REST & WebSocket client for the ResponsiveVoice API | [npm](https://www.npmjs.com/package/@responsivevoice/api-client) · [repo](https://github.com/responsivevoice/api-client) |

## Links

[responsivevoice.org](https://responsivevoice.org) · [Documentation](https://docs.responsivevoice.org) · [npm organization](https://www.npmjs.com/org/responsivevoice) · [Examples](https://github.com/responsivevoice/examples)
