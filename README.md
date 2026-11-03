# SkippHelp

Android start-sequence timer for sailing/foiling races: a big countdown
clock that switches to a stopwatch (`Chronometer`) once the race starts,
with a beep in the final second, alongside readouts for speed, VMG and
rig weight.

## Features

- Countdown timer (start / pause / reset) with large auto-sizing digits
- Automatic switch to an elapsed-time chronometer when the countdown ends
- Audio cue in the last second before start
- Static data row for speed (kn), VMG and rig/crew weight (kg) — currently
  placeholder values, not wired to a live sensor feed

## Stack

- Java, single-activity Android app (minSdk per `build.gradle.kts`)
- `CountDownTimer` + `Chronometer` (Android framework, no external deps)

## Build

```bash
./gradlew assembleDebug
```

Open in Android Studio and run on a device/emulator.

## Status / possible next steps

- Countdown length is hardcoded (`START_TIME_IN_MILLIS`) — not yet
  configurable from the UI.
- Speed/VMG/weight fields are static text, not backed by real data.
