# Requirements

Requires the [ldc-google](https://github.com/waikato-llm/ldc-gitingest) library.

# Plugins

## Converting repository clone into pretrain text

The following converts only Python files of a local repository clone into
a pretrain text file:

```bash
ldc-convert \
  -l INFO \
  from-gitingest-pt \
    -l INFO \
    --input "/some/where/local/myrepo" \
    --include_pattern "*.py" \
  to-txt-pt \
    -l INFO \
    --output "./output/myrepo.txt"
```

## Converting remote repositories into pretrain text

The following converts all files apart from Markdown and reStructured Text ones 
of two remote repositories into pretrain text files:

```bash
ldc-convert \
  -l INFO \
  from-gitingest-pt \
    -l INFO \
    --input \
      "https://github.com/fracpete/python-weka-wrapper3" \
      "https://github.com/fracpete/sklearn-weka-plugin" \
    --exclude_pattern "*.md" "*.rst" \
  to-txt-pt \
    -l INFO \
    --output "./output/"
```
