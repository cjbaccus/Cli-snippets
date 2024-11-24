# Cli-snippets
Bash, zsh, and general linux command line tool snippets and shortcuts.

## Sections

### Bash

#### Rename directories by taking out spaces in name

```bash
find . -name "* *" -type d -execdir rename -v 's/ /_/g' {} +
```

#### Make multiple directories at once

```bash
mkdir -p {dir1,dir2,dir3,dir1/tasks,dir1/templates,dir2/tasks,dir2/templates,dir3/tasks}
```
