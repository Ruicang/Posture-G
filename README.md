# Posture Guard

**Sit up straight — without thinking about it.**

Posture Guard is a privacy-first macOS app that watches your posture through your
webcam — entirely on your Mac — and gently **dims your whole screen across every app**
when you slouch past your own calibrated baseline, until you sit back up.

<!-- Tip: drag a screenshot or short GIF here once you've created the repo. -->

## ⬇️ Download

**[Download Posture Guard for macOS](../../releases/latest/download/Posture-Guard-1.0.0-macOS-arm64.zip)** (~107 MB)
— or browse all versions on the **[Releases page](../../releases)**.

**Requirements**
- **Apple Silicon Mac** (M1 or later) — this build is Apple-Silicon only.
- **macOS 11 (Big Sur) or later.**
- A built-in or external **webcam**.

## First launch (please read)

Posture Guard is a free, independent app and isn't signed with a paid Apple Developer
certificate, so macOS blocks it the first time with a message like *"Posture Guard can't
be opened because Apple cannot check it for malicious software."* That's expected — here's
how to open it (you only do this once):

1. Unzip the download and move **Posture Guard.app** into your **Applications** folder.
2. Double-click it once. macOS blocks it — click **Done**.
3. Open **System Settings → Privacy & Security**, scroll to *"Posture Guard was blocked…"*,
   and click **Open Anyway**.
4. Click **Open** to confirm.

<details>
<summary>Prefer the Terminal? One command instead of steps 2–4</summary>

```bash
xattr -dr com.apple.quarantine "/Applications/Posture Guard.app"
```

Then open the app normally.
</details>

On first run, macOS asks for **camera permission** — that's the system prompt. Your video
is processed locally and never leaves your Mac.

## How it works

1. **Align** — a live camera view with trackers that snap onto your eyes/ears (or nose)
   and your shoulders. Pick whichever head anchor tracks you most reliably.
2. **Calibrate** — sit up straight and tall, press **Start**, and hold for 3 seconds. That
   becomes your personal baseline.
3. **Monitor** — work normally. If you slouch past your baseline for a few seconds, the
   whole screen gently dims (over every app and Space) and deepens the longer it's ignored.
   Sit back up and it fades away.

Tune the **sensitivity** and **dim intensity**, **Snooze** for 15 minutes, or turn on
**Flow State** to pause checks while you're actively typing. Quit anytime from the
menu-bar icon, the Dock, or ⌘Q.

## Privacy

100% on-device. Webcam frames are read straight into an on-device pose model
(Google MediaPipe) and are **never stored or uploaded**. No account, no cloud, no tracking.

---

*Posture Guard is provided free and as-is, with no warranty.*
