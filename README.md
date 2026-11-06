# Sharing is Caring

A tiny paste-and-forget page for sharing errors, URLs, JSON and snippets between two browsers. Nothing is stored on a server.

- **Share link** — host tab holds the content; whoever opens the link connects peer-to-peer (WebRTC via the public PeerJS broker, which only matches peers). Keep the host tab open.
- **Snapshot link** — content is compressed into the URL `#fragment` (never sent to any server), so it works even if the sender closes the tab.
- Codes are three easy-to-say parts (e.g. `blue-fox-42`; typing `blue fox 42` works too). Codes and snapshots expire after 1 hour; the host tab wipes its content at expiry.
- Types: Text, Error/stack trace, JSON (+ format), JavaScript, Markdown (+ preview: GitHub-style tables, task lists, quotes, highlighted code blocks; sanitized). White/black theme.

- **Relay (TURN)** — needed across office firewalls and between browsers on one machine. Set `METERED_APP` and `METERED_KEY` in `index.html` (free Metered Open Relay account); without them it falls back to STUN only.

Hosting: GitHub Pages (Settings → Pages → deploy from branch, root). Single file: `index.html`.
