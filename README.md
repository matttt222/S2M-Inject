# S2M-Inject

> Prompt-Guided Zero-Shot Voice Cloning for Music Generation

S2M-Inject is a project page repository for showcasing cross-domain voice cloning from reference speech to generated music.

## Highlights

- Speech-to-music voice cloning with reference timbre
- Prompt-based control (genre, mood, instrumentation, etc.)
- Chinese and English demo samples

## Repository Structure

```text
S2M-Inject/
├── index.html          # demo page
├── model.png           # model architecture figure
└── wav/
    ├── speech/         # reference speech
    │   ├── espeech*.wav
    │   └── cspeech*.wav
    └── music/          # generated music
        ├── esyn*.wav
        └── csyn*.wav
```

## Samples

This repository currently includes 20 speech-to-music pairs:
- English: `espeech1-10.wav` -> `esyn1-10.wav`
- Chinese: `cspeech1-10.wav` -> `csyn1-10.wav`

Each row in `index.html` includes:
- text
- instruction
- speech input
- generated music

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

1. Put reference speech files in `wav/speech/`.
2. Put generated music files in `wav/music/`.
3. Add a new row in the table in `index.html` with text, instruction, and audio paths.

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
