# Requirements

Requires the [ldc-openai](https://github.com/waikato-llm/ldc-openai) library.

# Plugins

## Count tokens

In order to determine how costly the OpenAI usage is, you can apply the 
`openai-count-tokens` filter to your data (in the example below, 1k tokens 
cost $0.002):  

```bash
ldc-convert \
  -l INFO \
  from-alpaca \ 
    -l INFO \
    --input "./input/alpaca_data_cleaned.json" \
  openai-count-tokens \
    -l INFO \
    -m gpt-3.5-turbo \
    -t 0.002 \
    -p "You will be provided with a sentence in English, and your task is to translate it into Māori."
```

Will output something like this:

```
INFO:openai-count-tokens:# tokens (prompt): 22
INFO:openai-count-tokens:# tokens: 11512740
INFO:openai-count-tokens:total price (1k tokens = 0.002000): 23.025480
```
