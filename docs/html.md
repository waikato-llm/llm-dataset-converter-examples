# Requirements

Requires the [ldc-html](https://github.com/waikato-llm/ldc-html) library.

# Plugins

## Extracting text from HTML files

```bash
ldc-convert \
  -l INFO \
  from-html-pt \
    -l INFO \
    --input "./input/*.html" \
    -s "\n" \
  to-txt-pt \
    -l INFO \
    --output "./output/"
```
