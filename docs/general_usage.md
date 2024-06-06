A conversion pipeline is executed via the `llm-convert` tool, with a pipeline
typically consisting of a reader and writer, with optional filters in-between.
However, only the reader is required.

The following loads the [Alpaca JSON](https://github.com/gururise/AlpacaDataCleaned/blob/main/alpaca_data_cleaned.json)
file and stores it in CSV format (P/R):

```bash
llm-convert \
  from-alpaca \
    --input ./alpaca_data_cleaned.json \
  to-csv-pr \
    --output alpaca_data_cleaned.csv
```

If you want some logging output, e.g., on progress and what files are being 
processed/generated:

```bash
llm-convert \
  -l INFO \
  from-alpaca \
    --input ./alpaca_data_cleaned.json \
    -l INFO \
  to-csv-pr \
    --output alpaca_data_cleaned.csv
    -l INFO
```
