# TIL
Today I learned

# 2020-01-14

### Memory usage/profiling in our python code

Tags: `python`

Here, the heroe is `tracemalloc` from the stdlib (>= python3.4).

```python
#!/usr/bin/env python
# From:  https://medium.com/python-features/understanding-memory-usage-and-leaks-in-our-python-code-beginners-c9dc211887af

import tracemalloc
tracemalloc.start(6)

time1 = tracemalloc.take_snapshot()
ref = 'Sarah ' * 51200000
time2 = tracemalloc.take_snapshot()

stats = time2.compare_to(time1, 'lineno')
for stat in stats:
    print(stat)

print('\nWho is consuming more mem?:\n')
top = stats[0]
print('\n'.join(top.traceback.format()))

```


# 2019-12-19

### Using multiple python versions

Tags: `python`

Install different python versions and use them like `virtualenvs`. Also, it supports define which `python version` do you want to use by `application`, creating a `.python-version` file in the current app/directory.

To create a `.python-version` file, issue the command: `pyenv local 3.8.0`

Docs at: https://github.com/pyenv/pyenv/blob/master/COMMANDS.md#pyenv-local

### Instant realtime GraphQL engine 

Tags: `graphql`


# 2019-12-11

### Instant realtime GraphQL engine 

Tags: `graphql`

https://hasura.io/

How to use Hasura with Django, the eassy way: https://medium.com/free-code-camp/how-to-get-instant-graphql-apis-on-your-existing-django-application-c8fcfdb945aa

# 2019-12-09

### SSR to Vue apps, the easy way 

Tags: `javascript`, `vuejs` 

https://medium.com/swlh/how-to-add-server-side-rendering-to-vue-js-app-the-easy-way-a38fc32c9bf2

# 2019-12-03

### Don't reassign your function arguments

Tags: `javascript`

https://spin.atomicobject.com/2011/04/10/javascript-don-t-reassign-your-function-arguments/
http://bonsaiden.github.io/JavaScript-Garden/#function.arguments

# 2019-12-02

### Deno, a new runtime for typescript and javascript

Tags: `typescript`, `javascript`

https://dev.to/wuz/getting-started-with-deno-e1m


# 2019-11-25

### Delete locally those branches removed from origin/remote

Tags: `git`

Use `git fetch -p origin`. It will delete locally all those branches that dont exists on origin anymore.
 
