# SYNC

**A motor-skills measurement tool that looks like a very calm game.**

**Try it:** https://alyzaabdullah.github.io/sync/
Best on a tablet. Tilt needs a real motion sensor, so on a laptop it will just sit there looking pretty.

## The problem

At the moment, if you want to know how a child's motor skills are changing, the usual answer is a standardized assessment like the BOT-2 (now the BOT-3). These are good tests. But they take 45 to 60 minutes with a trained examiner and a kit that costs hundreds of dollars, so in practice a child gets tested months apart, often once before an intervention and once after. Everything that happens in between is a blur.

SYNC is my attempt at filling in the blur. It uses short, play-based sessions that measure the same things the same way every time, so a child's progress can be tracked continuously, alongside whatever intervention they're getting.

## What the child sees

A dark, starry screen and a little light. They tilt the tablet to guide the light onto a target, in time with a soft beat, and hold it there for a moment. That's it.

Misses are never punished. There's no red, no sad sounds, no "try again", and no scores on screen. The child is just playing, and the measuring happens quietly in the background.

## What SYNC measures

Every trial is recorded at the device's own sensor rate, with real timestamps:

| Measure | What it tells you |
|---|---|
| Hit rate | How often the child reached the target and held it there (350 ms) |
| Target accuracy | How close they got to the centre of the target, recorded even on trials they never finished |
| Re-entries and time in target | How steadily they stay on a target once they reach it |
| Reaction time | Time from the scheduled beat to the start of movement |
| Movement time | Time from the start of movement to first entering the target (the classic Fitts measure) |
| Beat offset | How far off the beat they arrived. How much this varies is the timing and synchronization measure |
| Task difficulty | A Fitts index of difficulty for every trial, so harder and easier trials can be compared fairly |
| Raw motion | The full tilt trajectory, plus the accelerometer and gyroscope streams |

Smoothness (based on jerk) and path efficiency are calculated from the raw motion streams during analysis, after resampling them onto an even time grid. Taking derivatives of an unevenly sampled signal makes the noise much worse, which is why everything gets logged raw first.

The therapist screen exports everything as JSON or CSV.

## Who sees what

- **The child** just plays. There's no login, no permission pop-up and no numbers.
- **The therapist** sets up the session behind a PIN (demo PIN: `1234`), does the quick sensor calibration, and sees the session data and a plot of the trajectory.

## Where it's going

The goal is a standardized measure, and a tool only gets to call itself that once it has earned it. Next steps:

- Fixed, documented protocols, so every session can be compared directly
- Test-retest reliability: does the same child get the same numbers on different days?
- Validity: do SYNC's measures line up with established assessments like the BOT?
- Reference data across ages, so a single result means something on its own

SYNC was designed with autistic children with dyspraxia (developmental coordination disorder) in mind, and should work for any child who finds coordination tricky.

## Privacy

SYNC runs entirely in the browser. There are no accounts and no server, and nothing is sent anywhere. Session data stays on the device until the therapist exports it.

## Status

Research prototype. No data has been collected from children yet. That will only happen after research-ethics approval.

---

Built by Alyza Abdullah, McGill University
