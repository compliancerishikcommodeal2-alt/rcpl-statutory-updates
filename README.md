# RCPL Statutory Updates

Live data for the **Statutory Updates** page on [rishikcommodeal.com](https://rishikcommodeal.com/statutory-updates.html).

The page reads `notifications.json` from this repository each time someone opens it, so anything added here appears on the website within a few minutes, with no change to the website files.

## How it is updated

A scheduled job runs every working day (Monday to Saturday). It looks for new central and state labour-law notifications across India and adds them to `notifications.json`:

- It finds candidates on Simpliance's notification pages, EPFO and ESIC circulars, the Ministry of Labour and Employment, state labour departments and the e-Gazette.
- It confirms each one against the official notification or a second reliable source.
- It writes a short summary in RCPL's own words. Text from other sites is never copied.
- It adds the entry, updates `updated`, and commits the change.

You can also edit `notifications.json` by hand on GitHub (pencil icon, then **Commit changes**).

## File format

```json
{
  "updated": "2026-11-19",
  "categories": ["Labour Codes", "Provident Fund", "ESIC", "Trade Licence", "..."],
  "notifications": [
    {
      "id": "2026-11-04-bihar-minimum-wages-revised-with-vda",
      "date": "2026-11-04",
      "category": "Minimum Wages",
      "state": "Bihar",
      "title": "Minimum wages revised with VDA under the Code on Wages",
      "summary": "Two to four plain sentences: what changed, for whom, key figures.",
      "effective": "1 October 2026",
      "source": "TeamLease RegTech",
      "url": "https://..."
    }
  ]
}
```

| Field | Rules |
|---|---|
| `id` | Date, state and a short slug of the title. Must be unique. |
| `date` | Date the notification was issued or released, `YYYY-MM-DD`. |
| `category` | One of the names in `categories`. |
| `state` | `Central` for Government of India, EPFO, ESIC and Labour Bureau; otherwise the full state or UT name, e.g. `West Bengal`. |
| `title` | Short plain-English headline, under about 90 characters. |
| `summary` | RCPL's own words, 2 to 4 sentences, with the figures employers need. |
| `effective` | Effective date, or `As notified` / `Draft stage` if not stated. |
| `source`, `url` | Where to read more: the official notification where possible. |

Keep the list newest first. The website sorts by `date` anyway, so order mistakes do no harm.
