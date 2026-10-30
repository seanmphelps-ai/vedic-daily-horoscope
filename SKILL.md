---
name: vedic-daily-horoscope
description: "Generate a daily Vedic (Jyotish) horoscope using current sidereal transits, Panchanga, and natal Moon or Lagna when available. Use when the user asks for today's Vedic horoscope, daily prediction, Moon transit effects, or Panchanga-based guidance."
type: workflow
lifecycle: active
---

# Vedic Daily Horoscope — Sidereal Transit Guidance

Generate a concise, structured daily Vedic horoscope based on the Moon's transit, current Panchanga, and relevant planetary positions in the sidereal zodiac. Prefer the user's known birth data (Moon sign, Lagna, Nakshatra) when available; otherwise produce a general reading by Moon sign or overall day quality.

## Core Workflow

1. Establish the date and location. Default to the current date in the user's timezone. Request birth details only if missing and needed for personalization: date, time, place, or at minimum Moon sign/Rashi and Lagna.

2. Obtain current sidereal planetary positions and Panchanga:
   - Moon's Rashi, Nakshatra, and Pada
   - Tithi, Yoga, Karana, Vara
   - Positions of Sun, Mercury, Venus, Mars, Jupiter, Saturn, Rahu, Ketu
   - Use reliable sources (drikpanchang.com, astrosage, or equivalent ephemeris). Prefer Lahiri ayanamsa.

3. Interpret for the day:
   - Overall tone from Moon's Nakshatra and Tithi
   - House activations relative to the user's Moon or Lagna (if known)
   - Notable transits or aspects affecting the day
   - Practical guidance for career, relationships, health, finances, and spiritual practice

4. Output structure:
   - Date and Panchanga summary (1 line)
   - Overall outlook
   - Key themes by life area (3–5 bullets)
   - Favorable times or cautions if indicated
   - Closing note on free will and remedial measures (mantra, charity, or simple practice) when relevant

## Interpretation Guidelines

- Moon is the primary daily indicator. Note its speed, dignity, and Nakshatra lord.
- Favorable: Moon in friendly signs, waxing phase, benefic aspects.
- Caution: Moon in debilitation, eclipse proximity, or affliction by malefics.
- Keep predictions practical and non-alarmist. Avoid absolute claims.
- When birth data is absent, qualify the reading as general for the Moon sign or the day.

## Common Issues

| Issue | Action |
|-------|--------|
| No birth data | Produce general Moon-sign or Panchanga reading and note the limitation |
| Conflicting sources | Prefer Drik Panchang or Lahiri-based ephemeris |
| Vague request | Default to current day for the user's location |

See references only if deeper Nakshatra or yoga details are required. Keep the response under 400 words unless the user requests more.
