# RCPL Statutory Updates

PAN India statutory and labour-law notifications published by **Rishik Commodeal Pvt. Ltd. (RCPL)**, Kolkata.
The Statutory Updates page on rishikcommodeal.com reads `notifications.json` from this repository, so anything committed here appears on the website automatically.

## Files

- `notifications.json` – the notification list (data format version 2).
- `copies/<id>.pdf` – a downloadable copy of each notification. The website's **Download** button points here for any notification that is not bundled with the website itself.

## Format of `notifications.json`

```json
{
  "version": 2,
  "updated": "YYYY-MM-DD",
  "categories": ["Labour Codes", "Provident Fund", "..."],
  "notifications": [
    {
      "id": "YYYY-MM-DD-state-short-title",
      "date": "YYYY-MM-DD",
      "category": "Provident Fund",
      "jurisdiction": "Central | State",
      "state": "Central | <State name>",
      "title": "...",
      "summary": "RCPL's own summary",
      "effective": "text shown on the card",
      "effective_date": "YYYY-MM-DD or empty",
      "authority": "Issuing authority",
      "notification_no": "...",
      "url": "official source (kept for reference, not shown as a link)",
      "url_type": "pdf | page",
      "copy_type": "official | rcpl"
    }
  ]
}
```

- `copy_type: "official"` – `copies/<id>.pdf` is the government's own PDF.
- `copy_type: "rcpl"` – the official portal could not be reached when the item was added, so `copies/<id>.pdf` is an RCPL-letterhead summary. Replace it with the official PDF when available and change `copy_type` to `official`.

## Rules

- Official government sources only. Summaries are written in RCPL's own words.
- Newest notifications first.
- Large official gazettes bundled with the website (Bihar Gazette 22 Jul 2026 and the two Uttarakhand Labour Code rules of 24 Sep 2026) are served from the website and are not duplicated here.

Rishik Commodeal Pvt. Ltd., Rishi Tech Park, Office E4, 5th Floor, New Town, Kolkata 700156 · +91 97485 31156 · debraj@rishikcommodeal.com
