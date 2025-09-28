# CLI Snippets

A collection of useful bash, zsh, and general Linux command line tool snippets and shortcuts for common development and system administration tasks.

## Table of Contents

- [File and Directory Operations](#file-and-directory-operations)
  - [Directory Management](#directory-management)
  - [File Creation](#file-creation)
  - [Text Processing](#text-processing)
- [Cloud Tools](#cloud-tools)
  - [Azure CLI](#azure-cli)
- [Scripting Examples](#scripting-examples)
  - [Python](#python)

## File and Directory Operations

### Directory Management

#### Rename directories by removing spaces from names

```bash
find . -name "* *" -type d -execdir rename -v 's/ /_/g' {} +
```

#### Create multiple directories at once

```bash
mkdir -p {dir1,dir2,dir3,dir1/tasks,dir1/templates,dir2/tasks,dir2/templates,dir3/tasks}
```

### File Creation

#### Create multiple files at once using brace expansion

```bash
touch file{1..34}.txt
```

### Text Processing

#### Extract contents between double quotes and assign to a variable

```bash
PANAPI=$(cat .panrc01 | grep -o '"[^"]*"')
```

## Cloud Tools

### Azure CLI

#### List all virtual machines

```bash
az vm list
```

#### List available VM sizes

```bash
az vm list-sizes
```

## Scripting Examples

### Python

#### Generate IP address range

```python
ips = [f"{i}.{i}.{i}.{i}" for i in range(1, 11)]
for ip in ips:
    print(ip)
```