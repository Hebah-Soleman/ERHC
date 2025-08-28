
![Banner](logos/sp.jpg)

# Event-Recognition & Highlight Clipping ⚽

## Short highlights + a live mini-map for every key moment.

This project enhances the sports viewing experience by automatically spotting key events in full match videos, clipping each moment with context, and overlaying a dynamic tactical mini-map that tracks players and the ball.

- Detected events (6 classes): goal, penalty, foul, shot_on_target, red_card, yellow_card, direct_free_kick.
- Highlights: 10-second clips (5s before → 5s after the detected timestamp).
- Mini-map: Per-clip top-down view with real-time player/ball trajectories.

Event spotting is powered by the CALF model (Context-Aware Loss for Action Spotting) adapted from the [SoccerNet sn-spotting benchmarks](https://github.com/SoccerNet/sn-spotting/tree/main/Benchmarks/CALF).

✨ Features:
- Robust event spotting using the CALF benchmark model (feature-based).
- Automatic highlight generation around each detected timestamp (configurable pre/post padding).
- Per-clip tactical mini-map showing player/ball movement and event location.
- Batch processing for full matches; resumable & deterministic runs.
- Export to MP4 clips + JSON sidecar metadata for downstream use.
