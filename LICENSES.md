# Third-party components in SirAud-Studio v1.2

SirAud-Studio runs in your browser. No account, no API key, no analytics. Text, voices and recordings stay on your device
(except the one-time downloads you choose: voices, voice list, samples and, if the `vendor/` folder is missing, the engine files from jsDelivr).

| Component | Role | License |
|---|---|---|
| Piper (rhasspy/piper) and Piper voices | Neural voice models (VITS, ONNX) | Code: MIT. **Each voice has its own license** on its model card |
| ONNX Runtime Web (Microsoft) | Runs the voice models in WebAssembly (`vendor/ort/`) | MIT |
| piper_phonemize WASM build (diffusion-studio/piper-wasm) | Text to phonemes (`vendor/piper/`) | MIT |
| eSpeak NG, bundled in `piper_phonemize.data/.wasm` | Pronunciation rules | GPL-3.0-or-later |
| Resemblyzer speaker encoder (resemble-ai/Resemblyzer), weights inlined in index.html | Voice print for the Voice lab | Apache-2.0 (from Real-Time-Voice-Cloning, MIT) |
| lamejs | MP3 encoder (inlined in index.html) | LGPL-3.0 |
| Bricolage Grotesque, Instrument Sans (via Fontsource) | Fonts in `fonts/` | SIL OFL 1.1 |

## Notes
- **Voices** are not part of this package. The app downloads them from the Piper collection
  (https://huggingface.co/rhasspy/piper-voices) or from a repository you configure. Several voices have restrictions
  (non-commercial use, attribution). Read the MODEL_CARD of a voice before using its audio commercially.
- **Voice lab**: only create profiles from your own voice or with clear consent of the speaker.
- **GPL / LGPL**: eSpeak NG (GPL-3.0) and lamejs (LGPL-3.0) are distributed unmodified. If you redistribute this package keep this file and
  make the corresponding source available (https://github.com/rhasspy/espeak-ng, https://github.com/zhuker/lamejs).
- The speaker-encoder weights come from https://github.com/resemble-ai/Resemblyzer (Apache-2.0).
