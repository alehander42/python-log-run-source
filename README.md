# python-log-run-source

A decorator that logs (optionally in a file) each executed line in a function

```python
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
```
