# CLI Snippets

A collection of useful bash, zsh, and general Linux command line tool snippets and shortcuts for common development and system administration tasks.

## Table of Contents

- [File and Directory Operations](#file-and-directory-operations)
  - [Directory Management](#directory-management)
  - [File Creation](#file-creation)
  - [Text Processing](#text-processing)
- [Scripting Examples](#scripting-examples)
  - [Bash](#bash)
- [Cloud Tools](#cloud-tools)
  - [Azure CLI](#azure-cli)
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

## Scripting Examples

### Bash

#### Add colored output to bash scripts

```bash
# Color variables
RED='\033[0;31m'
GREEN='\033[0;32m'
YELLOW='\033[1;33m'
BLUE='\033[0;34m'
PURPLE='\033[0;35m'
CYAN='\033[0;36m'
WHITE='\033[1;37m'
NC='\033[0m' # No Color

# Usage examples
echo -e "${RED}This is red text${NC}"
echo -e "${GREEN}This is green text${NC}"
echo -e "${YELLOW}This is yellow text${NC}"
echo -e "${BLUE}This is blue text${NC}"

# Function for colored output
print_color() {
    local color=$1
    local message=$2
    echo -e "${color}${message}${NC}"
}

# Using the function
print_color "$RED" "Error: Something went wrong!"
print_color "$GREEN" "Success: Operation completed!"
print_color "$YELLOW" "Warning: Check this setting"
```

## Cloud Tools

### Azure CLI

See [azure-cli.md](azure-cli.md) for Azure CLI command snippets.

## Python

See [python-snippets.md](python-snippets.md) for Python code snippets.