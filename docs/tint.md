# Requirements

Requires the [ldc-tint](https://github.com/waikato-llm/ldc-tint) library.

# Plugins

## Detect Māori language

The `detect-maori` can be used for filtering out records that don't have enough Māori characters or
too many non-Māori ones by applying user-supplied threshold. Below, a maximum on 10% of non-Māori 
characters are tolerated before the record gets discarded:

```bash
ldc-convert \
  -l INFO \
  from-alpaca \
    -l INFO \
    -i "./input/alpaca_data_cleaned-mi.json" \
  detect-maori \
    -l INFO \
    -M 0.1
```

An alternative filter `is-maori` uses the [reo-toolkit](https://github.com/TeHikuMedia/reo-toolkit)
to determine whether text is Māori or not. Below, a minimum of 70% words must be Māori:

```bash
ldc-convert \
  -l INFO \
  from-alpaca \
    -l INFO \
    -i "./input/alpaca_data_cleaned-mi.json"
  is-maori \
    -l INFO \
    -m 0.7  
```

## Handling macrons

You can use the `de-macronize` filter to remove/replace macrons:

```bash
ldc-convert \
  -l INFO \
  from-txt-pt \
    -l INFO \
    -i "./input/māori.txt" \
  de-macronize \
    -d strip \
    -l INFO \
  to-txt-pt \
    -l INFO \
    -o "./output/maori_stripped.txt"  
```
