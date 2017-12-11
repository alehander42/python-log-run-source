# python-log-run-source

A decorator that logs (optionally in a file) each executed line in a function

```python
from log_run_source import log

log('a.txt') # or log() PARENS IMPORTANT
def f(n):
  if n > 2:
    s = a(n)
    weird_call(s)
  else:
    f(n + 2)

# => def f:8   if n > 2:
# => def f:11  else:
# => def f:12    f(n + 2)
# => def f:8   if n > 2:
# => def f:9     s = a(n)
# => def f:10    weird_call(s)
# maybe timeout?
```

## installation

```bash
pip install log-run-source
```

## explain

it uses `trace` under the hood, I played with directly updating the bytecode of a function, but trace is simpler (and I am not sure how to compile back dis)
