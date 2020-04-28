<!-- Template repository: https://github.com/pawamoy/jinja-templates
     Template path: credits.md
-->

# Credits
These projects were used to build `{{ project_name }}`. **Thank you!**

[`python`](https://www.python.org/) |
[`poetry`](https://poetry.eustace.io/) |
[`copier-poetry`](https://github.com/pawamoy/copier-poetry)

### Direct dependencies
{%- for dep in direct_dependencies -%}
{%- with package = package_info.get(dep, {}) %}
[`{{ package.get("name", dep) }}`]({{ package.get("home-page", "") }}){% if not loop.last %} |{% endif %}
{%- endwith -%}
{%- endfor %}

### Indirect dependencies
{%- for dep in indirect_dependencies -%}
{%- with package = package_info.get(dep, {}) %}
[`{{ package.get("name", dep) }}`]({{ package.get("home-page", "") }}){% if not loop.last %} |{% endif %}
{%- endwith -%}
{%- endfor %}

**[More credits from the author](http://pawamoy.github.io/credits/)**
