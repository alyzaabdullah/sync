# SYNC

**Calm, rhythm-cued motor practice for children who struggle with coordination.**

▶ **Try it:** https://alyzaabdullah.github.io/sync/ (best on a tablet; tilt needs a phone or tablet with a motion sensor)

SYNC is a tablet game for motor-planning practice. It was designed for autistic children with dyspraxia (developmental coordination disorder), and it can help any child who finds coordination hard. The child tilts the tablet to guide a light onto a target in time with a calm beat, then taps to commit.

## Design principles
- **Errorless.** Hits get a soft chime and a visual bloom. Misses are never punished: no red, no sad sounds, no "try again".
- **Child and therapist are separate.** The child just plays. The therapist sets up the session behind a PIN (demo PIN: `1234`), does the sensor setup so the child never sees a permission dialog, and sees the session data.
- **Calm and predictable.** Low-stimulation palette, a break screen the child can open at any time.

## What it measures
Each trial records the timestamped tilt trajectory, as well as hit/miss and timing. The therapist can export the session as JSON or CSV. The child never sees scores.

## Privacy
Everything runs in the browser. There are no accounts and no server, and nothing is sent anywhere. Session data stays on the device until the therapist exports it.

## Status
Prototype for research use. It has not been used to collect data from children; that will only happen after research-ethics approval.

---
Built by Alyza Abdullah · McGill University
