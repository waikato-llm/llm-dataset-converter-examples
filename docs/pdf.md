# Requirements

Requires the [ldc-pdf](https://github.com/waikato-llm/ldc-pdf) library.

# Plugins

## Extracting text from PDFs

The following pipeline extracts the text from a thesis PDF, skipping the first and last page (`-p`):

```bash
ldc-convert \
  -l INFO \
  from-pdf-pt \
    -l INFO \
    --input "./input/thesis.pdf" \
    -p 2-last_1 \
  to-txt-pt \
    -l INFO \
    --output "./output/thesis.txt"
```
