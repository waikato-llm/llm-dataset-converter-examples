The following command scans the `/some/dir` directory recursively for `.txt`
files that do not have `raw` in the file path:

```
llm-find \
    -l INFO \
    -i /some/dir/
    -r \
    -m ".*\.txt" \
    -n ".*\/raw\/.*" \
    -o ./files.txt
```

The same command, but splitting the files into training, validation and test 
lists, using a ratio of 70/15/15:

```
llm-find \
    -l INFO \
    -i /some/dir/
    -r \
    -m ".*\.txt" \
    -n ".*\/raw\/.*" \
    --split_ratios 70 15 15 \
    --split_names train val test \
    -o ./files.txt
```

This results in the following three files: `files-train.txt`, `files-val.txt` 
and `files-test.txt`.
