---
layout: api-command 
language: Ruby
permalink: api/ruby/limit/
command: limit 
github_doc: https://github.com/rethinkdb/docs/edit/master/2-query-language/api/ruby/transformations/limit.md
related_commands:
    order_by: order_by/
    skip: skip/
    []: slice/
---

{% apibody %}
sequence.limit(n) → stream
array.limit(n) → array
{% endapibody %}


End the sequence after the given number of elements.

__Example:__ Only so many can fit in our Pantheon of heroes.

```rb
r.table('marvel').order_by(:belovedness).limit(10).run(conn)
```

