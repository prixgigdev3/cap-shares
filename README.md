# Cap Shares

Loom-style public links for videos recorded with [Cap](https://github.com/CapSoftware/Cap).

Each recording gets a GitHub Pages player URL:

```
https://prixgigdev3.github.io/cap-shares/v/<id>/
```

The MP4 itself is stored as a GitHub Release asset, so files can be larger than GitHub’s git-file limit.

## Record, then share

1. Open **Cap** (`/Applications/Cap.app`) and grant Screen Recording (and mic/camera if you need them).
2. Record in Instant or Studio mode. Export an `.mp4` from Studio, or share a `.cap` project folder.
3. Publish:

```bash
share-cap ~/Desktop/my-recording.mp4 --title "Checkout flow bug"
```

or the newest Cap library recording:

```bash
share-cap --latest --title "Walkthrough"
```

The command prints three GitHub URLs: the player page, the release, and the raw MP4.

## Install notes (this machine)

- Cap Desktop **0.6.2** is in `/Applications/Cap.app`
- Cap CLI shim: `~/.local/bin/cap` → bundled `cap-cli`
- Publisher: `~/.local/bin/share-cap` → `~/Sites/cap-shares/scripts/share-cap`

Cap’s own `cap upload` still sends files to Cap Cloud (`cap.so`). `share-cap` is the GitHub path.

## Privacy

This repository is **public**. Anyone with the link can watch. Do not publish recordings that should stay private.
