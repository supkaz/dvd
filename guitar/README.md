# Fretwise: guitar tuner, lessons and songbook

A guitar practice app in one file (`index.html`). It has no build step and no server. Open it in a browser, or host the folder on GitHub Pages.

## Features

- **Tuner**: a live microphone tuner with a cents gauge that detects which string you're playing. It supports Standard, Drop D, Half step down, Open G and DADGAD. Tap a string to hear its reference note.
- **Learn**: a 17-lesson path for players who already know the open chords:
  1. Solid foundations: chord changes, strumming, reading tabs.
  2. More sounds: 7ths and sus chords, power chords and palm muting, capo and transposing.
  3. Barre chords: the F chord, movable E and A shapes.
  4. Picking and lead: fingerpicking, the minor pentatonic, hammer-ons, pull-offs, slides and bends.
  5. Theory: keys and chord families.

  6. Music theory: notes on the fretboard (with a note quiz), intervals (with ear-training cues), how chords are built (interactive chord builder), the major scale and keys (key explorer), rhythm and time signatures.

  Each lesson has diagrams, tabs you can listen to, play-along strum patterns and practice goals you can tick off. Progress is saved.
- **Chord plan**: tick the chords you can play. The app suggests the next chord to learn, chosen by how many songs it unlocks and a sensible learning order. It also lists the songs you can play now and the ones that are one chord away. Each lesson also links songs that practise it.
- **Practice**: a metronome with tap tempo, a random chord-switch trainer and a "one-minute changes" log.
- **Chords**: a chord library with diagrams and sound. The lookup can draw any chord, such as `C#m7` or `Bb7`.
- **Songs**: 11 public-domain or traditional starter songs plus your own songs. Each song has transpose, text size, auto-scroll, a chord-diagram strip and tap-to-hear chords.
  - **Add from text**: paste chords-over-lyrics, ChordPro (`[G]inline chords`) or ASCII tabs. The format is detected automatically and you get a live preview.
  - **Add from screenshots**: drop, paste or pick images. The standalone page reads them with Tesseract OCR. Inside Claude's viewer, Claude reads them instead. The screenshot is always saved with the song.
  - **Songs to look up**: about 30 popular songs listed with their chords only, sorted by how ready you are. Tap one to start a song entry, then paste the chart or a screenshot.
  - **Back up**: export or import your songs and progress as JSON. You can also import `.txt` and ChordPro files.

## Storage

Opened directly, the app saves songs and progress in the browser's local storage. Opened as a Claude artifact, it saves them to your Claude account.

## Running it

```
# any static server works; the microphone needs https or localhost
python3 -m http.server -d guitar 8000
# then open http://localhost:8000
```
