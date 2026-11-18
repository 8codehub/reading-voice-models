# Reading — voice models

Mirror of the [Kitten TTS 2 Nano](https://huggingface.co/KittenML/kitten-tts-2-nano) files the
Reading app downloads for read-aloud in languages other than English (English is built into the app).

The files are in the **Releases** of this repository, not in the git tree:

| Language | Model | Voices |
|---|---|---|
| German | `kitten_tts_2_nano_de.onnx` | `voices_de.npz` |
| Spanish | `kitten_tts_2_nano_es.onnx` | `voices_es.npz` |
| Italian | `kitten_tts_2_nano_it.onnx` | `voices_it.npz` |
| Portuguese (Brazil) | `kitten_tts_2_nano_pt.onnx` | `voices_pt.npz` |
| Russian | `kitten_tts_2_nano_ru.onnx` | `voices_ru.npz` |
| Hindi | `kitten_tts_2_nano_hi.onnx` | `voices_hi.npz` |
| French | `kitten_tts_2_nano_fr.onnx` | `voices_fr.npz` |

Download URL: `https://github.com/8codehub/reading-voice-models/releases/download/kitten-tts-2-nano-v1/<file>`

- **Unmodified** copies of KittenML's revision `54526b8d8e45333cd720d3a082c106aacf416064`.
  [`SHA256SUMS`](SHA256SUMS) lists each file's hash; the app checks every download against it.
- A release is never edited after publishing. New model versions get a new tag, so the files an
  app version was tested with never change underneath it.

## License

The models are KittenML's, under the [Apache License 2.0](LICENSE). See [`NOTICE`](NOTICE).
