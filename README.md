# Street Crime Map UK – open data

Processed open data used by the Street Crime Map UK iOS app. No user data is ever stored here.

## Files (published at https://chigz90.github.io/streetcrimemapuk-data/)

- `flood_history.json.gz` – for each Environment Agency flood warning/alert area (keyed by its area code, e.g.
  `063WAT232S`): warnings per year by severity (flood alert / flood warning / severe flood warning), totals,
  first and most recent dates, and the 20 most recent events (date and severity).
- `manifest.json` – version, the date of the latest event (`dataUpTo`), when it was generated, the source file
  date, size, SHA-256 and schema version. The app downloads the summary only when `version` increases.

Built monthly (only when the source changes) by `Tools/FloodHistory/build_flood_history.py` from the Environment
Agency's **Historic Flood Warnings** dataset (AfA435), which lists flood alerts, flood warnings and severe flood
warnings issued since 26 January 2006 for England. "Update …" re-issues aren't counted as new events, and the
pre-2011 "Flood Watch" is counted as a flood alert.

## Attribution and licence

Contains Environment Agency information © Environment Agency and/or database right. Licensed under the
[Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).

Source: [Historic Flood Warnings on data.gov.uk](https://www.data.gov.uk/dataset/d4fb2591-f4dd-4e7f-9aaf-49af94437b36/historic-flood-warnings2).

No record of flooding doesn't mean an area has never flooded – only that the Environment Agency has no record of
it. Flood warnings are issued for whole warning areas, not individual properties.
