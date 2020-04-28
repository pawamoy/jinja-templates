# Command line usage

```
{{ main_usage }}
```

Commands:

{% for command in commands %}
- [`{{ command.name }}`](#{{ command.name }}){% endfor %}

{% for command in commands %}
---

### `{{ command.name }}`

```
{{ command.usage }}
```
{% endfor %}
