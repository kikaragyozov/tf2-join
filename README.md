# tf2-join

A tiny **static** `steam://connect` redirect page for the TF2 lobby bot, hosted free on GitHub Pages.

The bot's lobby "Join" buttons link here:

    https://kikaragyozov.github.io/tf2-join/#<host:port>/<password>

This page reads the address from the URL **fragment** (`#…`) — which browsers never send to any
server — and hands your own Steam client a `steam://connect/<host:port>/<password>` link.
One click → Steam launches and joins.

**No secrets live here.** This repo is a generic redirector: no server address, no password, no bot
code. The connect details only ever exist in the link the bot generates, inside your browser. That is
why it is safe to be public — and public means free GitHub Pages.

Formats:
- `#host:port`           → `steam://connect/host:port`            (e.g. SourceTV, no password)
- `#host:port/password`  → `steam://connect/host:port/password`
