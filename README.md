# Unmixing the Crowd: listening examples

These are audio examples for our SANE 2026 paper, "Mixture-Derived Speaker Embeddings: Can They Replace Enrollment in Pre-trained Target Speech Extractors?" (Soundability Lab, University of Michigan).

Target speech extractors usually need a short clip of someone talking alone before they can pull that person out of a mix. We wanted to see how far you can get without one, by taking the speaker embeddings from the mixture itself and feeding them to a frozen, pre-trained extractor.

There are six two-person LibriSpeech mixtures here, with 50–80% overlap, some with WHAM! noise added. For each speaker you can compare three versions, all from the same extractor:

- **Clean reference**: the person's own clean speech
- **Ours**: embeddings taken directly from the mixture
- **Diarize-then-enroll**: pyannote 3.1 finds where each person talks alone, and the same encoder embeds those parts

We picked these six from mixtures where ours does better, so they're not a random sample. Over all 3,000 test mixtures, ours averages 10.8 dB SI-SDR improvement and diarize-then-enroll averages 6.8 dB.

The page is `index.html` (served by GitHub Pages). Audio lives in `audio/` and spectrograms in `spec/`.
