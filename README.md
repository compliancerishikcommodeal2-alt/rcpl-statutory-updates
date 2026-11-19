# RCPL Statutory Updates

PAN India statutory and labour-law notifications published by **Rishik Commodeal Pvt. Ltd. (RCPL)**, Kolkata.
The Statutory Updates page on rishikcommodeal.com reads `notifications.json` from this repository, so anything committed here appears on the website automatically.

## File: `notifications.json`

```json
{
  "updated": "YYYY-MM-DD",
  "categories": ["Labour Codes", "Provident Fund", "..."],
  "notifications": [
    {
      "id": "YYYY-MM-DD-state-short-title",
      "date": "YYYY-MM-DD",
      "category": "one of categories",
      "state": "Central | state / UT name",
      "title": "Short title",
      "summary": "2-4 sentences in RCPL's own words",
      "effective": "YYYY-MM-DD or text",
      "source": "Issuing authority / gazette",
      "url": "Link to the official notification"
    }
  ]
}
```

## Rules
- Newest notifications first; `id` must be unique.
- Summaries are written by RCPL; third-party trackers are used only to discover notifications, never copied.
- Each notification is verified against an official or second source before it is added.
- Update `updated` whenever the file changes.

Updated every working day (Mon–Sat, IST).
