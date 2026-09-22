# MiniMax

MiniMax is the Shanghai AI lab behind the Hailuo video models, the Speech and Music APIs and the M-series language models.

> **Try MiniMax online →** [https://kyncept.com/video/pro](https://kyncept.com/video/pro?utm_source=github&utm_medium=ugc&utm_campaign=minimax-official&utm_content=readme-top&utm_term=tier-b)

MiniMax is a Shanghai-based AI company founded in late 2021 by former SenseTime researchers. Outside China it is best known for Hailuo, its video generation model, which went viral in September 2024 as video-01 and has since been updated through Hailuo 02 and Hailuo 2.3; inside China it also runs the consumer apps Talkie and Xingye and the Hailuo AI creative app. The company listed on the Hong Kong Stock Exchange in January 2026, one of the first of the large Chinese model labs to go public.

MiniMax is unusual among the model labs in that it ships a full stack of modalities under one API. The video line offers 768p and 1080p clips of 6 or 10 seconds with subject-reference and first-and-last-frame control; the Speech line (Speech-02 and later) is one of the highest-rated text-to-speech systems on public arenas, with voice cloning from a few seconds of audio and more than thirty languages; the Music line generates full songs with vocals from lyrics; and the Image-01 model handles stills. Alongside these closed models the company publishes open-weight language models, MiniMax-Text-01, M1 and the M2 series, which are aimed at long-context and agentic coding use.

In the video market Hailuo competes directly with Kuaishou Kling, ByteDance Seedance, Google Veo 3 and OpenAI Sora 2. Its reputation is for motion realism and physically plausible action at a low price per clip, and Hailuo 02 briefly held the top spot on public image-to-video leaderboards at launch. It does not yet generate audio with the video, which is the main gap against Veo 3, Sora 2 and Kling 2.6.

## Contents

- [What MiniMax can do](#what-minimax-can-do)
- [Versions](#versions)
- [How to access MiniMax](#how-to-access-minimax)
- [Prompt examples](#prompt-examples)
- [MiniMax vs alternatives](#minimax-vs-alternatives)
- [Pricing](#pricing)
- [FAQ](#faq)
- [Links](#links)

## What MiniMax can do

- Hailuo video: text-to-video and image-to-video at 768p or 1080p, in 6 or 10 second clips, with landscape and portrait framing.
- Subject reference (S2V): supply a photo of a person and keep that face consistent across the generated clip.
- First-and-last-frame control in Hailuo 02 and later, so a clip starts on one image and ends on another.
- Director-style camera commands written in square brackets inside the prompt, such as [Pan left], [Zoom in], [Tracking shot] and [Static shot], which the model parses into camera motion.
- MiniMax Speech: text-to-speech in more than thirty languages with emotion control, streaming output and voice cloning from a short reference sample.
- MiniMax Music: full-length songs with vocals and instrumentation generated from lyrics and a style description.
- Image-01: text-to-image with subject reference for consistent characters.
- M-series language models: open-weight MiniMax-M1 and M2 with contexts up to one million tokens, positioned for coding agents and tool use, and also served through the MiniMax API.

Known limitations: Hailuo does not generate audio with the video, so sound has to be added separately; each generation is capped at 10 seconds and 1080p is not available at every length; readable text inside the frame is unreliable; hands, fast multi-person action and long camera moves can still deform; the content filter blocks violent, sexual and some real-person prompts; and the international and China platforms are separate services with separate accounts, billing and model availability.

## Versions

| Version | Released | Notes |
|---|---|---|
| video-01 (Hailuo) | 2024-09 | First public text-to-video model; 720p 6 second clips that went viral for motion realism |
| MiniMax-Text-01 / VL-01 | 2025-01 | Open-weight 456B-parameter language and vision-language models with lightning attention and a 4 million token context |
| Hailuo 02 (MiniMax-Hailuo-02) | 2025-06 | 1080p output, 6 or 10 second clips, first-and-last-frame control; ranked near the top of public image-to-video leaderboards at launch |
| MiniMax-M2 | 2025-10 | Open-weight 230B mixture-of-experts language model with about 10B active parameters, aimed at coding agents; followed by M2.1 and later point releases |
| Hailuo 2.3 | 2025-10 | Improved motion realism, physics and stylised output, plus a Fast variant for cheaper generation |

## How to access MiniMax

MiniMax's video, speech, music and image models are closed and hosted. The official ways to use them are:

- The Hailuo AI web app (hailuoai.video for the international edition, hailuoai.com for China), which offers free daily credits and paid subscription tiers for video and image generation.
- MiniMax Audio and MiniMax Agent, the company's web products for speech generation and agentic tasks.
- The MiniMax open platform API (platform.minimax.io internationally, platform.minimaxi.com in China), which exposes the Hailuo video models, Speech, Music, Image-01 and the M-series language models on pay-as-you-go billing.
- Third-party platforms: Hailuo is available on fal.ai and Replicate, and the M-series language models on OpenRouter and similar routers.

The international and China platforms are separate services with separate accounts, and new model versions sometimes appear on one before the other. Free credits on the web app reset daily and free generations are watermarked and queued. If you want to generate a Hailuo clip without a subscription or API setup, [MiniMax](https://kyncept.com/video/pro) offers pay-per-generation access in the browser with no waitlist.

**Fastest way to try it:** [Try MiniMax online](https://kyncept.com/video/pro?utm_source=github&utm_medium=ugc&utm_campaign=minimax-official&utm_content=readme-access&utm_term=tier-b) — no waitlist, runs in the browser.

## Prompt examples

**Camera command showcase**

```text
[Truck left, Pan right] A street vendor flips noodles in a flaming wok at a night market in Taipei, steam and sparks rising, lanterns glowing overhead, crowd blurred in the background, cinematic 24fps look
```

**Subject reference portrait**

```text
The person in the reference image walks through a sunlit wheat field toward the camera, wind moving the wheat and their hair, [Tracking shot] keeping the face centred and consistent, warm late-afternoon light, shallow depth of field
```

**Physics and action**

```text
A glass of orange juice tips over on a white kitchen table in slow motion, liquid arcs through the air and splashes across the surface, droplets catching the morning light, [Static shot] at table level, photorealistic
```

**First-and-last-frame transition**

```text
First frame: a caterpillar on a green leaf. Last frame: a monarch butterfly on the same leaf with wings open. In between, a time-lapse of the chrysalis forming and the butterfly emerging, macro lens, soft diffused light, [Zoom in] slowly
```

**Stylised animation**

```text
A 3D animated corgi in a tiny astronaut suit bounces across the lunar surface, Earth rising over the horizon, dust puffs with each hop, Pixar-style lighting and materials, [Pan right] following the dog
```

## MiniMax vs alternatives

| Model | Max resolution / duration | Native audio | Editing and reference support | Access | Price tier |
|---|---|---|---|---|---|
| MiniMax Hailuo 2.3 | 1080p, 6 or 10 s | No | Subject reference, first/last frame, bracketed camera commands | Hailuo web app, MiniMax API, fal.ai, Replicate | Low |
| Kling 2.6 / 3.0 (Kuaishou) | 1080p, 10 s, extendable to about 3 min | Yes (2.6 onward) | Start/end frame, Elements references, Motion Brush, lip sync, multi-shot | Kling web app, API, fal.ai | Low to mid |
| Google Veo 3 / 3.1 | 1080p (4K in some tiers), 8 s | Yes, including dialogue | Reference images, first/last frame, extend | Gemini app, Flow, Vertex AI API | Mid to high |
| OpenAI Sora 2 | Up to 1080p-class, 4 to 12 s via API | Yes, including dialogue | Image input, Remix, Cameos | Sora app, sora.com, OpenAI API | Mid to high |
| ByteDance Seedance 1.0 | 1080p, 5 to 10 s | No (1.0) | Multi-shot, image reference | Dreamina, Volcano Engine API, fal.ai | Low to mid |

Hailuo's case is motion realism at a low price: on image-to-video tasks with a single subject and a clear action it produces some of the most physically convincing clips of any model, and the bracketed camera syntax makes framing more predictable than free-text prompting. It loses to Veo 3, Sora 2 and Kling 2.6 the moment sound matters, since audio has to be added afterwards, and Kling offers more control tools for production work. For cheap, silent, realistic clips from a still image, Hailuo is usually the first model to try.

## Pricing

As of the last public information, the Hailuo AI web app runs on credits: every account receives free credits each day, and paid tiers add monthly credit allowances, remove the watermark, unlock 1080p and faster queues, with an unlimited relaxed-mode option on the higher plan. Video generations cost more credits at 1080p and at 10 seconds than at 768p and 6 seconds.

The MiniMax API is pay-as-you-go: video is billed per clip by resolution and length, Speech is billed per character of input, Music per track, and the M-series language models per million tokens, with MiniMax-M2 launched at roughly $0.30 per million input tokens and $1.20 per million output tokens. The official platform pricing pages are the only authoritative source and rates change with each release. For occasional video clips, pay-per-generation access such as the [MiniMax](https://kyncept.com/video/pro) link on this page avoids both a subscription and API setup.

## FAQ

**What is MiniMax?**

MiniMax is a Shanghai-based AI company that builds the Hailuo video generation models, the MiniMax Speech and Music models, the Image-01 image model and the open-weight M-series language models. Outside China it is known mainly for Hailuo, which produces 6 or 10 second clips at up to 1080p.

**Is MiniMax free?**

Partly. The Hailuo AI web app gives every account free daily credits, but free generations are watermarked, queued and limited in resolution. Paid subscriptions and the pay-as-you-go API remove those limits, and the M-series language model weights can be downloaded and run for free.

**Is there a MiniMax API?**

Yes. The MiniMax open platform exposes the Hailuo video models, Speech, Music, Image-01 and the M-series language models on pay-as-you-go billing, with separate international and China endpoints. Hailuo is also available through fal.ai and Replicate.

**Does MiniMax have an official GitHub repository?**

Not for its video, speech, music or image models, which are closed and available only through the company's products and API. MiniMax does publish its open-weight language models such as M1 and M2 on GitHub; this page is an independent collection of public information about the closed models.

**How do I try MiniMax online?**

The official route is the Hailuo AI web app, which needs an account and gives daily free credits. The fastest route without a subscription or waitlist is https://kyncept.com/video/pro, which offers pay-per-generation access in the browser.

**What are the limits?**

Hailuo clips are 6 or 10 seconds at 768p or 1080p and contain no audio, so sound must be added separately. Text inside the frame is unreliable, fast multi-person action can deform, the content filter blocks violent, sexual and some real-person prompts, and the international and China platforms are separate services.

**What is the difference between MiniMax and Hailuo?**

MiniMax is the company; Hailuo is the brand name of its video generation models and of the Hailuo AI creative app. Model IDs such as video-01, MiniMax-Hailuo-02 and Hailuo 2.3 all refer to generations of the same video line.

## Links

- [MiniMax official site](https://www.minimax.io)
- [Hailuo AI video app](https://hailuoai.video)
- [MiniMax open platform (API)](https://platform.minimax.io)
- [MiniMax open-weight models on GitHub](https://github.com/MiniMax-AI)
- [Try MiniMax online](https://kyncept.com/video/pro)

---

*This is an independent, community-maintained information repository about MiniMax. It is not affiliated with, endorsed by, or sponsored by MiniMax. All trademarks belong to their respective owners. Corrections welcome via issues.*



_Last reviewed: 2026-09-22_
