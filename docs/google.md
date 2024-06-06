# Requirements

Requires the [ldc-google](https://github.com/waikato-llm/ldc-google) library.

# Plugins

## Translating text using the Google Translate API

The following translates the [Alpaca JSON](https://github.com/gururise/AlpacaDataCleaned/blob/main/alpaca_data_cleaned.json)
dataset from English into Māori:

```bash
ldc-convert \
  -l INFO \
  -u 100 \
  from-alpaca \
    -l INFO \
    --input "./input/alpaca_data_cleaned.json" \
  google-translate \
    -l INFO \
    -p PROJECTNAME \
    -s en \
    -t mi \
  to-alpaca \
    -l INFO \
    --output "./output/alpaca_data_cleaned-mi.json" \
    --pretty_print \
    --ensure_ascii
```

**NB:** 

* Replace `PROJECTNAME` with your own Google project ID.
* Requires local dev credentials for Google's cloud API:
  https://cloud.google.com/docs/authentication/provide-credentials-adc#local-dev
