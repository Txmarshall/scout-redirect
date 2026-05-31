# scout-redirect

A tiny static page that relays an https click to an `obsidian://` deep link, because some mail
clients strip custom URL schemes from HTML email but allow `https`.

**Contract:** `GET /?v=<vault name>&f=<vault-relative note path, no .md>` rebuilds
`obsidian://open?vault=<v>&file=<f>` and navigates to it (with a manual "Open in Obsidian" button
fallback). Fully static, no dependencies, stores nothing — parameters ride in the query string at
click time only.
