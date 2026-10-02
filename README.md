# Sharing is Caring

A tiny paste-and-forget page for sharing errors, URLs, JSON and snippets between two browsers. Nothing is stored on a server.

- **Share link** — host tab holds the content; whoever opens the link connects peer-to-peer (WebRTC via the public PeerJS broker, which only matches peers). Keep the host tab open.
- **Snapshot link** — content is compressed into the URL `#fragment` (never sent to any server), so it works even if the sender closes the tab.
- Codes and snapshots expire after 1 hour; the host tab wipes its content at expiry.
- Types: Text, Error/stack trace, JSON (+ format), JavaScript, Markdown (+ preview). White/black theme.

Hosting: GitHub Pages (Settings → Pages → deploy from branch, root). Single file: `index.html`.
