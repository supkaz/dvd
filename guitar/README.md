# Fretwise: guitar tuner, lessons and songbook

A guitar practice app in one file (`index.html`). It has no build step and no server. Open it in a browser, or host the folder on GitHub Pages.

## Features

- **Tuner**: a live microphone tuner with a cents gauge that detects which string you're playing. It supports Standard, Drop D, Half step down, Open G and DADGAD. Tap a string to hear its reference note.
- **Learn**: a 12-lesson path for players who already know the open chords:
  1. Solid foundations: chord changes, strumming, reading tabs.
  2. More sounds: 7ths and sus chords, power chords and palm muting, capo and transposing.
  3. Barre chords: the F chord, movable E and A shapes.
  4. Picking and lead: fingerpicking, the minor pentatonic, hammer-ons, pull-offs, slides and bends.
  5. Theory: keys and chord families.

  Each lesson has diagrams, tabs you can listen to, play-along strum patterns and practice goals you can tick off. Progress is saved.
- **Practice**: a metronome with tap tempo, a random chord-switch trainer and a "one-minute changes" log.
- **Chords**: a chord library with diagrams and sound. The lookup can draw any chord, such as `C#m7` or `Bb7`.
- **Songs**: 11 public-domain or traditional starter songs plus your own songs. Each song has transpose, text size, auto-scroll, a chord-diagram strip and tap-to-hear chords.
  - **Add from text**: paste chords-over-lyrics, ChordPro (`[G]inline chords`) or ASCII tabs. The format is detected automatically and you get a live preview.
  - **Add from screenshots**: drop, paste or pick images. The standalone page reads them with Tesseract OCR. Inside Claude's viewer, Claude reads them instead. The screenshot is always saved with the song.
  - **Back up**: export or import your songs and progress as JSON. You can also import `.txt` and ChordPro files.

## Storage

Opened directly, the app saves songs and progress in the browser's local storage. Opened as a Claude artifact, it saves them to your Claude account.

## Running it

```
# any static server works; the microphone needs https or localhost
python3 -m http.server -d guitar 8000
# then open http://localhost:8000
```
