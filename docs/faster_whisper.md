# Requirements

Requires the [ldc-faster-whisper](https://github.com/waikato-llm/ldc-faster-whisper) library.

# Plugins

## Transcribing audio

The following commands transcribes raw audio files using faster-whisper (`from-fwaudio-pt`),
with the result then being stored in pretrain text format:

```bash
ldc-convert \
  -l INFO \
  from-fwaudio-pt
    -l INFO \
    --input "./input/*.wav" \
    -1 \
  to-txt-pt \
    -l INFO \
    --output "./output/"
```
