# LRC Lyrics

Time-synced lyrics for songs that don't have timings on [LRCLIB](https://lrclib.net) yet.
The timings are made by forced alignment against the audio, then kept here until
they're ready to upload to LRCLIB.

## Layout

```
lyrics/
  <spotify track id>.lrc
```

Each file is named by the song's Spotify track ID, the part after `spotify:track:`.
For example, `3uVXrgObuBcBMUOsvwQtob.lrc` is
`https://open.spotify.com/track/3uVXrgObuBcBMUOsvwQtob`.

Files are [LRC](https://en.wikipedia.org/wiki/LRC_(file_format)): one
`[mm:ss.xx] text` line per lyric line. Metadata tags such as `[ti:...]`, `[ar:...]`
and `[id:...]` are allowed and ignored by readers that don't need them.

## Use

The lyrics app checks this repo before LRCLIB, by fetching

    https://raw.githubusercontent.com/belambert/lrc-lyrics/main/lyrics/<spotify track id>.lrc

To add a song, commit its `.lrc` file under `lyrics/`. GitHub's raw file cache can
take a few minutes to serve a new or changed file.

Lyrics are copyrighted. They're shared here for personal use.
