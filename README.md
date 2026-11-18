# Reading — voice models

Files the Reading app downloads for read-aloud: the [Kitten TTS 2 Nano](https://huggingface.co/KittenML/kitten-tts-2-nano)
models and voices, Piper's Armenian voice, and the word → pronunciation dictionaries. Nothing is built into the app; a
language is downloaded the first time it's chosen.

The files are in the **Releases** of this repository, not in the git tree:

### Release `kitten-tts-2-nano-v1` — models and voices

| Language | Model | Voices |
|---|---|---|
| English | `kitten_tts_2_nano_en.onnx` | `voices_en.npz` |
| German | `kitten_tts_2_nano_de.onnx` | `voices_de.npz` |
| Spanish | `kitten_tts_2_nano_es.onnx` | `voices_es.npz` |
| Italian | `kitten_tts_2_nano_it.onnx` | `voices_it.npz` |
| Portuguese (Brazil) | `kitten_tts_2_nano_pt.onnx` | `voices_pt.npz` |
| Russian | `kitten_tts_2_nano_ru.onnx` | `voices_ru.npz` |
| Hindi | `kitten_tts_2_nano_hi.onnx` | `voices_hi.npz` |
| French | `kitten_tts_2_nano_fr.onnx` | `voices_fr.npz` |

Download URL: `https://github.com/8codehub/reading-voice-models/releases/download/kitten-tts-2-nano-v1/<file>`

### Release `lexicons-v1` — pronunciation dictionaries

`lexicon_<code>.tsvz` for en, de, es, it, pt, ru, hi, fr: gzip-compressed, sorted `word<TAB>phonemes`
lines (named `.tsvz`, not `.gz`, because Android's packager unzips `.gz` files). Hashes in
[`SHA256SUMS-lexicons`](SHA256SUMS-lexicons).

Download URL: `https://github.com/8codehub/reading-voice-models/releases/download/lexicons-v1/<file>`

### Release `armenian-gor-v1` — Armenian

`hy_AM-gor-medium.onnx` + `hy_AM-gor-medium.onnx.json` (Piper voice "gor", unmodified from
[rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices/tree/main/hy/hy_AM/gor/medium)) and
`lexicon_hy.tsvz`. Hashes in `SHA256SUMS-armenian` (in the release).

Download URL: `https://github.com/8codehub/reading-voice-models/releases/download/armenian-gor-v1/<file>`

- **Unmodified** copies of KittenML's revision `54526b8d8e45333cd720d3a082c106aacf416064`.
  [`SHA256SUMS`](SHA256SUMS) lists each file's hash; the app checks every download against it.
- A release is never edited after publishing. New model versions get a new tag, so the files an
  app version was tested with never change underneath it.

## License

- **Models and voices**: KittenML's, under the [Apache License 2.0](LICENSE). See [`NOTICE`](NOTICE).
- **`lexicon_en.tsvz`**: from [misaki](https://github.com/hexgrad/misaki) (Apache 2.0), which includes
  the CMU Pronouncing Dictionary (BSD-style).
- **The other `lexicon_*.tsvz`**: words chosen from [FrequencyWords](https://github.com/hermitdave/FrequencyWords)
  by Hermit Dave (CC BY-SA 4.0), pronunciations generated with espeak-ng used as a tool. Shared under
  [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
- **Armenian voice (`armenian-gor-v1`)**: [GPL-2.0](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html),
  from the dataset [davit312/piper-TTS-Armenian](https://huggingface.co/davit312/piper-TTS-Armenian); licence
  text and model card are in the release. `lexicon_hy.tsvz`: words from the
  [Leipzig Corpora Collection](https://wortschatz.uni-leipzig.de), pronunciations generated with espeak-ng used as a tool.
