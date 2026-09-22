# LIFEPAK 15 CPR/AED Trainer

A phone-based soundboard for a cardboard LIFEPAK 15 cosplay prop. Open `index.html`
on a phone, prop the phone inside the case, and use the on-screen buttons to run
CPR metronome cycles and a scripted AED shock sequence.

## Hosting it on GitHub Pages

1. Create a new GitHub repository (public is fine, e.g. `lifepak-prop`).
2. Upload this whole folder (`index.html`, the `sounds` folder, this `README.md`)
   to the repo, keeping the folder structure exactly as-is.
3. In the repo, go to **Settings → Pages**, set the source to your main branch
   (root folder), and save.
4. GitHub will give you a URL like `https://yourusername.github.io/lifepak-prop/`.
   Open that on your phone and bookmark it or add it to your home screen.

## Adding your own sound clips

Drop MP3 files into the `sounds` folder using **these exact filenames**:

| Filename                    | When it plays                                   |
|------------------------------|--------------------------------------------------|
| `ventilate.mp3`              | End of a compression cycle ("stop, ventilate")   |
| `analyzing.mp3`               | Right after pressing ANALYZE                     |
| `shock-advised.mp3`          | When the outcome is set to "Shock advised"        |
| `charged.mp3`                | After the charging tone finishes                  |
| `no-shock.mp3`               | When the outcome is set to "No shock advised"     |
| `shock-delivered.mp3`        | After pressing SHOCK                              |

You don't have to add all of them at once — any filename that's missing just
falls back to the phone's built-in voice automatically, so the app always
works even with an empty `sounds` folder. The small line under the title
tells you how many custom clips it found.

Good places to get clips:
- Record your own voice reading the lines above (a flat, unhurried delivery
  reads as more "device-like" than you'd expect).
- Generate them with any free text-to-speech tool and export as MP3.
- Keep each clip short and trimmed of silence at the start/end so the timing
  feels snappy.

## What's synthesized vs. file-based

The compression metronome beep and the AED charging tone are generated in
the browser (Web Audio), so you don't need files for those — only the six
spoken lines above use the `sounds` folder.

## Notes

- Works fully offline once loaded, aside from needing to load `index.html`
  itself.
- Uses `localStorage` to remember your last CPR ratio and AED outcome choice
  between visits.
- Not a real medical device — arts & crafts prop only.
