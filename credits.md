<!-- Template repository: https://github.com/pawamoy/jinja-templates
     Template path: credits.md
-->

# Credits
These projects were used to build `{{ project_name }}`. **Thank you!**

[`python`](https://www.python.org/) |
[`pdm`](https://pdm.fming.dev/) |
[`copier-pdm`](https://github.com/pawamoy/copier-pdm)

### Direct dependencies
{%- for dep in direct_dependencies -%}
[`{{ dep }}`](https://pypi.org/project/{{ dep }}/){% if not loop.last %} |{% endif %}
{%- endfor %}

### Indirect dependencies
{%- for dep in indirect_dependencies -%}
[`{{ dep }}`](https://pypi.org/project/{{ dep }}/){% if not loop.last %} |{% endif %}
{%- endfor %}
{%- if more_credits %}

**[More credits from the author]({{ more_credits }})**
{%- endif %}
