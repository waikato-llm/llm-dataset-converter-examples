Instead of just reading and writing the data records, you can also inject
filters in between them. E.g., the following command-line will load the
[Alpaca JSON](https://github.com/gururise/AlpacaDataCleaned/blob/main/alpaca_data_cleaned.json) 
dataset and only keep records that have the keyword `function`
in either the `instruction`, `input` or `output` data of the record:

```bash
llm-convert \
  -l INFO \
  from-alpaca \
    -l INFO \
    --input alpaca_data_cleaned.json \
  keyword \
    -l INFO \
    --keyword function \
    --location any \
    --action keep \
  to-alpaca \
    -l INFO \
    --output alpaca_data_cleaned-filtered.json 
```

**NB:** When chaining filters, the tool checks whether accepted input and 
generated output is compatible (including from reader/writer).
