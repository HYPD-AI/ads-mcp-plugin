# Known failure modes and how to avoid them

The validation errors HYPD sees most, by tool family. Respecting these saves
a failed round trip; when a tool still errors, report the error — never
invent data the tool did not return.

## Google Ads (`google_ads_run_gaql`)

- **`change_event` queries REQUIRE both** a `change_date_time` filter within
  the **last 30 days** and a `LIMIT` clause. Older change history does not
  exist in the API — say so instead of retrying wider ranges.
- Account IDs are 10 digits, dashless (`2712366093`, never `271-236-6093`).
- Standard GAQL only: no `OR` across fields, no parentheses in WHERE, no
  `SELECT *`. Metrics must be compatible with the `FROM` resource — e.g.
  conversion values segment via `segments.conversion_action` on `campaign`,
  not `FROM conversion_action`.
- Date literals: `BETWEEN 'YYYY-MM-DD' AND 'YYYY-MM-DD'`; `LAST_90_DAYS` is
  not a valid range keyword.

## Google Analytics 4

- **Realtime reports cannot combine most dimensions with metrics** — keep
  realtime requests minimal rather than mirroring a standard report.
- Exactly one filter object per request where the schema says so — do not
  pass an empty `dimensionFilter`.

## Research tools (SERP, keywords)

- Always pass a country and a language; use standard names (`Germany`,
  `German`) — invented `location_name`/`language_name` values are the most
  common research-tool failure.
- Pass `itemTypes` explicitly on SERP requests (e.g. `["organic"]`).

## LinkedIn Ads

- Call LinkedIn tools **one at a time, never in parallel**.
- `endDate` on the Ad Library is exclusive — for one day, pass the next day.

## General

- Everything is read-only: no HYPD tool can change anything in a connected
  platform — state what the data shows, never that an action was taken.
- Cap list-style requests (top 5/10) so responses stay fast.
