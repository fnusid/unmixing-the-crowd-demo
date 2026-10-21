# Unmixing the Crowd: listening examples

Audio examples for "Mixture-Derived Speaker Embeddings: Can They Replace Enrollment in Pre-trained Target Speech Extractors?" (SANE 2026, Soundability Lab, University of Michigan).

Six two-talker LibriSpeech mixtures (50–80% overlap, with or without WHAM! noise). Each talker is extracted by the same frozen target speech extractor, conditioned on:

- **Clean reference**: the talker's own clean speech
- **Ours**: speaker embeddings taken directly from the mixture
- **Diarize-then-enroll**: pyannote 3.1 solo regions embedded by the same encoder

The six were chosen from mixtures where ours scores higher; across all 3,000 test mixtures ours averages 10.8 dB SI-SDR improvement and diarize-then-enroll 6.8 dB.

Open `index.html` (served by GitHub Pages). Audio in `audio/`, spectrograms in `spec/`.
