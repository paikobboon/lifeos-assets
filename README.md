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
| `lucky.png` | Lucky's Hark notification avatar (512×512) — the illustration she already uses on LINE, resized only. A mascot drawing carrying no personal information, which is the only reason it can live in a public repo. |
