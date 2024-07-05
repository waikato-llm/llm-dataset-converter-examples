The [llm-dataset-converter](https://github.com/waikato-llm/llm-dataset-converter) 
library (and its dependent libraries) can be used for converting **Large Language Model (LLM) datasets** 
from one format into another. It has support for the following domains:

* Pretrain
* Supervised

    * Classification
    * Pairs (Q&A, P/R)

* Translation

Please refer to the [dataset formats](https://github.com/waikato-llm/llm-dataset-converter?tab=readme-ov-file#dataset-formats)
section for more details on supported formats.

But the library does not just convert datasets, you can also slot in complex
filter pipelines to process/clean the data.

On this website you can find examples for:

* [Downloader usage](downloaders.md)
* [General usage](general_usage.md)
* [Processing multiple files](processing_multiple_files.md)
* [Locating files](locating_files.md)
* [Compression](compression.md)
* [Filter usage](filters.md)
* [Docker usage](docker.md)

Examples for the additional libraries:

* [Faster whisper](faster_whisper.md)
* [Google](google.md)
* [HTML](html.md)
* [MS Word (doc)](doc.md)
* [MS Word (docx)](docx.md)
* [OpenAI](openai.md)
* [PDF](pdf.md)
* [TinT](tint.md)
