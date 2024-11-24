# Cli-snippets
Bash, zsh, and general linux command line tool snippets and shortcuts.

[toc]

## Sections

### Bash

#### Rename lots of directories

```bash
find . -name "* *" -type d -execdir rename -v 's/ /_/g' {} +
```
