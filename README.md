# Stadium Events Data

Static JSON/JSONL dataset of sports events (schedules + results).

## Layout
- `events/{sport}/{season}/{YYYY}/{MM}/{YYYY-MM-DD}.jsonl` — one JSON object per line
- `indexes/dates/{YYYY-MM-DD}.json` — list of event IDs for a date
- `indexes/seasons/{sport}/{season}.json` — list of event IDs for a season
- `entities/venues/*.json` — normalized venue metadata

## Schema
See `/schema/*.json`. Each line in an events JSONL file validates against:
- team-vs-team: `event.team.schema.json`
- multi-entry (golf/racing): `event.multi.schema.json`
