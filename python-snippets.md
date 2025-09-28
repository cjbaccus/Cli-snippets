# Python Snippets

A collection of useful Python code snippets.

## Data Generation

### Generate IP address range

```python
ips = [f"{i}.{i}.{i}.{i}" for i in range(1, 11)]
for ip in ips:
    print(ip)
```