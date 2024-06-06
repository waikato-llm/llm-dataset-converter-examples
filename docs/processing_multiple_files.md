Provided that the reader supports, you can also process multiple files, one
after the other. For that you either specify them explicitly (multiple 
arguments to the `--input` option) or use a glob syntax (e.g., `--input "*.json"`).
For the latter, you should surround the argument with double quotes to avoid
the shell expanding the names automatically.

If you have a lot of files, it will be more efficient to store these in text
files (with one file per line) and pass these to the reader using the 
`--input_list` option (assuming that the reader supports this). Such file
lists can be generated with the `llm-find` tool. See [Locating files](locating_files.md) 
for examples.

As for specifying the output, you simply specify the output directory. An output
file name gets automatically generated from the name of the current input file
that is being processed.

If you want to compress the output files, you need to specify your preferred
compression format via the global `-c/--compression` option of the `llm-convert`
tool. By default, no compression is used.

Please note, that when using a *stream writer* (e.g., for text or jsonlines 
output) in conjunction with an output directory, each record will be stored 
in a separate file. In order to transfer all the records into a single file, 
you have to explicitly specify that file as output.
