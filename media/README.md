# Work videos

Clips shown on `work.html`. To add one, drop the file here (or upload it to
YouTube) and add a single entry to the `WORK` array near the bottom of
`work.html` — it is the only part of that file you need to touch.

```js
{
  cat: "teacher",                 // systems | teacher | automation | marketing | reels
  tag: "gold",                    // "" | gold | blue — the colour of the little chip
  vertical: true,                 // reels only: switches the box to 9:16
  file: "media/teacher-demo.mp4", // EITHER a file here…
  youtube: "dQw4w9WgXcQ",         // …OR a YouTube id. Never both.
  poster: "media/teacher.jpg",    // optional still shown before play
  link: "https://…",              // optional "open the live demo" button
  ar: { title: "…", desc: "…" },
  en: { title: "…", desc: "…" }
}
```

## Which one: a file here, or YouTube?

**Put it on YouTube (unlisted is fine) if the clip is over ~20 MB.** GitHub
warns above 50 MB and hard-refuses at 100 MB per file, and every version you
ever commit stays in the repo's history forever — a handful of re-uploaded
demo videos will bloat the clone for good. Pages also serves everything from
one bandwidth budget.

The page loads YouTube through `youtube-nocookie.com` and only after the
visitor clicks play, so nothing is requested from Google until they ask.

**Commit the file here** for genuinely short clips — a 15-second reel, a
20-second automation loop.

## If you do commit a file

- MP4, H.264 + AAC. It plays everywhere; `.mov` and `.mkv` do not.
- Cap the long edge at 1280px for landscape, 1080px for vertical reels.
- Add a `poster` still — without one the box is black until play is pressed.
- Name files in lowercase with hyphens: `clinic-booking.mp4`.

Re-encode an oversized clip before committing:

```sh
ffmpeg -i input.mov -vf "scale='min(1280,iw)':-2" -c:v libx264 -crf 28 \
       -preset slow -c:a aac -b:a 96k media/clinic-booking.mp4
```

## Before you film

Every clip is a real screen recording of a real system. Blur or replace any
real customer name, phone number, or patient detail before recording — a
demo reel is a public page, and the data on those screens belongs to the
people it describes.
