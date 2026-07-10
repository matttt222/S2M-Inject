# S2M-Inject

> Prompt-Guided Zero-Shot Voice Cloning for Music Generation

S2M-Inject is a project page repository for showcasing cross-domain voice cloning from reference speech to generated music.

## Highlights

- Speech-to-music voice cloning with reference timbre
- Prompt-based control (genre, mood, instrumentation, etc.)
- Chinese and English demo samples
- Representative failure-case analysis for high-pitch and sustained-vowel regions

## Repository Structure

```text
S2M-Inject/
├── index.html          # demo page
├── model.png           # model architecture figure
└── wav/
    ├── speech/         # reference speech for main samples
    │   ├── espeech*.wav
    │   └── cspeech*.wav
    ├── music/          # generated music for main samples
    │   ├── esyn*.wav
    │   └── csyn*.wav
    └── failure/        # representative failure cases
        ├── failure_speech*.wav
        └── failure_music*.wav
```

## Samples

This repository currently includes 20 regular speech-to-music pairs and 2 representative failure cases.

Regular samples:
- English: `espeech1-10.wav` -> `esyn1-10.wav`
- Chinese: `cspeech1-10.wav` -> `csyn1-10.wav`

Failure cases:
- `failure_speech1.wav` -> `failure_music1.wav`
- `failure_speech2.wav` -> `failure_music2.wav`

Each regular row in `index.html` includes:
- text
- instruction
- speech input
- generated music

The failure-case section additionally includes:
- failure mode
- short analysis

## Quick Start

Run a local static server:

```bash
cd S2M-Inject
python3 -m http.server 8000
```

Open:

```text
http://localhost:8000
```

## Add or Replace Samples

For regular demo samples:

1. Put reference speech files in `wav/speech/`.
2. Put generated music files in `wav/music/`.
3. Add or edit a row in the main sample table in `index.html`.

For failure-case samples:

1. Put reference speech and generated music files in `wav/failure/`.
2. Edit the `Failure Case Analysis` table in `index.html`.
3. Use relative paths such as `wav/failure/failure_speech1.wav`.

## Deployment

This repo is ready for static hosting (for example, GitHub Pages):
- entry: `index.html`
- assets: `model.png`, `wav/*`

## Paper & Citation

If you use this work, please add and cite the paper links:
- Paper: `TBD`
- arXiv: `TBD`

## License

The page footer currently states `© 2025 S2M-Inject. All rights reserved.`  
Add an explicit open-source license if needed.
