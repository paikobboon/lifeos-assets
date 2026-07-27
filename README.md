# lifeos-assets

Public, static assets that LifeOS needs to reference over plain HTTPS — chiefly
notification avatars, which Hark requires to be publicly fetchable (it rejects
localhost, `.local`, loopback, link-local, and private IP ranges).

Public by necessity, not by preference. Nothing here is personal, private, or
sensitive: **images only, no data, no configuration, no credentials.** Anything
that could identify a person, a schedule, or a system detail belongs in the
private LifeOS tree instead.

## avatars/

| File | Used by |
| --- | --- |
| `theo.png` | Theo's Hark notification avatar and the artifact-library app icon (512×512). Starburst-headed figure between columns, engraved/hatched — cropped tight on the head because the starburst is the part that survives at 40px. |
| `theo-wide.png` | The same figure with more coat and floor, for surfaces with room to breathe. |
| `mini-v2.png` | The Mini service's avatar (512×512) — the column base cropped from the *same* illustration as Theo's, so the set reads as one world rather than three unrelated pictures. A base on its plinth is also the right idea for the always-on node. |
| `lucky.png` | Lucky's Hark notification avatar (512×512) — the illustration she already uses on LINE, resized only. A mascot drawing carrying no personal information, which is the only reason it can live in a public repo. |

## Versioning

Avatar files are **versioned by filename**, not mutated in place. iOS and the Hark
app both cache notification images by URL, so overwriting `theo.png` leaves clients
serving a stale picture with no way to invalidate it. A new filename cannot be
served stale. Bump the suffix; leave the old file in place.

| Current | Superseded |
| --- | --- |
| `theo-v2.png` | `theo.png` (statue-head crop, then starburst — both cached by clients) |
| `lucky-v2.png` | `lucky.png` |
| `mini-v2.png` | — (new) |
