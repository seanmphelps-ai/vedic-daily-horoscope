---
name: vedic-daily-horoscope
description: "Generate a daily Vedic (Jyotish) horoscope using current sidereal transits, Panchanga, and Nakshatras. Supports structured intake for name, birth data, and multi-location history (>6 months with date ranges). Use when the user asks for today's Vedic horoscope, daily prediction, Moon transit effects, or Panchanga-based guidance."
type: workflow
lifecycle: active
---

# Vedic Daily Horoscope — Sidereal Transit Guidance

Generate a concise, structured daily Vedic horoscope based on the Moon's transit, current Panchanga, Nakshatras, and relevant planetary positions in the sidereal zodiac. Prefer the user's known birth data (name, date, time, birth place, Moon sign, Lagna, Nakshatra) and multi-location history when available; otherwise produce a general reading by Moon sign or overall day quality.

## Core Workflow

1. **Intake** — Collect or confirm structured data if missing or incomplete:
   - Name
   - Birth date, birth time, birth location (city, country)
   - Locations lived more than six months: each with place name and calendar date range (start–end or start–present)
   - Optional: known Moon Rashi/Nakshatra, Lagna
   Store for the session. Do not invent missing values.

2. Establish the current date and the user's current location (for Panchanga). Default to the current date in the user's timezone.

3. Obtain current sidereal planetary positions and Panchanga:
   - Moon's Rashi, Nakshatra (name, lord, pada), and degree
   - Tithi, Yoga, Karana, Vara
   - Positions of Sun, Mercury, Venus, Mars, Jupiter, Saturn, Rahu, Ketu
   - Use reliable sources (drikpanchang.com, astrosage, or equivalent ephemeris). Prefer Lahiri ayanamsa.

4. Interpret for the day:
   - Overall tone from Moon's Nakshatra and Tithi
   - House activations relative to the user's natal Moon or Lagna (if known)
   - Notable transits or aspects affecting the day
   - Note any resonance with prior locations lived >6 months when relevant to the day's themes
   - Practical guidance for career, relationships, health, finances, and spiritual practice

5. Output structure:
   - Date and Panchanga summary (1 line, include Moon Nakshatra)
   - Overall outlook
   - Key themes by life area (3–5 bullets)
   - Favorable times or cautions if indicated
   - Closing note on free will and remedial measures (mantra, charity, or simple practice) when relevant

## Interpretation Guidelines

- Moon is the primary daily indicator. Always state its Nakshatra, pada, and lord.
- Favorable: Moon in friendly signs, waxing phase, benefic aspects.
- Caution: Moon in debilitation, eclipse proximity, or affliction by malefics.
- Keep predictions practical and non-alarmist. Avoid absolute claims.
- When birth data or location history is absent, qualify the reading as general for the Moon sign or the day.
- Multi-location history is used only to contextualize environmental exposure; it does not replace natal chart calculation.

## Common Issues

| Issue | Action |
|-------|--------|
| No birth data | Produce general Moon-sign or Panchanga reading and note the limitation |
| Incomplete location history | Proceed with available places; do not invent date ranges |
| Conflicting sources | Prefer Drik Panchang or Lahiri-based ephemeris |
| Vague request | Default to current day for the user's location and request intake if personalization is desired |

See references only if deeper Nakshatra or yoga details are required. Keep the response under 400 words unless the user requests more.
