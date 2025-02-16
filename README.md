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


### azure-cli

#### az virtual machine list

```bash
az vm list
```

#### az vm list-sizes
```bash
az vm list-sizes
```
```python
ips = [f"{i}.{i}.{i}.{i}"for i in range(1,11)]
for ip in ips:
    print(ip)


```
