# KUBESTANUT — SS Komodor

> **An interactive Kubernetes SRE simulation game by [Komodor](https://komodor.com)**

You are the captain of the SS Komodor — a deep-space vessel running on Kubernetes. An incident has just fired. Your crew is counting on you to investigate the logs, identify the root cause, apply the fix, and restore power before the ship goes dark.

Oh, and you have an AI on board. Her name is Klaudia.

---

## Play Now

👉 **[Launch the game](https://kentchance.github.io/TOF_BETA_TESTING/)**

No install. No signup. Opens in any modern browser.

---

## Why We Built This

Kubernetes incidents are hard to explain to people who haven't been paged at 2am. This game puts you through a real incident response workflow — the same one your SRE team runs every time something breaks in production — so you can feel the difference between doing it manually and doing it with an AI SRE by your side.

The twist: your first run has no AI assistance. Your second run, Klaudia is online. The end screen shows you exactly how much faster you were and projects that delta onto a real-world 45-minute MTTR.

---

## How It Works

The game follows the same phases as a real Kubernetes incident response:

### Phase 1 — Root Cause Analysis
Browse cluster logs across five ship systems. One system is showing an active incident. Identify it, read the logs, and confirm your RCA before moving on.

### Phase 2 — Troubleshoot
Pick the correct `kubectl` command to address the root cause. Wrong answers trigger a fault — pick carefully.

### Phase 3 — Remedy
Apply the fix and restore the affected system to a healthy state.

### Phase 4 — Power Optimization
The remediation triggered a power surge. Redistribute CPU and Memory allocation across all five ship systems to bring everything back within optimal range.

---

## Klaudia — The Ship's AI SRE

Klaudia is locked out on your first playthrough. You run the incident solo so there's a real baseline to compare against.

On your second playthrough she comes online automatically. Here's what she does:

- **Reads the logs** and produces a structured analysis — Timeline, Evidence, Related Changes, and a one-click Remediation block
- **Highlights suspicious log lines** so you know exactly where to look
- **Applies remediation for you** and skips straight to the power phase
- **Auto-optimizes** CPU and Memory allocation across all five systems

When you finish the second run, the game shows you a side-by-side comparison of your two times and calculates what that speed improvement would mean on a real 45-minute production incident.

---

## Incident Scenarios

Three scenarios are in rotation, selected randomly each run:

| Incident | Description |
|---|---|
| **OOMKill (Exit 137)** | A container blows past its memory limit and gets killed. Pods are crash-looping. |
| **ImagePullBackOff** | A CD pipeline pushed a deployment referencing an image tag that was never pushed to the registry. |
| **CPU Throttle** | CPU requests were set too high after a config change. Pods are stuck Pending — no node has capacity to schedule them. |

---

## The Point

Klaudia isn't a game character. She's a real AI SRE built into the Komodor platform that works inside your actual Kubernetes estate — reading your real logs, surfacing real RCAs, and cutting your real MTTR.

This game is a 5-minute way to feel what that looks like before you ever see a live cluster.

**[Book a demo with our team →](https://komodor.com/contact-sales/)**

---

## Technical Notes

- Single-file HTML5 Canvas application — `index.html` is the entire game
- No frameworks, no build pipeline, no backend
- All game state is held in memory and `localStorage`
- Runs in any modern browser directly from the file system or a static host
