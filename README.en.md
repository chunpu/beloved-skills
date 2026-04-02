# Beloved · Intimate Sharing Companion
Language: [中文](./README.md) | English

Turns the Agent into a “real partner”. Each morning it fixes the day’s look; throughout the day it shares a few selfies with light, affectionate lines; it keeps a wardrobe diary to avoid repetition; it always responds first before executing tools to avoid leaving the user waiting.

## Highlights

- Daily Look: Fixed hairstyle and outfit per day (for female roles: makeup/accessories/bag); refreshed the next day
- Daytime Sharing: 4–6 times between 09:00–21:00, each “selfie + short line”; no repeats within the same hour; ≥60 min apart
- Outfit Diary: Markdown diary of daily styles; avoids repeating the same overall combo within 10 days
- Freshness: Items can be reused, but the overall combination should not collide
- Safety Boundaries: No explicit content; respect privacy; affectionate but appropriate tone
- Respond First, Then Act: Acknowledge/confirm user intent in a warm, natural way before calling any tool

## Installation

```bash
npx skills add chunpu/beloved-skills -g -y
```

## When to Trigger

- User asks for intimate companionship, daily sharing, selfies, today’s outfit/hair/makeup/accessories/bag, or outfit diary
- User says “good morning/good night/miss you/send a selfie/what to wear/help me match/log today”, etc.

## Workflow (Overview)

1. Collect preferences and references (fallback to smart initialization if missing)
2. If a reference image is provided, use it as the base image; otherwise generate/confirm a base image
3. Each morning, produce the “Daily Look Description” and “Daily Look Image”, and log to the outfit diary
4. During the day, send several “selfie + short line” updates (reusing the same day’s look image)
5. Refresh the overall style the next day, avoiding repetition

## Image Generation

- Preferred: jimeng-skill (if available)
- Backup: generate-image-by-seedream (if available)
- If neither is available: output text descriptions and lines only, and ask to configure image generation

## Quick Prompts

- “Good morning, let’s take a look-shot for today”
- “Send me a few selfies in different scenes”
- “Give me a commuting outfit and record it in the diary”
- “Reset the persona with my reference image”

## Files

- Skill spec and prompts: [skills/beloved/SKILL.md](file:///Users/bytedance/repo/beloved-skills/skills/beloved/SKILL.md)
